```python
from urllib.request import Request, urlopen
from bs4 import BeautifulSoup
```


```python
url_base = 'http://www.chicagomag.com'
url_sub = '/Chicago-Magazine/November-2012/Best-Sandwiches-Chicago/'
url = url_base + url_sub

# modified on Jun.20,2021
req = Request(url, headers={'User-Agent': 'Mozilla/5.0'})
html = urlopen(req).read()
#html = urlopen(url)
soup = BeautifulSoup(html, 'html.parser')
```


```python
soup
```


```python
items =soup.find_all('div',{'class':'sammy'})
```


```python
len(items)
```


```python
rank = []
menu = []
cafe = []
link = []
```


```python
import re
for item in items:
    rank.append(item.find('div',{'class':'sammyRank'}).text)
    temp = item.find('div', {'class':'sammyListing'})
#    print(temp)
    menu.append(re.split(('\r\n|\n'),temp.text)[0])
    cafe.append(re.split(('\r\n|\n'),temp.text)[1])
    if (item.find('a')['href'][0:4]) == 'http' :
        link.append(item.find('a')['href'])
    else :
        link.append(url_base + item.find('a')['href'])
    
cafe[:5]    
```


```python
link[0:11]
```


```python
import pandas as pd
```


```python
data = {'Rank':rank, 'Menu':menu, 'Cafe':cafe, 'URL':link}
```


```python
df = pd.DataFrame(data)
df.head()
```


```python
df.head(10)
```


```python
df.to_csv('best_sandwiches_list_chicago.csv', sep=',',encoding='UTF-8')
```


```python
pwd
```


```python
from bs4 import BeautifulSoup
from urllib.request import Request, urlopen
import pandas as pd
```


```python
df = pd.read_csv('best_sandwiches_list_chicago.csv', index_col=0)
df.head(10)
```


```python
df.tail(10)
```


```python
df.index
```


```python
price = []
address = []

for n in df.index:

    # modified on Jun.20,2021
    url = df['URL'][n]
    req = Request(url, headers={'User-Agent': 'Mozilla/5.0'})
    html = urlopen(req).read()
#   html = urlopen(df['URL'][n])
    soup_tmp = BeautifulSoup(html, 'lxml')
    
    gettings = soup_tmp.find('p', 'addy').get_text()
    
    price.append(gettings.split()[0][:-1])
    address.append(' '.join(gettings.split()[1:-2]))
```


```python
from tqdm import tqdm_notebook

price = []
address = []

for n in tqdm_notebook(df.index):
    # modified on Jun.20,2021
    url = df['URL'][n]
    req = Request(url, headers={'User-Agent': 'Mozilla/5.0'})
    html = urlopen(req).read()
    
    # html = urlopen(df['URL'][n])
    soup_tmp = BeautifulSoup(html, 'lxml')
    
    gettings = soup_tmp.find('p', 'addy').get_text()
    
    price.append(gettings.split()[0][:-1])
    address.append(' '.join(gettings.split()[1:-2]))
```


```python
len(price)
```


```python
len(address)
```


```python
df['Price'] = price
df['Address'] = address

df = df.loc[:,['Rank', 'Cafe', 'Menu', 'Price', 'Address']]
df.set_index('Rank', inplace=True)
df.head()
```


```python
df.to_csv('best_sandwiches_list_chicago2.csv', sep=',', encoding='UTF-8')
```


```python
pip install folium
```


```python
pip install googlemaps
```


```python
import folium
import pandas as pd
import googlemaps
import numpy as np
```


```python
df = pd.read_csv('best_sandwiches_list_chicago2.csv', index_col=0)
df.head()
```


```python
#gmaps_key ='AIzaSyCWTVUAdJaFfj41etI2b_EBBRsHYet1VZQ'
gmaps_key ='AIzaSyB7Lq1eQOfGMZuzKYBw9EnPQf1eq0GkQ0I'
gmaps = googlemaps.Client(key=gmaps_key)
```


```python
lat = []
lng = []

for n in tqdm_notebook(df.index):
    if df['Address'][n] != 'Multiple':
        target_name = df['Address'][n]+', '+'Chicago'
        gmaps_output = gmaps.geocode(target_name)
        location_output = gmaps_output[0].get('geometry')
        lat.append(location_output['location']['lat'])
        lng.append(location_output['location']['lng'])
    
    else:
        lat.append(np.nan)
        lng.append(np.nan)
        
df['lat'] = lat
df['lng'] = lng
df.head()
```


```python
mapping = folium.Map(location=[df['lat'].mean(), df['lng'].mean()],
                    zoom_start=11)

for n in df.index:
    if df['Address'][n] != 'Multiple':
        folium.Marker([df['lat'][n], df['lng'][n]],
                     popup=df['Cafe'][n]).add_to(mapping)
mapping
```


```python

```
