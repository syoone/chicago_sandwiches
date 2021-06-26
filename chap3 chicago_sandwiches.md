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




    <!DOCTYPE html>
    
    <html lang="en-US">
    <head>
    <meta charset="utf-8"/>
    <meta content="IE=edge" http-equiv="X-UA-Compatible">
    <link href="https://gmpg.org/xfn/11" rel="profile"/>
    <title>The 50 Best Sandwiches in Chicago – Chicago Magazine</title>
    <style type="text/css">			.heateorSssInstagramBackground{background:radial-gradient(circle at 30% 107%,#fdf497 0,#fdf497 5%,#fd5949 45%,#d6249f 60%,#285aeb 90%)}
    						div.heateor_sss_horizontal_sharing i.heateorSssInstagramBackground{background:#000!important;}div.heateor_sss_standard_follow_icons_container i.heateorSssInstagramBackground{background:#000;}
    										.heateor_sss_horizontal_sharing .heateorSssSharing,.heateor_sss_standard_follow_icons_container .heateorSssSharing{
    							background-color: #000;
    							color: #fff;
    						border-width: 0px;
    			border-style: solid;
    			border-color: transparent;
    		}
    				.heateor_sss_horizontal_sharing .heateorSssTCBackground{
    			color:#666;
    		}
    				.heateor_sss_horizontal_sharing .heateorSssSharing:hover,.heateor_sss_standard_follow_icons_container .heateorSssSharing:hover{
    						border-color: transparent;
    		}
    		.heateor_sss_vertical_sharing .heateorSssSharing,.heateor_sss_floating_follow_icons_container .heateorSssSharing{
    							color: #fff;
    						border-width: 0px;
    			border-style: solid;
    			border-color: transparent;
    		}
    				.heateor_sss_vertical_sharing .heateorSssTCBackground{
    			color:#666;
    		}
    				.heateor_sss_vertical_sharing .heateorSssSharing:hover,.heateor_sss_floating_follow_icons_container .heateorSssSharing:hover{
    						border-color: transparent;
    		}
    		
    		@media screen and (max-width:783px) {.heateor_sss_vertical_sharing{display:none!important}}@media screen and (max-width:783px) {.heateor_sss_floating_follow_icons_container{display:none!important}}</style><meta content="max-image-preview:large" name="robots"/>
    <link href="//use.fontawesome.com" rel="dns-prefetch">
    <link href="//s.w.org" rel="dns-prefetch"/>
    <link href="https://www.chicagomag.com/feed/" rel="alternate" title="Chicago Magazine » Feed" type="application/rss+xml"/>
    <link href="https://www.chicagomag.com/comments/feed/" rel="alternate" title="Chicago Magazine » Comments Feed" type="application/rss+xml"/>
    <link href="https://www.chicagomag.com/chicago-magazine/november-2012/best-sandwiches-chicago/feed/" rel="alternate" title="Chicago Magazine » The 50 Best Sandwiches in Chicago Comments Feed" type="application/rss+xml"/>
    <link href="https://www.chicagomag.com/wp-includes/css/dist/block-library/style.min.css?ver=5.7.2" id="wp-block-library-css" media="all" rel="stylesheet"/>
    <link href="https://www.chicagomag.com/wp-content/plugins/wordpress-popular-posts/assets/css/wpp.css?ver=5.2.4" id="wordpress-popular-posts-css-css" media="all" rel="stylesheet"/>
    <link href="//use.fontawesome.com/releases/v5.13.0/css/all.css?ver=5.7.2" id="font-awesome-free-css" media="all" rel="stylesheet"/>
    <link href="https://www.chicagomag.com/wp-content/themes/generatepress/assets/css/unsemantic-grid.min.css?ver=3.0.2" id="generate-style-grid-css" media="all" rel="stylesheet"/>
    <link href="https://www.chicagomag.com/wp-content/themes/generatepress/assets/css/style.min.css?ver=3.0.2" id="generate-style-css" media="all" rel="stylesheet"/>
    <style id="generate-style-inline-css">
    body{background-color:#efefef;color:#3a3a3a;}a{color:#1e73be;}a:hover, a:focus, a:active{color:#000000;}body .grid-container{max-width:1100px;}.wp-block-group__inner-container{max-width:1100px;margin-left:auto;margin-right:auto;}body, button, input, select, textarea{font-family:-apple-system, system-ui, BlinkMacSystemFont, "Segoe UI", Helvetica, Arial, sans-serif, "Apple Color Emoji", "Segoe UI Emoji", "Segoe UI Symbol";}body{line-height:1.5;}.entry-content > [class*="wp-block-"]:not(:last-child){margin-bottom:1.5em;}.main-title{font-size:45px;}.main-navigation .main-nav ul ul li a{font-size:14px;}.sidebar .widget, .footer-widgets .widget{font-size:17px;}h1{font-weight:300;font-size:40px;}h2{font-weight:300;font-size:30px;}h3{font-size:20px;}h4{font-size:inherit;}h5{font-size:inherit;}@media (max-width:768px){.main-title{font-size:30px;}h1{font-size:30px;}h2{font-size:25px;}}.top-bar{background-color:#636363;color:#ffffff;}.top-bar a{color:#ffffff;}.top-bar a:hover{color:#303030;}.site-header{background-color:#ffffff;color:#3a3a3a;}.site-header a{color:#3a3a3a;}.main-title a,.main-title a:hover{color:#222222;}.site-description{color:#757575;}.main-navigation,.main-navigation ul ul{background-color:#222222;}.main-navigation .main-nav ul li a,.menu-toggle, .main-navigation .menu-bar-items{color:#ffffff;}.main-navigation .main-nav ul li:hover > a,.main-navigation .main-nav ul li:focus > a, .main-navigation .main-nav ul li.sfHover > a, .main-navigation .menu-bar-item:hover > a, .main-navigation .menu-bar-item.sfHover > a{color:#ffffff;background-color:#3f3f3f;}button.menu-toggle:hover,button.menu-toggle:focus,.main-navigation .mobile-bar-items a,.main-navigation .mobile-bar-items a:hover,.main-navigation .mobile-bar-items a:focus{color:#ffffff;}.main-navigation .main-nav ul li[class*="current-menu-"] > a{color:#ffffff;background-color:#3f3f3f;}.main-navigation .main-nav ul li[class*="current-menu-"] > a:hover,.main-navigation .main-nav ul li[class*="current-menu-"].sfHover > a{color:#ffffff;background-color:#3f3f3f;}.navigation-search input[type="search"],.navigation-search input[type="search"]:active, .navigation-search input[type="search"]:focus, .main-navigation .main-nav ul li.search-item.active > a, .main-navigation .menu-bar-items .search-item.active > a{color:#ffffff;background-color:#3f3f3f;}.main-navigation ul ul{background-color:#3f3f3f;}.main-navigation .main-nav ul ul li a{color:#ffffff;}.main-navigation .main-nav ul ul li:hover > a,.main-navigation .main-nav ul ul li:focus > a,.main-navigation .main-nav ul ul li.sfHover > a{color:#ffffff;background-color:#4f4f4f;}.main-navigation .main-nav ul ul li[class*="current-menu-"] > a{color:#ffffff;background-color:#4f4f4f;}.main-navigation .main-nav ul ul li[class*="current-menu-"] > a:hover,.main-navigation .main-nav ul ul li[class*="current-menu-"].sfHover > a{color:#ffffff;background-color:#4f4f4f;}.separate-containers .inside-article, .separate-containers .comments-area, .separate-containers .page-header, .one-container .container, .separate-containers .paging-navigation, .inside-page-header{background-color:#ffffff;}.entry-meta{color:#595959;}.entry-meta a{color:#595959;}.entry-meta a:hover{color:#1e73be;}.sidebar .widget{background-color:#ffffff;}.sidebar .widget .widget-title{color:#000000;}.footer-widgets{background-color:#ffffff;}.footer-widgets .widget-title{color:#000000;}.site-info{color:#ffffff;background-color:#222222;}.site-info a{color:#ffffff;}.site-info a:hover{color:#606060;}.footer-bar .widget_nav_menu .current-menu-item a{color:#606060;}input[type="text"],input[type="email"],input[type="url"],input[type="password"],input[type="search"],input[type="tel"],input[type="number"],textarea,select{color:#666666;background-color:#fafafa;border-color:#cccccc;}input[type="text"]:focus,input[type="email"]:focus,input[type="url"]:focus,input[type="password"]:focus,input[type="search"]:focus,input[type="tel"]:focus,input[type="number"]:focus,textarea:focus,select:focus{color:#666666;background-color:#ffffff;border-color:#bfbfbf;}button,html input[type="button"],input[type="reset"],input[type="submit"],a.button,a.wp-block-button__link:not(.has-background){color:#ffffff;background-color:#666666;}button:hover,html input[type="button"]:hover,input[type="reset"]:hover,input[type="submit"]:hover,a.button:hover,button:focus,html input[type="button"]:focus,input[type="reset"]:focus,input[type="submit"]:focus,a.button:focus,a.wp-block-button__link:not(.has-background):active,a.wp-block-button__link:not(.has-background):focus,a.wp-block-button__link:not(.has-background):hover{color:#ffffff;background-color:#3f3f3f;}a.generate-back-to-top{background-color:rgba( 0,0,0,0.4 );color:#ffffff;}a.generate-back-to-top:hover,a.generate-back-to-top:focus{background-color:rgba( 0,0,0,0.6 );color:#ffffff;}@media (max-width:768px){.main-navigation .menu-bar-item:hover > a, .main-navigation .menu-bar-item.sfHover > a{background:none;color:#ffffff;}}.inside-top-bar{padding:10px;}.inside-header{padding:40px;}.entry-content .alignwide, body:not(.no-sidebar) .entry-content .alignfull{margin-left:-40px;width:calc(100% + 80px);max-width:calc(100% + 80px);}.rtl .menu-item-has-children .dropdown-menu-toggle{padding-left:20px;}.rtl .main-navigation .main-nav ul li.menu-item-has-children > a{padding-right:20px;}.site-info{padding:20px;}@media (max-width:768px){.separate-containers .inside-article, .separate-containers .comments-area, .separate-containers .page-header, .separate-containers .paging-navigation, .one-container .site-content, .inside-page-header, .wp-block-group__inner-container{padding:30px;}.site-info{padding-right:10px;padding-left:10px;}.entry-content .alignwide, body:not(.no-sidebar) .entry-content .alignfull{margin-left:-30px;width:calc(100% + 60px);max-width:calc(100% + 60px);}}.one-container .sidebar .widget{padding:0px;}@media (max-width:768px){.main-navigation .menu-toggle,.main-navigation .mobile-bar-items,.sidebar-nav-mobile:not(#sticky-placeholder){display:block;}.main-navigation ul,.gen-sidebar-nav{display:none;}[class*="nav-float-"] .site-header .inside-header > *{float:none;clear:both;}}
    </style>
    <link href="https://www.chicagomag.com/wp-content/themes/generatepress/assets/css/mobile.min.css?ver=3.0.2" id="generate-mobile-style-css" media="all" rel="stylesheet"/>
    <link href="https://www.chicagomag.com/wp-content/themes/generatepress/assets/css/components/font-icons.min.css?ver=3.0.2" id="generate-font-icons-css" media="all" rel="stylesheet"/>
    <link href="https://www.chicagomag.com/wp-content/themes/Chicago%20Magazine/style.css?ver=1621974083" id="generate-child-css" media="all" rel="stylesheet"/>
    <link href="https://www.chicagomag.com/wp-content/plugins/sassy-social-share/public/css/sassy-social-share-public.css?ver=3.3.20" id="heateor_sss_frontend_css-css" media="all" rel="stylesheet"/>
    <link href="https://www.chicagomag.com/wp-content/plugins/sassy-social-share/admin/css/sassy-social-share-svg.css?ver=3.3.20" id="heateor_sss_sharing_default_svg-css" media="all" rel="stylesheet"/>
    <link href="https://www.chicagomag.com/wp-content/plugins/youtube-embed-plus-pro/styles/ytprefs.min.css?ver=13.4.2" id="__EPYT__style-css" media="all" rel="stylesheet"/>
    <style id="__EPYT__style-inline-css">
    
                    .epyt-gallery-thumb {
                            width: 33.333%;
                    }
                    
                             @media (min-width:0px) and (max-width: 767px) {
                                .epyt-gallery-rowbreak {
                                    display: none;
                                }
                                .epyt-gallery-allthumbs[class*="epyt-cols"] .epyt-gallery-thumb {
                                    width: 100% !important;
                                }
                              }
    </style>
    <link href="https://www.chicagomag.com/wp-content/plugins/youtube-embed-plus-pro/scripts/lity.min.css?ver=13.4.2" id="__disptype__-css" media="all" rel="stylesheet"/>
    <script id="wpp-json" type="application/json">
    {"sampling_active":0,"sampling_rate":100,"ajax_url":"https:\/\/www.chicagomag.com\/wp-json\/wordpress-popular-posts\/v1\/popular-posts","ID":11772,"token":"ee45fc0e1e","lang":0,"debug":0}
    </script>
    <script id="wpp-js-js" src="https://www.chicagomag.com/wp-content/plugins/wordpress-popular-posts/assets/js/wpp.min.js?ver=5.2.4"></script>
    <script id="jquery-core-js" src="https://www.chicagomag.com/wp-includes/js/jquery/jquery.min.js?ver=3.5.1"></script>
    <script id="jquery-migrate-js" src="https://www.chicagomag.com/wp-includes/js/jquery/jquery-migrate.min.js?ver=3.3.2"></script>
    <script id="__dispload__-js" src="https://www.chicagomag.com/wp-content/plugins/youtube-embed-plus-pro/scripts/lity.min.js?ver=13.4.2"></script>
    <script id="__ytprefs__-js-extra">
    var _EPYT_ = {"ajaxurl":"https:\/\/www.chicagomag.com\/wp-admin\/admin-ajax.php","security":"a0163cfb87","gallery_scrolloffset":"20","eppathtoscripts":"https:\/\/www.chicagomag.com\/wp-content\/plugins\/youtube-embed-plus-pro\/scripts\/","eppath":"https:\/\/www.chicagomag.com\/wp-content\/plugins\/youtube-embed-plus-pro\/","epresponsiveselector":"[\"iframe.__youtube_prefs_widget__\"]","epdovol":"1","version":"13.4.2","evselector":"iframe.__youtube_prefs__[src], iframe[src*=\"youtube.com\/embed\/\"], iframe[src*=\"youtube-nocookie.com\/embed\/\"]","ajax_compat":"","ytapi_load":"light","pause_others":"","stopMobileBuffer":"1","vi_active":"","vi_js_posttypes":[]};
    </script>
    <script id="__ytprefs__-js" src="https://www.chicagomag.com/wp-content/plugins/youtube-embed-plus-pro/scripts/ytprefs.min.js?ver=13.4.2"></script>
    <link href="https://www.chicagomag.com/wp-json/" rel="https://api.w.org/"/><link href="https://www.chicagomag.com/wp-json/wp/v2/posts/11772" rel="alternate" type="application/json"/><link href="https://www.chicagomag.com/xmlrpc.php?rsd" rel="EditURI" title="RSD" type="application/rsd+xml"/>
    <link href="https://www.chicagomag.com/wp-includes/wlwmanifest.xml" rel="wlwmanifest" type="application/wlwmanifest+xml"/>
    <link href="https://www.chicagomag.com/chicago-magazine/november-2012/best-sandwiches-chicago/" rel="canonical"/>
    <link href="https://www.chicagomag.com/?p=11772" rel="shortlink"/>
    <link href="https://www.chicagomag.com/wp-json/oembed/1.0/embed?url=https%3A%2F%2Fwww.chicagomag.com%2Fchicago-magazine%2Fnovember-2012%2Fbest-sandwiches-chicago%2F" rel="alternate" type="application/json+oembed"/>
    <link href="https://www.chicagomag.com/wp-json/oembed/1.0/embed?url=https%3A%2F%2Fwww.chicagomag.com%2Fchicago-magazine%2Fnovember-2012%2Fbest-sandwiches-chicago%2F&amp;format=xml" rel="alternate" type="text/xml+oembed"/>
    <link href="https://www.chicagomag.com/xmlrpc.php" rel="pingback"/>
    <meta content="width=device-width, initial-scale=1" name="viewport"/><link href="https://www.chicagomag.com/wp-content/uploads/2021/02/favicon.png" rel="icon" sizes="32x32">
    <link href="https://www.chicagomag.com/wp-content/uploads/2021/02/favicon.png" rel="icon" sizes="192x192"/>
    <link href="https://www.chicagomag.com/wp-content/uploads/2021/02/favicon.png" rel="apple-touch-icon"/>
    <meta content="https://www.chicagomag.com/wp-content/uploads/2021/02/favicon.png" name="msapplication-TileImage">
    <!-- BEGIN Typekit Fonts for WordPress -->
    <link href="https://use.typekit.net/ukb3erh.css" rel="stylesheet"/>
    <!-- END Typekit Fonts for WordPress -->
    <!-- start seo fields -->
    <meta content="Our list of Chicago’s 50 best sandwiches, ranked in order of deliciousness" name="description"/>
    <meta content="sandwiches, dining" name="keywords"/>
    <meta content="en_US" property="og:locale"/>
    <meta content="article" property="og:type"/>
    <meta content="The 50 Best Sandwiches in Chicago" property="og:title"/>
    <meta content="https://www.chicagomag.com/wp-content/archive/Chicago-Magazine/November-2012/Best-Sandwiches-Chicago/sandwich-old-oak.jpg" property="og:image"/>
    <link href="https://www.chicagomag.com/Chicago-Magazine/November-2012/Best-Sandwiches-Chicago/" rel="canonical">
    <meta content="https://www.chicagomag.com/Chicago-Magazine/November-2012/Best-Sandwiches-Chicago/" property="og:url"/>
    <meta content="Chicago Magazine" property="og:site_name"/>
    <!--<meta property="article:tag" content="" />-->
    <meta content="Chicago Magazine" property="article:section"/>
    <!--
    <meta property="article:published_time" content="" />
    <meta property="article:modified_time" content="" />
    <meta property="og:updated_time" content="" />
    -->
    <meta content="summary_large_image" name="twitter:card"/>
    <meta content="https://www.chicagomag.com/wp-content/archive/Chicago-Magazine/November-2012/Best-Sandwiches-Chicago/sandwich-old-oak.jpg" name="twitter:image"/>
    <meta content="Our list of Chicago’s 50 best sandwiches, ranked in order of deliciousness" name="twitter:description"/>
    <meta content="The 50 Best Sandwiches in Chicago" name="twitter:title"/>
    <!-- end seo fields -->
    <!-- GA Google Analytics @ https://m0n.co/ga -->
    <script async="" src="https://www.googletagmanager.com/gtag/js?id=UA-297666-1"></script>
    <script>
    	window.dataLayer = window.dataLayer || [];
    	function gtag(){dataLayer.push(arguments);}
    	gtag('js', new Date());
    	gtag('config', 'UA-297666-1');
    </script>
    <!-- Google Tag Manager -->
    <script>(function(w,d,s,l,i){w[l]=w[l]||[];w[l].push({'gtm.start':
    new Date().getTime(),event:'gtm.js'});var f=d.getElementsByTagName(s)[0],
    j=d.createElement(s),dl=l!='dataLayer'?'&l='+l:'';j.async=true;j.src=
    'https://www.googletagmanager.com/gtm.js?id='+i+dl;f.parentNode.insertBefore(j,f);
    })(window,document,'script','dataLayer','GTM-P4M4MH7');</script>
    <!-- End Google Tag Manager -->
    <!-- start chartbeat code -->
    <script type="text/javascript">
     (function() {
     /** CONFIGURATION START **/
     var _sf_async_config = window._sf_async_config = (window._sf_async_config || {});
     _sf_async_config.uid = 25745;
     _sf_async_config.domain = 'chicagomag.com';
     _sf_async_config.flickerControl = false;
     _sf_async_config.useCanonical = true;
     _sf_async_config.useCanonicalDomain = true;
     _sf_async_config.sections = 'Chicago Magazine';
     _sf_async_config.authors = 'Chicago Magazine';
     /** CONFIGURATION END **/
     function loadChartbeat() {
     var e = document.createElement('script');
     var n = document.getElementsByTagName('script')[0];
     e.type = 'text/javascript';
     e.async = true;
     e.src = '//static.chartbeat.com/js/chartbeat.js';
     n.parentNode.insertBefore(e, n);
     }
     loadChartbeat();
     })();
    </script>
    <script async="" src="//static.chartbeat.com/js/chartbeat_mab.js"></script>
    <!-- end chartbeat code -->
    <!-- Start GPT Tag -->
    <script async="" src="https://securepubads.g.doubleclick.net/tag/js/gpt.js"></script>
    <script>
    	window.googletag = window.googletag || {cmd: []};
    	googletag.cmd.push(function() {
    		googletag.defineSlot('/4011/trb.chicagomag/hp', [[728,90]], 'div-gpt-ad-2789321-1')
    			.setTargeting('pos', ['1'])
    			.addService(googletag.pubads());
    		googletag.defineSlot('/4011/trb.chicagomag/hp', [[728,90]], 'div-gpt-ad-2789321-2')
    			.setTargeting('pos', ['2'])
    			.addService(googletag.pubads());
    		googletag.defineSlot('/4011/trb.chicagomag/hp', [[728,90]], 'div-gpt-ad-2789321-3')
    			.setTargeting('pos', ['3'])
    			.addService(googletag.pubads());
    		googletag.defineSlot('/4011/trb.chicagomag/hp', [[728,90]], 'div-gpt-ad-2789321-4')
    			.setTargeting('pos', ['4'])
    			.addService(googletag.pubads());
    		googletag.defineSlot('/4011/trb.chicagomag/hp', [[728,90]], 'div-gpt-ad-2789321-5')
    			.setTargeting('pos', ['5'])
    			.addService(googletag.pubads());
    		googletag.defineSlot('/4011/trb.chicagomag/hp', [[320,50]], 'div-gpt-ad-2789321-6')
    			.setTargeting('pos', ['1'])
    			.addService(googletag.pubads());
    		googletag.defineSlot('/4011/trb.chicagomag/hp', [[320,50]], 'div-gpt-ad-2789321-7')
    			.setTargeting('pos', ['2'])
    			.addService(googletag.pubads());
    		googletag.defineSlot('/4011/trb.chicagomag/hp', [[320,50]], 'div-gpt-ad-2789321-8')
    			.setTargeting('pos', ['3'])
    			.addService(googletag.pubads());
    		googletag.defineSlot('/4011/trb.chicagomag/hp', [[320,50]], 'div-gpt-ad-2789321-9')
    			.setTargeting('pos', ['4'])
    			.addService(googletag.pubads());
    		googletag.defineSlot('/4011/trb.chicagomag/hp', [[320,50]], 'div-gpt-ad-2789321-10')
    			.setTargeting('pos', ['5'])
    			.addService(googletag.pubads());
    		googletag.defineSlot('/4011/trb.chicagomag/hp', [[300,250]], 'div-gpt-ad-2789321-11')
    			.setTargeting('pos', ['1'])
    			.addService(googletag.pubads());
    		googletag.defineSlot('/4011/trb.chicagomag/hp', [[300,250],[300,600]], 'div-gpt-ad-2789321-12')
    			.setTargeting('pos', ['2'])
    			.addService(googletag.pubads());
    		googletag.defineSlot('/4011/trb.chicagomag/hp', [[300,250]], 'div-gpt-ad-2789321-13')
    			.setTargeting('pos', ['3'])
    			.addService(googletag.pubads());
    		googletag.defineSlot('/4011/trb.chicagomag/hp', [[300,250]], 'div-gpt-ad-2789321-14')
    			.setTargeting('pos', ['4'])
    			.addService(googletag.pubads());
    		googletag.defineSlot('/4011/trb.chicagomag/hp', [[300,250]], 'div-gpt-ad-2789321-15')
    			.setTargeting('pos', ['2'])
    			.addService(googletag.pubads());	
    
    		googletag.pubads().setTargeting('adcat', ['dining-drinking']);				
    		googletag.enableServices();
    	});
    </script>
    <!-- End GPT Tag -->
    <!-- below is header style for all pages besides home -->
    <style>
    
    	/* logo / nav
    	-------------------------------------------------------------- */
    	.site-header {
    		width: 18% !important;
    		display: table !important;
    		float: left !important;
    		height: 90px;
    	}
    
    	.inside-header {
    		display: table-cell !important;
    		vertical-align: bottom !important;
    		padding: 0 !important;
    		padding-left: 5vw !important;
    	}
    
    	.main-navigation {
    		width: 82% !important;
    		display: table !important;
    		position: relative !important;
    		float: left !important;
    		clear: inherit !important;
    		height: 90px;
    	}
    
    	.inside-navigation {
    		display: table-cell !important;
    		vertical-align: bottom !important;
    		padding-right: 5vw !important;
    		text-align: right !important;
    	}
    
    	.main-navigation ul {
    		border: 0 !important;
    		line-height: 1em !important;
    	}
    
    	.main-navigation .main-nav ul li a {
    		padding-left: 15px !important;
    		padding-right: 15px !important;
    		line-height: 1em !important;
    	}
    
    	.main-navigation .main-nav ul li:last-of-type a {
    		padding-right: 0 !important;
    	}
    
    	/* layout
    	-------------------------------------------------------------- */
    	.separate-containers .site-main {
    		margin-top: 0 !important;
    	}
    	
    .post-template-single-package-child.separate-containers .site-main {
    	margin-top: 3.05555vw !important;
    }
    
    	@media only screen and (max-width: 1024px) {
    		
    		.site-header {
    			width: 100% !important;
    			display: block !important;
    			float: none !important;
    			height: inherit !important;
    	}
    
    		.main-navigation ul {
    			border: 0 !important;
    			line-height: 1em !important;
    		}
    
    		.main-navigation .main-nav ul li a {
    			padding-left: 10px !important;
    			padding-right: 10px !important;
    			line-height: 1em !important;
    		}
    		
    		.inside-header {
    			display: block !important;
    			vertical-align: inherit !important;
    			padding: 3.75vw 0 0 0 !important;
    		}
    	
    		.site-logo {
    			display: inline-block;
    		}
    
    		.nav-aligned-center .main-navigation {
    			text-align: center;
    		}
    
    		.main-navigation {
    			width: 100% !important;
    			display: inline-block !important;
    			position: relative !important;
    			float: none !important;
    			clear: inherit !important;
    			height: inherit !important;
    		}
    
    		.inside-navigation {
    			display: inline-block !important;
    			vertical-align: inherit !important;
    			padding-right: 0 !important;
    			text-align: center !important;
    			margin: 0 auto !important;
    			margin-top: 3.75vw !important;
    		}
    
    	}
    
    	@media only screen and (max-width: 768px) {
    
    		.site-header {
    			width: 100% !important;
    			display: table !important;
    			float: left !important;
    			height: 90px;
    		}
    
    		.main-navigation, .inside-navigation {
    			display: none !important;
    		}
    
    	}
    
    </style>
    <style></style></link></meta></link></link></meta></head>
    <body class="post-template-default single single-post postid-11772 single-format-standard wp-custom-logo wp-embed-responsive no-sidebar nav-below-header separate-containers fluid-header active-footer-widgets-3 nav-aligned-center header-aligned-center dropdown-hover" itemscope="" itemtype="https://schema.org/Blog">
    <div class="grid-toggle-wrap"><a class="grid-toggle">.</a></div>
    <div class="grid-guide">
    <div class="grid-guide-col"><span>1</span></div>
    <div class="grid-guide-col"><span>2</span></div>
    <div class="grid-guide-col"><span>3</span></div>
    <div class="grid-guide-col"><span>4</span></div>
    <div class="grid-guide-col"><span>5</span></div>
    <div class="grid-guide-col"><span>6</span></div>
    <div class="grid-guide-col"><span>7</span></div>
    <div class="grid-guide-col"><span>8</span></div>
    <div class="grid-guide-col"><span>9</span></div>
    <div class="grid-guide-col"><span>10</span></div>
    <div class="grid-guide-col"><span>11</span></div>
    <div class="grid-guide-col"><span>12</span></div>
    <div class="grid-guide-col"><span>13</span></div>
    <div class="grid-guide-col"><span>14</span></div>
    <div class="grid-guide-col"><span>15</span></div>
    <div class="grid-guide-col"><span>16</span></div>
    <div class="grid-guide-col"><span>17</span></div>
    <div class="grid-guide-col"><span>18</span></div>
    <div class="grid-guide-col"><span>19</span></div>
    <div class="grid-guide-col"><span>20</span></div>
    <div class="grid-guide-col"><span>21</span></div>
    <div class="grid-guide-col"><span>22</span></div>
    <div class="grid-guide-col"><span>23</span></div>
    <div class="grid-guide-col"><span>24</span></div>
    </div>
    <div class="ad-space ad-space-leader top-ad-space hide-on-mobile">
    <!-- GPT AdSlot 1 for Ad unit 'trb.chicagomag/hp' ### Size: [[728,90]] -->
    <div id="div-gpt-ad-2789321-1">
    <script>
    			googletag.cmd.push(function() { googletag.display('div-gpt-ad-2789321-1'); });
    		</script>
    </div>
    <!-- End AdSlot 1 -->
    </div>
    <div class="ad-space ad-space-leader top-ad-space hide-on-desktop hide-on-tablet">
    <!-- GPT AdSlot 6 for Ad unit 'trb.chicagomag/hp' ### Size: [[320,50]] -->
    <div id="div-gpt-ad-2789321-6">
    <script>
    			googletag.cmd.push(function() { googletag.display('div-gpt-ad-2789321-6'); });
    		</script>
    </div>
    <!-- End AdSlot 6 -->
    </div>
    <div id="nav2-open">
    <a class="nav2-toggle"><i class="fa fa-bars"></i></a>
    </div>
    <div id="nav2-close">
    <a class="nav2-toggle"><i class="fa fa-times"></i></a>
    </div>
    <div id="nav2-overlay"></div>
    <div id="nav2-overlay-top"></div>
    <div id="nav2-overlay-btm"></div>
    <div id="nav2-inner-overlay">
    <div id="nav2-inner">
    <div class="grid-container grid-parent">
    <div class="grid-5 prefix-1 suffix-1 nav2-cover hide-on-mobile">
    <img src="/wp-content/uploads/2020/12/logo-alt.jpg"/>
    <img src=""/>
    <a href="https://cma.pcdfusion.com/pcd/Order?iKey=I**D7B" target="_blank">Subscribe</a>
    <a href="">Newsletters</a>
    <a class="nav-social" href="https://www.facebook.com/ChicagoMagazine" target="_blank"><i class="fab fa-facebook-f"></i></a>
    <a class="nav-social" href="http://www.twitter.com/chicagomag/" target="_blank"><i class="fab fa-twitter"></i></a>
    <a class="nav-social" href="http://instagram.com/chicagomag" target="_blank"><i class="fab fa-instagram"></i></a>
    <a class="nav-social" href="https://www.youtube.com/channel/UCOkRC6Y4LUyvglGmyC52KPw" target="_blank"><i class="fab fa-youtube"></i></a>
    </div>
    <div class="grid-100 nav2-cover hide-on-desktop">
    <img src="/wp-content/uploads/2020/12/logo-alt.jpg"/>
    <form action="https://www.chicagomag.com/" class="search-form" method="get">
    <label>
    <span class="screen-reader-text">Search for:</span>
    <input class="search-field" name="s" placeholder="Search …" title="Search for:" type="search" value=""/>
    </label>
    <input class="search-submit" type="submit" value="Search"/></form>
    </div>
    <div class="grid-7 prefix-1 suffix-1 mobile-grid-100 mobile-prefix-0 mobile-suffix-0">
    <div class="section-header">
    <div class="section-divide"></div>
    <h2>Sections</h2>
    </div>
    <a href="https://www.chicagomag.com/news/">News &amp; Politics</a>
    <a href="https://www.chicagomag.com/dining-drinking/">Dining &amp; Drinking</a>
    <a href="https://www.chicagomag.com/city-life/">City Life</a>
    <a href="https://www.chicagomag.com/arts-culture/">Culture</a>
    <a href="https://www.chicagomag.com/real-estate/">Real Estate</a>
    <a href="https://www.chicagomag.com/style-shopping/">Style</a>
    <div class="section-header">
    <div class="section-divide"></div>
    <h2>Featured</h2>
    </div>
    <a href="https://www.chicagomag.com/video/">Video</a>
    <a href="https://www.chicagomag.com/long-reads/">Long Reads</a>
    <a href="https://www.chicagomag.com/chicago-magazine/april-2020/best-new-restaurants/">Best New Restaurants</a>
    <a href="https://www.chicagomag.com/top-doctors/">Top Doctors</a>
    </div>
    <div class="grid-7 suffix-1 mobile-grid-100 mobile-suffix-1">
    <div class="section-header">
    <div class="section-divide"></div>
    <h2>Magazine</h2>
    </div>
    <a href="https://www.chicagomag.com/issue-archive/">All Issues</a>
    <a href="https://cma.pcdfusion.com/pcd/Order?iKey=I**D7B">Subscribe</a>
    <a href="https://cma.pcdfusion.com/pcd/CustomerSupport/Account/Login?ReturnUrl=%2fpcd%2fCustomerSupport%2fApp%2f3141">Manage Subscription</a>
    <a href="https://www.chicagomag.com/advertise/">Advertise</a>
    <div class="section-header">
    <div class="section-divide"></div>
    <h2>More</h2>
    </div>
    <a href="https://www.chicagomag.com/events/">Events</a>
    <a href="https://www.chicagomag.com/about-the-magazine/">About Us</a>
    <a href="https://www.chicagomag.com/contact-us/">Contact Us</a>
    <a href="https://www.chicagomag.com/follow-us/">Follow Us</a>
    <a href="https://www.chicagomag.com/resource-guide/">Resource Guide</a>
    </div>
    <div class="mobile-grid-100 hide-on-desktop" style="margin-bottom: 10vw;">
    <img src="/wp-content/archive/Chicago-Magazine/December-2020/CMAG1220.jpg" style="margin-top: 5vw;"/>
    <a href="https://cma.pcdfusion.com/pcd/Order?iKey=I**D7B">Subscribe</a>
    <a href="">Newsletters</a>
    <a class="nav-social" href="https://www.facebook.com/ChicagoMagazine" target="_blank"><i class="fab fa-facebook-f"></i></a>
    <a class="nav-social" href="http://www.twitter.com/chicagomag/" target="_blank"><i class="fab fa-twitter"></i></a>
    <a class="nav-social" href="http://instagram.com/chicagomag" target="_blank"><i class="fab fa-instagram"></i></a>
    <a class="nav-social" href="https://www.youtube.com/channel/UCOkRC6Y4LUyvglGmyC52KPw" target="_blank"><i class="fab fa-youtube"></i></a>
    </div>
    </div>
    </div>
    </div>
    <div id="top-right-nav">
    <div id="search-overlay">
    <div id="search-close">
    <a class="search-close-btn">
    <i class="fas fa-times"></i>
    </a>
    </div>
    <form action="https://www.chicagomag.com/" class="search-form" method="get">
    <label>
    <span class="screen-reader-text">Search for:</span>
    <input class="search-field" name="s" placeholder="Search …" title="Search for:" type="search" value=""/>
    </label>
    <input class="search-submit" type="submit" value="Search"/></form>
    </div>
    <div class="top-right-nav-links">
    <a class="search-open"><i class="fa fa-search"></i></a>
    <a href="/events/">Events</a>
    <a href="https://cma.pcdfusion.com/pcd/Order?iKey=I**D7B">Subscribe</a>
    </div>
    </div>
    <div id="navbar">
    <div id="nav2-open">
    <a class="nav2-toggle"><i class="fa fa-bars"></i></a>
    </div>
    <a href="/"><img class="navbar-logo" src="/wp-content/uploads/2020/10/logo.png"/></a>
    </div>
    <a class="screen-reader-text skip-link" href="#content" title="Skip to content">Skip to content</a> <header class="site-header" id="masthead" itemscope="" itemtype="https://schema.org/WPHeader">
    <div class="inside-header grid-container grid-parent">
    <div class="site-logo">
    <a href="https://www.chicagomag.com/" rel="home" title="Chicago Magazine">
    <img alt="Chicago Magazine" class="header-image is-logo-image" src="https://www.chicagomag.com/wp-content/uploads/2020/10/logo.png" title="Chicago Magazine">
    </img></a>
    </div> </div>
    </header>
    <nav class="main-navigation sub-menu-right" id="site-navigation" itemscope="" itemtype="https://schema.org/SiteNavigationElement">
    <div class="inside-navigation grid-container grid-parent">
    <button aria-controls="primary-menu" aria-expanded="false" class="menu-toggle">
    <span class="mobile-menu">Menu</span> </button>
    <div class="main-nav" id="primary-menu"><ul class=" menu sf-menu" id="menu-main"><li class="menu-item menu-item-type-taxonomy menu-item-object-category menu-item-32855" id="menu-item-32855"><a href="https://www.chicagomag.com/news/">News &amp; Politics</a></li>
    <li class="menu-item menu-item-type-taxonomy menu-item-object-category menu-item-32856" id="menu-item-32856"><a href="https://www.chicagomag.com/dining-drinking/">Dining &amp; Drinking</a></li>
    <li class="menu-item menu-item-type-taxonomy menu-item-object-category menu-item-33687" id="menu-item-33687"><a href="https://www.chicagomag.com/city-life/">City Life</a></li>
    <li class="menu-item menu-item-type-taxonomy menu-item-object-category menu-item-32857" id="menu-item-32857"><a href="https://www.chicagomag.com/arts-culture/">Culture</a></li>
    <li class="menu-item menu-item-type-taxonomy menu-item-object-category menu-item-32858" id="menu-item-32858"><a href="https://www.chicagomag.com/real-estate/">Real Estate</a></li>
    <li class="menu-item menu-item-type-taxonomy menu-item-object-category menu-item-32859" id="menu-item-32859"><a href="https://www.chicagomag.com/style-shopping/">Style</a></li>
    <li class="menu-item menu-item-type-post_type menu-item-object-page menu-item-29785" id="menu-item-29785"><a href="https://www.chicagomag.com/top-doctors/">Top Docs</a></li>
    </ul></div> </div>
    </nav>
    <div class="hfeed site grid-container container grid-parent" id="page">
    <div class="site-content" id="content">
    <div id="page-title"></div>
    <!-- start external content -->
    <!-- end external content -->
    <div class="content-area grid-parent mobile-grid-100 grid-100 tablet-grid-100" id="primary">
    <main class="site-main" id="main">
    <style>
    	
      .article-wrap {
    		margin-top: 2.22222vw !important;
    	}
    	
    	.single .article-img {
    		text-align: left;
    	}
      
      @media only screen and (max-width: 1024px) {
       
    		.container.grid-container {
          width: 100%;
        }
        
        .article-wrap .grid-10:first-of-type {
          display: none;
        }
    		
        .article-side {
          padding-left: 0 !important;
        }
        
        .article-img {
          max-width: 100%;
        }
        
      }
    
      @media only screen and (max-width: 480px) {
        
        .site-header {
    			width: 100% !important;
          height: 70px;
        }
        
        .main-navigation {
          display: none !important;
        }
        
        .article-body p, .article-body li {
          font-size: 18px;
        }
        
        .drop-cap {
          width: 70px;
          height: 70px;
          font-size: 60px;
          line-height: 70px;
        }
        
        .drop-cap-secondary {
          font-size: 60px;
          height: 45px;
        }
        
      }
      
    </style>
    <!-- start featured -->
    <!-- start super article featured image -->
    <!-- end super article featured image -->
    <!-- start head and deck -->
    <div class="grid-container grid-parent art-head-deck">
    <div class="grid-12 prefix-5 tablet-grid-14 tablet-prefix-0 mobile-grid-100 mobile-prefix-0">
    <div class="art-head h60">The 50 Best Sandwiches in Chicago</div>
    <div class="art-deck"><p>Our list of Chicago’s 50 best sandwiches, ranked in order of deliciousness</p>
    </div>
    <div class="art-byline-wrap">
    </div>
    <div class="art-timestamp">October 9, 2012, 6:12 pm</div>
    <div class="heateor_sss_sharing_container heateor_sss_horizontal_sharing" heateor-sss-data-href="https://www.chicagomag.com/chicago-magazine/november-2012/best-sandwiches-chicago/" ss-offset="0"><ul class="heateor_sss_sharing_ul"><li class="heateorSssSharingRound"><i alt="Facebook" class="heateorSssSharing heateorSssFacebookBackground" onclick='heateorSssPopup("https://www.facebook.com/sharer/sharer.php?u=https%3A%2F%2Fwww.chicagomag.com%2Fchicago-magazine%2Fnovember-2012%2Fbest-sandwiches-chicago%2F")' style="width:24px;height:24px;border-radius:999px;" title="Facebook"><ss class="heateorSssSharingSvg heateorSssFacebookSvg" style="display:block;border-radius:999px;"></ss></i></li><li class="heateorSssSharingRound"><i alt="Twitter" class="heateorSssSharing heateorSssTwitterBackground" onclick='heateorSssPopup("http://twitter.com/intent/tweet?text=The%2050%20Best%20Sandwiches%20in%20Chicago&amp;url=https%3A%2F%2Fwww.chicagomag.com%2Fchicago-magazine%2Fnovember-2012%2Fbest-sandwiches-chicago%2F")' style="width:24px;height:24px;border-radius:999px;" title="Twitter"><ss class="heateorSssSharingSvg heateorSssTwitterSvg" style="display:block;border-radius:999px;"></ss></i></li><li class="heateorSssSharingRound"><i alt="Email" class="heateorSssSharing heateorSssEmailBackground" onclick="window.open('mailto:?subject=' + decodeURIComponent('The%2050%20Best%20Sandwiches%20in%20Chicago' ).replace('&amp;', '%26') + '&amp;body=' + decodeURIComponent('https%3A%2F%2Fwww.chicagomag.com%2Fchicago-magazine%2Fnovember-2012%2Fbest-sandwiches-chicago%2F' ), '_blank')" style="width:24px;height:24px;border-radius:999px;" title="Email"><ss class="heateorSssSharingSvg heateorSssEmailSvg" style="display:block"></ss></i></li><li class="heateorSssSharingRound"><i alt="Copy Link" class="heateorSssSharing heateorSssCopyLinkBackground" style="width:24px;height:24px;border-radius:999px;" title="Copy Link"><ss class="heateorSssSharingSvg heateorSssCopyLinkSvg" style="display:block;border-radius:999px;"></ss></i></li><li class="heateorSssSharingRound"><i alt="Comment" class="heateorSssSharing heateorSssCommentBackground" style="width:24px;height:24px;border-radius:999px;" title="Comment"><a href="https://www.chicagomag.com/chicago-magazine/november-2012/best-sandwiches-chicago/#respond" rel="nofollow"><ss class="heateorSssSharingSvg heateorSssCommentSvg" style="display:block"></ss></a></i></li></ul><div class="heateorSssClear"></div></div>
    </div>
    </div>
    <!-- end head and deck -->
    <!-- start featured image below meta data -->
    <div class="grid-container grid-parent featured-img">
    <div class="grid-12 prefix-5 tablet-grid-14 tablet-prefix-0 mobile-grid-100 mobile-prefix-0">
    <div class="article-img">
    <figure>
    <img src="/wp-content/archive/Chicago-Magazine/November-2012/Best-Sandwiches-Chicago/sandwich-old-oak.jpg"/>
    <figcaption>BLT at Old Oak Tap, the No. 1 sandwich in Chicago. <span class="photo-credit">Photograph: Anna Knott; Food Stylist: Lisa Kuehl</span></figcaption>
    </figure>
    </div>
    </div>
    </div>
    <!-- end featured image below meta data -->
    <!-- end featured -->
    <!-- start article wrap -->
    <div class="grid-container grid-parent article-wrap">
    <div class="grid-4 hide-on-tablet hide-on-mobile"> </div>
    <div class="grid-12 prefix-1 tablet-grid-14 tablet-prefix-0 suffix-1 mobile-grid-100 mobile-prefix-0 mobile-suffix-0">
    <div class="article-body">
    <p><span class="dropcap">F</span>or generations, sandwiches were the ultimate guilty pleasure of subcultures that had no patience for guilt: hungry bachelors, school kids, working stiffs, old men in delis. To fridge-foraging rubes like Dagwood, quality wasn’t half as important as quantity. The sandwich was one of the only snacks you were allowed to pile as high as you wanted with anything you desired and cram into your face with both hands—a meal so inelegant and blithely proud of its inelegance that it came in six-foot segments for parties. And we ate it. Standing up.</p>
    <section class="related-content pull-right">
    <h3>Related Content</h3>
    <ul>
    <li><a href="https://www.chicagomag.com/Chicago-Magazine/November-2012/Best-Sandwiches-in-
    Chicago-The-Best-Sliders-in-Town">The Best Sliders in Town</a></li>
    <li><a href="https://www.chicagomag.com/Chicago-Magazine/November-2012/Best-Sandwiches-in-
    Chicago-Where-to-Get-Your-Fix-Around-the-Clock">Where to Get Your Fix Around the Clock</a></li>
    </ul>
    </section>
    <p>Now we’ve got French dips made with shaved prime rib, po’ boys with organic shrimp, and grilled cheese with fancy pimiento cheese. Hell, you can get a buttered ciabatta layered with local eggs, house-cured speck, and fontina for breakfast at Balsan if the idea of spending $19 for a ham and egg sandwich does not scandalize you. What in the name of John Montagu is going on here?</p>
    <p>The sandwich pendulum has always swung erratically from the treat of the nobility to the fuel of the proletariat. But what we’re witnessing now is the sharpest swerve yet toward the land of fine dining—a shift that overlaps, not coincidentally, with the great democratization of Chicago’s restaurants. Ground zero for the boom is Publican Quality Meats, where Paul Kahan regards sandwiches as serious dishes. So does Acadia’s Ryan McCaskey, who makes a mean lobster roll, and Rick Bayless, who offers up a vegetarian stunner at Xoco.</p>
    <p>To guide you through the bustling sandscape, we fanned out across the city and suburbs, hitting spots high and low in search of anything delicious between two slices of bread. For the purposes of this story, we defined “sandwich” in the strictest of terms: no wraps, dumplings, or open-faced pretenders. Hamburgers and hot dogs didn’t qualify. Italian beef sandwiches did, but not one made this list. (Face facts: Chicago’s spongy grease bomb is not among the better contributions to the genre.) We gave points to the well crafted, the fresh, and the robust, anchored by bread with enough distinct character to bolster the proceedings without overshadowing or interfering.</p>
    <p>The result: our list of Chicago’s 50 best sandwiches, ranked in order of deliciousness. Some are ingenious, such as Scofflaw’s layered masterpiece of braised brisket, pork belly, and pork loin. Others are blunt and glorious classics, done simply and done right. (Meatball sub from Bari, take a bow.)</p>
    <p>In our research, we learned that the sandwich is a wily chameleon, soaking up and synthesizing every trend, be it the resurgence of house-cured charcuterie or the sudden ubiquity of arugula. We learned to ask for extra napkins ahead of time. And we learned, above all, that quality and quantity can intersect in restaurants, and there’s no shame in that. Only joy.</p>
    <div class="sammy" style="position: relative;">
    <div class="sammyRank">1</div>
    <div class="sammyListing"><a href="/Chicago-Magazine/November-2012/Best-Sandwiches-in-Chicago-Old-Oak-Tap-BLT/"><b>BLT</b><br/>
    Old Oak Tap<br/>
    <em>Read more</em> </a></div>
    </div>
    <div class="sammy" style="position: relative;">
    <div class="sammyRank">2</div>
    <div class="sammyListing"><a href="/Chicago-Magazine/November-2012/Best-Sandwiches-in-Chicago-Au-Cheval-Fried-Bologna/"><b>Fried Bologna</b><br/>
    Au Cheval<br/>
    <em>Read more</em> </a></div>
    </div>
    <div class="sammy" style="position: relative;">
    <div class="sammyRank">3</div>
    <div class="sammyListing"><a href="/Chicago-Magazine/November-2012/Best-Sandwiches-in-Chicago-Xoco-Woodland-Mushroom/"><b>Woodland Mushroom</b><br/>
    Xoco<br/>
    <em>Read more</em> </a></div>
    </div>
    <div class="sammy" style="position: relative;">
    <div class="sammyRank">4</div>
    <div class="sammyListing"><a href="/Chicago-Magazine/November-2012/Best-Sandwiches-in-Chicago-Als-Deli-Roast-Beef/"><b>Roast Beef</b><br/>
    Al’s Deli<br/>
    <em>Read more</em> </a></div>
    </div>
    <div class="sammy" style="position: relative;">
    <div class="sammyRank">5</div>
    <div class="sammyListing"><a href="/Chicago-Magazine/November-2012/Best-Sandwiches-in-Chicago-Publican-Quality-Meats-PB-L/"><b>PB&amp;L</b><br/>
    Publican Quality Meats<br/>
    <em>Read more</em> </a></div>
    </div>
    <div class="sammy" style="position: relative;">
    <div class="sammyRank">6</div>
    <div class="sammyListing"><a href="https://www.chicagomag.com/Chicago-Magazine/November-2012/Best-Sandwiches-in-Chicago-Hendrickx-Belgian-Bread-Crafter-Belgian-Chicken-Curry-Salad/"><b>Belgian Chicken Curry Salad</b><br/>
    Hendrickx Belgian Bread Crafter<br/>
    <em>Read more</em> </a></div>
    </div>
    <div class="sammy" style="position: relative;">
    <div class="sammyRank">7</div>
    <div class="sammyListing"><a href="/Chicago-Magazine/November-2012/Best-Sandwiches-in-Chicago-Acadia-Lobster-Roll/"><b>Lobster Roll</b><br/>
    Acadia<br/>
    <em>Read more</em> </a></div>
    </div>
    <div class="sammy" style="position: relative;">
    <div class="sammyRank">8</div>
    <div class="sammyListing"><a href="/Chicago-Magazine/November-2012/Best-Sandwiches-in-Chicago-Birchwood-Kitchen-Smoked-Salmon-Salad/"><b>Smoked Salmon Salad</b><br/>
    Birchwood Kitchen<br/>
    <em>Read more</em> </a></div>
    </div>
    <div class="sammy" style="position: relative;">
    <div class="sammyRank">9</div>
    <div class="sammyListing"><a href="/Chicago-Magazine/November-2012/Best-Sandwiches-in-Chicago-Cemitas-Puebla-Atomica-Cemitas/"><b>Atomica Cemitas</b><br/>
    Cemitas Puebla<br/>
    <em>Read more</em> </a></div>
    </div>
    <div class="sammy" style="position: relative;">
    <div class="sammyRank">10</div>
    <div class="sammyListing"><a href="/Chicago-Magazine/November-2012/Best-Sandwiches-in-Chicago-Nana-Grilled-Laughing-Bird-Shrimp-and-Fried-Oyster-Po-Boy/"><b>Grilled Laughing Bird Shrimp and Fried Po’ Boy</b><br/>
    Nana<br/>
    <em>Read more</em> </a></div>
    </div>
    <div class="sammy" style="position: relative;">
    <div class="sammyRank">11</div>
    <div class="sammyListing"><a href="https://www.chicagomag.com/Chicago-Magazine/November-2012/Best-Sandwiches-in-Chicago-Lula-Cafe-Ham-and-Raclette-Panino/"><b>Ham and Raclette Panino</b><br/>
    Lula Cafe<br/>
    <em>Read more</em> </a></div>
    </div>
    <div class="sammy" style="position: relative;">
    <div class="sammyRank">12</div>
    <div class="sammyListing"><a href="https://www.chicagomag.com/Chicago-Magazine/November-2012/Best-Sandwiches-in-Chicago-Ricobenes-Breaded-Steak/"><b>Breaded Steak</b><br/>
    Ricobene’s<br/>
    <em>Read more</em> </a></div>
    </div>
    <div class="sammy" style="position: relative;">
    <div class="sammyRank">13</div>
    <div class="sammyListing"><a href="https://www.chicagomag.com/Chicago-Magazine/November-2012/Best-Sandwiches-in-Chicago-Frog-n-Snail-The-Hawkeye/"><b>The Hawkeye</b><br/>
    Frog n Snail<br/>
    <em>Read more</em> </a></div>
    </div>
    <div class="sammy" style="position: relative;">
    <div class="sammyRank">14</div>
    <div class="sammyListing"><a href="https://www.chicagomag.com/Chicago-Magazine/November-2012/Best-Sandwiches-in-Chicago-Crosbys-Kitchen-Chicken-Dip/"><b>Chicken Dip</b><br/>
    Crosby’s Kitchen<br/>
    <em>Read more</em> </a></div>
    </div>
    <div class="sammy" style="position: relative;">
    <div class="sammyRank">15</div>
    <div class="sammyListing"><a href="https://www.chicagomag.com/Chicago-Magazine/November-2012/Best-Sandwiches-in-Chicago-Longman-and-Eagle-Wild-Boar-Sloppy-Joe/"><b>Wild Boar Sloppy Joe</b><br/>
    Longman &amp; Eagle<br/>
    <em>Read more</em> </a></div>
    </div>
    <div class="sammy" style="position: relative;">
    <div class="sammyRank">16</div>
    <div class="sammyListing"><a href="https://www.chicagomag.com/Chicago-Magazine/November-2012/Best-Sandwiches-in-Chicago-Bari-Meatball-Sub/"><b>Meatball Sub</b><br/>
    Bari<br/>
    <em>Read more</em> </a></div>
    </div>
    <div class="sammy" style="position: relative;">
    <div class="sammyRank">17</div>
    <div class="sammyListing"><a href="https://www.chicagomag.com/Chicago-Magazine/November-2012/Best-Sandwiches-in-Chicago-Mannys-Corned-Beef/"><b>Corned Beef</b><br/>
    Manny’s<br/>
    <em>Read more</em> </a></div>
    </div>
    <div class="sammy" style="position: relative;">
    <div class="sammyRank">18</div>
    <div class="sammyListing"><a href="https://www.chicagomag.com/Chicago-Magazine/November-2012/Best-Sandwiches-in-Chicago-Eggys-Turkey-Club/"><b>Turkey Club</b><br/>
    Eggy’s<br/>
    <em>Read more</em> </a></div>
    </div>
    <div class="sammy" style="position: relative;">
    <div class="sammyRank">19</div>
    <div class="sammyListing"><a href="https://www.chicagomag.com/Chicago-Magazine/November-2012/Best-Sandwiches-in-Chicago-Old-Jerusalem-Falafel/"><b>Falafel</b><br/>
    Old Jerusalem<br/>
    <em>Read more</em> </a></div>
    </div>
    <div class="sammy" style="position: relative;">
    <div class="sammyRank">20</div>
    <div class="sammyListing"><a href="https://www.chicagomag.com/Chicago-Magazine/November-2012/Best-Sandwiches-in-Chicago-Mindys-HotChocolate-Crab-Cake/"><b>Crab Cake</b><br/>
    Mindy’s HotChocolate<br/>
    <em>Read more</em> </a></div>
    </div>
    <div class="sammy" style="position: relative;">
    <div class="sammyRank">21</div>
    <div class="sammyListing"><a href="https://www.chicagomag.com/Chicago-Magazine/November-2012/Best-Sandwiches-in-Chicago-Olgas-Delicatessen-Chicken-Schnitzel/"><b>Chicken Schnitzel</b><br/>
    Olga’s Delicatessen<br/>
    <em>Read more</em> </a></div>
    </div>
    <div class="sammy" style="position: relative;">
    <div class="sammyRank">22</div>
    <div class="sammyListing"><a href="https://www.chicagomag.com/Chicago-Magazine/November-2012/Best-Sandwiches-in-Chicago-Dawali-Mediterranean-Kitchen-Shawarma/"><b>Shawarma</b><br/>
    Dawali Mediterranean Kitchen<br/>
    <em>Read more</em> </a></div>
    </div>
    <div class="sammy" style="position: relative;">
    <div class="sammyRank">23</div>
    <div class="sammyListing"><a href="https://www.chicagomag.com/Chicago-Magazine/November-2012/Best-Sandwiches-in-Chicago-Big-Jones-Toasted-Pimiento-Cheese/"><b>Toasted Pimiento Cheese</b><br/>
    Big Jones<br/>
    <em>Read more</em> </a></div>
    </div>
    <div class="sammy" style="position: relative;">
    <div class="sammyRank">24</div>
    <div class="sammyListing"><a href="https://www.chicagomag.com/Chicago-Magazine/November-2012/Best-Sandwiches-in-Chicago-La-Pane-Vegetarian-Panino/"><b>Vegetarian Panino</b><br/>
    La Pane<br/>
    <em>Read more</em> </a></div>
    </div>
    <div class="sammy" style="position: relative;">
    <div class="sammyRank">25</div>
    <div class="sammyListing"><a href="/Chicago-Magazine/November-2012/Best-Sandwiches-in-Chicago-Pastoral-Cali-Chevre/"><b>Cali Chèvre</b><br/>
    Pastoral<br/>
    <em>Read more</em> </a></div>
    </div>
    <div class="sammy" style="position: relative;">
    <div class="sammyRank">26</div>
    <div class="sammyListing"><a href="https://www.chicagomag.com/Chicago-Magazine/November-2012/Best-Sandwiches-in-Chicago-Maxs-Deli-Pastrami/"><b>Pastrami</b><br/>
    Max’s Deli<br/>
    <em>Read more</em> </a></div>
    </div>
    <div class="sammy" style="position: relative;">
    <div class="sammyRank">27</div>
    <div class="sammyListing"><a href="https://www.chicagomag.com/Chicago-Magazine/November-2012/Best-Sandwiches-in-Chicago-Luckys-Sandwich-Co-The-Fredo/"><b>The Fredo</b><br/>
    Lucky’s Sandwich Co.<br/>
    <em>Read more</em> </a></div>
    </div>
    <div class="sammy" style="position: relative;">
    <div class="sammyRank">28</div>
    <div class="sammyListing"><a href="https://www.chicagomag.com/Chicago-Magazine/November-2012/Best-Sandwiches-in-Chicago-City-Provisions-Smoked-Ham/"><b>Smoked Ham</b><br/>
    City Provisions<br/>
    <em>Read more</em> </a></div>
    </div>
    <div class="sammy" style="position: relative;">
    <div class="sammyRank">29</div>
    <div class="sammyListing"><a href="https://www.chicagomag.com/Chicago-Magazine/November-2012/Best-Sandwiches-in-Chicago-Papas-Cache-Sabroso-Jibarito/"><b>Jibarito</b><br/>
    Papa’s Cache Sabroso<br/>
    <em>Read more</em> </a></div>
    </div>
    <div class="sammy" style="position: relative;">
    <div class="sammyRank">30</div>
    <div class="sammyListing"><a href="https://www.chicagomag.com/Chicago-Magazine/November-2012/Best-Sandwiches-in-Chicago-Bavettes-Bar-and-Boeuf-Shaved-Prime-Rib/"><b>Shaved Prime Rib</b><br/>
    Bavette’s Bar &amp; Boeuf<br/>
    <em>Read more</em> </a></div>
    </div>
    <div class="sammy" style="position: relative;">
    <div class="sammyRank">31</div>
    <div class="sammyListing"><a href="https://www.chicagomag.com/Chicago-Magazine/November-2012/Best-Sandwiches-in-Chicago-Hannahs-Bretzel-Serrano-Ham-and-Manchego-Cheese/"><b>Serrano Ham and Manchego Cheese</b><br/>
    Hannah’s Bretzel<br/>
    <em>Read more</em> </a></div>
    </div>
    <div class="sammy" style="position: relative;">
    <div class="sammyRank">32</div>
    <div class="sammyListing"><a href="https://www.chicagomag.com/Chicago-Magazine/November-2012/Best-Sandwiches-in-Chicago-La-Fournette-Tuna-Salad/"><b>Tuna Salad</b><br/>
    La Fournette<br/>
    <em>Read more</em> </a></div>
    </div>
    <div class="sammy" style="position: relative;">
    <div class="sammyRank">33</div>
    <div class="sammyListing"><a href="https://www.chicagomag.com/Chicago-Magazine/November-2012/Best-Sandwiches-in-Chicago-Paramount-Room-Paramount-Reuben/"><b>Paramount Reuben</b><br/>
    Paramount Room<br/>
    <em>Read more</em> </a></div>
    </div>
    <div class="sammy" style="position: relative;">
    <div class="sammyRank">34</div>
    <div class="sammyListing"><a href="https://www.chicagomag.com/Chicago-Magazine/November-2012/Best-Sandwiches-in-Chicago-Melt-Sandwich-Shoppe-The-Istanbul/"><b>The Istanbul</b><br/>
    Melt Sandwich Shoppe<br/>
    <em>Read more</em> </a></div>
    </div>
    <div class="sammy" style="position: relative;">
    <div class="sammyRank">35</div>
    <div class="sammyListing"><a href="https://www.chicagomag.com/Chicago-Magazine/November-2012/Best-Sandwiches-in-Chicago-Floriole-Cafe-and-Bakery-BAD/"><b>B.A.D.</b><br/>
    Floriole Cafe &amp; Bakery<br/>
    <em>Read more</em> </a></div>
    </div>
    <div class="sammy" style="position: relative;">
    <div class="sammyRank">36</div>
    <div class="sammyListing"><a href="https://www.chicagomag.com/Chicago-Magazine/November-2012/Best-Sandwiches-in-Chicago-First-Slice-Pie-Cafe-Duck-Confit-and-Mozzarella/"><b>Duck Confit and Mozzarella</b><br/>
    First Slice Pie Café<br/>
    <em>Read more</em> </a></div>
    </div>
    <div class="sammy" style="position: relative;">
    <div class="sammyRank">37</div>
    <div class="sammyListing"><a href="https://www.chicagomag.com/Chicago-Magazine/November-2012/Best-Sandwiches-in-Chicago-Troquet-Croque-Monsieur/"><b>Croque Monsieur</b><br/>
    Troquet<br/>
    <em>Read more</em> </a></div>
    </div>
    <div class="sammy" style="position: relative;">
    <div class="sammyRank">38</div>
    <div class="sammyListing"><a href="https://www.chicagomag.com/Chicago-Magazine/November-2012/Best-Sandwiches-in-Chicago-Grahamwich-Green-Garbanzo/"><b>Green Garbanzo</b><br/>
    Grahamwich<br/>
    <em>Read more</em> </a></div>
    </div>
    <div class="sammy" style="position: relative;">
    <div class="sammyRank">39</div>
    <div class="sammyListing"><a href="https://www.chicagomag.com/Chicago-Magazine/November-2012/Best-Sandwiches-in-Chicago-Saigon-Sisters-The-Hen-House/"><b>The Hen House</b><br/>
    Saigon Sisters<br/>
    <em>Read more</em> </a></div>
    </div>
    <div class="sammy" style="position: relative;">
    <div class="sammyRank">40</div>
    <div class="sammyListing"><a href="https://www.chicagomag.com/Chicago-Magazine/November-2012/Best-Sandwiches-in-Chicago-Rosalias-Deli-Tuscan-Chicken/"><b>Tuscan Chicken</b><br/>
    Rosalia’s Deli<br/>
    <em>Read more</em> </a></div>
    </div>
    <div class="sammy" style="position: relative;">
    <div class="sammyRank">41</div>
    <div class="sammyListing"><a href="https://www.chicagomag.com/Chicago-Magazine/November-2012/Best-Sandwiches-in-Chicago-Z-and-H-MarketCafe-The-Marty/"><b>The Marty </b><br/>
    Z&amp;H MarketCafe<br/>
    <em>Read more</em> </a></div>
    </div>
    <div class="sammy" style="position: relative;">
    <div class="sammyRank">42</div>
    <div class="sammyListing"><a href="https://www.chicagomag.com/Chicago-Magazine/November-2012/Best-Sandwiches-in-Chicago-Market-House-on-the-Square-Whitefish/"><b>Whitefish</b><br/>
    Market House on the Square<br/>
    <em>Read more</em> </a></div>
    </div>
    <div class="sammy" style="position: relative;">
    <div class="sammyRank">43</div>
    <div class="sammyListing"><a href="https://www.chicagomag.com/Chicago-Magazine/November-2012/Best-Sandwiches-in-Chicago-Elaines-Coffee-Call-Oat-Bread-Pecan-Butter-and-Fruit-Jam/"><b>Oat Bread, Pecan Butter, and Fruit Jam</b><br/>
    Elaine’s Coffee Call<br/>
    <em>Read more</em> </a></div>
    </div>
    <div class="sammy" style="position: relative;">
    <div class="sammyRank">44</div>
    <div class="sammyListing"><a href="https://www.chicagomag.com/Chicago-Magazine/November-2012/Best-Sandwiches-in-Chicago-Marion-Street-Cheese-Market-Cauliflower-Melt/"><b>Cauliflower Melt</b><br/>
    Marion Street Cheese Market<br/>
    <em>Read more</em> </a></div>
    </div>
    <div class="sammy" style="position: relative;">
    <div class="sammyRank">45</div>
    <div class="sammyListing"><a href="https://www.chicagomag.com/Chicago-Magazine/November-2012/Best-Sandwiches-in-Chicago-Cafecito-Cubano/"><b>Cubana</b><br/>
    Cafecito<br/>
    <em>Read more</em> </a></div>
    </div>
    <div class="sammy" style="position: relative;">
    <div class="sammyRank">46</div>
    <div class="sammyListing"><a href="https://www.chicagomag.com/Chicago-Magazine/November-2012/Best-Sandwiches-in-Chicago-Chickpea-Kufta/"><b>Kufta</b><br/>
    Chickpea<br/>
    <em>Read more</em> </a></div>
    </div>
    <div class="sammy" style="position: relative;">
    <div class="sammyRank">47</div>
    <div class="sammyListing"><a href="https://www.chicagomag.com/Chicago-Magazine/November-2012/Best-Sandwiches-in-Chicago-The-Goddess-and-Grocer-Debbies-Egg-Salad/"><b>Debbie’s Egg Salad</b><br/>
    The Goddess and Grocer<br/>
    <em>Read more</em> </a></div>
    </div>
    <div class="sammy" style="position: relative;">
    <div class="sammyRank">48</div>
    <div class="sammyListing"><a href="https://www.chicagomag.com/Chicago-Magazine/November-2012/Best-Sandwiches-in-Chicago-Zenwich-Beef-Curry/"><b>Beef Curry</b><br/>
    Zenwich<br/>
    <em>Read more</em> </a></div>
    </div>
    <div class="sammy" style="position: relative;">
    <div class="sammyRank">49</div>
    <div class="sammyListing"><a href="https://www.chicagomag.com/Chicago-Magazine/November-2012/Best-Sandwiches-in-Chicago-Toni-Patisserie-Le-Vegetarien/"><b>Le Végétarien</b><br/>
    Toni Patisserie<br/>
    <em>Read more</em> </a></div>
    </div>
    <div class="sammy" style="position: relative; border-bottom: 0">
    <div class="sammyRank">50</div>
    <div class="sammyListing"><a href="https://www.chicagomag.com/Chicago-Magazine/November-2012/Best-Sandwiches-in-Chicago-Phoebes-Bakery-The-Gatsby/"><b>The Gatsby</b><br/>
    Phoebe’s Bakery<br/>
    <em>Read more</em> </a></div>
    </div>
    <p><!-- /#sandwichFront --></p>
    <footer>Edited by Carly Boers, Penny Pollack, and Jeff Ruby; Contributors: Cassie Walker Burke, Elly Fishman, Peter Gianopulos, Noah Isackson, Maryanne Johnson, Esther Kang, Megan Lovejoy, Graham Meyer, Matt Schur, Lena Singer, Emmet Sullivan, Jennifer Tanaka, Joanne Trestrail</footer>
    </div>
    <div class="article-tags">
    <p>Tags: <a href="https://www.chicagomag.com/tag/best-of-chicago/" rel="tag">Best of Chicago</a>, <a href="https://www.chicagomag.com/tag/dining-drinking/" rel="tag">Dining &amp; Drinking</a>, <a href="https://www.chicagomag.com/tag/print-specific-tags-cover-story/" rel="tag">Print-Specific Tags - Cover Story</a></p> </div>
    </div>
    <div class="article-side grid-6 tablet-grid-9 mobile-grid-100 most-pop">
    <div class="ad-space">
    <!-- GPT AdSlot 12 for Ad unit 'trb.chicagomag/hp' ### Size: [[300,250],[300,600]] -->
    <div class="hide-on-mobile" id="div-gpt-ad-2789321-12">
    <script>
    					googletag.cmd.push(function() { googletag.display('div-gpt-ad-2789321-12'); });
    				</script>
    </div>
    <!-- End AdSlot 12 -->
    <!-- GPT AdSlot 15 for Ad unit 'trb.chicagomag/hp' ### Size: [[300,250] -->
    <div class="hide-on-desktop hide-on-tablet" id="div-gpt-ad-2789321-15">
    <script>
    					googletag.cmd.push(function() { googletag.display('div-gpt-ad-2789321-15'); });
    				</script>
    </div>
    <!-- End AdSlot 15 -->
    <!-- GPT AdSlot 11 for Ad unit 'trb.chicagomag/hp' ### Size: [[300,250]] -->
    <div id="div-gpt-ad-2789321-11">
    <script>
    					googletag.cmd.push(function() { googletag.display('div-gpt-ad-2789321-11'); });
    				</script>
    </div>
    <!-- End AdSlot 11 -->
    </div>
    </div>
    </div>
    <!-- end article wrap -->
    <!-- start ad -->
    <div class="grid-container grid-parent ad-space ad-space-leader hide-on-mobile mb-0">
    <!-- GPT AdSlot 5 for Ad unit 'trb.chicagomag/hp' ### Size: [[728,90]] -->
    <div id="div-gpt-ad-2789321-5">
    <script>
    			googletag.cmd.push(function() { googletag.display('div-gpt-ad-2789321-5'); });
    		</script>
    </div>
    <!-- End AdSlot 5 -->
    </div>
    <div class="grid-container grid-parent ad-space ad-space-leader hide-on-desktop hide-on-tablet">
    <!-- GPT AdSlot 10 for Ad unit 'trb.chicagomag/hp' ### Size: [[320,50]] -->
    <div id="div-gpt-ad-2789321-10">
    <script>
    			googletag.cmd.push(function() { googletag.display('div-gpt-ad-2789321-10'); });
    		</script>
    </div>
    <!-- End AdSlot 10 -->
    </div>
    <!-- end ad -->
    <div class="comments-area grid-container grid-parent">
    <div class="grid-12 prefix-5 mobile-grid-100 mobile-prefix-0">
    <div id="comments">
    <div class="comment-respond" id="respond">
    <h3 class="comment-reply-title" id="reply-title">Leave a Comment <small><a href="/Chicago-Magazine/November-2012/Best-Sandwiches-Chicago/#respond" id="cancel-comment-reply-link" rel="nofollow" style="display:none;">Cancel reply</a></small></h3><form action="https://www.chicagomag.com/wp-comments-post.php?wpe-comment-post=chicagomag" class="comment-form" id="commentform" method="post" novalidate=""><p class="comment-form-comment"><label class="screen-reader-text" for="comment">Comment</label><textarea aria-required="true" autocomplete="new-password" cols="45" id="c2cc66bfa4" name="c2cc66bfa4" required="" rows="8"></textarea><textarea aria-hidden="true" autocomplete="new-password" id="comment" name="comment" style="padding:0 !important;clip:rect(1px, 1px, 1px, 1px) !important;position:absolute !important;white-space:nowrap !important;height:1px !important;width:1px !important;overflow:hidden !important;" tabindex="-1"></textarea><script data-noptimize="" type="text/javascript">document.getElementById("comment").setAttribute( "id", "af362f7da489aa7be7d3f27c31e01a2f" );document.getElementById("c2cc66bfa4").setAttribute( "id", "comment" );</script></p><label class="screen-reader-text" for="author">Name</label><input id="author" name="author" placeholder="Name *" size="30" type="text" value="">
    <label class="screen-reader-text" for="email">Email</label><input id="email" name="email" placeholder="Email *" size="30" type="email" value="">
    <label class="screen-reader-text" for="url">Website</label><input id="url" name="url" placeholder="Website" size="30" type="url" value="">
    <p class="comment-form-cookies-consent"><input id="wp-comment-cookies-consent" name="wp-comment-cookies-consent" type="checkbox" value="yes"> <label for="wp-comment-cookies-consent">Save my name, email, and website in this browser for the next time I comment.</label></input></p>
    <p class="form-submit"><input class="submit" id="submit" name="submit" type="submit" value="Post Comment"/> <input id="comment_post_ID" name="comment_post_ID" type="hidden" value="11772"/>
    <input id="comment_parent" name="comment_parent" type="hidden" value="0"/>
    </p></input></input></input></form> </div><!-- #respond -->
    </div><!-- #comments -->
    </div>
    </div>
    </main><!-- #main -->
    </div><!-- #primary -->
    </div><!-- #content -->
    </div><!-- #page -->
    <!-- start footer -->
    <div id="footer">
    <div class="grid-container">
    <div class="grid-5 suffix-1 mobile-grid-12 mobile-suffix-0 grid-parent-mobile left">
    <div class="wrap">
    <a href="https://cma.pcdfusion.com/pcd/Order?iKey=I**D7B">Subscribe</a>
    <a href="https://cma.pcdfusion.com/pcd/CustomerSupport/Account/Login?ReturnUrl=%2fpcd%2fCustomerSupport%2fApp%2f3141">Manage Subscription</a>
    <a href="https://www.chicagomag.com/issue-archive/">Issue Archive</a>
    <a href="http://www.tronc.com/privacy-policy/">Privacy Policy</a>
    <a href="http://www.tronc.com/central-terms-of-service/">Terms of Service</a>
    </div>
    </div>
    <div class="grid-10 prefix-1 suffix-1 mobile-grid-100 mobile-prefix-0 grid-parent-mobile middle hide-on-mobile">
    <div class="wrap">
    <h2>Follow Us</h2>
    <div class="footer-social">
    <a href="https://www.facebook.com/ChicagoMagazine" target="_blank"><i class="fab fa-facebook-f"></i></a>
    <a href="http://www.twitter.com/chicagomag/" target="_blank"><i class="fab fa-twitter"></i></a>
    <a href="http://instagram.com/chicagomag" target="_blank"><i class="fab fa-instagram"></i></a>
    <a href="https://www.youtube.com/channel/UCOkRC6Y4LUyvglGmyC52KPw" target="_blank"><i class="fab fa-youtube"></i></a>
    </div>
    <h2>Get Our Newsletters</h2>
    <p>Subscribe to one or more of our free e-mail newsletters to get instant updates on local news, events, and opportunities in Chicago.</p>
    <div class="footer-form" style="display:flex; margin-top:60px;">
    <table>
    <tr>
    <td><input type="text"/></td>
    <td><button style="background:#d2232a; color:#fff;">Sign Up</button></td>
    </tr>
    </table>
    </div>
    <div class="copyright">©2020 Chicago magazine / A Chicago Tribune Media Group website</div>
    </div>
    </div>
    <div class="grid-5 prefix-1 mobile-grid-12 mobile-prefix-0 mobile-suffix-0 grid-parent-mobile right">
    <div class="wrap">
    <a href="https://www.chicagomag.com/about-the-magazine/">About the Magazine</a>
    <a href="https://www.chicagomag.com/contact-us/">Contact Us</a>
    <a href="https://www.chicagomag.com/advertise/">Advertise</a>
    <a href="https://www.chicagomag.com/resource-guide/">Resource Guide</a>
    <a href="https://www.chicagomag.com/events/">Events</a>
    </div>
    </div>
    <div class="mobile-grid-100 mobile-prefix-0 mobile-suffix-1 grid-parent-mobile middle hide-on-desktop hide-on-tablet">
    <div class="wrap">
    <h2>Follow Us</h2>
    <div class="footer-social">
    <a href="https://www.facebook.com/ChicagoMagazine" target="_blank"><i class="fab fa-facebook-f"></i></a>
    <a href="http://www.twitter.com/chicagomag/" target="_blank"><i class="fab fa-twitter"></i></a>
    <a href="http://instagram.com/chicagomag" target="_blank"><i class="fab fa-instagram"></i></a>
    <a href="https://www.youtube.com/channel/UCOkRC6Y4LUyvglGmyC52KPw" target="_blank"><i class="fab fa-youtube"></i></a>
    </div>
    <h2>Get Our Newsletters</h2>
    <p>Subscribe to one or more of our free e-mail newsletters to get instant updates on local news, events, and opportunities in Chicago.</p>
    <div class="footer-form" style="display:flex; margin-top:60px;">
    <input style="width:80%;" type="text"/>
    <button style="width:20%; background:#d2232a; color:#fff;">Sign Up</button>
    </div>
    <div class="copyright">©2020 Chicago magazine / A Chicago Tribune Media Group website</div>
    </div>
    </div>
    </div>
    </div>
    <!-- end footer -->
    <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.4.1/jquery.min.js"></script>
    <script>
    
    	jQuery(document).ready(function($) {
    
    		$(".grid-toggle").click(function(){
    			$(".grid-guide").toggle();
    		});
    
    		$(".nav2-toggle").click(function(){
    			$("#nav2-overlay").toggle();
    			$("#nav2-overlay-top").toggle();
    			$("#nav2-overlay-btm").toggle();
    			$("#nav2-inner-overlay").toggle();
    			$("#nav2-inner").toggle();
    			$("#nav2-open").toggle();
    			$("#nav2-close").toggle();
    		});
    
    		$(".search-open").click(function(){
    			$('#search-overlay').fadeIn().css('display', 'inline-block');
    			$('.search-field').focus();
    			//$('#search-close').fadeIn().css('display', 'block');
    		});
    
    		$(".search-close-btn").click(function(){
    			$("#search-overlay").fadeOut().toggle();
    			$("#search-close").fadeOut().toggle();
    		});
      
    	});
    
    </script>
    <script>
    
    	jQuery(document).ready(function($) {
    
    		$(".toggle-rock").click(function(){
    			$('.indie-rock').fadeOut().css('display', 'none');
    			$('.new-music').fadeOut().css('display', 'none');
    			$('.rock').fadeIn().css('display', 'block');
    		});
    
    		$(".toggle-indie-rock").click(function(){
    			$('.rock').fadeOut().css('display', 'none');
    			$('.new-music').fadeOut().css('display', 'none');
    			$('.indie-rock').fadeIn().css('display', 'block');
    		});
    
    		$(".toggle-new-music").click(function(){
    			$('.indie-rock').fadeOut().css('display', 'none');
    			$('.rock').fadeOut().css('display', 'none');
    			$('.new-music').fadeIn().css('display', 'block');
    		});
    
    		$(".toggle-all-genre").click(function(){
    			$('.indie-rock').fadeIn().css('display', 'block');
    			$('.rock').fadeIn().css('display', 'block');
    			$('.new-music').fadeIn().css('display', 'block');
    		});
      
    	});
    
    </script>
    <div class="site-footer">
    <footer class="site-info" itemscope="" itemtype="https://schema.org/WPFooter">
    <div class="inside-site-info grid-container grid-parent">
    <div class="copyright-bar">
    <span class="copyright">© 2021 Chicago Magazine</span> • Built with <a href="https://generatepress.com" itemprop="url">GeneratePress</a> </div>
    </div>
    </footer>
    </div><!-- .site-footer -->
    <script src="https://ajax.googleapis.com/ajax/libs/jquery/1.7.1/jquery.min.js" type="text/javascript"></script>
    <script type="text/javascript">
    		$(document).ready(function($) {
    			if($('#load_more').length > 0){
    			//$('#load_more').click(function(){
    				var page=1,
    				canBeLoaded = true,
    				category = $('input[name="category"]').val(),
    				ajaxurl="https://www.chicagomag.com/wp-admin/admin-ajax.php";
    				$(window).scroll(function(){
    					if( (canBeLoaded == true) && (($(document).scrollTop()) > ( $(document).height()-2000 )) ){
    						page=page+1;
    						canBeLoaded = false;
    						var data = {
    							'action': 'my_action',
    							'page': page,
    							'category':category
    						};
    						$.post(ajaxurl, data, function(response) {
    							$('#post_latest').append(response);
    							canBeLoaded = true;
    							if($.trim(response)==="<p>Sorry, no posts matched your criteria.</p>")
    							{
    								canBeLoaded = false;
    								$('#load_more').hide();
    							}
    							
    						});
    					}
    				});
    			}
    		});
    	</script>
    <!--[if lte IE 11]>
    <script src='https://www.chicagomag.com/wp-content/themes/generatepress/assets/js/classList.min.js?ver=3.0.2' id='generate-classlist-js'></script>
    <![endif]-->
    <script id="generate-main-js-extra">
    var generatepressMenu = {"toggleOpenedSubMenus":"1","openSubMenuLabel":"Open Sub-Menu","closeSubMenuLabel":"Close Sub-Menu"};
    </script>
    <script id="generate-main-js" src="https://www.chicagomag.com/wp-content/themes/generatepress/assets/js/main.min.js?ver=3.0.2"></script>
    <script id="comment-reply-js" src="https://www.chicagomag.com/wp-includes/js/comment-reply.min.js?ver=5.7.2"></script>
    <script id="heateor_sss_sharing_js-js-before">
    function heateorSssLoadEvent(e) {var t=window.onload;if (typeof window.onload!="function") {window.onload=e}else{window.onload=function() {t();e()}}};	var heateorSssSharingAjaxUrl = 'https://www.chicagomag.com/wp-admin/admin-ajax.php', heateorSssCloseIconPath = 'https://www.chicagomag.com/wp-content/plugins/sassy-social-share/public/../images/close.png', heateorSssPluginIconPath = 'https://www.chicagomag.com/wp-content/plugins/sassy-social-share/public/../images/logo.png', heateorSssHorizontalSharingCountEnable = 0, heateorSssVerticalSharingCountEnable = 0, heateorSssSharingOffset = -10; var heateorSssMobileStickySharingEnabled = 0;var heateorSssCopyLinkMessage = "Link copied.";var heateorSssUrlCountFetched = [], heateorSssSharesText = 'Shares', heateorSssShareText = 'Share';function heateorSssPopup(e) {window.open(e,"popUpWindow","height=400,width=600,left=400,top=100,resizable,scrollbars,toolbar=0,personalbar=0,menubar=no,location=no,directories=no,status")};var heateorSssWhatsappShareAPI = "web";
    </script>
    <script id="heateor_sss_sharing_js-js" src="https://www.chicagomag.com/wp-content/plugins/sassy-social-share/public/js/sassy-social-share-public.js?ver=3.3.20"></script>
    <script id="__ytprefsfitvids__-js" src="https://www.chicagomag.com/wp-content/plugins/youtube-embed-plus-pro/scripts/fitvids.min.js?ver=13.4.2"></script>
    <script id="wp-embed-js" src="https://www.chicagomag.com/wp-includes/js/wp-embed.min.js?ver=5.7.2"></script>
    <script>
    // When the user scrolls down 20px from the top of the document, slide down the navbar
    window.onscroll = function() {scrollFunction()};
    
    function scrollFunction() {
      if (document.body.scrollTop > 240 || document.documentElement.scrollTop > 240) {
        document.getElementById("navbar").style.top = "0";
      } else {
        document.getElementById("navbar").style.top = "-45px";
      }
    }
    </script>
    </body>
    </html>




```python
items =soup.find_all('div',{'class':'sammy'})
```


```python
len(items)
```




    50




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




    ['Old Oak Tap', 'Au Cheval', 'Xoco', 'Al’s Deli', 'Publican Quality Meats']




```python
link[0:11]
```




    ['http://www.chicagomag.com/Chicago-Magazine/November-2012/Best-Sandwiches-in-Chicago-Old-Oak-Tap-BLT/',
     'http://www.chicagomag.com/Chicago-Magazine/November-2012/Best-Sandwiches-in-Chicago-Au-Cheval-Fried-Bologna/',
     'http://www.chicagomag.com/Chicago-Magazine/November-2012/Best-Sandwiches-in-Chicago-Xoco-Woodland-Mushroom/',
     'http://www.chicagomag.com/Chicago-Magazine/November-2012/Best-Sandwiches-in-Chicago-Als-Deli-Roast-Beef/',
     'http://www.chicagomag.com/Chicago-Magazine/November-2012/Best-Sandwiches-in-Chicago-Publican-Quality-Meats-PB-L/',
     'https://www.chicagomag.com/Chicago-Magazine/November-2012/Best-Sandwiches-in-Chicago-Hendrickx-Belgian-Bread-Crafter-Belgian-Chicken-Curry-Salad/',
     'http://www.chicagomag.com/Chicago-Magazine/November-2012/Best-Sandwiches-in-Chicago-Acadia-Lobster-Roll/',
     'http://www.chicagomag.com/Chicago-Magazine/November-2012/Best-Sandwiches-in-Chicago-Birchwood-Kitchen-Smoked-Salmon-Salad/',
     'http://www.chicagomag.com/Chicago-Magazine/November-2012/Best-Sandwiches-in-Chicago-Cemitas-Puebla-Atomica-Cemitas/',
     'http://www.chicagomag.com/Chicago-Magazine/November-2012/Best-Sandwiches-in-Chicago-Nana-Grilled-Laughing-Bird-Shrimp-and-Fried-Oyster-Po-Boy/',
     'https://www.chicagomag.com/Chicago-Magazine/November-2012/Best-Sandwiches-in-Chicago-Lula-Cafe-Ham-and-Raclette-Panino/']




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




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Rank</th>
      <th>Menu</th>
      <th>Cafe</th>
      <th>URL</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1</td>
      <td>BLT</td>
      <td>Old Oak Tap</td>
      <td>http://www.chicagomag.com/Chicago-Magazine/Nov...</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2</td>
      <td>Fried Bologna</td>
      <td>Au Cheval</td>
      <td>http://www.chicagomag.com/Chicago-Magazine/Nov...</td>
    </tr>
    <tr>
      <th>2</th>
      <td>3</td>
      <td>Woodland Mushroom</td>
      <td>Xoco</td>
      <td>http://www.chicagomag.com/Chicago-Magazine/Nov...</td>
    </tr>
    <tr>
      <th>3</th>
      <td>4</td>
      <td>Roast Beef</td>
      <td>Al’s Deli</td>
      <td>http://www.chicagomag.com/Chicago-Magazine/Nov...</td>
    </tr>
    <tr>
      <th>4</th>
      <td>5</td>
      <td>PB&amp;L</td>
      <td>Publican Quality Meats</td>
      <td>http://www.chicagomag.com/Chicago-Magazine/Nov...</td>
    </tr>
  </tbody>
</table>
</div>




```python
df.head(10)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Rank</th>
      <th>Menu</th>
      <th>Cafe</th>
      <th>URL</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1</td>
      <td>BLT</td>
      <td>Old Oak Tap</td>
      <td>http://www.chicagomag.com/Chicago-Magazine/Nov...</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2</td>
      <td>Fried Bologna</td>
      <td>Au Cheval</td>
      <td>http://www.chicagomag.com/Chicago-Magazine/Nov...</td>
    </tr>
    <tr>
      <th>2</th>
      <td>3</td>
      <td>Woodland Mushroom</td>
      <td>Xoco</td>
      <td>http://www.chicagomag.com/Chicago-Magazine/Nov...</td>
    </tr>
    <tr>
      <th>3</th>
      <td>4</td>
      <td>Roast Beef</td>
      <td>Al’s Deli</td>
      <td>http://www.chicagomag.com/Chicago-Magazine/Nov...</td>
    </tr>
    <tr>
      <th>4</th>
      <td>5</td>
      <td>PB&amp;L</td>
      <td>Publican Quality Meats</td>
      <td>http://www.chicagomag.com/Chicago-Magazine/Nov...</td>
    </tr>
    <tr>
      <th>5</th>
      <td>6</td>
      <td>Belgian Chicken Curry Salad</td>
      <td>Hendrickx Belgian Bread Crafter</td>
      <td>https://www.chicagomag.com/Chicago-Magazine/No...</td>
    </tr>
    <tr>
      <th>6</th>
      <td>7</td>
      <td>Lobster Roll</td>
      <td>Acadia</td>
      <td>http://www.chicagomag.com/Chicago-Magazine/Nov...</td>
    </tr>
    <tr>
      <th>7</th>
      <td>8</td>
      <td>Smoked Salmon Salad</td>
      <td>Birchwood Kitchen</td>
      <td>http://www.chicagomag.com/Chicago-Magazine/Nov...</td>
    </tr>
    <tr>
      <th>8</th>
      <td>9</td>
      <td>Atomica Cemitas</td>
      <td>Cemitas Puebla</td>
      <td>http://www.chicagomag.com/Chicago-Magazine/Nov...</td>
    </tr>
    <tr>
      <th>9</th>
      <td>10</td>
      <td>Grilled Laughing Bird Shrimp and Fried Po’ Boy</td>
      <td>Nana</td>
      <td>http://www.chicagomag.com/Chicago-Magazine/Nov...</td>
    </tr>
  </tbody>
</table>
</div>




```python
df.to_csv('best_sandwiches_list_chicago.csv', sep=',',encoding='UTF-8')
```


```python
pwd
```




    '/Users/seongy.yoon'




```python
from bs4 import BeautifulSoup
from urllib.request import Request, urlopen
import pandas as pd
```


```python
df = pd.read_csv('best_sandwiches_list_chicago.csv', index_col=0)
df.head(10)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Rank</th>
      <th>Menu</th>
      <th>Cafe</th>
      <th>URL</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1</td>
      <td>BLT</td>
      <td>Old Oak Tap</td>
      <td>http://www.chicagomag.com/Chicago-Magazine/Nov...</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2</td>
      <td>Fried Bologna</td>
      <td>Au Cheval</td>
      <td>http://www.chicagomag.com/Chicago-Magazine/Nov...</td>
    </tr>
    <tr>
      <th>2</th>
      <td>3</td>
      <td>Woodland Mushroom</td>
      <td>Xoco</td>
      <td>http://www.chicagomag.com/Chicago-Magazine/Nov...</td>
    </tr>
    <tr>
      <th>3</th>
      <td>4</td>
      <td>Roast Beef</td>
      <td>Al’s Deli</td>
      <td>http://www.chicagomag.com/Chicago-Magazine/Nov...</td>
    </tr>
    <tr>
      <th>4</th>
      <td>5</td>
      <td>PB&amp;L</td>
      <td>Publican Quality Meats</td>
      <td>http://www.chicagomag.com/Chicago-Magazine/Nov...</td>
    </tr>
    <tr>
      <th>5</th>
      <td>6</td>
      <td>Belgian Chicken Curry Salad</td>
      <td>Hendrickx Belgian Bread Crafter</td>
      <td>https://www.chicagomag.com/Chicago-Magazine/No...</td>
    </tr>
    <tr>
      <th>6</th>
      <td>7</td>
      <td>Lobster Roll</td>
      <td>Acadia</td>
      <td>http://www.chicagomag.com/Chicago-Magazine/Nov...</td>
    </tr>
    <tr>
      <th>7</th>
      <td>8</td>
      <td>Smoked Salmon Salad</td>
      <td>Birchwood Kitchen</td>
      <td>http://www.chicagomag.com/Chicago-Magazine/Nov...</td>
    </tr>
    <tr>
      <th>8</th>
      <td>9</td>
      <td>Atomica Cemitas</td>
      <td>Cemitas Puebla</td>
      <td>http://www.chicagomag.com/Chicago-Magazine/Nov...</td>
    </tr>
    <tr>
      <th>9</th>
      <td>10</td>
      <td>Grilled Laughing Bird Shrimp and Fried Po’ Boy</td>
      <td>Nana</td>
      <td>http://www.chicagomag.com/Chicago-Magazine/Nov...</td>
    </tr>
  </tbody>
</table>
</div>




```python
df.tail(10)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Rank</th>
      <th>Menu</th>
      <th>Cafe</th>
      <th>URL</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>40</th>
      <td>41</td>
      <td>The Marty</td>
      <td>Z&amp;H MarketCafe</td>
      <td>https://www.chicagomag.com/Chicago-Magazine/No...</td>
    </tr>
    <tr>
      <th>41</th>
      <td>42</td>
      <td>Whitefish</td>
      <td>Market House on the Square</td>
      <td>https://www.chicagomag.com/Chicago-Magazine/No...</td>
    </tr>
    <tr>
      <th>42</th>
      <td>43</td>
      <td>Oat Bread, Pecan Butter, and Fruit Jam</td>
      <td>Elaine’s Coffee Call</td>
      <td>https://www.chicagomag.com/Chicago-Magazine/No...</td>
    </tr>
    <tr>
      <th>43</th>
      <td>44</td>
      <td>Cauliflower Melt</td>
      <td>Marion Street Cheese Market</td>
      <td>https://www.chicagomag.com/Chicago-Magazine/No...</td>
    </tr>
    <tr>
      <th>44</th>
      <td>45</td>
      <td>Cubana</td>
      <td>Cafecito</td>
      <td>https://www.chicagomag.com/Chicago-Magazine/No...</td>
    </tr>
    <tr>
      <th>45</th>
      <td>46</td>
      <td>Kufta</td>
      <td>Chickpea</td>
      <td>https://www.chicagomag.com/Chicago-Magazine/No...</td>
    </tr>
    <tr>
      <th>46</th>
      <td>47</td>
      <td>Debbie’s Egg Salad</td>
      <td>The Goddess and Grocer</td>
      <td>https://www.chicagomag.com/Chicago-Magazine/No...</td>
    </tr>
    <tr>
      <th>47</th>
      <td>48</td>
      <td>Beef Curry</td>
      <td>Zenwich</td>
      <td>https://www.chicagomag.com/Chicago-Magazine/No...</td>
    </tr>
    <tr>
      <th>48</th>
      <td>49</td>
      <td>Le Végétarien</td>
      <td>Toni Patisserie</td>
      <td>https://www.chicagomag.com/Chicago-Magazine/No...</td>
    </tr>
    <tr>
      <th>49</th>
      <td>50</td>
      <td>The Gatsby</td>
      <td>Phoebe’s Bakery</td>
      <td>https://www.chicagomag.com/Chicago-Magazine/No...</td>
    </tr>
  </tbody>
</table>
</div>




```python
df.index
```




    Int64Index([ 0,  1,  2,  3,  4,  5,  6,  7,  8,  9, 10, 11, 12, 13, 14, 15, 16,
                17, 18, 19, 20, 21, 22, 23, 24, 25, 26, 27, 28, 29, 30, 31, 32, 33,
                34, 35, 36, 37, 38, 39, 40, 41, 42, 43, 44, 45, 46, 47, 48, 49],
               dtype='int64')




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

    <ipython-input-20-3283781f8f36>:6: TqdmDeprecationWarning: This function will be removed in tqdm==5.0.0
    Please use `tqdm.notebook.tqdm` instead of `tqdm.tqdm_notebook`
      for n in tqdm_notebook(df.index):



    HBox(children=(FloatProgress(value=0.0, max=50.0), HTML(value='')))


    



```python
len(price)
```




    50




```python
len(address)
```




    50




```python
df['Price'] = price
df['Address'] = address

df = df.loc[:,['Rank', 'Cafe', 'Menu', 'Price', 'Address']]
df.set_index('Rank', inplace=True)
df.head()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Cafe</th>
      <th>Menu</th>
      <th>Price</th>
      <th>Address</th>
    </tr>
    <tr>
      <th>Rank</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>1</th>
      <td>Old Oak Tap</td>
      <td>BLT</td>
      <td>$10</td>
      <td>2109 W. Chicago Ave.,</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Au Cheval</td>
      <td>Fried Bologna</td>
      <td>$9</td>
      <td>800 W. Randolph St.,</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Xoco</td>
      <td>Woodland Mushroom</td>
      <td>$9.50</td>
      <td>445 N. Clark St.,</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Al’s Deli</td>
      <td>Roast Beef</td>
      <td>$9.40</td>
      <td>914 Noyes St., Evanston,</td>
    </tr>
    <tr>
      <th>5</th>
      <td>Publican Quality Meats</td>
      <td>PB&amp;L</td>
      <td>$10</td>
      <td>825 W. Fulton Mkt.,</td>
    </tr>
  </tbody>
</table>
</div>




```python
df.to_csv('best_sandwiches_list_chicago2.csv', sep=',', encoding='UTF-8')
```


```python
pip install folium
```

    Requirement already satisfied: folium in ./opt/anaconda3/lib/python3.8/site-packages (0.11.0)
    Requirement already satisfied: numpy in ./opt/anaconda3/lib/python3.8/site-packages (from folium) (1.19.5)
    Requirement already satisfied: jinja2>=2.9 in ./opt/anaconda3/lib/python3.8/site-packages (from folium) (2.11.2)
    Requirement already satisfied: requests in ./opt/anaconda3/lib/python3.8/site-packages (from folium) (2.24.0)
    Requirement already satisfied: branca>=0.3.0 in ./opt/anaconda3/lib/python3.8/site-packages (from folium) (0.4.1)
    Requirement already satisfied: MarkupSafe>=0.23 in ./opt/anaconda3/lib/python3.8/site-packages (from jinja2>=2.9->folium) (1.1.1)
    Requirement already satisfied: idna<3,>=2.5 in ./opt/anaconda3/lib/python3.8/site-packages (from requests->folium) (2.10)
    Requirement already satisfied: chardet<4,>=3.0.2 in ./opt/anaconda3/lib/python3.8/site-packages (from requests->folium) (3.0.4)
    Requirement already satisfied: urllib3!=1.25.0,!=1.25.1,<1.26,>=1.21.1 in ./opt/anaconda3/lib/python3.8/site-packages (from requests->folium) (1.25.9)
    Requirement already satisfied: certifi>=2017.4.17 in ./opt/anaconda3/lib/python3.8/site-packages (from requests->folium) (2020.6.20)
    Note: you may need to restart the kernel to use updated packages.



```python
pip install googlemaps
```

    Requirement already satisfied: googlemaps in ./opt/anaconda3/lib/python3.8/site-packages (4.4.2)
    Requirement already satisfied: requests<3.0,>=2.20.0 in ./opt/anaconda3/lib/python3.8/site-packages (from googlemaps) (2.24.0)
    Requirement already satisfied: certifi>=2017.4.17 in ./opt/anaconda3/lib/python3.8/site-packages (from requests<3.0,>=2.20.0->googlemaps) (2020.6.20)
    Requirement already satisfied: urllib3!=1.25.0,!=1.25.1,<1.26,>=1.21.1 in ./opt/anaconda3/lib/python3.8/site-packages (from requests<3.0,>=2.20.0->googlemaps) (1.25.9)
    Requirement already satisfied: idna<3,>=2.5 in ./opt/anaconda3/lib/python3.8/site-packages (from requests<3.0,>=2.20.0->googlemaps) (2.10)
    Requirement already satisfied: chardet<4,>=3.0.2 in ./opt/anaconda3/lib/python3.8/site-packages (from requests<3.0,>=2.20.0->googlemaps) (3.0.4)
    Note: you may need to restart the kernel to use updated packages.



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




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Cafe</th>
      <th>Menu</th>
      <th>Price</th>
      <th>Address</th>
    </tr>
    <tr>
      <th>Rank</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>1</th>
      <td>Old Oak Tap</td>
      <td>BLT</td>
      <td>$10</td>
      <td>2109 W. Chicago Ave.,</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Au Cheval</td>
      <td>Fried Bologna</td>
      <td>$9</td>
      <td>800 W. Randolph St.,</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Xoco</td>
      <td>Woodland Mushroom</td>
      <td>$9.50</td>
      <td>445 N. Clark St.,</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Al’s Deli</td>
      <td>Roast Beef</td>
      <td>$9.40</td>
      <td>914 Noyes St., Evanston,</td>
    </tr>
    <tr>
      <th>5</th>
      <td>Publican Quality Meats</td>
      <td>PB&amp;L</td>
      <td>$10</td>
      <td>825 W. Fulton Mkt.,</td>
    </tr>
  </tbody>
</table>
</div>




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

    <ipython-input-30-f55bc718478b>:4: TqdmDeprecationWarning: This function will be removed in tqdm==5.0.0
    Please use `tqdm.notebook.tqdm` instead of `tqdm.tqdm_notebook`
      for n in tqdm_notebook(df.index):



    HBox(children=(FloatProgress(value=0.0, max=50.0), HTML(value='')))


    





<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Cafe</th>
      <th>Menu</th>
      <th>Price</th>
      <th>Address</th>
      <th>lat</th>
      <th>lng</th>
    </tr>
    <tr>
      <th>Rank</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>1</th>
      <td>Old Oak Tap</td>
      <td>BLT</td>
      <td>$10</td>
      <td>2109 W. Chicago Ave.,</td>
      <td>41.895605</td>
      <td>-87.679961</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Au Cheval</td>
      <td>Fried Bologna</td>
      <td>$9</td>
      <td>800 W. Randolph St.,</td>
      <td>41.884658</td>
      <td>-87.647667</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Xoco</td>
      <td>Woodland Mushroom</td>
      <td>$9.50</td>
      <td>445 N. Clark St.,</td>
      <td>41.890523</td>
      <td>-87.630783</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Al’s Deli</td>
      <td>Roast Beef</td>
      <td>$9.40</td>
      <td>914 Noyes St., Evanston,</td>
      <td>42.058322</td>
      <td>-87.683748</td>
    </tr>
    <tr>
      <th>5</th>
      <td>Publican Quality Meats</td>
      <td>PB&amp;L</td>
      <td>$10</td>
      <td>825 W. Fulton Mkt.,</td>
      <td>41.886604</td>
      <td>-87.648536</td>
    </tr>
  </tbody>
</table>
</div>




```python
mapping = folium.Map(location=[df['lat'].mean(), df['lng'].mean()],
                    zoom_start=11)

for n in df.index:
    if df['Address'][n] != 'Multiple':
        folium.Marker([df['lat'][n], df['lng'][n]],
                     popup=df['Cafe'][n]).add_to(mapping)
mapping
```




<div style="width:100%;"><div style="position:relative;width:100%;height:0;padding-bottom:60%;"><span style="color:#565656">Make this Notebook Trusted to load map: File -> Trust Notebook</span><iframe src="about:blank" style="position:absolute;width:100%;height:100%;left:0;top:0;border:none !important;" data-html=PCFET0NUWVBFIGh0bWw+CjxoZWFkPiAgICAKICAgIDxtZXRhIGh0dHAtZXF1aXY9ImNvbnRlbnQtdHlwZSIgY29udGVudD0idGV4dC9odG1sOyBjaGFyc2V0PVVURi04IiAvPgogICAgCiAgICAgICAgPHNjcmlwdD4KICAgICAgICAgICAgTF9OT19UT1VDSCA9IGZhbHNlOwogICAgICAgICAgICBMX0RJU0FCTEVfM0QgPSBmYWxzZTsKICAgICAgICA8L3NjcmlwdD4KICAgIAogICAgPHNjcmlwdCBzcmM9Imh0dHBzOi8vY2RuLmpzZGVsaXZyLm5ldC9ucG0vbGVhZmxldEAxLjYuMC9kaXN0L2xlYWZsZXQuanMiPjwvc2NyaXB0PgogICAgPHNjcmlwdCBzcmM9Imh0dHBzOi8vY29kZS5qcXVlcnkuY29tL2pxdWVyeS0xLjEyLjQubWluLmpzIj48L3NjcmlwdD4KICAgIDxzY3JpcHQgc3JjPSJodHRwczovL21heGNkbi5ib290c3RyYXBjZG4uY29tL2Jvb3RzdHJhcC8zLjIuMC9qcy9ib290c3RyYXAubWluLmpzIj48L3NjcmlwdD4KICAgIDxzY3JpcHQgc3JjPSJodHRwczovL2NkbmpzLmNsb3VkZmxhcmUuY29tL2FqYXgvbGlicy9MZWFmbGV0LmF3ZXNvbWUtbWFya2Vycy8yLjAuMi9sZWFmbGV0LmF3ZXNvbWUtbWFya2Vycy5qcyI+PC9zY3JpcHQ+CiAgICA8bGluayByZWw9InN0eWxlc2hlZXQiIGhyZWY9Imh0dHBzOi8vY2RuLmpzZGVsaXZyLm5ldC9ucG0vbGVhZmxldEAxLjYuMC9kaXN0L2xlYWZsZXQuY3NzIi8+CiAgICA8bGluayByZWw9InN0eWxlc2hlZXQiIGhyZWY9Imh0dHBzOi8vbWF4Y2RuLmJvb3RzdHJhcGNkbi5jb20vYm9vdHN0cmFwLzMuMi4wL2Nzcy9ib290c3RyYXAubWluLmNzcyIvPgogICAgPGxpbmsgcmVsPSJzdHlsZXNoZWV0IiBocmVmPSJodHRwczovL21heGNkbi5ib290c3RyYXBjZG4uY29tL2Jvb3RzdHJhcC8zLjIuMC9jc3MvYm9vdHN0cmFwLXRoZW1lLm1pbi5jc3MiLz4KICAgIDxsaW5rIHJlbD0ic3R5bGVzaGVldCIgaHJlZj0iaHR0cHM6Ly9tYXhjZG4uYm9vdHN0cmFwY2RuLmNvbS9mb250LWF3ZXNvbWUvNC42LjMvY3NzL2ZvbnQtYXdlc29tZS5taW4uY3NzIi8+CiAgICA8bGluayByZWw9InN0eWxlc2hlZXQiIGhyZWY9Imh0dHBzOi8vY2RuanMuY2xvdWRmbGFyZS5jb20vYWpheC9saWJzL0xlYWZsZXQuYXdlc29tZS1tYXJrZXJzLzIuMC4yL2xlYWZsZXQuYXdlc29tZS1tYXJrZXJzLmNzcyIvPgogICAgPGxpbmsgcmVsPSJzdHlsZXNoZWV0IiBocmVmPSJodHRwczovL3Jhd2Nkbi5naXRoYWNrLmNvbS9weXRob24tdmlzdWFsaXphdGlvbi9mb2xpdW0vbWFzdGVyL2ZvbGl1bS90ZW1wbGF0ZXMvbGVhZmxldC5hd2Vzb21lLnJvdGF0ZS5jc3MiLz4KICAgIDxzdHlsZT5odG1sLCBib2R5IHt3aWR0aDogMTAwJTtoZWlnaHQ6IDEwMCU7bWFyZ2luOiAwO3BhZGRpbmc6IDA7fTwvc3R5bGU+CiAgICA8c3R5bGU+I21hcCB7cG9zaXRpb246YWJzb2x1dGU7dG9wOjA7Ym90dG9tOjA7cmlnaHQ6MDtsZWZ0OjA7fTwvc3R5bGU+CiAgICAKICAgICAgICAgICAgPG1ldGEgbmFtZT0idmlld3BvcnQiIGNvbnRlbnQ9IndpZHRoPWRldmljZS13aWR0aCwKICAgICAgICAgICAgICAgIGluaXRpYWwtc2NhbGU9MS4wLCBtYXhpbXVtLXNjYWxlPTEuMCwgdXNlci1zY2FsYWJsZT1ubyIgLz4KICAgICAgICAgICAgPHN0eWxlPgogICAgICAgICAgICAgICAgI21hcF9iNmQxZDk1Yjk5OTA0MDMyYTdiZjI1YTI1NWYzMzExOCB7CiAgICAgICAgICAgICAgICAgICAgcG9zaXRpb246IHJlbGF0aXZlOwogICAgICAgICAgICAgICAgICAgIHdpZHRoOiAxMDAuMCU7CiAgICAgICAgICAgICAgICAgICAgaGVpZ2h0OiAxMDAuMCU7CiAgICAgICAgICAgICAgICAgICAgbGVmdDogMC4wJTsKICAgICAgICAgICAgICAgICAgICB0b3A6IDAuMCU7CiAgICAgICAgICAgICAgICB9CiAgICAgICAgICAgIDwvc3R5bGU+CiAgICAgICAgCjwvaGVhZD4KPGJvZHk+ICAgIAogICAgCiAgICAgICAgICAgIDxkaXYgY2xhc3M9ImZvbGl1bS1tYXAiIGlkPSJtYXBfYjZkMWQ5NWI5OTkwNDAzMmE3YmYyNWEyNTVmMzMxMTgiID48L2Rpdj4KICAgICAgICAKPC9ib2R5Pgo8c2NyaXB0PiAgICAKICAgIAogICAgICAgICAgICB2YXIgbWFwX2I2ZDFkOTViOTk5MDQwMzJhN2JmMjVhMjU1ZjMzMTE4ID0gTC5tYXAoCiAgICAgICAgICAgICAgICAibWFwX2I2ZDFkOTViOTk5MDQwMzJhN2JmMjVhMjU1ZjMzMTE4IiwKICAgICAgICAgICAgICAgIHsKICAgICAgICAgICAgICAgICAgICBjZW50ZXI6IFs0MS45MjQyNDU3ODg2MzYzNywgLTg3LjY4MDk4NjkzNjM2MzYyXSwKICAgICAgICAgICAgICAgICAgICBjcnM6IEwuQ1JTLkVQU0czODU3LAogICAgICAgICAgICAgICAgICAgIHpvb206IDExLAogICAgICAgICAgICAgICAgICAgIHpvb21Db250cm9sOiB0cnVlLAogICAgICAgICAgICAgICAgICAgIHByZWZlckNhbnZhczogZmFsc2UsCiAgICAgICAgICAgICAgICB9CiAgICAgICAgICAgICk7CgogICAgICAgICAgICAKCiAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIHRpbGVfbGF5ZXJfODM2N2IzMTIxZDNlNDZiN2FmZWZhMTdiMjZjY2U1OTcgPSBMLnRpbGVMYXllcigKICAgICAgICAgICAgICAgICJodHRwczovL3tzfS50aWxlLm9wZW5zdHJlZXRtYXAub3JnL3t6fS97eH0ve3l9LnBuZyIsCiAgICAgICAgICAgICAgICB7ImF0dHJpYnV0aW9uIjogIkRhdGEgYnkgXHUwMDI2Y29weTsgXHUwMDNjYSBocmVmPVwiaHR0cDovL29wZW5zdHJlZXRtYXAub3JnXCJcdTAwM2VPcGVuU3RyZWV0TWFwXHUwMDNjL2FcdTAwM2UsIHVuZGVyIFx1MDAzY2EgaHJlZj1cImh0dHA6Ly93d3cub3BlbnN0cmVldG1hcC5vcmcvY29weXJpZ2h0XCJcdTAwM2VPRGJMXHUwMDNjL2FcdTAwM2UuIiwgImRldGVjdFJldGluYSI6IGZhbHNlLCAibWF4TmF0aXZlWm9vbSI6IDE4LCAibWF4Wm9vbSI6IDE4LCAibWluWm9vbSI6IDAsICJub1dyYXAiOiBmYWxzZSwgIm9wYWNpdHkiOiAxLCAic3ViZG9tYWlucyI6ICJhYmMiLCAidG1zIjogZmFsc2V9CiAgICAgICAgICAgICkuYWRkVG8obWFwX2I2ZDFkOTViOTk5MDQwMzJhN2JmMjVhMjU1ZjMzMTE4KTsKICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgbWFya2VyX2FhMjkxZWVmN2IzMDRlNzM4MDIyZWJmMzI2MzQzY2MwID0gTC5tYXJrZXIoCiAgICAgICAgICAgICAgICBbNDEuODk1NjA0OSwgLTg3LjY3OTk2MTQ5OTk5OTk5XSwKICAgICAgICAgICAgICAgIHt9CiAgICAgICAgICAgICkuYWRkVG8obWFwX2I2ZDFkOTViOTk5MDQwMzJhN2JmMjVhMjU1ZjMzMTE4KTsKICAgICAgICAKICAgIAogICAgICAgIHZhciBwb3B1cF84OTc3ZjVjZDNlMWU0NzgwYTEyOGQ3NzFiYTQ2NWY4OSA9IEwucG9wdXAoeyJtYXhXaWR0aCI6ICIxMDAlIn0pOwoKICAgICAgICAKICAgICAgICAgICAgdmFyIGh0bWxfOTlmNDhkNmRmYmRmNDJiMTg0MDcwNjk3NGM0YzI3OTIgPSAkKGA8ZGl2IGlkPSJodG1sXzk5ZjQ4ZDZkZmJkZjQyYjE4NDA3MDY5NzRjNGMyNzkyIiBzdHlsZT0id2lkdGg6IDEwMC4wJTsgaGVpZ2h0OiAxMDAuMCU7Ij5PbGQgT2FrIFRhcDwvZGl2PmApWzBdOwogICAgICAgICAgICBwb3B1cF84OTc3ZjVjZDNlMWU0NzgwYTEyOGQ3NzFiYTQ2NWY4OS5zZXRDb250ZW50KGh0bWxfOTlmNDhkNmRmYmRmNDJiMTg0MDcwNjk3NGM0YzI3OTIpOwogICAgICAgIAoKICAgICAgICBtYXJrZXJfYWEyOTFlZWY3YjMwNGU3MzgwMjJlYmYzMjYzNDNjYzAuYmluZFBvcHVwKHBvcHVwXzg5NzdmNWNkM2UxZTQ3ODBhMTI4ZDc3MWJhNDY1Zjg5KQogICAgICAgIDsKCiAgICAgICAgCiAgICAKICAgIAogICAgICAgICAgICB2YXIgbWFya2VyX2M4NWMzNzhmOTE0MjRjYzY4ODMzZDI2ZjExMDQ3YmY0ID0gTC5tYXJrZXIoCiAgICAgICAgICAgICAgICBbNDEuODg0NjU4MiwgLTg3LjY0NzY2NjhdLAogICAgICAgICAgICAgICAge30KICAgICAgICAgICAgKS5hZGRUbyhtYXBfYjZkMWQ5NWI5OTkwNDAzMmE3YmYyNWEyNTVmMzMxMTgpOwogICAgICAgIAogICAgCiAgICAgICAgdmFyIHBvcHVwXzE4MGU3NTk0MzJmMTQ2YjJhNWNmMTc4NjdkYjRjZTgxID0gTC5wb3B1cCh7Im1heFdpZHRoIjogIjEwMCUifSk7CgogICAgICAgIAogICAgICAgICAgICB2YXIgaHRtbF9jNTI4OWRlYTU1MTI0YmVlODMwZjJiY2NjNWJlNTBiNCA9ICQoYDxkaXYgaWQ9Imh0bWxfYzUyODlkZWE1NTEyNGJlZTgzMGYyYmNjYzViZTUwYjQiIHN0eWxlPSJ3aWR0aDogMTAwLjAlOyBoZWlnaHQ6IDEwMC4wJTsiPkF1IENoZXZhbDwvZGl2PmApWzBdOwogICAgICAgICAgICBwb3B1cF8xODBlNzU5NDMyZjE0NmIyYTVjZjE3ODY3ZGI0Y2U4MS5zZXRDb250ZW50KGh0bWxfYzUyODlkZWE1NTEyNGJlZTgzMGYyYmNjYzViZTUwYjQpOwogICAgICAgIAoKICAgICAgICBtYXJrZXJfYzg1YzM3OGY5MTQyNGNjNjg4MzNkMjZmMTEwNDdiZjQuYmluZFBvcHVwKHBvcHVwXzE4MGU3NTk0MzJmMTQ2YjJhNWNmMTc4NjdkYjRjZTgxKQogICAgICAgIDsKCiAgICAgICAgCiAgICAKICAgIAogICAgICAgICAgICB2YXIgbWFya2VyXzg4NDdiODA4ZjFkYTQ4OGE4M2MxNDg2ODBjNzgyNzFhID0gTC5tYXJrZXIoCiAgICAgICAgICAgICAgICBbNDEuODkwNTIyNiwgLTg3LjYzMDc4MzRdLAogICAgICAgICAgICAgICAge30KICAgICAgICAgICAgKS5hZGRUbyhtYXBfYjZkMWQ5NWI5OTkwNDAzMmE3YmYyNWEyNTVmMzMxMTgpOwogICAgICAgIAogICAgCiAgICAgICAgdmFyIHBvcHVwXzNmZmIyNDY0ZDE0ODQ3ZjRhMDliYmIzZTYwZDJiM2Q5ID0gTC5wb3B1cCh7Im1heFdpZHRoIjogIjEwMCUifSk7CgogICAgICAgIAogICAgICAgICAgICB2YXIgaHRtbF83NzA1ZTlmOWUzNTQ0ZDJjOTcxNDU3ZmQ5ZDM2Yzk3NCA9ICQoYDxkaXYgaWQ9Imh0bWxfNzcwNWU5ZjllMzU0NGQyYzk3MTQ1N2ZkOWQzNmM5NzQiIHN0eWxlPSJ3aWR0aDogMTAwLjAlOyBoZWlnaHQ6IDEwMC4wJTsiPlhvY288L2Rpdj5gKVswXTsKICAgICAgICAgICAgcG9wdXBfM2ZmYjI0NjRkMTQ4NDdmNGEwOWJiYjNlNjBkMmIzZDkuc2V0Q29udGVudChodG1sXzc3MDVlOWY5ZTM1NDRkMmM5NzE0NTdmZDlkMzZjOTc0KTsKICAgICAgICAKCiAgICAgICAgbWFya2VyXzg4NDdiODA4ZjFkYTQ4OGE4M2MxNDg2ODBjNzgyNzFhLmJpbmRQb3B1cChwb3B1cF8zZmZiMjQ2NGQxNDg0N2Y0YTA5YmJiM2U2MGQyYjNkOSkKICAgICAgICA7CgogICAgICAgIAogICAgCiAgICAKICAgICAgICAgICAgdmFyIG1hcmtlcl85YTJjN2Q2Zjg3NGI0Zjg0YjVjNGQ3YWViZmZkZmI4NSA9IEwubWFya2VyKAogICAgICAgICAgICAgICAgWzQyLjA1ODMyMTcsIC04Ny42ODM3NDc5XSwKICAgICAgICAgICAgICAgIHt9CiAgICAgICAgICAgICkuYWRkVG8obWFwX2I2ZDFkOTViOTk5MDQwMzJhN2JmMjVhMjU1ZjMzMTE4KTsKICAgICAgICAKICAgIAogICAgICAgIHZhciBwb3B1cF83MzBkNTYyMTczM2M0ZDVkOWFkYjVlMTYyOGU4MTYxYiA9IEwucG9wdXAoeyJtYXhXaWR0aCI6ICIxMDAlIn0pOwoKICAgICAgICAKICAgICAgICAgICAgdmFyIGh0bWxfYTg2Y2FjZmM5MWNkNGYzNjk1OGE4YzNiM2VlZjc4NjEgPSAkKGA8ZGl2IGlkPSJodG1sX2E4NmNhY2ZjOTFjZDRmMzY5NThhOGMzYjNlZWY3ODYxIiBzdHlsZT0id2lkdGg6IDEwMC4wJTsgaGVpZ2h0OiAxMDAuMCU7Ij5BbOKAmXMgRGVsaTwvZGl2PmApWzBdOwogICAgICAgICAgICBwb3B1cF83MzBkNTYyMTczM2M0ZDVkOWFkYjVlMTYyOGU4MTYxYi5zZXRDb250ZW50KGh0bWxfYTg2Y2FjZmM5MWNkNGYzNjk1OGE4YzNiM2VlZjc4NjEpOwogICAgICAgIAoKICAgICAgICBtYXJrZXJfOWEyYzdkNmY4NzRiNGY4NGI1YzRkN2FlYmZmZGZiODUuYmluZFBvcHVwKHBvcHVwXzczMGQ1NjIxNzMzYzRkNWQ5YWRiNWUxNjI4ZTgxNjFiKQogICAgICAgIDsKCiAgICAgICAgCiAgICAKICAgIAogICAgICAgICAgICB2YXIgbWFya2VyXzNkOWZlMTFmODIzNDQ0NzA4YjAxMmExNWMzYWEwNjhmID0gTC5tYXJrZXIoCiAgICAgICAgICAgICAgICBbNDEuODg2NjAzNiwgLTg3LjY0ODUzNjQ5OTk5OTk5XSwKICAgICAgICAgICAgICAgIHt9CiAgICAgICAgICAgICkuYWRkVG8obWFwX2I2ZDFkOTViOTk5MDQwMzJhN2JmMjVhMjU1ZjMzMTE4KTsKICAgICAgICAKICAgIAogICAgICAgIHZhciBwb3B1cF8yMmIzM2FlZTFjODk0ZTI3OTY3NzVkMzE5NmVhYzZlOSA9IEwucG9wdXAoeyJtYXhXaWR0aCI6ICIxMDAlIn0pOwoKICAgICAgICAKICAgICAgICAgICAgdmFyIGh0bWxfNTQ5MDQ4Yzg2MGI1NGE1MzljYWZkM2JiNTRhMWVkMDggPSAkKGA8ZGl2IGlkPSJodG1sXzU0OTA0OGM4NjBiNTRhNTM5Y2FmZDNiYjU0YTFlZDA4IiBzdHlsZT0id2lkdGg6IDEwMC4wJTsgaGVpZ2h0OiAxMDAuMCU7Ij5QdWJsaWNhbiBRdWFsaXR5IE1lYXRzPC9kaXY+YClbMF07CiAgICAgICAgICAgIHBvcHVwXzIyYjMzYWVlMWM4OTRlMjc5Njc3NWQzMTk2ZWFjNmU5LnNldENvbnRlbnQoaHRtbF81NDkwNDhjODYwYjU0YTUzOWNhZmQzYmI1NGExZWQwOCk7CiAgICAgICAgCgogICAgICAgIG1hcmtlcl8zZDlmZTExZjgyMzQ0NDcwOGIwMTJhMTVjM2FhMDY4Zi5iaW5kUG9wdXAocG9wdXBfMjJiMzNhZWUxYzg5NGUyNzk2Nzc1ZDMxOTZlYWM2ZTkpCiAgICAgICAgOwoKICAgICAgICAKICAgIAogICAgCiAgICAgICAgICAgIHZhciBtYXJrZXJfNmQ2MDJkMDJlYjY2NDhhZDhkMWUxZDhlMzkwMWIwY2YgPSBMLm1hcmtlcigKICAgICAgICAgICAgICAgIFs0MS45MDAwODY5LCAtODcuNjI1MzM2Nl0sCiAgICAgICAgICAgICAgICB7fQogICAgICAgICAgICApLmFkZFRvKG1hcF9iNmQxZDk1Yjk5OTA0MDMyYTdiZjI1YTI1NWYzMzExOCk7CiAgICAgICAgCiAgICAKICAgICAgICB2YXIgcG9wdXBfNWY0MzYyYzcwYTkxNGZlYTkwNjk1MDllOTBjMGU0MmMgPSBMLnBvcHVwKHsibWF4V2lkdGgiOiAiMTAwJSJ9KTsKCiAgICAgICAgCiAgICAgICAgICAgIHZhciBodG1sX2M1ZDc2MThlMmQwNzQxNjBiMDFhOTkzYjM2NjA0ZTFlID0gJChgPGRpdiBpZD0iaHRtbF9jNWQ3NjE4ZTJkMDc0MTYwYjAxYTk5M2IzNjYwNGUxZSIgc3R5bGU9IndpZHRoOiAxMDAuMCU7IGhlaWdodDogMTAwLjAlOyI+SGVuZHJpY2t4IEJlbGdpYW4gQnJlYWQgQ3JhZnRlcjwvZGl2PmApWzBdOwogICAgICAgICAgICBwb3B1cF81ZjQzNjJjNzBhOTE0ZmVhOTA2OTUwOWU5MGMwZTQyYy5zZXRDb250ZW50KGh0bWxfYzVkNzYxOGUyZDA3NDE2MGIwMWE5OTNiMzY2MDRlMWUpOwogICAgICAgIAoKICAgICAgICBtYXJrZXJfNmQ2MDJkMDJlYjY2NDhhZDhkMWUxZDhlMzkwMWIwY2YuYmluZFBvcHVwKHBvcHVwXzVmNDM2MmM3MGE5MTRmZWE5MDY5NTA5ZTkwYzBlNDJjKQogICAgICAgIDsKCiAgICAgICAgCiAgICAKICAgIAogICAgICAgICAgICB2YXIgbWFya2VyXzRhNGY3YmI3Y2FiNzQ4ZGQ4NWQ1OTcxYWEzMGNlZDJiID0gTC5tYXJrZXIoCiAgICAgICAgICAgICAgICBbNDEuODU5MDU0MSwgLTg3LjYyNTIwMDddLAogICAgICAgICAgICAgICAge30KICAgICAgICAgICAgKS5hZGRUbyhtYXBfYjZkMWQ5NWI5OTkwNDAzMmE3YmYyNWEyNTVmMzMxMTgpOwogICAgICAgIAogICAgCiAgICAgICAgdmFyIHBvcHVwXzI0YTVhN2IyMzQwMzRjZjY4Y2U3OWVlZWU3OGM5ZDZmID0gTC5wb3B1cCh7Im1heFdpZHRoIjogIjEwMCUifSk7CgogICAgICAgIAogICAgICAgICAgICB2YXIgaHRtbF8wOTkwY2YyN2Y0MTY0ZDRiYjJiZmU3YzFlOTc2NTM0NSA9ICQoYDxkaXYgaWQ9Imh0bWxfMDk5MGNmMjdmNDE2NGQ0YmIyYmZlN2MxZTk3NjUzNDUiIHN0eWxlPSJ3aWR0aDogMTAwLjAlOyBoZWlnaHQ6IDEwMC4wJTsiPkFjYWRpYTwvZGl2PmApWzBdOwogICAgICAgICAgICBwb3B1cF8yNGE1YTdiMjM0MDM0Y2Y2OGNlNzllZWVlNzhjOWQ2Zi5zZXRDb250ZW50KGh0bWxfMDk5MGNmMjdmNDE2NGQ0YmIyYmZlN2MxZTk3NjUzNDUpOwogICAgICAgIAoKICAgICAgICBtYXJrZXJfNGE0ZjdiYjdjYWI3NDhkZDg1ZDU5NzFhYTMwY2VkMmIuYmluZFBvcHVwKHBvcHVwXzI0YTVhN2IyMzQwMzRjZjY4Y2U3OWVlZWU3OGM5ZDZmKQogICAgICAgIDsKCiAgICAgICAgCiAgICAKICAgIAogICAgICAgICAgICB2YXIgbWFya2VyXzJlYjg5NWE0MDU3OTRiZTc5ZmVjYzEyZTJlZGYzZDgxID0gTC5tYXJrZXIoCiAgICAgICAgICAgICAgICBbNDEuOTEwMjAzMSwgLTg3LjY4Mjg3NTI5OTk5OTk5XSwKICAgICAgICAgICAgICAgIHt9CiAgICAgICAgICAgICkuYWRkVG8obWFwX2I2ZDFkOTViOTk5MDQwMzJhN2JmMjVhMjU1ZjMzMTE4KTsKICAgICAgICAKICAgIAogICAgICAgIHZhciBwb3B1cF9iMmQwOTdjN2NjMTY0ZmMxOWJhM2ExNGNiMDk4ZWE0OCA9IEwucG9wdXAoeyJtYXhXaWR0aCI6ICIxMDAlIn0pOwoKICAgICAgICAKICAgICAgICAgICAgdmFyIGh0bWxfY2U0YTBmMDI4NDkzNDA2NjgyMzUyMjc3YzY4N2YyYzkgPSAkKGA8ZGl2IGlkPSJodG1sX2NlNGEwZjAyODQ5MzQwNjY4MjM1MjI3N2M2ODdmMmM5IiBzdHlsZT0id2lkdGg6IDEwMC4wJTsgaGVpZ2h0OiAxMDAuMCU7Ij5CaXJjaHdvb2QgS2l0Y2hlbjwvZGl2PmApWzBdOwogICAgICAgICAgICBwb3B1cF9iMmQwOTdjN2NjMTY0ZmMxOWJhM2ExNGNiMDk4ZWE0OC5zZXRDb250ZW50KGh0bWxfY2U0YTBmMDI4NDkzNDA2NjgyMzUyMjc3YzY4N2YyYzkpOwogICAgICAgIAoKICAgICAgICBtYXJrZXJfMmViODk1YTQwNTc5NGJlNzlmZWNjMTJlMmVkZjNkODEuYmluZFBvcHVwKHBvcHVwX2IyZDA5N2M3Y2MxNjRmYzE5YmEzYTE0Y2IwOThlYTQ4KQogICAgICAgIDsKCiAgICAgICAgCiAgICAKICAgIAogICAgICAgICAgICB2YXIgbWFya2VyXzg1ZTc4ZTkwNTEyMDQwOGE4Y2UwNjY4ZGU5NTAzNzFhID0gTC5tYXJrZXIoCiAgICAgICAgICAgICAgICBbNDEuOTA5NzU1OCwgLTg3LjcxNzY3MjddLAogICAgICAgICAgICAgICAge30KICAgICAgICAgICAgKS5hZGRUbyhtYXBfYjZkMWQ5NWI5OTkwNDAzMmE3YmYyNWEyNTVmMzMxMTgpOwogICAgICAgIAogICAgCiAgICAgICAgdmFyIHBvcHVwXzk1MTcxMjEyYTA0OTQ2ZGZiZjM2M2U0ZjM1NDFhOTQxID0gTC5wb3B1cCh7Im1heFdpZHRoIjogIjEwMCUifSk7CgogICAgICAgIAogICAgICAgICAgICB2YXIgaHRtbF80YTE1YzE3NTc3ODk0OWQ1OGQzMzkwZTRmZjg0NzEyMiA9ICQoYDxkaXYgaWQ9Imh0bWxfNGExNWMxNzU3Nzg5NDlkNThkMzM5MGU0ZmY4NDcxMjIiIHN0eWxlPSJ3aWR0aDogMTAwLjAlOyBoZWlnaHQ6IDEwMC4wJTsiPkNlbWl0YXMgUHVlYmxhPC9kaXY+YClbMF07CiAgICAgICAgICAgIHBvcHVwXzk1MTcxMjEyYTA0OTQ2ZGZiZjM2M2U0ZjM1NDFhOTQxLnNldENvbnRlbnQoaHRtbF80YTE1YzE3NTc3ODk0OWQ1OGQzMzkwZTRmZjg0NzEyMik7CiAgICAgICAgCgogICAgICAgIG1hcmtlcl84NWU3OGU5MDUxMjA0MDhhOGNlMDY2OGRlOTUwMzcxYS5iaW5kUG9wdXAocG9wdXBfOTUxNzEyMTJhMDQ5NDZkZmJmMzYzZTRmMzU0MWE5NDEpCiAgICAgICAgOwoKICAgICAgICAKICAgIAogICAgCiAgICAgICAgICAgIHZhciBtYXJrZXJfYTVjZDk5YTJlYzEyNDYxOWI0NmFlMjYxNDY4MWFiZmUgPSBMLm1hcmtlcigKICAgICAgICAgICAgICAgIFs0MS44MzQ1MzAyLCAtODcuNjQ1NjQ5Ml0sCiAgICAgICAgICAgICAgICB7fQogICAgICAgICAgICApLmFkZFRvKG1hcF9iNmQxZDk1Yjk5OTA0MDMyYTdiZjI1YTI1NWYzMzExOCk7CiAgICAgICAgCiAgICAKICAgICAgICB2YXIgcG9wdXBfNTJhYzMxYWRmOTYwNGFhOWI4NDRjMzhlZWVmYjUwNjEgPSBMLnBvcHVwKHsibWF4V2lkdGgiOiAiMTAwJSJ9KTsKCiAgICAgICAgCiAgICAgICAgICAgIHZhciBodG1sX2VhYjcyNTAwOWYzNzQ0N2FiNDRhZjc2MDg2YTc3YWIxID0gJChgPGRpdiBpZD0iaHRtbF9lYWI3MjUwMDlmMzc0NDdhYjQ0YWY3NjA4NmE3N2FiMSIgc3R5bGU9IndpZHRoOiAxMDAuMCU7IGhlaWdodDogMTAwLjAlOyI+TmFuYTwvZGl2PmApWzBdOwogICAgICAgICAgICBwb3B1cF81MmFjMzFhZGY5NjA0YWE5Yjg0NGMzOGVlZWZiNTA2MS5zZXRDb250ZW50KGh0bWxfZWFiNzI1MDA5ZjM3NDQ3YWI0NGFmNzYwODZhNzdhYjEpOwogICAgICAgIAoKICAgICAgICBtYXJrZXJfYTVjZDk5YTJlYzEyNDYxOWI0NmFlMjYxNDY4MWFiZmUuYmluZFBvcHVwKHBvcHVwXzUyYWMzMWFkZjk2MDRhYTliODQ0YzM4ZWVlZmI1MDYxKQogICAgICAgIDsKCiAgICAgICAgCiAgICAKICAgIAogICAgICAgICAgICB2YXIgbWFya2VyXzcxOGFkMjQ0Mzk5ZDRhNjI5ZmI0MDY4YjA2OGQ1MGU2ID0gTC5tYXJrZXIoCiAgICAgICAgICAgICAgICBbNDEuOTI3NjIwNywgLTg3LjcwNjc5Ml0sCiAgICAgICAgICAgICAgICB7fQogICAgICAgICAgICApLmFkZFRvKG1hcF9iNmQxZDk1Yjk5OTA0MDMyYTdiZjI1YTI1NWYzMzExOCk7CiAgICAgICAgCiAgICAKICAgICAgICB2YXIgcG9wdXBfYzJkOTI4MjgxNzRiNGFkZDlmMTZjOWJjMjRkMGYxYjggPSBMLnBvcHVwKHsibWF4V2lkdGgiOiAiMTAwJSJ9KTsKCiAgICAgICAgCiAgICAgICAgICAgIHZhciBodG1sX2QxOTdhZWE5NmQ4ODQyNjJiNmI5OTJmZTU3OWM1NTcxID0gJChgPGRpdiBpZD0iaHRtbF9kMTk3YWVhOTZkODg0MjYyYjZiOTkyZmU1NzljNTU3MSIgc3R5bGU9IndpZHRoOiAxMDAuMCU7IGhlaWdodDogMTAwLjAlOyI+THVsYSBDYWZlPC9kaXY+YClbMF07CiAgICAgICAgICAgIHBvcHVwX2MyZDkyODI4MTc0YjRhZGQ5ZjE2YzliYzI0ZDBmMWI4LnNldENvbnRlbnQoaHRtbF9kMTk3YWVhOTZkODg0MjYyYjZiOTkyZmU1NzljNTU3MSk7CiAgICAgICAgCgogICAgICAgIG1hcmtlcl83MThhZDI0NDM5OWQ0YTYyOWZiNDA2OGIwNjhkNTBlNi5iaW5kUG9wdXAocG9wdXBfYzJkOTI4MjgxNzRiNGFkZDlmMTZjOWJjMjRkMGYxYjgpCiAgICAgICAgOwoKICAgICAgICAKICAgIAogICAgCiAgICAgICAgICAgIHZhciBtYXJrZXJfMTA2NzcwZWNmYzk4NGYzNTllMjg5ODAxMjBiMzE2NGUgPSBMLm1hcmtlcigKICAgICAgICAgICAgICAgIFs0MS45Mzg0NDE5LCAtODcuNjQ0NjQzNjk5OTk5OTldLAogICAgICAgICAgICAgICAge30KICAgICAgICAgICAgKS5hZGRUbyhtYXBfYjZkMWQ5NWI5OTkwNDAzMmE3YmYyNWEyNTVmMzMxMTgpOwogICAgICAgIAogICAgCiAgICAgICAgdmFyIHBvcHVwX2E5YzAyYWVkMzNiNjQxZDBiYjJkMjkyZWIzMWI2YmVkID0gTC5wb3B1cCh7Im1heFdpZHRoIjogIjEwMCUifSk7CgogICAgICAgIAogICAgICAgICAgICB2YXIgaHRtbF9kYzFiMzRiYTk3OWU0YWQ2YmM3ZTMzMTczYzIyNzY1YyA9ICQoYDxkaXYgaWQ9Imh0bWxfZGMxYjM0YmE5NzllNGFkNmJjN2UzMzE3M2MyMjc2NWMiIHN0eWxlPSJ3aWR0aDogMTAwLjAlOyBoZWlnaHQ6IDEwMC4wJTsiPkZyb2cgbiBTbmFpbDwvZGl2PmApWzBdOwogICAgICAgICAgICBwb3B1cF9hOWMwMmFlZDMzYjY0MWQwYmIyZDI5MmViMzFiNmJlZC5zZXRDb250ZW50KGh0bWxfZGMxYjM0YmE5NzllNGFkNmJjN2UzMzE3M2MyMjc2NWMpOwogICAgICAgIAoKICAgICAgICBtYXJrZXJfMTA2NzcwZWNmYzk4NGYzNTllMjg5ODAxMjBiMzE2NGUuYmluZFBvcHVwKHBvcHVwX2E5YzAyYWVkMzNiNjQxZDBiYjJkMjkyZWIzMWI2YmVkKQogICAgICAgIDsKCiAgICAgICAgCiAgICAKICAgIAogICAgICAgICAgICB2YXIgbWFya2VyXzQyMDUwZmE5ZGMxYzQwYzdiYzVjYTY3OWU2YzIwZDdhID0gTC5tYXJrZXIoCiAgICAgICAgICAgICAgICBbNDEuOTQ1MTA0NCwgLTg3LjY2MzY4MTJdLAogICAgICAgICAgICAgICAge30KICAgICAgICAgICAgKS5hZGRUbyhtYXBfYjZkMWQ5NWI5OTkwNDAzMmE3YmYyNWEyNTVmMzMxMTgpOwogICAgICAgIAogICAgCiAgICAgICAgdmFyIHBvcHVwX2I5YWNkZjZhY2U0NTQ1Yzc4NGJjZGM2MjBjYzY2NzE2ID0gTC5wb3B1cCh7Im1heFdpZHRoIjogIjEwMCUifSk7CgogICAgICAgIAogICAgICAgICAgICB2YXIgaHRtbF8xNDJkMGVhMzMwMmM0MDYwYTdiNjk1ZDdiNDk1OTE2ZCA9ICQoYDxkaXYgaWQ9Imh0bWxfMTQyZDBlYTMzMDJjNDA2MGE3YjY5NWQ3YjQ5NTkxNmQiIHN0eWxlPSJ3aWR0aDogMTAwLjAlOyBoZWlnaHQ6IDEwMC4wJTsiPkNyb3NieeKAmXMgS2l0Y2hlbjwvZGl2PmApWzBdOwogICAgICAgICAgICBwb3B1cF9iOWFjZGY2YWNlNDU0NWM3ODRiY2RjNjIwY2M2NjcxNi5zZXRDb250ZW50KGh0bWxfMTQyZDBlYTMzMDJjNDA2MGE3YjY5NWQ3YjQ5NTkxNmQpOwogICAgICAgIAoKICAgICAgICBtYXJrZXJfNDIwNTBmYTlkYzFjNDBjN2JjNWNhNjc5ZTZjMjBkN2EuYmluZFBvcHVwKHBvcHVwX2I5YWNkZjZhY2U0NTQ1Yzc4NGJjZGM2MjBjYzY2NzE2KQogICAgICAgIDsKCiAgICAgICAgCiAgICAKICAgIAogICAgICAgICAgICB2YXIgbWFya2VyXzhkOGIxMjA3MTBkYTQ2ZTliNmUxZjQzNzZmMGM4YWRmID0gTC5tYXJrZXIoCiAgICAgICAgICAgICAgICBbNDEuOTMwMTA5LCAtODcuNzA3MjQwOF0sCiAgICAgICAgICAgICAgICB7fQogICAgICAgICAgICApLmFkZFRvKG1hcF9iNmQxZDk1Yjk5OTA0MDMyYTdiZjI1YTI1NWYzMzExOCk7CiAgICAgICAgCiAgICAKICAgICAgICB2YXIgcG9wdXBfM2FhZDRmYzFlZTdiNGVjZDk0NDc4NWQyNzE3YTNjMzcgPSBMLnBvcHVwKHsibWF4V2lkdGgiOiAiMTAwJSJ9KTsKCiAgICAgICAgCiAgICAgICAgICAgIHZhciBodG1sX2NmYTEwZTk1OWZiZjQzNDg5MWJmMDRiNTVjNjk5NmMzID0gJChgPGRpdiBpZD0iaHRtbF9jZmExMGU5NTlmYmY0MzQ4OTFiZjA0YjU1YzY5OTZjMyIgc3R5bGU9IndpZHRoOiAxMDAuMCU7IGhlaWdodDogMTAwLjAlOyI+TG9uZ21hbiAmIEVhZ2xlPC9kaXY+YClbMF07CiAgICAgICAgICAgIHBvcHVwXzNhYWQ0ZmMxZWU3YjRlY2Q5NDQ3ODVkMjcxN2EzYzM3LnNldENvbnRlbnQoaHRtbF9jZmExMGU5NTlmYmY0MzQ4OTFiZjA0YjU1YzY5OTZjMyk7CiAgICAgICAgCgogICAgICAgIG1hcmtlcl84ZDhiMTIwNzEwZGE0NmU5YjZlMWY0Mzc2ZjBjOGFkZi5iaW5kUG9wdXAocG9wdXBfM2FhZDRmYzFlZTdiNGVjZDk0NDc4NWQyNzE3YTNjMzcpCiAgICAgICAgOwoKICAgICAgICAKICAgIAogICAgCiAgICAgICAgICAgIHZhciBtYXJrZXJfZWNlMzFmMjYzMTM5NDM4ZjhlNjRjMjQyZjkzMWFmNTIgPSBMLm1hcmtlcigKICAgICAgICAgICAgICAgIFs0MS44OTEyOTcxLCAtODcuNjU1NTQ1M10sCiAgICAgICAgICAgICAgICB7fQogICAgICAgICAgICApLmFkZFRvKG1hcF9iNmQxZDk1Yjk5OTA0MDMyYTdiZjI1YTI1NWYzMzExOCk7CiAgICAgICAgCiAgICAKICAgICAgICB2YXIgcG9wdXBfZTg2YTcwNTk0N2E0NGIxOWJjNmMzYmM5MmNmYWJiMDEgPSBMLnBvcHVwKHsibWF4V2lkdGgiOiAiMTAwJSJ9KTsKCiAgICAgICAgCiAgICAgICAgICAgIHZhciBodG1sXzQzMjRlNDE2NTk3YjQ1YzRiYWZmZjBmMDFiODJhMjdjID0gJChgPGRpdiBpZD0iaHRtbF80MzI0ZTQxNjU5N2I0NWM0YmFmZmYwZjAxYjgyYTI3YyIgc3R5bGU9IndpZHRoOiAxMDAuMCU7IGhlaWdodDogMTAwLjAlOyI+QmFyaTwvZGl2PmApWzBdOwogICAgICAgICAgICBwb3B1cF9lODZhNzA1OTQ3YTQ0YjE5YmM2YzNiYzkyY2ZhYmIwMS5zZXRDb250ZW50KGh0bWxfNDMyNGU0MTY1OTdiNDVjNGJhZmZmMGYwMWI4MmEyN2MpOwogICAgICAgIAoKICAgICAgICBtYXJrZXJfZWNlMzFmMjYzMTM5NDM4ZjhlNjRjMjQyZjkzMWFmNTIuYmluZFBvcHVwKHBvcHVwX2U4NmE3MDU5NDdhNDRiMTliYzZjM2JjOTJjZmFiYjAxKQogICAgICAgIDsKCiAgICAgICAgCiAgICAKICAgIAogICAgICAgICAgICB2YXIgbWFya2VyXzMyYmJiMDE0MjJiMDQ2NTQ5NWJiMjJkYjgwZDNlZWJjID0gTC5tYXJrZXIoCiAgICAgICAgICAgICAgICBbNDEuODY3ODUyOSwgLTg3LjY0MTkyODldLAogICAgICAgICAgICAgICAge30KICAgICAgICAgICAgKS5hZGRUbyhtYXBfYjZkMWQ5NWI5OTkwNDAzMmE3YmYyNWEyNTVmMzMxMTgpOwogICAgICAgIAogICAgCiAgICAgICAgdmFyIHBvcHVwXzcxZTRhYzdmY2VlOTQ4NmVhMzNiYjkwOTBmNWE2OWRiID0gTC5wb3B1cCh7Im1heFdpZHRoIjogIjEwMCUifSk7CgogICAgICAgIAogICAgICAgICAgICB2YXIgaHRtbF9iOTgxMmVlYTYyOTM0MWFiOGQ5Nzc5YzZiY2I1ZTU2NyA9ICQoYDxkaXYgaWQ9Imh0bWxfYjk4MTJlZWE2MjkzNDFhYjhkOTc3OWM2YmNiNWU1NjciIHN0eWxlPSJ3aWR0aDogMTAwLjAlOyBoZWlnaHQ6IDEwMC4wJTsiPk1hbm554oCZczwvZGl2PmApWzBdOwogICAgICAgICAgICBwb3B1cF83MWU0YWM3ZmNlZTk0ODZlYTMzYmI5MDkwZjVhNjlkYi5zZXRDb250ZW50KGh0bWxfYjk4MTJlZWE2MjkzNDFhYjhkOTc3OWM2YmNiNWU1NjcpOwogICAgICAgIAoKICAgICAgICBtYXJrZXJfMzJiYmIwMTQyMmIwNDY1NDk1YmIyMmRiODBkM2VlYmMuYmluZFBvcHVwKHBvcHVwXzcxZTRhYzdmY2VlOTQ4NmVhMzNiYjkwOTBmNWE2OWRiKQogICAgICAgIDsKCiAgICAgICAgCiAgICAKICAgIAogICAgICAgICAgICB2YXIgbWFya2VyX2QyZGRlNDkwN2RkOTRlNDU5OWFmYjhkMDE3MjMxMzk3ID0gTC5tYXJrZXIoCiAgICAgICAgICAgICAgICBbNDEuODg1MjY5MSwgLTg3LjYxODQ4MzddLAogICAgICAgICAgICAgICAge30KICAgICAgICAgICAgKS5hZGRUbyhtYXBfYjZkMWQ5NWI5OTkwNDAzMmE3YmYyNWEyNTVmMzMxMTgpOwogICAgICAgIAogICAgCiAgICAgICAgdmFyIHBvcHVwX2QwNTY2YWIzODdjNzQ0YzY4YjgzZmE1ZDNkZGNhZTY3ID0gTC5wb3B1cCh7Im1heFdpZHRoIjogIjEwMCUifSk7CgogICAgICAgIAogICAgICAgICAgICB2YXIgaHRtbF9mYWE1ZDcwY2ZmYzM0YWZjODU2ZjliYmY5OWJhYzVlMyA9ICQoYDxkaXYgaWQ9Imh0bWxfZmFhNWQ3MGNmZmMzNGFmYzg1NmY5YmJmOTliYWM1ZTMiIHN0eWxlPSJ3aWR0aDogMTAwLjAlOyBoZWlnaHQ6IDEwMC4wJTsiPkVnZ3nigJlzPC9kaXY+YClbMF07CiAgICAgICAgICAgIHBvcHVwX2QwNTY2YWIzODdjNzQ0YzY4YjgzZmE1ZDNkZGNhZTY3LnNldENvbnRlbnQoaHRtbF9mYWE1ZDcwY2ZmYzM0YWZjODU2ZjliYmY5OWJhYzVlMyk7CiAgICAgICAgCgogICAgICAgIG1hcmtlcl9kMmRkZTQ5MDdkZDk0ZTQ1OTlhZmI4ZDAxNzIzMTM5Ny5iaW5kUG9wdXAocG9wdXBfZDA1NjZhYjM4N2M3NDRjNjhiODNmYTVkM2RkY2FlNjcpCiAgICAgICAgOwoKICAgICAgICAKICAgIAogICAgCiAgICAgICAgICAgIHZhciBtYXJrZXJfNzAxOGU0YWI1NjExNGE1YmJhZjM3NDNkZTFlYmZkMTAgPSBMLm1hcmtlcigKICAgICAgICAgICAgICAgIFs0MS45MDgwNTM5LCAtODcuNjM0MzExM10sCiAgICAgICAgICAgICAgICB7fQogICAgICAgICAgICApLmFkZFRvKG1hcF9iNmQxZDk1Yjk5OTA0MDMyYTdiZjI1YTI1NWYzMzExOCk7CiAgICAgICAgCiAgICAKICAgICAgICB2YXIgcG9wdXBfNGY3NWZiNmQ5ZDRkNDQzZjlkOGJmMGRiZDkyMjZiMjEgPSBMLnBvcHVwKHsibWF4V2lkdGgiOiAiMTAwJSJ9KTsKCiAgICAgICAgCiAgICAgICAgICAgIHZhciBodG1sX2NhZTc3ZDBkNTY3YzQ2ZTBiMDRkYjI1ZDYyZTg5OWJmID0gJChgPGRpdiBpZD0iaHRtbF9jYWU3N2QwZDU2N2M0NmUwYjA0ZGIyNWQ2MmU4OTliZiIgc3R5bGU9IndpZHRoOiAxMDAuMCU7IGhlaWdodDogMTAwLjAlOyI+T2xkIEplcnVzYWxlbTwvZGl2PmApWzBdOwogICAgICAgICAgICBwb3B1cF80Zjc1ZmI2ZDlkNGQ0NDNmOWQ4YmYwZGJkOTIyNmIyMS5zZXRDb250ZW50KGh0bWxfY2FlNzdkMGQ1NjdjNDZlMGIwNGRiMjVkNjJlODk5YmYpOwogICAgICAgIAoKICAgICAgICBtYXJrZXJfNzAxOGU0YWI1NjExNGE1YmJhZjM3NDNkZTFlYmZkMTAuYmluZFBvcHVwKHBvcHVwXzRmNzVmYjZkOWQ0ZDQ0M2Y5ZDhiZjBkYmQ5MjI2YjIxKQogICAgICAgIDsKCiAgICAgICAgCiAgICAKICAgIAogICAgICAgICAgICB2YXIgbWFya2VyXzMxNGU0ZmZmYzA5YjQwNGZiNGY4MDAxNTQ1NGVjYzIwID0gTC5tYXJrZXIoCiAgICAgICAgICAgICAgICBbNDEuOTEzNjk1Mzk5OTk5OTksIC04Ny42NzcxMjczXSwKICAgICAgICAgICAgICAgIHt9CiAgICAgICAgICAgICkuYWRkVG8obWFwX2I2ZDFkOTViOTk5MDQwMzJhN2JmMjVhMjU1ZjMzMTE4KTsKICAgICAgICAKICAgIAogICAgICAgIHZhciBwb3B1cF9kZWM2ZGJiZmUxZDY0MWQwYjI3ZTgzYjc3OWZhMjMwOSA9IEwucG9wdXAoeyJtYXhXaWR0aCI6ICIxMDAlIn0pOwoKICAgICAgICAKICAgICAgICAgICAgdmFyIGh0bWxfZjE4ZWFhNTUxYzVhNGQxYjgyZTNjM2Q3OTZiOGFhNzIgPSAkKGA8ZGl2IGlkPSJodG1sX2YxOGVhYTU1MWM1YTRkMWI4MmUzYzNkNzk2YjhhYTcyIiBzdHlsZT0id2lkdGg6IDEwMC4wJTsgaGVpZ2h0OiAxMDAuMCU7Ij5NaW5keeKAmXMgSG90Q2hvY29sYXRlPC9kaXY+YClbMF07CiAgICAgICAgICAgIHBvcHVwX2RlYzZkYmJmZTFkNjQxZDBiMjdlODNiNzc5ZmEyMzA5LnNldENvbnRlbnQoaHRtbF9mMThlYWE1NTFjNWE0ZDFiODJlM2MzZDc5NmI4YWE3Mik7CiAgICAgICAgCgogICAgICAgIG1hcmtlcl8zMTRlNGZmZmMwOWI0MDRmYjRmODAwMTU0NTRlY2MyMC5iaW5kUG9wdXAocG9wdXBfZGVjNmRiYmZlMWQ2NDFkMGIyN2U4M2I3NzlmYTIzMDkpCiAgICAgICAgOwoKICAgICAgICAKICAgIAogICAgCiAgICAgICAgICAgIHZhciBtYXJrZXJfMjQyY2VlNTU1YWVkNDdhZGE2MWI4NTBjNjAzMzZjZWMgPSBMLm1hcmtlcigKICAgICAgICAgICAgICAgIFs0MS45NTM2ODg3LCAtODcuNzA4NDQ5OF0sCiAgICAgICAgICAgICAgICB7fQogICAgICAgICAgICApLmFkZFRvKG1hcF9iNmQxZDk1Yjk5OTA0MDMyYTdiZjI1YTI1NWYzMzExOCk7CiAgICAgICAgCiAgICAKICAgICAgICB2YXIgcG9wdXBfZjcwZGVmMmNmZjc2NGRkNWFjYjk2ZTE1OGJkNWIwNDQgPSBMLnBvcHVwKHsibWF4V2lkdGgiOiAiMTAwJSJ9KTsKCiAgICAgICAgCiAgICAgICAgICAgIHZhciBodG1sX2RhYTI2ZGVmOGY5ZTRhNWE4YjI1ZmRiMGQxNjJkN2QxID0gJChgPGRpdiBpZD0iaHRtbF9kYWEyNmRlZjhmOWU0YTVhOGIyNWZkYjBkMTYyZDdkMSIgc3R5bGU9IndpZHRoOiAxMDAuMCU7IGhlaWdodDogMTAwLjAlOyI+T2xnYeKAmXMgRGVsaWNhdGVzc2VuPC9kaXY+YClbMF07CiAgICAgICAgICAgIHBvcHVwX2Y3MGRlZjJjZmY3NjRkZDVhY2I5NmUxNThiZDViMDQ0LnNldENvbnRlbnQoaHRtbF9kYWEyNmRlZjhmOWU0YTVhOGIyNWZkYjBkMTYyZDdkMSk7CiAgICAgICAgCgogICAgICAgIG1hcmtlcl8yNDJjZWU1NTVhZWQ0N2FkYTYxYjg1MGM2MDMzNmNlYy5iaW5kUG9wdXAocG9wdXBfZjcwZGVmMmNmZjc2NGRkNWFjYjk2ZTE1OGJkNWIwNDQpCiAgICAgICAgOwoKICAgICAgICAKICAgIAogICAgCiAgICAgICAgICAgIHZhciBtYXJrZXJfYmExMTIwZDI3N2NjNDM2NDg0MzhkZmQwYTEzMmQ1NzEgPSBMLm1hcmtlcigKICAgICAgICAgICAgICAgIFs0MS45Nzk0NDk2LCAtODcuNjY3OTU3MTk5OTk5OTldLAogICAgICAgICAgICAgICAge30KICAgICAgICAgICAgKS5hZGRUbyhtYXBfYjZkMWQ5NWI5OTkwNDAzMmE3YmYyNWEyNTVmMzMxMTgpOwogICAgICAgIAogICAgCiAgICAgICAgdmFyIHBvcHVwXzllZTZkNmNlZWRmMDQzMWZhZTJkYjI2YWMxNjNhYzE3ID0gTC5wb3B1cCh7Im1heFdpZHRoIjogIjEwMCUifSk7CgogICAgICAgIAogICAgICAgICAgICB2YXIgaHRtbF9kYzAzMmQyNzJmMmI0ODJlOGZmODY5ZDk1OWQ2OWU2OSA9ICQoYDxkaXYgaWQ9Imh0bWxfZGMwMzJkMjcyZjJiNDgyZThmZjg2OWQ5NTlkNjllNjkiIHN0eWxlPSJ3aWR0aDogMTAwLjAlOyBoZWlnaHQ6IDEwMC4wJTsiPkJpZyBKb25lczwvZGl2PmApWzBdOwogICAgICAgICAgICBwb3B1cF85ZWU2ZDZjZWVkZjA0MzFmYWUyZGIyNmFjMTYzYWMxNy5zZXRDb250ZW50KGh0bWxfZGMwMzJkMjcyZjJiNDgyZThmZjg2OWQ5NTlkNjllNjkpOwogICAgICAgIAoKICAgICAgICBtYXJrZXJfYmExMTIwZDI3N2NjNDM2NDg0MzhkZmQwYTEzMmQ1NzEuYmluZFBvcHVwKHBvcHVwXzllZTZkNmNlZWRmMDQzMWZhZTJkYjI2YWMxNjNhYzE3KQogICAgICAgIDsKCiAgICAgICAgCiAgICAKICAgIAogICAgICAgICAgICB2YXIgbWFya2VyX2M5Nzc1NGJjMmQ1YzQ1MmViZGFjZTZkMTdhZGM1ZjIxID0gTC5tYXJrZXIoCiAgICAgICAgICAgICAgICBbNDEuOTU0MTU5MiwgLTg3LjcwMjcxMDc5OTk5OTk5XSwKICAgICAgICAgICAgICAgIHt9CiAgICAgICAgICAgICkuYWRkVG8obWFwX2I2ZDFkOTViOTk5MDQwMzJhN2JmMjVhMjU1ZjMzMTE4KTsKICAgICAgICAKICAgIAogICAgICAgIHZhciBwb3B1cF9lNTc3OGE5NDE1ODg0YTZiODMzMzY2NzRlY2JjNmYxNSA9IEwucG9wdXAoeyJtYXhXaWR0aCI6ICIxMDAlIn0pOwoKICAgICAgICAKICAgICAgICAgICAgdmFyIGh0bWxfNzE0MmQwYmE3MmVmNDdhNjhlMmM5NGVlODJjYzlhZTIgPSAkKGA8ZGl2IGlkPSJodG1sXzcxNDJkMGJhNzJlZjQ3YTY4ZTJjOTRlZTgyY2M5YWUyIiBzdHlsZT0id2lkdGg6IDEwMC4wJTsgaGVpZ2h0OiAxMDAuMCU7Ij5MYSBQYW5lPC9kaXY+YClbMF07CiAgICAgICAgICAgIHBvcHVwX2U1Nzc4YTk0MTU4ODRhNmI4MzMzNjY3NGVjYmM2ZjE1LnNldENvbnRlbnQoaHRtbF83MTQyZDBiYTcyZWY0N2E2OGUyYzk0ZWU4MmNjOWFlMik7CiAgICAgICAgCgogICAgICAgIG1hcmtlcl9jOTc3NTRiYzJkNWM0NTJlYmRhY2U2ZDE3YWRjNWYyMS5iaW5kUG9wdXAocG9wdXBfZTU3NzhhOTQxNTg4NGE2YjgzMzM2Njc0ZWNiYzZmMTUpCiAgICAgICAgOwoKICAgICAgICAKICAgIAogICAgCiAgICAgICAgICAgIHZhciBtYXJrZXJfNzc2ZTNmNTYyNDhhNDBhMTkwYzdjYzFjNThkMWZhYTIgPSBMLm1hcmtlcigKICAgICAgICAgICAgICAgIFs0Mi4xNTY2OTEsIC04Ny44MDM2MThdLAogICAgICAgICAgICAgICAge30KICAgICAgICAgICAgKS5hZGRUbyhtYXBfYjZkMWQ5NWI5OTkwNDAzMmE3YmYyNWEyNTVmMzMxMTgpOwogICAgICAgIAogICAgCiAgICAgICAgdmFyIHBvcHVwX2RjMGM2N2MwOGQxNzQ1Mzk5NzY2YmVhZTkwMDVjNDU2ID0gTC5wb3B1cCh7Im1heFdpZHRoIjogIjEwMCUifSk7CgogICAgICAgIAogICAgICAgICAgICB2YXIgaHRtbF84NDllZDFlYzg5ZWE0YTcxYWMyMDA4NTZkNzEzOTYzZCA9ICQoYDxkaXYgaWQ9Imh0bWxfODQ5ZWQxZWM4OWVhNGE3MWFjMjAwODU2ZDcxMzk2M2QiIHN0eWxlPSJ3aWR0aDogMTAwLjAlOyBoZWlnaHQ6IDEwMC4wJTsiPk1heOKAmXMgRGVsaTwvZGl2PmApWzBdOwogICAgICAgICAgICBwb3B1cF9kYzBjNjdjMDhkMTc0NTM5OTc2NmJlYWU5MDA1YzQ1Ni5zZXRDb250ZW50KGh0bWxfODQ5ZWQxZWM4OWVhNGE3MWFjMjAwODU2ZDcxMzk2M2QpOwogICAgICAgIAoKICAgICAgICBtYXJrZXJfNzc2ZTNmNTYyNDhhNDBhMTkwYzdjYzFjNThkMWZhYTIuYmluZFBvcHVwKHBvcHVwX2RjMGM2N2MwOGQxNzQ1Mzk5NzY2YmVhZTkwMDVjNDU2KQogICAgICAgIDsKCiAgICAgICAgCiAgICAKICAgIAogICAgICAgICAgICB2YXIgbWFya2VyX2UwYmJkNGExYWIxYTQyMTJiZjM5ODg2YzA4N2I1OGNmID0gTC5tYXJrZXIoCiAgICAgICAgICAgICAgICBbNDEuOTY1MjYyNywgLTg3LjY3NTUyMjE5OTk5OTk5XSwKICAgICAgICAgICAgICAgIHt9CiAgICAgICAgICAgICkuYWRkVG8obWFwX2I2ZDFkOTViOTk5MDQwMzJhN2JmMjVhMjU1ZjMzMTE4KTsKICAgICAgICAKICAgIAogICAgICAgIHZhciBwb3B1cF8yNTEwZDQ1MTVmODM0M2YzYTJjM2JjNzQ2MzMxYzM1MyA9IEwucG9wdXAoeyJtYXhXaWR0aCI6ICIxMDAlIn0pOwoKICAgICAgICAKICAgICAgICAgICAgdmFyIGh0bWxfZThhNDcyYTk5ZDE2NDM4NmJhZWNjNzgwMTE0MThiNjggPSAkKGA8ZGl2IGlkPSJodG1sX2U4YTQ3MmE5OWQxNjQzODZiYWVjYzc4MDExNDE4YjY4IiBzdHlsZT0id2lkdGg6IDEwMC4wJTsgaGVpZ2h0OiAxMDAuMCU7Ij5DaXR5IFByb3Zpc2lvbnM8L2Rpdj5gKVswXTsKICAgICAgICAgICAgcG9wdXBfMjUxMGQ0NTE1ZjgzNDNmM2EyYzNiYzc0NjMzMWMzNTMuc2V0Q29udGVudChodG1sX2U4YTQ3MmE5OWQxNjQzODZiYWVjYzc4MDExNDE4YjY4KTsKICAgICAgICAKCiAgICAgICAgbWFya2VyX2UwYmJkNGExYWIxYTQyMTJiZjM5ODg2YzA4N2I1OGNmLmJpbmRQb3B1cChwb3B1cF8yNTEwZDQ1MTVmODM0M2YzYTJjM2JjNzQ2MzMxYzM1MykKICAgICAgICA7CgogICAgICAgIAogICAgCiAgICAKICAgICAgICAgICAgdmFyIG1hcmtlcl9kN2IxN2UyNjBjN2M0Nzc3YTE4YjMzNzUzNjFkOGYxMyA9IEwubWFya2VyKAogICAgICAgICAgICAgICAgWzQxLjkwMjcxNzgsIC04Ny42OTAyMTkyXSwKICAgICAgICAgICAgICAgIHt9CiAgICAgICAgICAgICkuYWRkVG8obWFwX2I2ZDFkOTViOTk5MDQwMzJhN2JmMjVhMjU1ZjMzMTE4KTsKICAgICAgICAKICAgIAogICAgICAgIHZhciBwb3B1cF8yZTZiZWM3OGU3MWI0ODgyYWI1MjdlMjQwYTQ3NzE5ZSA9IEwucG9wdXAoeyJtYXhXaWR0aCI6ICIxMDAlIn0pOwoKICAgICAgICAKICAgICAgICAgICAgdmFyIGh0bWxfMTA1ODliYWZhNWNiNDExYzg4OTQ1ZDM5OTI1NzljZWUgPSAkKGA8ZGl2IGlkPSJodG1sXzEwNTg5YmFmYTVjYjQxMWM4ODk0NWQzOTkyNTc5Y2VlIiBzdHlsZT0id2lkdGg6IDEwMC4wJTsgaGVpZ2h0OiAxMDAuMCU7Ij5QYXBh4oCZcyBDYWNoZSBTYWJyb3NvPC9kaXY+YClbMF07CiAgICAgICAgICAgIHBvcHVwXzJlNmJlYzc4ZTcxYjQ4ODJhYjUyN2UyNDBhNDc3MTllLnNldENvbnRlbnQoaHRtbF8xMDU4OWJhZmE1Y2I0MTFjODg5NDVkMzk5MjU3OWNlZSk7CiAgICAgICAgCgogICAgICAgIG1hcmtlcl9kN2IxN2UyNjBjN2M0Nzc3YTE4YjMzNzUzNjFkOGYxMy5iaW5kUG9wdXAocG9wdXBfMmU2YmVjNzhlNzFiNDg4MmFiNTI3ZTI0MGE0NzcxOWUpCiAgICAgICAgOwoKICAgICAgICAKICAgIAogICAgCiAgICAgICAgICAgIHZhciBtYXJrZXJfNDE1NTNkNGQxODBiNDBhOGJjYTZhZThhMjEyNjJkMjMgPSBMLm1hcmtlcigKICAgICAgICAgICAgICAgIFs0MS44ODkzNjgzLCAtODcuNjM0OTQ4N10sCiAgICAgICAgICAgICAgICB7fQogICAgICAgICAgICApLmFkZFRvKG1hcF9iNmQxZDk1Yjk5OTA0MDMyYTdiZjI1YTI1NWYzMzExOCk7CiAgICAgICAgCiAgICAKICAgICAgICB2YXIgcG9wdXBfNGFkY2JkMWFjOTZlNDE0ZTljOTU2NTcwYTlhOWEzZjQgPSBMLnBvcHVwKHsibWF4V2lkdGgiOiAiMTAwJSJ9KTsKCiAgICAgICAgCiAgICAgICAgICAgIHZhciBodG1sXzM5ZDBiNWNjZTczMzRjNWZhM2VjZDJjNmJjNTlkZTdiID0gJChgPGRpdiBpZD0iaHRtbF8zOWQwYjVjY2U3MzM0YzVmYTNlY2QyYzZiYzU5ZGU3YiIgc3R5bGU9IndpZHRoOiAxMDAuMCU7IGhlaWdodDogMTAwLjAlOyI+QmF2ZXR0ZeKAmXMgQmFyICYgQm9ldWY8L2Rpdj5gKVswXTsKICAgICAgICAgICAgcG9wdXBfNGFkY2JkMWFjOTZlNDE0ZTljOTU2NTcwYTlhOWEzZjQuc2V0Q29udGVudChodG1sXzM5ZDBiNWNjZTczMzRjNWZhM2VjZDJjNmJjNTlkZTdiKTsKICAgICAgICAKCiAgICAgICAgbWFya2VyXzQxNTUzZDRkMTgwYjQwYThiY2E2YWU4YTIxMjYyZDIzLmJpbmRQb3B1cChwb3B1cF80YWRjYmQxYWM5NmU0MTRlOWM5NTY1NzBhOWE5YTNmNCkKICAgICAgICA7CgogICAgICAgIAogICAgCiAgICAKICAgICAgICAgICAgdmFyIG1hcmtlcl8zZjIyZWExNzE0ZGI0ZTA3YTNmYjI4MTZjZmM2ZTI5MyA9IEwubWFya2VyKAogICAgICAgICAgICAgICAgWzQxLjkxMDUyNTgsIC04Ny42MzQzNzc1XSwKICAgICAgICAgICAgICAgIHt9CiAgICAgICAgICAgICkuYWRkVG8obWFwX2I2ZDFkOTViOTk5MDQwMzJhN2JmMjVhMjU1ZjMzMTE4KTsKICAgICAgICAKICAgIAogICAgICAgIHZhciBwb3B1cF80MmU3NjUzNDljNzY0ODg4YjViOGVhMGIzYzk3MzgwNiA9IEwucG9wdXAoeyJtYXhXaWR0aCI6ICIxMDAlIn0pOwoKICAgICAgICAKICAgICAgICAgICAgdmFyIGh0bWxfMjdkZmMwNjFhYTE2NGVhNTlhNmUzMWVhMjZkMmU3ODcgPSAkKGA8ZGl2IGlkPSJodG1sXzI3ZGZjMDYxYWExNjRlYTU5YTZlMzFlYTI2ZDJlNzg3IiBzdHlsZT0id2lkdGg6IDEwMC4wJTsgaGVpZ2h0OiAxMDAuMCU7Ij5MYSBGb3VybmV0dGU8L2Rpdj5gKVswXTsKICAgICAgICAgICAgcG9wdXBfNDJlNzY1MzQ5Yzc2NDg4OGI1YjhlYTBiM2M5NzM4MDYuc2V0Q29udGVudChodG1sXzI3ZGZjMDYxYWExNjRlYTU5YTZlMzFlYTI2ZDJlNzg3KTsKICAgICAgICAKCiAgICAgICAgbWFya2VyXzNmMjJlYTE3MTRkYjRlMDdhM2ZiMjgxNmNmYzZlMjkzLmJpbmRQb3B1cChwb3B1cF80MmU3NjUzNDljNzY0ODg4YjViOGVhMGIzYzk3MzgwNikKICAgICAgICA7CgogICAgICAgIAogICAgCiAgICAKICAgICAgICAgICAgdmFyIG1hcmtlcl8wNDEzNTBlNWE0Mzk0NjFjYmYyYjcxYTNjNmQwNjIyYiA9IEwubWFya2VyKAogICAgICAgICAgICAgICAgWzQxLjg4OTYxODgsIC04Ny42NDQ4NDI1OTk5OTk5OV0sCiAgICAgICAgICAgICAgICB7fQogICAgICAgICAgICApLmFkZFRvKG1hcF9iNmQxZDk1Yjk5OTA0MDMyYTdiZjI1YTI1NWYzMzExOCk7CiAgICAgICAgCiAgICAKICAgICAgICB2YXIgcG9wdXBfNDBhNjBmYTE2NGNhNGE5Y2ExMTkwN2Y3NDJkMDI1ZjcgPSBMLnBvcHVwKHsibWF4V2lkdGgiOiAiMTAwJSJ9KTsKCiAgICAgICAgCiAgICAgICAgICAgIHZhciBodG1sXzkyZTdiZmNlNjZiYTRhZWFhMmRhZmEzMDE0OTExZDkyID0gJChgPGRpdiBpZD0iaHRtbF85MmU3YmZjZTY2YmE0YWVhYTJkYWZhMzAxNDkxMWQ5MiIgc3R5bGU9IndpZHRoOiAxMDAuMCU7IGhlaWdodDogMTAwLjAlOyI+UGFyYW1vdW50IFJvb208L2Rpdj5gKVswXTsKICAgICAgICAgICAgcG9wdXBfNDBhNjBmYTE2NGNhNGE5Y2ExMTkwN2Y3NDJkMDI1Zjcuc2V0Q29udGVudChodG1sXzkyZTdiZmNlNjZiYTRhZWFhMmRhZmEzMDE0OTExZDkyKTsKICAgICAgICAKCiAgICAgICAgbWFya2VyXzA0MTM1MGU1YTQzOTQ2MWNiZjJiNzFhM2M2ZDA2MjJiLmJpbmRQb3B1cChwb3B1cF80MGE2MGZhMTY0Y2E0YTljYTExOTA3Zjc0MmQwMjVmNykKICAgICAgICA7CgogICAgICAgIAogICAgCiAgICAKICAgICAgICAgICAgdmFyIG1hcmtlcl9jNTZkMGMzMjIzYTI0MmY2OTZkZGVlZWNhNDdiZWViNiA9IEwubWFya2VyKAogICAgICAgICAgICAgICAgWzQxLjkxNTA0OTkwMDAwMDAxLCAtODcuNjc3ODA0N10sCiAgICAgICAgICAgICAgICB7fQogICAgICAgICAgICApLmFkZFRvKG1hcF9iNmQxZDk1Yjk5OTA0MDMyYTdiZjI1YTI1NWYzMzExOCk7CiAgICAgICAgCiAgICAKICAgICAgICB2YXIgcG9wdXBfMTk3ZTAxNzdiYTJhNDA2MWE3MDIxY2UzMmZjNDY1MmIgPSBMLnBvcHVwKHsibWF4V2lkdGgiOiAiMTAwJSJ9KTsKCiAgICAgICAgCiAgICAgICAgICAgIHZhciBodG1sXzFiOTNkYTRiODI1MDRiOTViMjBlNWNmZWRiMmZmMDcxID0gJChgPGRpdiBpZD0iaHRtbF8xYjkzZGE0YjgyNTA0Yjk1YjIwZTVjZmVkYjJmZjA3MSIgc3R5bGU9IndpZHRoOiAxMDAuMCU7IGhlaWdodDogMTAwLjAlOyI+TWVsdCBTYW5kd2ljaCBTaG9wcGU8L2Rpdj5gKVswXTsKICAgICAgICAgICAgcG9wdXBfMTk3ZTAxNzdiYTJhNDA2MWE3MDIxY2UzMmZjNDY1MmIuc2V0Q29udGVudChodG1sXzFiOTNkYTRiODI1MDRiOTViMjBlNWNmZWRiMmZmMDcxKTsKICAgICAgICAKCiAgICAgICAgbWFya2VyX2M1NmQwYzMyMjNhMjQyZjY5NmRkZWVlY2E0N2JlZWI2LmJpbmRQb3B1cChwb3B1cF8xOTdlMDE3N2JhMmE0MDYxYTcwMjFjZTMyZmM0NjUyYikKICAgICAgICA7CgogICAgICAgIAogICAgCiAgICAKICAgICAgICAgICAgdmFyIG1hcmtlcl9jZjAyNjVmNzA4NmI0MzIwOTlkMGNiNzEyNzlmZTA3YSA9IEwubWFya2VyKAogICAgICAgICAgICAgICAgWzQxLjkyMTg1MjEsIC04Ny42NTkyMTI0XSwKICAgICAgICAgICAgICAgIHt9CiAgICAgICAgICAgICkuYWRkVG8obWFwX2I2ZDFkOTViOTk5MDQwMzJhN2JmMjVhMjU1ZjMzMTE4KTsKICAgICAgICAKICAgIAogICAgICAgIHZhciBwb3B1cF85MzA0YWI4MDc0MGM0Yzc0YjMxZDA5YjNjNDZkY2Q4NyA9IEwucG9wdXAoeyJtYXhXaWR0aCI6ICIxMDAlIn0pOwoKICAgICAgICAKICAgICAgICAgICAgdmFyIGh0bWxfMWU2OThiYThjODg3NGM5MGEzM2E0YjYyNzNiMjZkMDUgPSAkKGA8ZGl2IGlkPSJodG1sXzFlNjk4YmE4Yzg4NzRjOTBhMzNhNGI2MjczYjI2ZDA1IiBzdHlsZT0id2lkdGg6IDEwMC4wJTsgaGVpZ2h0OiAxMDAuMCU7Ij5GbG9yaW9sZSBDYWZlICYgQmFrZXJ5PC9kaXY+YClbMF07CiAgICAgICAgICAgIHBvcHVwXzkzMDRhYjgwNzQwYzRjNzRiMzFkMDliM2M0NmRjZDg3LnNldENvbnRlbnQoaHRtbF8xZTY5OGJhOGM4ODc0YzkwYTMzYTRiNjI3M2IyNmQwNSk7CiAgICAgICAgCgogICAgICAgIG1hcmtlcl9jZjAyNjVmNzA4NmI0MzIwOTlkMGNiNzEyNzlmZTA3YS5iaW5kUG9wdXAocG9wdXBfOTMwNGFiODA3NDBjNGM3NGIzMWQwOWIzYzQ2ZGNkODcpCiAgICAgICAgOwoKICAgICAgICAKICAgIAogICAgCiAgICAgICAgICAgIHZhciBtYXJrZXJfNDM1M2E1NjY2MjNjNDU1Nzk0ZTdiMTEzYTM1OWYxNzIgPSBMLm1hcmtlcigKICAgICAgICAgICAgICAgIFs0MS45Nzk3MDk5LCAtODcuNjY5MzQ0MDk5OTk5OTldLAogICAgICAgICAgICAgICAge30KICAgICAgICAgICAgKS5hZGRUbyhtYXBfYjZkMWQ5NWI5OTkwNDAzMmE3YmYyNWEyNTVmMzMxMTgpOwogICAgICAgIAogICAgCiAgICAgICAgdmFyIHBvcHVwXzFmY2M5ZDMwMzU2YzQ1YTZiYjU3NmJiNjQxOWIzYzFhID0gTC5wb3B1cCh7Im1heFdpZHRoIjogIjEwMCUifSk7CgogICAgICAgIAogICAgICAgICAgICB2YXIgaHRtbF8xYTIxMzQ0YjBjNGY0NDBjYTg3OTViZjZkYWQ5MDU2OSA9ICQoYDxkaXYgaWQ9Imh0bWxfMWEyMTM0NGIwYzRmNDQwY2E4Nzk1YmY2ZGFkOTA1NjkiIHN0eWxlPSJ3aWR0aDogMTAwLjAlOyBoZWlnaHQ6IDEwMC4wJTsiPkZpcnN0IFNsaWNlIFBpZSBDYWbDqTwvZGl2PmApWzBdOwogICAgICAgICAgICBwb3B1cF8xZmNjOWQzMDM1NmM0NWE2YmI1NzZiYjY0MTliM2MxYS5zZXRDb250ZW50KGh0bWxfMWEyMTM0NGIwYzRmNDQwY2E4Nzk1YmY2ZGFkOTA1NjkpOwogICAgICAgIAoKICAgICAgICBtYXJrZXJfNDM1M2E1NjY2MjNjNDU1Nzk0ZTdiMTEzYTM1OWYxNzIuYmluZFBvcHVwKHBvcHVwXzFmY2M5ZDMwMzU2YzQ1YTZiYjU3NmJiNjQxOWIzYzFhKQogICAgICAgIDsKCiAgICAgICAgCiAgICAKICAgIAogICAgICAgICAgICB2YXIgbWFya2VyX2M0NTA1ZjdlMWU3ODQ5OWFiMTRlOGIxYjIxMDIyNTExID0gTC5tYXJrZXIoCiAgICAgICAgICAgICAgICBbNDEuOTYxNzEyMiwgLTg3LjY3NTgxNjIwMDAwMDAxXSwKICAgICAgICAgICAgICAgIHt9CiAgICAgICAgICAgICkuYWRkVG8obWFwX2I2ZDFkOTViOTk5MDQwMzJhN2JmMjVhMjU1ZjMzMTE4KTsKICAgICAgICAKICAgIAogICAgICAgIHZhciBwb3B1cF9lM2Y5OWY5ZTc5M2M0YTM4OTIwMmFiYzBhZjI1Nzg2MSA9IEwucG9wdXAoeyJtYXhXaWR0aCI6ICIxMDAlIn0pOwoKICAgICAgICAKICAgICAgICAgICAgdmFyIGh0bWxfYzU1MDUyYzlkYjNjNDAzYzg0YmI3NGQyMjJlNTViYWMgPSAkKGA8ZGl2IGlkPSJodG1sX2M1NTA1MmM5ZGIzYzQwM2M4NGJiNzRkMjIyZTU1YmFjIiBzdHlsZT0id2lkdGg6IDEwMC4wJTsgaGVpZ2h0OiAxMDAuMCU7Ij5Ucm9xdWV0PC9kaXY+YClbMF07CiAgICAgICAgICAgIHBvcHVwX2UzZjk5ZjllNzkzYzRhMzg5MjAyYWJjMGFmMjU3ODYxLnNldENvbnRlbnQoaHRtbF9jNTUwNTJjOWRiM2M0MDNjODRiYjc0ZDIyMmU1NWJhYyk7CiAgICAgICAgCgogICAgICAgIG1hcmtlcl9jNDUwNWY3ZTFlNzg0OTlhYjE0ZThiMWIyMTAyMjUxMS5iaW5kUG9wdXAocG9wdXBfZTNmOTlmOWU3OTNjNGEzODkyMDJhYmMwYWYyNTc4NjEpCiAgICAgICAgOwoKICAgICAgICAKICAgIAogICAgCiAgICAgICAgICAgIHZhciBtYXJrZXJfOWZiZmVjNzE2NGUyNGRkYjhkMTMwMWZmNzIwZTE2OGUgPSBMLm1hcmtlcigKICAgICAgICAgICAgICAgIFs0MS44OTI5NjExOTk5OTk5OSwgLTg3LjYyNzgyMTRdLAogICAgICAgICAgICAgICAge30KICAgICAgICAgICAgKS5hZGRUbyhtYXBfYjZkMWQ5NWI5OTkwNDAzMmE3YmYyNWEyNTVmMzMxMTgpOwogICAgICAgIAogICAgCiAgICAgICAgdmFyIHBvcHVwX2ViNzA0N2U3NDA1MDQ1NWRiMDBjOTMyZGYyOWVlOTY1ID0gTC5wb3B1cCh7Im1heFdpZHRoIjogIjEwMCUifSk7CgogICAgICAgIAogICAgICAgICAgICB2YXIgaHRtbF8wYmQ5YzA4N2Q1MDE0NTU0ODA0YzY1YWMyMTVjYjg4YSA9ICQoYDxkaXYgaWQ9Imh0bWxfMGJkOWMwODdkNTAxNDU1NDgwNGM2NWFjMjE1Y2I4OGEiIHN0eWxlPSJ3aWR0aDogMTAwLjAlOyBoZWlnaHQ6IDEwMC4wJTsiPkdyYWhhbXdpY2g8L2Rpdj5gKVswXTsKICAgICAgICAgICAgcG9wdXBfZWI3MDQ3ZTc0MDUwNDU1ZGIwMGM5MzJkZjI5ZWU5NjUuc2V0Q29udGVudChodG1sXzBiZDljMDg3ZDUwMTQ1NTQ4MDRjNjVhYzIxNWNiODhhKTsKICAgICAgICAKCiAgICAgICAgbWFya2VyXzlmYmZlYzcxNjRlMjRkZGI4ZDEzMDFmZjcyMGUxNjhlLmJpbmRQb3B1cChwb3B1cF9lYjcwNDdlNzQwNTA0NTVkYjAwYzkzMmRmMjllZTk2NSkKICAgICAgICA7CgogICAgICAgIAogICAgCiAgICAKICAgICAgICAgICAgdmFyIG1hcmtlcl8xNDVhYmRkYzg0YTU0YTU2OGYwNDViNDcxNjEyZWUwYyA9IEwubWFya2VyKAogICAgICAgICAgICAgICAgWzQxLjkwNDc1NTEsIC04Ny45Mzk2NDU5XSwKICAgICAgICAgICAgICAgIHt9CiAgICAgICAgICAgICkuYWRkVG8obWFwX2I2ZDFkOTViOTk5MDQwMzJhN2JmMjVhMjU1ZjMzMTE4KTsKICAgICAgICAKICAgIAogICAgICAgIHZhciBwb3B1cF9kZmFiZjU1N2QxM2I0ODNjODgyZjQ1OTEyMGM2M2YxMSA9IEwucG9wdXAoeyJtYXhXaWR0aCI6ICIxMDAlIn0pOwoKICAgICAgICAKICAgICAgICAgICAgdmFyIGh0bWxfNGRhNTg5NGNhZWUxNDY5MGFiNzRhMGM3ZGQxOWNkZDggPSAkKGA8ZGl2IGlkPSJodG1sXzRkYTU4OTRjYWVlMTQ2OTBhYjc0YTBjN2RkMTljZGQ4IiBzdHlsZT0id2lkdGg6IDEwMC4wJTsgaGVpZ2h0OiAxMDAuMCU7Ij5Sb3NhbGlh4oCZcyBEZWxpPC9kaXY+YClbMF07CiAgICAgICAgICAgIHBvcHVwX2RmYWJmNTU3ZDEzYjQ4M2M4ODJmNDU5MTIwYzYzZjExLnNldENvbnRlbnQoaHRtbF80ZGE1ODk0Y2FlZTE0NjkwYWI3NGEwYzdkZDE5Y2RkOCk7CiAgICAgICAgCgogICAgICAgIG1hcmtlcl8xNDVhYmRkYzg0YTU0YTU2OGYwNDViNDcxNjEyZWUwYy5iaW5kUG9wdXAocG9wdXBfZGZhYmY1NTdkMTNiNDgzYzg4MmY0NTkxMjBjNjNmMTEpCiAgICAgICAgOwoKICAgICAgICAKICAgIAogICAgCiAgICAgICAgICAgIHZhciBtYXJrZXJfMzdlZTBiN2EyNGZkNGFmZmJmZWMyY2U0NDQ4NGVmM2EgPSBMLm1hcmtlcigKICAgICAgICAgICAgICAgIFs0MS43OTEzMTg1LCAtODcuNTkzODQ1Nl0sCiAgICAgICAgICAgICAgICB7fQogICAgICAgICAgICApLmFkZFRvKG1hcF9iNmQxZDk1Yjk5OTA0MDMyYTdiZjI1YTI1NWYzMzExOCk7CiAgICAgICAgCiAgICAKICAgICAgICB2YXIgcG9wdXBfZWQxZjkxMGZjNTU5NDkzYzgxZjA1YTkzZWQ3NzJjZTggPSBMLnBvcHVwKHsibWF4V2lkdGgiOiAiMTAwJSJ9KTsKCiAgICAgICAgCiAgICAgICAgICAgIHZhciBodG1sXzFlNTY5YjgzODNkYzRlZDRhY2E3NTliMmExOWUwMWY0ID0gJChgPGRpdiBpZD0iaHRtbF8xZTU2OWI4MzgzZGM0ZWQ0YWNhNzU5YjJhMTllMDFmNCIgc3R5bGU9IndpZHRoOiAxMDAuMCU7IGhlaWdodDogMTAwLjAlOyI+WiZIIE1hcmtldENhZmU8L2Rpdj5gKVswXTsKICAgICAgICAgICAgcG9wdXBfZWQxZjkxMGZjNTU5NDkzYzgxZjA1YTkzZWQ3NzJjZTguc2V0Q29udGVudChodG1sXzFlNTY5YjgzODNkYzRlZDRhY2E3NTliMmExOWUwMWY0KTsKICAgICAgICAKCiAgICAgICAgbWFya2VyXzM3ZWUwYjdhMjRmZDRhZmZiZmVjMmNlNDQ0ODRlZjNhLmJpbmRQb3B1cChwb3B1cF9lZDFmOTEwZmM1NTk0OTNjODFmMDVhOTNlZDc3MmNlOCkKICAgICAgICA7CgogICAgICAgIAogICAgCiAgICAKICAgICAgICAgICAgdmFyIG1hcmtlcl8zNzc4YTU5MzA1ZDI0YWE1YTBiZmVkMmE5OWI1ZjJjYyA9IEwubWFya2VyKAogICAgICAgICAgICAgICAgWzQyLjI1MTc4NDA5OTk5OTk5LCAtODcuODQxMzUzNV0sCiAgICAgICAgICAgICAgICB7fQogICAgICAgICAgICApLmFkZFRvKG1hcF9iNmQxZDk1Yjk5OTA0MDMyYTdiZjI1YTI1NWYzMzExOCk7CiAgICAgICAgCiAgICAKICAgICAgICB2YXIgcG9wdXBfYjczZjk1YjdiYjYxNDc2ODgxNmJiNDA1N2JkOTI4N2MgPSBMLnBvcHVwKHsibWF4V2lkdGgiOiAiMTAwJSJ9KTsKCiAgICAgICAgCiAgICAgICAgICAgIHZhciBodG1sX2VjYzA1ZDJhMmJjZjQzMzlhMDRkY2RkNTlkNjYwZTQzID0gJChgPGRpdiBpZD0iaHRtbF9lY2MwNWQyYTJiY2Y0MzM5YTA0ZGNkZDU5ZDY2MGU0MyIgc3R5bGU9IndpZHRoOiAxMDAuMCU7IGhlaWdodDogMTAwLjAlOyI+TWFya2V0IEhvdXNlIG9uIHRoZSBTcXVhcmU8L2Rpdj5gKVswXTsKICAgICAgICAgICAgcG9wdXBfYjczZjk1YjdiYjYxNDc2ODgxNmJiNDA1N2JkOTI4N2Muc2V0Q29udGVudChodG1sX2VjYzA1ZDJhMmJjZjQzMzlhMDRkY2RkNTlkNjYwZTQzKTsKICAgICAgICAKCiAgICAgICAgbWFya2VyXzM3NzhhNTkzMDVkMjRhYTVhMGJmZWQyYTk5YjVmMmNjLmJpbmRQb3B1cChwb3B1cF9iNzNmOTViN2JiNjE0NzY4ODE2YmI0MDU3YmQ5Mjg3YykKICAgICAgICA7CgogICAgICAgIAogICAgCiAgICAKICAgICAgICAgICAgdmFyIG1hcmtlcl9mZGQyYjlhMmVhM2Y0NWY1OTExN2FhNTIwZGVmMTJmYSA9IEwubWFya2VyKAogICAgICAgICAgICAgICAgWzQxLjkxNTI4NzUsIC04Ny42MzQzODg4XSwKICAgICAgICAgICAgICAgIHt9CiAgICAgICAgICAgICkuYWRkVG8obWFwX2I2ZDFkOTViOTk5MDQwMzJhN2JmMjVhMjU1ZjMzMTE4KTsKICAgICAgICAKICAgIAogICAgICAgIHZhciBwb3B1cF9jYmQ4NWYwZGI4OTk0Y2YyYTk0MTdlY2MwNWY2ZDZjYiA9IEwucG9wdXAoeyJtYXhXaWR0aCI6ICIxMDAlIn0pOwoKICAgICAgICAKICAgICAgICAgICAgdmFyIGh0bWxfYmVmOTMzNDQ0NDg1NGI2M2I0MTgyOTRkNWEzNzU5YzMgPSAkKGA8ZGl2IGlkPSJodG1sX2JlZjkzMzQ0NDQ4NTRiNjNiNDE4Mjk0ZDVhMzc1OWMzIiBzdHlsZT0id2lkdGg6IDEwMC4wJTsgaGVpZ2h0OiAxMDAuMCU7Ij5FbGFpbmXigJlzIENvZmZlZSBDYWxsPC9kaXY+YClbMF07CiAgICAgICAgICAgIHBvcHVwX2NiZDg1ZjBkYjg5OTRjZjJhOTQxN2VjYzA1ZjZkNmNiLnNldENvbnRlbnQoaHRtbF9iZWY5MzM0NDQ0ODU0YjYzYjQxODI5NGQ1YTM3NTljMyk7CiAgICAgICAgCgogICAgICAgIG1hcmtlcl9mZGQyYjlhMmVhM2Y0NWY1OTExN2FhNTIwZGVmMTJmYS5iaW5kUG9wdXAocG9wdXBfY2JkODVmMGRiODk5NGNmMmE5NDE3ZWNjMDVmNmQ2Y2IpCiAgICAgICAgOwoKICAgICAgICAKICAgIAogICAgCiAgICAgICAgICAgIHZhciBtYXJrZXJfMGY3NDI0ZWYzZDRhNDY4MWEzNmMxNzQzMDM4ZDEwNzIgPSBMLm1hcmtlcigKICAgICAgICAgICAgICAgIFs0MS44ODYzNjIyLCAtODcuODAyMjI5N10sCiAgICAgICAgICAgICAgICB7fQogICAgICAgICAgICApLmFkZFRvKG1hcF9iNmQxZDk1Yjk5OTA0MDMyYTdiZjI1YTI1NWYzMzExOCk7CiAgICAgICAgCiAgICAKICAgICAgICB2YXIgcG9wdXBfOTZkNWU2YWViNjBiNGRlODkzODY1NjljYTM3YmQ1ZWMgPSBMLnBvcHVwKHsibWF4V2lkdGgiOiAiMTAwJSJ9KTsKCiAgICAgICAgCiAgICAgICAgICAgIHZhciBodG1sXzRlYmZmMzJlMDExMDQ4ODZiMWE0YjkxNmM2NTBlMTY4ID0gJChgPGRpdiBpZD0iaHRtbF80ZWJmZjMyZTAxMTA0ODg2YjFhNGI5MTZjNjUwZTE2OCIgc3R5bGU9IndpZHRoOiAxMDAuMCU7IGhlaWdodDogMTAwLjAlOyI+TWFyaW9uIFN0cmVldCBDaGVlc2UgTWFya2V0PC9kaXY+YClbMF07CiAgICAgICAgICAgIHBvcHVwXzk2ZDVlNmFlYjYwYjRkZTg5Mzg2NTY5Y2EzN2JkNWVjLnNldENvbnRlbnQoaHRtbF80ZWJmZjMyZTAxMTA0ODg2YjFhNGI5MTZjNjUwZTE2OCk7CiAgICAgICAgCgogICAgICAgIG1hcmtlcl8wZjc0MjRlZjNkNGE0NjgxYTM2YzE3NDMwMzhkMTA3Mi5iaW5kUG9wdXAocG9wdXBfOTZkNWU2YWViNjBiNGRlODkzODY1NjljYTM3YmQ1ZWMpCiAgICAgICAgOwoKICAgICAgICAKICAgIAogICAgCiAgICAgICAgICAgIHZhciBtYXJrZXJfMTM3ODlmMTNjZGJiNGE1OGI2M2MzZTFkZDc0MTRmOGUgPSBMLm1hcmtlcigKICAgICAgICAgICAgICAgIFs0MS44NzU4MTAyLCAtODcuNjI2NDQ4OV0sCiAgICAgICAgICAgICAgICB7fQogICAgICAgICAgICApLmFkZFRvKG1hcF9iNmQxZDk1Yjk5OTA0MDMyYTdiZjI1YTI1NWYzMzExOCk7CiAgICAgICAgCiAgICAKICAgICAgICB2YXIgcG9wdXBfYzQ2NjQ3YTc1ZWFmNDRmMTkyMTk1ODRhM2FjNGEyZTUgPSBMLnBvcHVwKHsibWF4V2lkdGgiOiAiMTAwJSJ9KTsKCiAgICAgICAgCiAgICAgICAgICAgIHZhciBodG1sXzA1YjQ1OTBhMmU0YTQ4ZDFiOWNlYWYyNGM0Mzg3NzBlID0gJChgPGRpdiBpZD0iaHRtbF8wNWI0NTkwYTJlNGE0OGQxYjljZWFmMjRjNDM4NzcwZSIgc3R5bGU9IndpZHRoOiAxMDAuMCU7IGhlaWdodDogMTAwLjAlOyI+Q2FmZWNpdG88L2Rpdj5gKVswXTsKICAgICAgICAgICAgcG9wdXBfYzQ2NjQ3YTc1ZWFmNDRmMTkyMTk1ODRhM2FjNGEyZTUuc2V0Q29udGVudChodG1sXzA1YjQ1OTBhMmU0YTQ4ZDFiOWNlYWYyNGM0Mzg3NzBlKTsKICAgICAgICAKCiAgICAgICAgbWFya2VyXzEzNzg5ZjEzY2RiYjRhNThiNjNjM2UxZGQ3NDE0ZjhlLmJpbmRQb3B1cChwb3B1cF9jNDY2NDdhNzVlYWY0NGYxOTIxOTU4NGEzYWM0YTJlNSkKICAgICAgICA7CgogICAgICAgIAogICAgCiAgICAKICAgICAgICAgICAgdmFyIG1hcmtlcl9kZjRiOTU3YTQ2NzA0Y2MxYjBlNzUyZjAzMzM0MTI4MiA9IEwubWFya2VyKAogICAgICAgICAgICAgICAgWzQxLjg5NjExMzQsIC04Ny42Nzc4NTddLAogICAgICAgICAgICAgICAge30KICAgICAgICAgICAgKS5hZGRUbyhtYXBfYjZkMWQ5NWI5OTkwNDAzMmE3YmYyNWEyNTVmMzMxMTgpOwogICAgICAgIAogICAgCiAgICAgICAgdmFyIHBvcHVwXzE3ZDYwODJiZDdlYTQwY2E4MDBhYjdhY2U1NjQ1MzQ1ID0gTC5wb3B1cCh7Im1heFdpZHRoIjogIjEwMCUifSk7CgogICAgICAgIAogICAgICAgICAgICB2YXIgaHRtbF81OTI1YmM5Nzg3MmE0NGQ4OWZmMWM5N2E4ZTEzMjAxNyA9ICQoYDxkaXYgaWQ9Imh0bWxfNTkyNWJjOTc4NzJhNDRkODlmZjFjOTdhOGUxMzIwMTciIHN0eWxlPSJ3aWR0aDogMTAwLjAlOyBoZWlnaHQ6IDEwMC4wJTsiPkNoaWNrcGVhPC9kaXY+YClbMF07CiAgICAgICAgICAgIHBvcHVwXzE3ZDYwODJiZDdlYTQwY2E4MDBhYjdhY2U1NjQ1MzQ1LnNldENvbnRlbnQoaHRtbF81OTI1YmM5Nzg3MmE0NGQ4OWZmMWM5N2E4ZTEzMjAxNyk7CiAgICAgICAgCgogICAgICAgIG1hcmtlcl9kZjRiOTU3YTQ2NzA0Y2MxYjBlNzUyZjAzMzM0MTI4Mi5iaW5kUG9wdXAocG9wdXBfMTdkNjA4MmJkN2VhNDBjYTgwMGFiN2FjZTU2NDUzNDUpCiAgICAgICAgOwoKICAgICAgICAKICAgIAogICAgCiAgICAgICAgICAgIHZhciBtYXJrZXJfMGEyNzMyMDlkNzczNGI1ZTk5ZjBkYTUwMDg4OTFiMjAgPSBMLm1hcmtlcigKICAgICAgICAgICAgICAgIFs0MS44OTg5Nzg1MDAwMDAwMSwgLTg3LjYyNzM5MjZdLAogICAgICAgICAgICAgICAge30KICAgICAgICAgICAgKS5hZGRUbyhtYXBfYjZkMWQ5NWI5OTkwNDAzMmE3YmYyNWEyNTVmMzMxMTgpOwogICAgICAgIAogICAgCiAgICAgICAgdmFyIHBvcHVwXzhmNTAxMzFjYmNjYzQ2ZGNhMTliMTNiMzA4N2I2Njg2ID0gTC5wb3B1cCh7Im1heFdpZHRoIjogIjEwMCUifSk7CgogICAgICAgIAogICAgICAgICAgICB2YXIgaHRtbF81ZTEwODgzMjNjODQ0MmFhODc1MjRiNWM0OTJlZTBiNiA9ICQoYDxkaXYgaWQ9Imh0bWxfNWUxMDg4MzIzYzg0NDJhYTg3NTI0YjVjNDkyZWUwYjYiIHN0eWxlPSJ3aWR0aDogMTAwLjAlOyBoZWlnaHQ6IDEwMC4wJTsiPlRoZSBHb2RkZXNzIGFuZCBHcm9jZXI8L2Rpdj5gKVswXTsKICAgICAgICAgICAgcG9wdXBfOGY1MDEzMWNiY2NjNDZkY2ExOWIxM2IzMDg3YjY2ODYuc2V0Q29udGVudChodG1sXzVlMTA4ODMyM2M4NDQyYWE4NzUyNGI1YzQ5MmVlMGI2KTsKICAgICAgICAKCiAgICAgICAgbWFya2VyXzBhMjczMjA5ZDc3MzRiNWU5OWYwZGE1MDA4ODkxYjIwLmJpbmRQb3B1cChwb3B1cF84ZjUwMTMxY2JjY2M0NmRjYTE5YjEzYjMwODdiNjY4NikKICAgICAgICA7CgogICAgICAgIAogICAgCiAgICAKICAgICAgICAgICAgdmFyIG1hcmtlcl85NjNkNDZhZTFhMjg0M2Y2OGMyNGVhMjVjNGNmNjAyNSA9IEwubWFya2VyKAogICAgICAgICAgICAgICAgWzQxLjkxMDU4MzIsIC04Ny45NDA0ODgzOTk5OTk5OV0sCiAgICAgICAgICAgICAgICB7fQogICAgICAgICAgICApLmFkZFRvKG1hcF9iNmQxZDk1Yjk5OTA0MDMyYTdiZjI1YTI1NWYzMzExOCk7CiAgICAgICAgCiAgICAKICAgICAgICB2YXIgcG9wdXBfYzc4NDVjNDYzYzA3NDJiM2EwMzUzMmViYzI1MjkyNWYgPSBMLnBvcHVwKHsibWF4V2lkdGgiOiAiMTAwJSJ9KTsKCiAgICAgICAgCiAgICAgICAgICAgIHZhciBodG1sX2U0YWQ5YzY2YzIxMDQ0YzU4MDlhODlhMDFjOTEyYWJhID0gJChgPGRpdiBpZD0iaHRtbF9lNGFkOWM2NmMyMTA0NGM1ODA5YTg5YTAxYzkxMmFiYSIgc3R5bGU9IndpZHRoOiAxMDAuMCU7IGhlaWdodDogMTAwLjAlOyI+WmVud2ljaDwvZGl2PmApWzBdOwogICAgICAgICAgICBwb3B1cF9jNzg0NWM0NjNjMDc0MmIzYTAzNTMyZWJjMjUyOTI1Zi5zZXRDb250ZW50KGh0bWxfZTRhZDljNjZjMjEwNDRjNTgwOWE4OWEwMWM5MTJhYmEpOwogICAgICAgIAoKICAgICAgICBtYXJrZXJfOTYzZDQ2YWUxYTI4NDNmNjhjMjRlYTI1YzRjZjYwMjUuYmluZFBvcHVwKHBvcHVwX2M3ODQ1YzQ2M2MwNzQyYjNhMDM1MzJlYmMyNTI5MjVmKQogICAgICAgIDsKCiAgICAgICAgCiAgICAKICAgIAogICAgICAgICAgICB2YXIgbWFya2VyXzE4ODAxNTY2NTcyMTRmMDQ5NjJmODA2ZDBmODIzNjliID0gTC5tYXJrZXIoCiAgICAgICAgICAgICAgICBbNDEuODgzMTA2MSwgLTg3LjYyNTQzODFdLAogICAgICAgICAgICAgICAge30KICAgICAgICAgICAgKS5hZGRUbyhtYXBfYjZkMWQ5NWI5OTkwNDAzMmE3YmYyNWEyNTVmMzMxMTgpOwogICAgICAgIAogICAgCiAgICAgICAgdmFyIHBvcHVwXzFjNTVkOTQ2OWIwMjQxOGU5M2NhOGE0MTU1NTA5MjgyID0gTC5wb3B1cCh7Im1heFdpZHRoIjogIjEwMCUifSk7CgogICAgICAgIAogICAgICAgICAgICB2YXIgaHRtbF9hM2VkZjc1OWQxZGQ0NTQ2YmUwODViM2VhMmMxODRiNiA9ICQoYDxkaXYgaWQ9Imh0bWxfYTNlZGY3NTlkMWRkNDU0NmJlMDg1YjNlYTJjMTg0YjYiIHN0eWxlPSJ3aWR0aDogMTAwLjAlOyBoZWlnaHQ6IDEwMC4wJTsiPlRvbmkgUGF0aXNzZXJpZTwvZGl2PmApWzBdOwogICAgICAgICAgICBwb3B1cF8xYzU1ZDk0NjliMDI0MThlOTNjYThhNDE1NTUwOTI4Mi5zZXRDb250ZW50KGh0bWxfYTNlZGY3NTlkMWRkNDU0NmJlMDg1YjNlYTJjMTg0YjYpOwogICAgICAgIAoKICAgICAgICBtYXJrZXJfMTg4MDE1NjY1NzIxNGYwNDk2MmY4MDZkMGY4MjM2OWIuYmluZFBvcHVwKHBvcHVwXzFjNTVkOTQ2OWIwMjQxOGU5M2NhOGE0MTU1NTA5MjgyKQogICAgICAgIDsKCiAgICAgICAgCiAgICAKICAgIAogICAgICAgICAgICB2YXIgbWFya2VyXzhhOTg2OGM4MGNjYzRlZTM4NjdiM2VkNzdjODgwNDU0ID0gTC5tYXJrZXIoCiAgICAgICAgICAgICAgICBbNDEuOTQzMTYzMiwgLTg3LjY0NDUwNzFdLAogICAgICAgICAgICAgICAge30KICAgICAgICAgICAgKS5hZGRUbyhtYXBfYjZkMWQ5NWI5OTkwNDAzMmE3YmYyNWEyNTVmMzMxMTgpOwogICAgICAgIAogICAgCiAgICAgICAgdmFyIHBvcHVwX2IyZjBjOThjYzRkNTRlZTRhMDUyYjE4YjVmNDAzN2JhID0gTC5wb3B1cCh7Im1heFdpZHRoIjogIjEwMCUifSk7CgogICAgICAgIAogICAgICAgICAgICB2YXIgaHRtbF9lZmM0NzhkY2FjM2Q0MWIwYTNiOWNhNjBlZjk2MjNmNyA9ICQoYDxkaXYgaWQ9Imh0bWxfZWZjNDc4ZGNhYzNkNDFiMGEzYjljYTYwZWY5NjIzZjciIHN0eWxlPSJ3aWR0aDogMTAwLjAlOyBoZWlnaHQ6IDEwMC4wJTsiPlBob2ViZeKAmXMgQmFrZXJ5PC9kaXY+YClbMF07CiAgICAgICAgICAgIHBvcHVwX2IyZjBjOThjYzRkNTRlZTRhMDUyYjE4YjVmNDAzN2JhLnNldENvbnRlbnQoaHRtbF9lZmM0NzhkY2FjM2Q0MWIwYTNiOWNhNjBlZjk2MjNmNyk7CiAgICAgICAgCgogICAgICAgIG1hcmtlcl84YTk4NjhjODBjY2M0ZWUzODY3YjNlZDc3Yzg4MDQ1NC5iaW5kUG9wdXAocG9wdXBfYjJmMGM5OGNjNGQ1NGVlNGEwNTJiMThiNWY0MDM3YmEpCiAgICAgICAgOwoKICAgICAgICAKICAgIAo8L3NjcmlwdD4= onload="this.contentDocument.open();this.contentDocument.write(atob(this.getAttribute('data-html')));this.contentDocument.close();" allowfullscreen webkitallowfullscreen mozallowfullscreen></iframe></div></div>




```python

```
