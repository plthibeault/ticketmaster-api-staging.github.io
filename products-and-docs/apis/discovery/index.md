<!DOCTYPE html>
<html>
    <head>
    <meta charset="utf-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, target-densitydpi=medium-dpi, minimum-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <meta name="description" content="Use the Discovery API to search, look up and find events, attractions and venues.">
    <meta name="keywords" content="API, search events, attraction details, event images, category details, venue details, support">
    <title>Discovery API</title>
    <link rel="shortcut icon" href="/favicon.ico" />
    <link rel="apple-touch-icon" href="/apple-touch-icon.png" />
    <link rel="stylesheet" href="/css/main.css">
    <link rel="canonical" href="/products-and-docs/apis/discovery/">
    <link rel="alternate" type="application/rss+xml" title="Ticketmaster Developer Portal" href="/feed.xml">
    <script src="/scripts/vendors/jquery-1.11.3.min.js"></script>
    <script src="/scripts/components/header.js"></script>
</head>

    <body>
        <!-- Qualaroo for ticketmaster.com -->
        <!-- Paste this code right after the <body> tag on every page of your site. -->
        <script type="text/javascript">
          var _kiq = _kiq || [];
          (function(){
            setTimeout(function(){
            var d = document, f = d.getElementsByTagName('script')[0], s = d.createElement('script'); s.type = 'text/javascript';
            s.async = true; s.src = '//s3.amazonaws.com/ki.js/62776/euc.js'; f.parentNode.insertBefore(s, f);
            }, 1);
          })();
        </script>
        <div class="top-bar bg-header header-curtain">
<div class="body-wrapper">
    <div class="row">
        <div class="col-xs-7 col-lg-2 gray">
            <a id="header-logo" href="/">
            
            <img alt="Ticketmaster logo" src="/assets/img/header/tm-developer-logo.svg">
            
            </a>
        </div>
        <nav id="menu" class="col-xs-12 col-lg-8">
            <!-- links put into single line intentionally to avoid browser rendered spaces -->
            <a   class="one nav-item"  href="/products-and-docs/">Products & Docs</a><a
                 class="gray"  href="/partners/">Partners</a><a
                 class="gray"  href="/support/">Support</a><a
                 class="gray"  href="/blogs/">Blogs</a><a
                 class="gray"  href="/events/">Events</a><a
                 class="gray"  href="http://code.ticketmaster.com/">Open Source</a>
        </nav>
        <div class="col-xs-5 col-lg-2 gray">
            <a id="menu-btn"  class="white"></a>
            <div id="search"  class="white">
                <div class="search-button"></div>
                <form action="/search/" id="cse-search-box" autocomplete="off">
                    <div>
                        <input type="hidden" name="cx" value="000111791941460729347:zmu0d7yvkfq" />
                        <input type="hidden" name="ie" value="UTF-8" />
                        <input class="q" type="text" name="q" size="14" placeholder="Search for ..."/>
                        <input class="sa" type="submit" name="sa" value="" />
                    </div>
                </form>
                <script type="text/javascript" src="//www.google.com/jsapi"></script>
                <script type="text/javascript" src="//www.google.com.ua/cse/brand?form=cse-search-box&lang=en"></script>
                <!--<span tabindex="-1" id="search-alert" style="display: none;">Whoa! Search isn't quite ready yet! We're still working on it.</span>-->
            </div>
            <a class="apigee-login  white" href="https://live-livenation.devportal.apigee.com/user/login">Login</a>
        </div>
        <div id="rainbow">
            <span class="one"></span>
            <span class="two"></span>
            <span class="three"></span>
            <span class="four"></span>
            <span class="five"></span>
            <span class="six"></span>
        </div>
    </div>
</div>
</div>
<ul id="menu-dropdown" class="col-xs-12 col-sm-5 col-lg-3 closed" tabindex="-1">
    <li><a class="apgee-login" href="https://dev-livenation.devportal.apigee.com/user/login">Login</a></li>
    <li><a href="/products-and-docs/">Products & Docs</a></li>
    <li><a href="/partners/">Partners</a></li>
    <li><a href="/support/">Support</a></li>
    <li><a href="/blogs/">Blogs</a></li>
    <li><a href="/events/">Events</a></li>
    <li><a href="http://code.ticketmaster.com/">Open Source</a></li>
</ul>



<div class="documentation">

    <div class="maincontent">
        <div class="row" style="position: relative;">
            <div class="col-xs-12 col-sm-6 col-lg-3 has-bg" id="aside-block">
                <div class="wrapper-aside-menu">
                    <h3 class="menu-header" id="aside-heading">
                        <a href="/products-and-docs/"></a>Products &amp; Docs</a>
                        <span class="expanded" id="side-menu-btn"></span>
                    </h3>
                    <ul class="aside-menu" id="scrollable-element">
    <li>
        <h4><a href="/products-and-docs/apis/getting-started/">APIs</a></h4>
        <ul class="categories">
            <li><a href="/products-and-docs/apis/getting-started/">Getting Started</a>
                
            </li>
            <li><a href="/products-and-docs/apis/discovery/">Discovery API</a>
                
                <ul class="sections menu-highlight">
                    <li><a href="#overview">Overview</a></li>
                    <li><a href="#srch-events">Search Events</a></li>
                    <li><a href="#event-details">Get Event Details</a></li>
                    <li><a href="#event-img">Search Event Images</a></li>
                    <li><a href="#search-attractions">Search Attractions</a></li>
                    <li><a href="#attraction-details">Get Attraction Details</a></li>
                    <li><a href="#search-categories">Search Categories</a></li>
                    <li><a href="#category-details">Get Category Details</a></li>
                    <li><a href="#search-venues">Search Venues</a></li>
                    <li><a href="#venue-details">Get Venue Details</a></li>
                    <li><a href="#supported-markets">Supported Markets</a></li>
                    <li><a href="#supported-domains">Supported Domains</a></li>
                    <li><a href="#supported-sources">Supported Sources</a></li>
                    <li><a href="#supported-locales">Supported Locales</a></li>
                </ul>
                
            </li>
            <li><a href="/products-and-docs/apis/commerce/">Commerce API</a>
                
            </li>
            <li><a href="/products-and-docs/apis/partner/">Partner API</a>
                
            </li>
            <li><a href="/products-and-docs/apis/deals-api/">Deals API</a>
                
            </li>
            <li><a href="/products-and-docs/apis/international-discovery/">International Discovery API</a>
                
            </li>
            <li><a href="/products-and-docs/apis/interactive-console/">Interactive Docs</a></li>
            <li><a href="http://vmenshutin.github.io/">API Explorer</a></li>
        </ul>
    </li>
    <li>
        <h4><a href="/products-and-docs/sdks/"  >SDKs</a></h4>
        <!--<ul class="categories">
            <li><a href="/products-and-docs/under-development/">Getting Started</a></li>
            <li><a href="/products-and-docs/under-development/">Installation instruction</a></li>
            <li><a href="/products-and-docs/under-development/">Documentation</a></li>
            <li><a href="/products-and-docs/under-development/">Code samples</a></li>
        </ul>-->
    </li>
    <li>
        <h4><a href="/products-and-docs/widgets/"  >Widgets</a></h4>
        <!--<ul class="categories">
            <li><a href="/products-and-docs/under-development/">Getting started</a></li>
            <li><a href="/products-and-docs/under-development/">Configuration Docs</a></li>
            <li><a href="/products-and-docs/under-development/">Installation instructions</a></li>
        </ul>-->
    </li>
</ul>


                </div>
            </div>

            <div class="col-xs-12 col-lg-9" id="main-block">
                <div class="content" style="display: block;">
                    <h1 id="discovery-api">Discovery API</h1>

<p class="lead article">Use the Discovery API to search, look up and find events, attractions, venues and classifications. The API provides access to all Ticketmaster events, as well as Universe and TicketWeb events.</p>

<h4 class="aside gray" id="developer-console">Developer Console</h4>

<p>Make live API calls right now in the interactive docs:</p>

<p><a href="/products-and-docs/apis/interactive-console/" class="button">INTERACTIVE DOCS</a></p>

<h2 class="article" id="overview">Overview</h2>

<h3 id="authentication">Authentication</h3>

<p>To run a successful API call, you will need to pass your API Key as the query parameter  <strong>apikey</strong>.</p>

<p>Example: <code class="highlighter-rouge">https://app.ticketmaster.com/discovery/v2/events.json?apikey=3QIvq55bS608ai6r8moig1WdW57bONry</code></p>

<h3 id="root-url">Root URL</h3>

<p><code class="highlighter-rouge">https://app.ticketmaster.com/discovery/{API version}</code></p>

<h2 class="article console-link" id="srch-events">Search Events</h2>

<p><strong>Method:</strong> GET.
Authentication required.
Returns the 20 most recent events for the authenticating user.</p>

<p class="code red">discovery/{version}/events.{format}</p>

<h3 id="url-parameters">URL parameters:</h3>

<table>
  <thead>
    <tr>
      <th style="text-align: left">Parameter</th>
      <th style="text-align: left">Description</th>
      <th style="text-align: left">Type</th>
      <th style="text-align: left">Default Value</th>
      <th style="text-align: left">Required</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align: left"><code class="highlighter-rouge">version</code></td>
      <td style="text-align: left">The API Version.</td>
      <td style="text-align: left">string</td>
      <td style="text-align: left">“v2”</td>
      <td style="text-align: left">Yes</td>
    </tr>
    <tr>
      <td style="text-align: left"><code class="highlighter-rouge">format</code></td>
      <td style="text-align: left">API Response Format.</td>
      <td style="text-align: left">string</td>
      <td style="text-align: left">“json”</td>
      <td style="text-align: left">Yes</td>
    </tr>
  </tbody>
</table>

<h3 id="query-parameters">Query parameters:</h3>

<table>
  <thead>
    <tr>
      <th style="text-align: left">Parameter</th>
      <th style="text-align: left">Description</th>
      <th style="text-align: left">Type</th>
      <th style="text-align: left">Default Value</th>
      <th style="text-align: left">Required</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align: left"><code class="highlighter-rouge">keyword</code></td>
      <td style="text-align: left">A string to search against events, attractions and venues. The keyword will be checked against titles, descriptions, names and other logical fields that describe any of these data objects.</td>
      <td style="text-align: left">string</td>
      <td style="text-align: left"> </td>
      <td style="text-align: left">No</td>
    </tr>
    <tr>
      <td style="text-align: left"><code class="highlighter-rouge">attractionId</code></td>
      <td style="text-align: left">Attraction ID(s) separated by comma.</td>
      <td style="text-align: left">string</td>
      <td style="text-align: left">“K8vZ91713eV”</td>
      <td style="text-align: left">No</td>
    </tr>
    <tr>
      <td style="text-align: left"><code class="highlighter-rouge">venueId</code></td>
      <td style="text-align: left">Venue ID(s) separated by comma.</td>
      <td style="text-align: left">string</td>
      <td style="text-align: left">“KovZpZAEdFtJ”</td>
      <td style="text-align: left">No</td>
    </tr>
    <tr>
      <td style="text-align: left"><code class="highlighter-rouge">promoterId</code></td>
      <td style="text-align: left">Promoter ID(s) separated by comma.</td>
      <td style="text-align: left">string</td>
      <td style="text-align: left">“494”</td>
      <td style="text-align: left">No</td>
    </tr>
    <tr>
      <td style="text-align: left"><code class="highlighter-rouge">postalCode</code></td>
      <td style="text-align: left">Zipcode or Postal Code of the venue in which the event is taking place.</td>
      <td style="text-align: left">string</td>
      <td style="text-align: left">“90069”</td>
      <td style="text-align: left">No</td>
    </tr>
    <tr>
      <td style="text-align: left"><code class="highlighter-rouge">latlong</code></td>
      <td style="text-align: left">The Latitude,Longitude coordinates for the venue in which this event is taking place.</td>
      <td style="text-align: left">string</td>
      <td style="text-align: left">“34.0928090,-118.3286610”</td>
      <td style="text-align: left">No</td>
    </tr>
    <tr>
      <td style="text-align: left"><code class="highlighter-rouge">radius</code></td>
      <td style="text-align: left">The radius of the area in which we want to search for events.</td>
      <td style="text-align: left">string</td>
      <td style="text-align: left">“25”</td>
      <td style="text-align: left">No</td>
    </tr>
    <tr>
      <td style="text-align: left"><code class="highlighter-rouge">unit</code></td>
      <td style="text-align: left">The radius distance unit. Possible values: miles, km</td>
      <td style="text-align: left">string</td>
      <td style="text-align: left">“miles”</td>
      <td style="text-align: left">No</td>
    </tr>    
    <tr>
      <td style="text-align: left"><code class="highlighter-rouge">source</code></td>
      <td style="text-align: left">Source of the event. Possible values are '', 'ticketmaster', 'ticketweb', 'universe'.</td>
      <td style="text-align: left">string</td>
      <td style="text-align: left">“ticketmaster”</td>
      <td style="text-align: left">No</td>
    </tr>    
    <tr>
      <td style="text-align: left"><code class="highlighter-rouge">locale</code></td>
      <td style="text-align: left">The event locale, including country and localization. Values: “”, “en-us”, “en-gb”, “en-ca”, “es-us”, “en-mx”, “es-mx”, “en-au”, “en-nz”, “fr-fr”, “fr-ca”.</td>
      <td style="text-align: left">string</td>
      <td style="text-align: left"> </td>
      <td style="text-align: left">No</td>
    </tr>
    <tr>
      <td style="text-align: left"><code class="highlighter-rouge">marketId</code></td>
      <td style="text-align: left">The city/area in which this event takes place.</td>
      <td style="text-align: left">string</td>
      <td style="text-align: left">“27”</td>
      <td style="text-align: left">No</td>
    </tr>
    <tr>
      <td style="text-align: left"><code class="highlighter-rouge">startDateTime</code></td>
      <td style="text-align: left">Include events happening after this date.</td>
      <td style="text-align: left">string</td>
      <td style="text-align: left">“2017-01-01T00:00:00Z”</td>
      <td style="text-align: left">No</td>
    </tr>
    <tr>
      <td style="text-align: left"><code class="highlighter-rouge">endDateTime</code></td>
      <td style="text-align: left">Include events happening before this date.</td>
      <td style="text-align: left">string</td>
      <td style="text-align: left">“2017-01-01T00:00:00Z”</td>
      <td style="text-align: left">No</td>
    </tr>
    <tr>
      <td style="text-align: left"><code class="highlighter-rouge">includeTBA</code></td>
      <td style="text-align: left">Whether or not to return events with dates to be announced (TBA). Default is 'no', TBA events are not returned.</td>
      <td style="text-align: left">string</td>
      <td style="text-align: left">“yes|no|only”</td>
      <td style="text-align: left">No</td>
    </tr>
    <tr>
      <td style="text-align: left"><code class="highlighter-rouge">includeTBD</code></td>
      <td style="text-align: left">Whether or not to return events with dates to be determined (TBD). Default is 'no', TBD events are not returned.</td>
      <td style="text-align: left">string</td>
      <td style="text-align: left">“yes|no|only”</td>
      <td style="text-align: left">No</td>
    </tr>
    <tr>
      <td style="text-align: left"><code class="highlighter-rouge">includeTest</code></td>
      <td style="text-align: left">Whether or not to return test events. Default is 'no', test events are not returned.</td>
      <td style="text-align: left">string</td>
      <td style="text-align: left">“yes|no|only”</td>
      <td style="text-align: left">No</td>
    </tr>    
    <tr>
      <td style="text-align: left"><code class="highlighter-rouge">size</code></td>
      <td style="text-align: left">The number of events returned in the API response. Default is 20.</td>
      <td style="text-align: left">string</td>
      <td style="text-align: left">“10”</td>
      <td style="text-align: left">No</td>
    </tr>
    <tr>
      <td style="text-align: left"><code class="highlighter-rouge">page</code></td>
      <td style="text-align: left">The page for paginating through the results.</td>
      <td style="text-align: left">string</td>
      <td style="text-align: left">“1”</td>
      <td style="text-align: left">No</td>
    </tr>
    <tr>
      <td style="text-align: left"><code class="highlighter-rouge">sort</code></td>
      <td style="text-align: left">The search sort criteria. Values: 'name,asc', 'name,desc', 'eventDate,asc', 'eventDate,desc'.</td>
      <td style="text-align: left">string</td>
      <td style="text-align: left"> </td>
      <td style="text-align: left">No</td>
    </tr>        
  </tbody>
</table>

<h3 id="response-structure">Response structure:</h3>

<ul class="nested-list">
  <li><code class="highlighter-rouge">_embedded</code> (object) - container for events.
    <ul>
      <li><code class="highlighter-rouge">events</code> (array) - events.
        <ul>
          <li><code class="highlighter-rouge"><span class="p">{</span><span class="err">array</span><span class="w"> </span><span class="err">item</span><span class="w"> </span><span class="err">object</span><span class="p">}</span></code> - event.
            <ul>
              <li><code class="highlighter-rouge">name</code> (string) - name of event.</li>
              <li><code class="highlighter-rouge">locale</code> (string) - locale of event.</li>
              <li><code class="highlighter-rouge">eventUrl</code> (string) - links to event detail page.</li>
              <li><code class="highlighter-rouge">dates</code> (object) - dates of event.
                <ul>
                  <li><code class="highlighter-rouge">start</code> (object) - start of event.
                    <ul>
                      <li><code class="highlighter-rouge">dateTime</code> (string) - date and time start of event.</li>
                      <li><code class="highlighter-rouge">localDate</code> (string) - local date start of event.</li>
                      <li><code class="highlighter-rouge">localTime</code> (string) - local time start of event.</li>
                    </ul>
                  </li>
                  <li><code class="highlighter-rouge">end</code> (object) - end of event.
                    <ul>
                      <li><code class="highlighter-rouge">dateTime</code> (string) - date and time end of event.</li>
                      <li><code class="highlighter-rouge">localDate</code> (string) - local date end of event.</li>
                      <li><code class="highlighter-rouge">localTime</code> (string) - local time end of event.</li>
                    </ul>
                  </li>
                  <li><code class="highlighter-rouge">timezone</code> (string) - time zone of event.</li>
                  <li><code class="highlighter-rouge">displayOptions</code> (object) - display options of event.
                    <ul>
                      <li><code class="highlighter-rouge">range</code> (object) - range of event displayed.
                        <ul>
                          <li><code class="highlighter-rouge">localStartDate</code> (string) - local start date of event displayed.</li>
                          <li><code class="highlighter-rouge">localEndDate</code> (string) - local end date of event displayed.</li>
                        </ul>
                      </li>
                    </ul>
                  </li>
                  <li><code class="highlighter-rouge">status</code> (object) - status of event.
                    <ul>
                      <li><code class="highlighter-rouge">code</code> (string) - code of status.</li>
                    </ul>
                  </li>
                </ul>
              </li>
              <li><code class="highlighter-rouge">test</code> (boolean) - is test.</li>
              <li><code class="highlighter-rouge">id</code> (string) - id of event.</li>
              <li><code class="highlighter-rouge">_links</code> (object) - links to event.
                <ul>
                  <li><code class="highlighter-rouge">self</code> (object) - link to this event.
                    <ul>
                      <li><code class="highlighter-rouge">href</code> (string) - reference.</li>
                    </ul>
                  </li>
                  <li><code class="highlighter-rouge">categories</code> (array) - links to event categories.
                    <ul>
                      <li><code class="highlighter-rouge"><span class="p">{</span><span class="err">array</span><span class="w"> </span><span class="err">item</span><span class="w"> </span><span class="err">object</span><span class="p">}</span></code> - link.
                        <ul>
                          <li><code class="highlighter-rouge">href</code> (string) - reference to event category.</li>
                        </ul>
                      </li>
                    </ul>
                  </li>
                  <li><code class="highlighter-rouge">attractions</code> (object) - links to event attractions.
                    <ul>
                      <li><code class="highlighter-rouge"><span class="p">{</span><span class="err">array</span><span class="w"> </span><span class="err">item</span><span class="w"> </span><span class="err">object</span><span class="p">}</span></code> - link.
                        <ul>
                          <li><code class="highlighter-rouge">href</code> (string) - reference to event attraction.</li>
                        </ul>
                      </li>
                    </ul>
                  </li>
                  <li><code class="highlighter-rouge">venue</code> (object) - link to event venues.
                    <ul>
                      <li><code class="highlighter-rouge"><span class="p">{</span><span class="err">array</span><span class="w"> </span><span class="err">item</span><span class="w"> </span><span class="err">object</span><span class="p">}</span></code> - link.
                        <ul>
                          <li><code class="highlighter-rouge">href</code> (string) - reference to event venue.</li>
                        </ul>
                      </li>
                    </ul>
                  </li>
                </ul>
              </li>
              <li><code class="highlighter-rouge">_embedded</code> (object) - container for related items.
                <ul>
                  <li><code class="highlighter-rouge">venue</code> (array) - related venues.
                    <ul>
                      <li><code class="highlighter-rouge"><span class="p">{</span><span class="err">array</span><span class="w"> </span><span class="err">item</span><span class="w"> </span><span class="err">object</span><span class="p">}</span></code> - venue.
                        <ul>
                          <li><code class="highlighter-rouge">name</code> (string) - name of event venue.</li>
                          <li><code class="highlighter-rouge">marketId</code> (array) - id of venue markets.
                            <ul>
                              <li><code class="highlighter-rouge"><span class="p">{</span><span class="err">array</span><span class="w"> </span><span class="err">item</span><span class="w"> </span><span class="err">numbers</span><span class="p">}</span></code> - promoter id.</li>
                            </ul>
                          </li>
                          <li><code class="highlighter-rouge">country</code> (object) - country of venue.
                            <ul>
                              <li><code class="highlighter-rouge">countryCode</code> (string) - country code of venue.</li>
                            </ul>
                          </li>
                          <li><code class="highlighter-rouge">state</code> (object) - state of venue.
                            <ul>
                              <li><code class="highlighter-rouge">stateCode</code> (string) - state code of venue.</li>
                            </ul>
                          </li>
                          <li><code class="highlighter-rouge">city</code> (object) - city of venue.
                            <ul>
                              <li><code class="highlighter-rouge">name</code> (string) - city name of venue.</li>
                            </ul>
                          </li>
                          <li><code class="highlighter-rouge">location</code> (object) - location of venue.
                            <ul>
                              <li><code class="highlighter-rouge">latitude</code> (string) - latitude of venue.</li>
                              <li><code class="highlighter-rouge">longitude</code> (string) - longitude of venue.</li>
                            </ul>
                          </li>
                          <li><code class="highlighter-rouge">postalCode</code> (string) - postal code of venue.</li>
                          <li><code class="highlighter-rouge">address</code> (object) - address of venue.
                            <ul>
                              <li><code class="highlighter-rouge">line1</code> (string) - street name.</li>
                              <li><code class="highlighter-rouge">line2</code> (string) - city and state code where event happen.</li>
                            </ul>
                          </li>
                          <li><code class="highlighter-rouge">timeZone</code> (string) - time zone of event.</li>
                          <li><code class="highlighter-rouge">_links</code> (object) - links.
                            <ul>
                              <li><code class="highlighter-rouge">self</code> (object) - link to this venue.
                                <ul>
                                  <li><code class="highlighter-rouge">href</code> (string) - reference.</li>
                                </ul>
                              </li>
                            </ul>
                          </li>
                          <li><code class="highlighter-rouge">id</code> (string) - id of current venue.</li>
                          <li><code class="highlighter-rouge">type</code> (string) - type of current venue.</li>
                        </ul>
                      </li>
                    </ul>
                  </li>
                  <li><code class="highlighter-rouge">categories</code> (array) - related categories.
                    <ul>
                      <li><code class="highlighter-rouge"><span class="p">{</span><span class="err">array</span><span class="w"> </span><span class="err">item</span><span class="w"> </span><span class="err">object</span><span class="p">}</span></code> - categories.
                        <ul>
                          <li><code class="highlighter-rouge">name</code> (string) - name of event category.</li>
                          <li><code class="highlighter-rouge">level</code> (number) - level of event category.</li>
                          <li><code class="highlighter-rouge">_links</code> (object) - links to categories.
                            <ul>
                              <li><code class="highlighter-rouge">self</code> (object) - link to this category.
                                <ul>
                                  <li><code class="highlighter-rouge">href</code> (string) - reference.</li>
                                </ul>
                              </li>
                            </ul>
                          </li>
                        </ul>
                      </li>
                      <li><code class="highlighter-rouge">id</code> (string) - id of current category.</li>
                      <li><code class="highlighter-rouge">type</code> (string) - type of current category.</li>
                    </ul>
                  </li>
                  <li><code class="highlighter-rouge">attractions</code> (array) - related attractions.
                    <ul>
                      <li><code class="highlighter-rouge"><span class="p">{</span><span class="err">array</span><span class="w"> </span><span class="err">item</span><span class="w"> </span><span class="err">object</span><span class="p">}</span></code> - event attractions.
                        <ul>
                          <li><code class="highlighter-rouge">url</code> (string) - url to event attraction.</li>
                          <li><code class="highlighter-rouge">image</code> (object) - images of attraction.
                            <ul>
                              <li><code class="highlighter-rouge">url</code> (string) - images url of event.</li>
                            </ul>
                          </li>
                          <li><code class="highlighter-rouge">name</code> (string) - name of event attraction.</li>
                          <li><code class="highlighter-rouge">_links</code> (object) - links to attractions.
                            <ul>
                              <li><code class="highlighter-rouge">self</code> (object) - link to this attraction.
                                <ul>
                                  <li><code class="highlighter-rouge">href</code> (string) - reference.</li>
                                </ul>
                              </li>
                            </ul>
                          </li>
                          <li><code class="highlighter-rouge">id</code> (string) - id of current attraction.</li>
                          <li><code class="highlighter-rouge">type</code> (string) - type of current attraction.</li>
                        </ul>
                      </li>
                    </ul>
                  </li>
                </ul>
              </li>
              <li><code class="highlighter-rouge">type</code> (string) - type of event.</li>
            </ul>
          </li>
        </ul>
      </li>
    </ul>
  </li>
  <li><code class="highlighter-rouge">_links</code> (object) - links to data sets.
    <ul>
      <li><code class="highlighter-rouge">self</code> (object) - link to this data set.
        <ul>
          <li><code class="highlighter-rouge">href</code> (string) - reference.</li>
          <li><code class="highlighter-rouge">templated</code> (boolean) - ability to be templated.</li>
        </ul>
      </li>
      <li><code class="highlighter-rouge">next</code> (object) - link to the next data set.
        <ul>
          <li><code class="highlighter-rouge">href</code> (string) - reference.</li>
          <li><code class="highlighter-rouge">templated</code> (boolean) - ability to be templated.</li>
        </ul>
      </li>
    </ul>
  </li>
  <li><code class="highlighter-rouge">page</code> (object) - information about current page in data source.
    <ul>
      <li><code class="highlighter-rouge">size</code> (number) - size of page.</li>
      <li><code class="highlighter-rouge">totalElements</code> (number) - total number of available elements in server.</li>
      <li><code class="highlighter-rouge">totalPages</code> (number) - total number of available pages in server.</li>
      <li><code class="highlighter-rouge">number</code> (number) - current page number counted from 0.</li>
    </ul>
  </li>
</ul>

<blockquote class="aside lang-selector">
  <p><a href="#js">JavaScript</a>
<a href="#curl">cURL</a></p>
</blockquote>

<figure class="highlight"><pre><code class="language-js" data-lang="js"><span class="nx">$</span><span class="p">.</span><span class="nx">ajax</span><span class="p">({</span>
  <span class="na">type</span><span class="p">:</span><span class="s2">"GET"</span><span class="p">,</span>
  <span class="na">url</span><span class="p">:</span><span class="s2">"https://app.ticketmaster.com/discovery/v2/events.json?size=1&amp;apikey={apikey}"</span><span class="p">,</span>
  <span class="na">async</span><span class="p">:</span><span class="kc">true</span><span class="p">,</span>
  <span class="na">dataType</span><span class="p">:</span> <span class="s2">"json"</span><span class="p">,</span>
  <span class="na">success</span><span class="p">:</span> <span class="kd">function</span><span class="p">(</span><span class="nx">json</span><span class="p">)</span> <span class="p">{</span>
              <span class="nx">console</span><span class="p">.</span><span class="nx">log</span><span class="p">(</span><span class="nx">json</span><span class="p">);</span>
              <span class="c1">// Parse the response.</span>
              <span class="c1">// Do other things.</span>
           <span class="p">},</span>
  <span class="na">error</span><span class="p">:</span> <span class="kd">function</span><span class="p">(</span><span class="nx">xhr</span><span class="p">,</span> <span class="nx">status</span><span class="p">,</span> <span class="nx">err</span><span class="p">)</span> <span class="p">{</span>
              <span class="c1">// This time, we do not end up here!</span>
           <span class="p">}</span>
<span class="p">});</span></code></pre></figure>

<figure class="highlight"><pre><code class="language-bash" data-lang="bash">curl <span class="se">\</span>
--include <span class="s1">'https://app.ticketmaster.com/discovery/v2/events.json?size=1&amp;apikey={apikey}'</span></code></pre></figure>

<blockquote class="article reqres">
  <p><a href="#req">Request</a>
<a href="#res">Response</a></p>
</blockquote>

<figure class="highlight"><pre><code class="language-http" data-lang="http"><span class="nf">GET</span> <span class="nn">/discovery/v1/events.json?apikey=****&amp;size=1</span> <span class="k">HTTP</span><span class="o">/</span><span class="m">1.1</span>
<span class="na">Host</span><span class="p">:</span> <span class="s">app.ticketmaster.com</span>
<span class="na">X-Target-URI</span><span class="p">:</span> <span class="s">https://app.ticketmaster.com</span>
<span class="na">Connection</span><span class="p">:</span> <span class="s">Keep-Alive</span></code></pre></figure>

<figure class="highlight"><pre><code class="language-http" data-lang="http"><span class="k">HTTP</span><span class="o">/</span><span class="m">1.1</span> <span class="m">200</span> <span class="ne">OK</span>
<span class="na">Access-Control-Allow-Headers</span><span class="p">:</span> <span class="s">origin, x-requested-with, accept</span>
<span class="na">Access-Control-Allow-Origin</span><span class="p">:</span> <span class="s">*</span>
<span class="na">Date</span><span class="p">:</span> <span class="s">Tue, 01 Dec 2015 11:48:01 GMT</span>
<span class="na">Content-Length</span><span class="p">:</span> <span class="s">4174</span>
<span class="na">Access-Control-Max-Age</span><span class="p">:</span> <span class="s">3628800</span>
<span class="na">Access-Control-Allow-Methods</span><span class="p">:</span> <span class="s">GET, PUT, POST, DELETE</span>
<span class="na">X-Application-Context</span><span class="p">:</span> <span class="s">application:default,jetson4</span>
<span class="na">Connection</span><span class="p">:</span> <span class="s">keep-alive</span>
<span class="na">Content-Type</span><span class="p">:</span> <span class="s">application/json;charset=utf-8</span>
<span class="na">Server</span><span class="p">:</span> <span class="s">Apache-Coyote/1.1</span>
<span class="na">Set-Cookie</span><span class="p">:</span> <span class="s">****</span>

<span class="p">{</span><span class="w">
  </span><span class="nt">"_links"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
    </span><span class="nt">"self"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
      </span><span class="nt">"href"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/discovery/v1/events.json?size=1 {&amp;page,sort}"</span><span class="p">,</span><span class="w">
      </span><span class="nt">"templated"</span><span class="p">:</span><span class="w"> </span><span class="kc">true</span><span class="w">
    </span><span class="p">},</span><span class="w">
    </span><span class="nt">"next"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
      </span><span class="nt">"href"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/discovery/v1/events.json?page=1&amp;size=1 {&amp;sort}"</span><span class="p">,</span><span class="w">
      </span><span class="nt">"templated"</span><span class="p">:</span><span class="w"> </span><span class="kc">true</span><span class="w">
    </span><span class="p">}</span><span class="w">
  </span><span class="p">},</span><span class="w">
  </span><span class="nt">"_embedded"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
    </span><span class="nt">"events"</span><span class="p">:</span><span class="w">  </span><span class="p">[</span><span class="w">
       </span><span class="p">{</span><span class="w">
        </span><span class="nt">"name"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Hands On History At Yankee Stadium"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"locale"</span><span class="p">:</span><span class="w"> </span><span class="s2">"en-us"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"promoterId"</span><span class="p">:</span><span class="w">  </span><span class="p">[</span><span class="w">
          </span><span class="mi">685</span><span class="w">
        </span><span class="p">],</span><span class="w">
        </span><span class="nt">"dates"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
          </span><span class="nt">"start"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
            </span><span class="nt">"dateTime"</span><span class="p">:</span><span class="w"> </span><span class="s2">"2015-12-01T05:00:00.000+0000"</span><span class="p">,</span><span class="w">
            </span><span class="nt">"localDate"</span><span class="p">:</span><span class="w"> </span><span class="s2">"2015-12-01"</span><span class="p">,</span><span class="w">
            </span><span class="nt">"localTime"</span><span class="p">:</span><span class="w"> </span><span class="s2">"00:00:00"</span><span class="w">
          </span><span class="p">},</span><span class="w">
          </span><span class="nt">"end"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
            </span><span class="nt">"dateTime"</span><span class="p">:</span><span class="w"> </span><span class="s2">"2015-12-01T05:00:00.000+0000"</span><span class="p">,</span><span class="w">
            </span><span class="nt">"localDate"</span><span class="p">:</span><span class="w"> </span><span class="s2">"2015-12-01"</span><span class="p">,</span><span class="w">
            </span><span class="nt">"localTime"</span><span class="p">:</span><span class="w"> </span><span class="s2">"00:00:00"</span><span class="w">
          </span><span class="p">},</span><span class="w">
          </span><span class="nt">"timezone"</span><span class="p">:</span><span class="w"> </span><span class="s2">"America/New_York"</span><span class="p">,</span><span class="w">
          </span><span class="nt">"displayOptions"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
            </span><span class="nt">"range"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
              </span><span class="nt">"localStartDate"</span><span class="p">:</span><span class="w"> </span><span class="s2">"2015-12-01"</span><span class="p">,</span><span class="w">
              </span><span class="nt">"localEndDate"</span><span class="p">:</span><span class="w"> </span><span class="s2">"2015-12-01"</span><span class="w">
            </span><span class="p">}</span><span class="w">
          </span><span class="p">},</span><span class="w">
          </span><span class="nt">"status"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
            </span><span class="nt">"code"</span><span class="p">:</span><span class="w"> </span><span class="s2">"active"</span><span class="w">
          </span><span class="p">}</span><span class="w">
        </span><span class="p">},</span><span class="w">
        </span><span class="nt">"test"</span><span class="p">:</span><span class="w"> </span><span class="kc">false</span><span class="p">,</span><span class="w">
        </span><span class="nt">"groupId"</span><span class="p">:</span><span class="w"> </span><span class="s2">"BC473708"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"_links"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
          </span><span class="nt">"self"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
            </span><span class="nt">"href"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/discovery/v1/events/1D004E35E969579D?locale=en-us&amp;domain=ticketmaster.com"</span><span class="w">
          </span><span class="p">},</span><span class="w">
          </span><span class="nt">"categories"</span><span class="p">:</span><span class="w">  </span><span class="p">[</span><span class="w">
             </span><span class="p">{</span><span class="w">
              </span><span class="nt">"href"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/discovery/v1/categories/10005?locale=en-us&amp;domain=ticketmaster.com"</span><span class="w">
            </span><span class="p">},</span><span class="w">
             </span><span class="p">{</span><span class="w">
              </span><span class="nt">"href"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/discovery/v1/categories/106?locale=en-us&amp;domain=ticketmaster.com"</span><span class="w">
            </span><span class="p">}</span><span class="w">
          </span><span class="p">],</span><span class="w">
          </span><span class="nt">"venue"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
            </span><span class="nt">"href"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/discovery/v1/venues/237572?locale=en-us&amp;domain=ticketmaster.com"</span><span class="w">
          </span><span class="p">},</span><span class="w">
          </span><span class="nt">"attractions"</span><span class="p">:</span><span class="w">  </span><span class="p">[</span><span class="w">
             </span><span class="p">{</span><span class="w">
              </span><span class="nt">"href"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/discovery/v1/attractions/1982144?locale=en-us&amp;domain=ticketmaster.com"</span><span class="w">
            </span><span class="p">},</span><span class="w">
             </span><span class="p">{</span><span class="w">
              </span><span class="nt">"href"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/discovery/v1/attractions/875284?locale=en-us&amp;domain=ticketmaster.com"</span><span class="w">
            </span><span class="p">}</span><span class="w">
          </span><span class="p">]</span><span class="w">
        </span><span class="p">},</span><span class="w">
        </span><span class="nt">"id"</span><span class="p">:</span><span class="w"> </span><span class="s2">"1D004E35E969579D"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"_embedded"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
          </span><span class="nt">"venue"</span><span class="p">:</span><span class="w">  </span><span class="p">[</span><span class="w">
             </span><span class="p">{</span><span class="w">
              </span><span class="nt">"name"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Yankee Stadium"</span><span class="p">,</span><span class="w">
              </span><span class="nt">"marketId"</span><span class="p">:</span><span class="w">  </span><span class="p">[</span><span class="w">
                </span><span class="mi">124</span><span class="p">,</span><span class="w">
                </span><span class="mi">35</span><span class="p">,</span><span class="w">
                </span><span class="mi">55</span><span class="w">
              </span><span class="p">],</span><span class="w">
              </span><span class="nt">"country"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
                </span><span class="nt">"countryCode"</span><span class="p">:</span><span class="w"> </span><span class="s2">"US"</span><span class="w">
              </span><span class="p">},</span><span class="w">
              </span><span class="nt">"state"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
                </span><span class="nt">"stateCode"</span><span class="p">:</span><span class="w"> </span><span class="s2">"NY"</span><span class="w">
              </span><span class="p">},</span><span class="w">
              </span><span class="nt">"city"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
                </span><span class="nt">"name"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Bronx"</span><span class="w">
              </span><span class="p">},</span><span class="w">
              </span><span class="nt">"location"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
                </span><span class="nt">"latitude"</span><span class="p">:</span><span class="w"> </span><span class="s2">"40.828523700"</span><span class="p">,</span><span class="w">
                </span><span class="nt">"longitude"</span><span class="p">:</span><span class="w"> </span><span class="s2">"-73.927626400"</span><span class="w">
              </span><span class="p">},</span><span class="w">
              </span><span class="nt">"postalCode"</span><span class="p">:</span><span class="w"> </span><span class="s2">"10451"</span><span class="p">,</span><span class="w">
              </span><span class="nt">"address"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
                </span><span class="nt">"line1"</span><span class="p">:</span><span class="w"> </span><span class="s2">"1 East 161st Street"</span><span class="p">,</span><span class="w">
                </span><span class="nt">"line2"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Bronx, NY"</span><span class="w">
              </span><span class="p">},</span><span class="w">
              </span><span class="nt">"timeZone"</span><span class="p">:</span><span class="w"> </span><span class="s2">"America/New_York"</span><span class="p">,</span><span class="w">
              </span><span class="nt">"_links"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
                </span><span class="nt">"self"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
                  </span><span class="nt">"href"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/discovery/v1/venues/237572?locale=en-us&amp;domain=ticketmaster.com"</span><span class="w">
                </span><span class="p">}</span><span class="w">
              </span><span class="p">},</span><span class="w">
              </span><span class="nt">"id"</span><span class="p">:</span><span class="w"> </span><span class="s2">"237572"</span><span class="p">,</span><span class="w">
              </span><span class="nt">"type"</span><span class="p">:</span><span class="w"> </span><span class="s2">"venue"</span><span class="w">
            </span><span class="p">}</span><span class="w">
          </span><span class="p">],</span><span class="w">
          </span><span class="nt">"categories"</span><span class="p">:</span><span class="w">  </span><span class="p">[</span><span class="w">
             </span><span class="p">{</span><span class="w">
              </span><span class="nt">"name"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Miscellaneous"</span><span class="p">,</span><span class="w">
              </span><span class="nt">"level"</span><span class="p">:</span><span class="w"> </span><span class="mi">1</span><span class="p">,</span><span class="w">
              </span><span class="nt">"_links"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
                </span><span class="nt">"self"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
                  </span><span class="nt">"href"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/discovery/v1/categories/10005?locale=en-us&amp;domain=ticketmaster.com"</span><span class="w">
                </span><span class="p">}</span><span class="w">
              </span><span class="p">},</span><span class="w">
              </span><span class="nt">"id"</span><span class="p">:</span><span class="w"> </span><span class="s2">"10005"</span><span class="p">,</span><span class="w">
              </span><span class="nt">"type"</span><span class="p">:</span><span class="w"> </span><span class="s2">"category"</span><span class="w">
            </span><span class="p">},</span><span class="w">
             </span><span class="p">{</span><span class="w">
              </span><span class="nt">"name"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Cruise and Sightseeing"</span><span class="p">,</span><span class="w">
              </span><span class="nt">"level"</span><span class="p">:</span><span class="w"> </span><span class="mi">2</span><span class="p">,</span><span class="w">
              </span><span class="nt">"_links"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
                </span><span class="nt">"self"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
                  </span><span class="nt">"href"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/discovery/v1/categories/106?locale=en-us&amp;domain=ticketmaster.com"</span><span class="w">
                </span><span class="p">}</span><span class="w">
              </span><span class="p">},</span><span class="w">
              </span><span class="nt">"id"</span><span class="p">:</span><span class="w"> </span><span class="s2">"106"</span><span class="p">,</span><span class="w">
              </span><span class="nt">"type"</span><span class="p">:</span><span class="w"> </span><span class="s2">"category"</span><span class="w">
            </span><span class="p">}</span><span class="w">
          </span><span class="p">],</span><span class="w">
          </span><span class="nt">"attractions"</span><span class="p">:</span><span class="w">  </span><span class="p">[</span><span class="w">
             </span><span class="p">{</span><span class="w">
              </span><span class="nt">"url"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/Hands-On-History-At-Yankee-Stadium-tickets/artist/1982144"</span><span class="p">,</span><span class="w">
              </span><span class="nt">"image"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
                </span><span class="nt">"url"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/dbimages/173891a.jpg"</span><span class="w">
              </span><span class="p">},</span><span class="w">
              </span><span class="nt">"name"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Hands On History At Yankee Stadium"</span><span class="p">,</span><span class="w">
              </span><span class="nt">"_links"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
                </span><span class="nt">"self"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
                  </span><span class="nt">"href"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/discovery/v1/attractions/1982144?locale=en-us&amp;domain=ticketmaster.com"</span><span class="w">
                </span><span class="p">}</span><span class="w">
              </span><span class="p">},</span><span class="w">
              </span><span class="nt">"id"</span><span class="p">:</span><span class="w"> </span><span class="s2">"1982144"</span><span class="p">,</span><span class="w">
              </span><span class="nt">"type"</span><span class="p">:</span><span class="w"> </span><span class="s2">"attraction"</span><span class="w">
            </span><span class="p">},</span><span class="w">
             </span><span class="p">{</span><span class="w">
              </span><span class="nt">"_links"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
                </span><span class="nt">"self"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
                  </span><span class="nt">"href"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/discovery/v1/attractions/875284?locale=en-us&amp;domain=ticketmaster.com"</span><span class="w">
                </span><span class="p">}</span><span class="w">
              </span><span class="p">},</span><span class="w">
              </span><span class="nt">"id"</span><span class="p">:</span><span class="w"> </span><span class="s2">"875284"</span><span class="p">,</span><span class="w">
              </span><span class="nt">"type"</span><span class="p">:</span><span class="w"> </span><span class="s2">"attraction"</span><span class="w">
            </span><span class="p">}</span><span class="w">
          </span><span class="p">]</span><span class="w">
        </span><span class="p">},</span><span class="w">
        </span><span class="nt">"type"</span><span class="p">:</span><span class="w"> </span><span class="s2">"event"</span><span class="w">
      </span><span class="p">}</span><span class="w">
    </span><span class="p">]</span><span class="w">
  </span><span class="p">},</span><span class="w">
  </span><span class="nt">"page"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
    </span><span class="nt">"size"</span><span class="p">:</span><span class="w"> </span><span class="mi">1</span><span class="p">,</span><span class="w">
    </span><span class="nt">"totalElements"</span><span class="p">:</span><span class="w"> </span><span class="mi">56811</span><span class="p">,</span><span class="w">
    </span><span class="nt">"totalPages"</span><span class="p">:</span><span class="w"> </span><span class="mi">56811</span><span class="p">,</span><span class="w">
    </span><span class="nt">"number"</span><span class="p">:</span><span class="w"> </span><span class="mi">0</span><span class="w">
  </span><span class="p">}</span><span class="w">
</span><span class="p">}</span></code></pre></figure>

<h2 class="article console-link" id="event-details">Get Event Details</h2>

<p><strong>Method:</strong> GET.
Authentication required.
Returns the event detail by event ID.</p>

<p class="code red">discovery/{version}/events/{id}.{format}</p>

<h3 id="url-parameters-1">URL parameters:</h3>

<table>
  <thead>
    <tr>
      <th style="text-align: left">Parameter</th>
      <th style="text-align: left">Description</th>
      <th style="text-align: left">Type</th>
      <th style="text-align: left">Default Value</th>
      <th style="text-align: left">Required</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align: left"><code class="highlighter-rouge">version</code></td>
      <td style="text-align: left">The API Version.</td>
      <td style="text-align: left">string</td>
      <td style="text-align: left">“v2”</td>
      <td style="text-align: left">Yes</td>
    </tr>
    <tr>
      <td style="text-align: left"><code class="highlighter-rouge">id</code></td>
      <td style="text-align: left">Event ID. Required.</td>
      <td style="text-align: left">string</td>
      <td style="text-align: left">“1A4ZAZyGkeUYKaO”</td>
      <td style="text-align: left">Yes</td>
    </tr>
    <tr>
      <td style="text-align: left"><code class="highlighter-rouge">format</code></td>
      <td style="text-align: left">API Response Format.</td>
      <td style="text-align: left">string</td>
      <td style="text-align: left">“json”</td>
      <td style="text-align: left">Yes</td>
    </tr>
  </tbody>
</table>

<h3 id="query-parameters-1">Query parameters:</h3>

<table>
  <thead>
    <tr>
      <th style="text-align: left">Parameter</th>
      <th style="text-align: left">Description</th>
      <th style="text-align: left">Type</th>
      <th style="text-align: left">Default Value</th>
      <th style="text-align: left">Required</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align: left"><code class="highlighter-rouge">locale</code></td>
      <td style="text-align: left">The event locale, including country and localization. Values: “”, “en-us”, “en-gb”, “en-ca”, “es-us”, “en-mx”, “es-mx”, “en-au”, “en-nz”, “fr-fr”, “fr-ca”.</td>
      <td style="text-align: left">string</td>
      <td style="text-align: left">”en-us”</td>
      <td style="text-align: left">No</td>
    </tr>
  </tbody>
</table>

<h3 id="response-structure-1">Response structure:</h3>

<ul class="nested-list">
  <li><code class="highlighter-rouge">name</code> (string) - name of event.</li>
  <li><code class="highlighter-rouge">locale</code> (string) - locale of event.</li>
  <li><code class="highlighter-rouge">eventUrl</code> (string) - links to event detail page.</li>
  <li><code class="highlighter-rouge">promoterId</code> (array) - promoter ids of event.
    <ul>
      <li><code class="highlighter-rouge"><span class="p">{</span><span class="err">array</span><span class="w"> </span><span class="err">item</span><span class="w"> </span><span class="err">numbers</span><span class="p">}</span></code> - promoter id.</li>
    </ul>
  </li>
  <li><code class="highlighter-rouge">dates</code> (object) - dates of event.
    <ul>
      <li><code class="highlighter-rouge">start</code> (object) - start of event.
        <ul>
          <li><code class="highlighter-rouge">dateTime</code> (string) - date and time start of event.</li>
          <li><code class="highlighter-rouge">localDate</code> (string) - local date start of event.</li>
          <li><code class="highlighter-rouge">localTime</code> (string) - local time start of event.</li>
        </ul>
      </li>
      <li><code class="highlighter-rouge">end</code> (object) - end of event.
        <ul>
          <li><code class="highlighter-rouge">dateTime</code> (string) - date and time end of event.</li>
          <li><code class="highlighter-rouge">localDate</code> (string) - local date end of event.</li>
          <li><code class="highlighter-rouge">localTime</code> (string) - local time end of event.</li>
        </ul>
      </li>
      <li><code class="highlighter-rouge">timezone</code> (string) - time zone of event.</li>
      <li><code class="highlighter-rouge">displayOptions</code> (object) - display options of event.
        <ul>
          <li><code class="highlighter-rouge">range</code> (object) - range of event displayed.
            <ul>
              <li><code class="highlighter-rouge">localStartDate</code> (string) - local start date of event displayed.</li>
              <li><code class="highlighter-rouge">localEndDate</code> (string) - local end date of event displayed.</li>
            </ul>
          </li>
        </ul>
      </li>
      <li><code class="highlighter-rouge">status</code> (object) - status of event.
        <ul>
          <li><code class="highlighter-rouge">code</code> (string) - code of status.</li>
        </ul>
      </li>
    </ul>
  </li>
  <li><code class="highlighter-rouge">test</code> (boolean) - is test.</li>
  <li><code class="highlighter-rouge">_links</code> (object) - links to event.
    <ul>
      <li><code class="highlighter-rouge">self</code> (object) - link to this event.
        <ul>
          <li><code class="highlighter-rouge">href</code> (string) - reference.</li>
        </ul>
      </li>
      <li><code class="highlighter-rouge">categories</code> (array) - links to event categories.
        <ul>
          <li><code class="highlighter-rouge"><span class="p">{</span><span class="err">array</span><span class="w"> </span><span class="err">item</span><span class="w"> </span><span class="err">object</span><span class="p">}</span></code> - link.
            <ul>
              <li><code class="highlighter-rouge">href</code> (string) - reference to event category.</li>
            </ul>
          </li>
        </ul>
      </li>
      <li><code class="highlighter-rouge">attractions</code> (object) - links to event attractions.
        <ul>
          <li><code class="highlighter-rouge"><span class="p">{</span><span class="err">array</span><span class="w"> </span><span class="err">item</span><span class="w"> </span><span class="err">object</span><span class="p">}</span></code> - link.
            <ul>
              <li><code class="highlighter-rouge">href</code> (string) - reference to event attraction.</li>
            </ul>
          </li>
        </ul>
      </li>
      <li><code class="highlighter-rouge">venue</code> (object) - link to event venues.
        <ul>
          <li><code class="highlighter-rouge"><span class="p">{</span><span class="err">array</span><span class="w"> </span><span class="err">item</span><span class="w"> </span><span class="err">object</span><span class="p">}</span></code> - link.
            <ul>
              <li><code class="highlighter-rouge">href</code> (string) - reference to event venue.</li>
            </ul>
          </li>
        </ul>
      </li>
    </ul>
  </li>
  <li><code class="highlighter-rouge">id</code> (string) - id of current event.</li>
  <li><code class="highlighter-rouge">_embedded</code> (object) - container for data.
    <ul>
      <li><code class="highlighter-rouge">venue</code> (array) - event venues.
        <ul>
          <li><code class="highlighter-rouge"><span class="p">{</span><span class="err">array</span><span class="w"> </span><span class="err">item</span><span class="w"> </span><span class="err">object</span><span class="p">}</span></code> - event venues.
            <ul>
              <li><code class="highlighter-rouge">name</code> (string) - name of event venue.</li>
              <li><code class="highlighter-rouge">marketId</code> (array) - id of venue markets.
                <ul>
                  <li><code class="highlighter-rouge"><span class="p">{</span><span class="err">array</span><span class="w"> </span><span class="err">item</span><span class="w"> </span><span class="err">numbers</span><span class="p">}</span></code> - promoter id.</li>
                </ul>
              </li>
              <li><code class="highlighter-rouge">country</code> (object) - country of venue.
                <ul>
                  <li><code class="highlighter-rouge">countryCode</code> (string) - country code of venue.</li>
                </ul>
              </li>
              <li><code class="highlighter-rouge">state</code> (object) - state of venue.
                <ul>
                  <li><code class="highlighter-rouge">stateCode</code> (string) - state code of venue.</li>
                </ul>
              </li>
              <li><code class="highlighter-rouge">city</code> (object) - city of venue.
                <ul>
                  <li><code class="highlighter-rouge">name</code> (string) - city name of venue.</li>
                </ul>
              </li>
              <li><code class="highlighter-rouge">location</code> (object) - location of venue.
                <ul>
                  <li><code class="highlighter-rouge">latitude</code> (string) - latitude of venue.</li>
                  <li><code class="highlighter-rouge">longitude</code> (string) - longitude of venue.</li>
                </ul>
              </li>
              <li><code class="highlighter-rouge">postalCode</code> (string) - postal code of venue.</li>
              <li><code class="highlighter-rouge">address</code> (object) - address of venue.
                <ul>
                  <li><code class="highlighter-rouge">line1</code> (string) - street name.</li>
                  <li><code class="highlighter-rouge">line2</code> (string) - city and state code where event happen.</li>
                </ul>
              </li>
              <li><code class="highlighter-rouge">timeZone</code> (string) - time zone of event.</li>
              <li><code class="highlighter-rouge">_links</code> (object) - links to event.
                <ul>
                  <li><code class="highlighter-rouge">self</code> (object) - link to this event.
                    <ul>
                      <li><code class="highlighter-rouge">href</code> (string) - reference.</li>
                    </ul>
                  </li>
                </ul>
              </li>
              <li><code class="highlighter-rouge">id</code> (string) - id of current venue.</li>
              <li><code class="highlighter-rouge">type</code> (string) - type of current venue.</li>
            </ul>
          </li>
        </ul>
      </li>
      <li><code class="highlighter-rouge">categories</code> (array) - link to event categories.
        <ul>
          <li><code class="highlighter-rouge"><span class="p">{</span><span class="err">array</span><span class="w"> </span><span class="err">item</span><span class="w"> </span><span class="err">object</span><span class="p">}</span></code> - event categories.
            <ul>
              <li><code class="highlighter-rouge">name</code> (string) - name of event category.</li>
              <li><code class="highlighter-rouge">level</code> (number) - level of event category.</li>
              <li><code class="highlighter-rouge">_links</code> (object) - links to categories.
                <ul>
                  <li><code class="highlighter-rouge">self</code> (object) - link to this category.
                    <ul>
                      <li><code class="highlighter-rouge">href</code> (string) - reference.</li>
                    </ul>
                  </li>
                </ul>
              </li>
            </ul>
          </li>
          <li><code class="highlighter-rouge">id</code> (string) - id of current category.</li>
          <li><code class="highlighter-rouge">type</code> (string) - type of current category.</li>
        </ul>
      </li>
      <li><code class="highlighter-rouge">attractions</code> (array) - event attractions.
        <ul>
          <li><code class="highlighter-rouge"><span class="p">{</span><span class="err">array</span><span class="w"> </span><span class="err">item</span><span class="w"> </span><span class="err">object</span><span class="p">}</span></code> - event attractions.
            <ul>
              <li><code class="highlighter-rouge">url</code> (string) - url to event attraction.</li>
              <li><code class="highlighter-rouge">image</code> (object) - images of attraction.
                <ul>
                  <li><code class="highlighter-rouge">url</code> (string) - images url of event.</li>
                </ul>
              </li>
              <li><code class="highlighter-rouge">name</code> (string) - name of event attraction.</li>
              <li><code class="highlighter-rouge">_links</code> (object) - links to attractions.
                <ul>
                  <li><code class="highlighter-rouge">self</code> (object) - link to this attraction.
                    <ul>
                      <li><code class="highlighter-rouge">href</code> (string) - reference.</li>
                    </ul>
                  </li>
                </ul>
              </li>
              <li><code class="highlighter-rouge">id</code> (string) - id of current attraction.</li>
              <li><code class="highlighter-rouge">type</code> (string) - type of current attraction.</li>
            </ul>
          </li>
        </ul>
      </li>
    </ul>
  </li>
  <li><code class="highlighter-rouge">type</code> (string) - type of event.</li>
</ul>

<blockquote class="aside lang-selector">
  <p><a href="#js">JavaScript</a>
<a href="#curl">cURL</a></p>
</blockquote>

<figure class="highlight"><pre><code class="language-js" data-lang="js"><span class="nx">$</span><span class="p">.</span><span class="nx">ajax</span><span class="p">({</span>
  <span class="na">type</span><span class="p">:</span><span class="s2">"GET"</span><span class="p">,</span>
  <span class="na">url</span><span class="p">:</span><span class="s2">"https://app.ticketmaster.com/discovery/v1/events/0B004F0401BD55E5.json?apikey={apikey}"</span><span class="p">,</span>
  <span class="na">async</span><span class="p">:</span><span class="kc">true</span><span class="p">,</span>
  <span class="na">dataType</span><span class="p">:</span> <span class="s2">"json"</span><span class="p">,</span>
  <span class="na">success</span><span class="p">:</span> <span class="kd">function</span><span class="p">(</span><span class="nx">json</span><span class="p">)</span> <span class="p">{</span>
              <span class="nx">console</span><span class="p">.</span><span class="nx">log</span><span class="p">(</span><span class="nx">json</span><span class="p">);</span>
              <span class="c1">// Parse the response.</span>
              <span class="c1">// Do other things.</span>
           <span class="p">},</span>
  <span class="na">error</span><span class="p">:</span> <span class="kd">function</span><span class="p">(</span><span class="nx">xhr</span><span class="p">,</span> <span class="nx">status</span><span class="p">,</span> <span class="nx">err</span><span class="p">)</span> <span class="p">{</span>
              <span class="c1">// This time, we do not end up here!</span>
           <span class="p">}</span>
<span class="p">});</span></code></pre></figure>

<figure class="highlight"><pre><code class="language-bash" data-lang="bash">curl <span class="se">\</span>
--include <span class="s1">'https://app.ticketmaster.com/discovery/v1/events/0B004F0401BD55E5.json?apikey={apikey}'</span></code></pre></figure>

<blockquote class="article reqres">
  <p><a href="#req">Request</a>
<a href="#res">Response</a></p>
</blockquote>

<figure class="highlight"><pre><code class="language-http" data-lang="http"><span class="nf">GET</span> <span class="nn">/discovery/v1/events/15004F83A3383A3E.json?apikey=****</span> <span class="k">HTTP</span><span class="o">/</span><span class="m">1.1</span>
<span class="na">Host</span><span class="p">:</span> <span class="s">app.ticketmaster.com</span>
<span class="na">X-Target-URI</span><span class="p">:</span> <span class="s">https://app.ticketmaster.com</span>
<span class="na">Connection</span><span class="p">:</span> <span class="s">Keep-Alive</span></code></pre></figure>

<figure class="highlight"><pre><code class="language-http" data-lang="http"><span class="k">HTTP</span><span class="o">/</span><span class="m">1.1</span> <span class="m">200</span> <span class="ne">OK</span>
<span class="na">Access-Control-Allow-Headers</span><span class="p">:</span> <span class="s">origin, x-requested-with, accept</span>
<span class="na">Access-Control-Allow-Origin</span><span class="p">:</span> <span class="s">*</span>
<span class="na">Date</span><span class="p">:</span> <span class="s">Tue, 15 Dec 2015 13:43:46 GMT</span>
<span class="na">Content-Length</span><span class="p">:</span> <span class="s">3485</span>
<span class="na">Access-Control-Max-Age</span><span class="p">:</span> <span class="s">3628800</span>
<span class="na">Access-Control-Allow-Methods</span><span class="p">:</span> <span class="s">GET, PUT, POST, DELETE</span>
<span class="na">X-Application-Context</span><span class="p">:</span> <span class="s">application:default,jetson1</span>
<span class="na">Connection</span><span class="p">:</span> <span class="s">keep-alive</span>
<span class="na">Content-Type</span><span class="p">:</span> <span class="s">application/json;charset=utf-8</span>
<span class="na">Server</span><span class="p">:</span> <span class="s">Apache-Coyote/1.1</span>
<span class="na">Set-Cookie</span><span class="p">:</span> <span class="s">****</span>

<span class="p">{</span><span class="w">
  </span><span class="nt">"name"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Aquarium Admission"</span><span class="p">,</span><span class="w">
  </span><span class="nt">"locale"</span><span class="p">:</span><span class="w"> </span><span class="s2">"en-us"</span><span class="p">,</span><span class="w">
  </span><span class="nt">"promoterId"</span><span class="p">:</span><span class="w">  </span><span class="p">[</span><span class="w">
    </span><span class="mi">494</span><span class="w">
  </span><span class="p">],</span><span class="w">
  </span><span class="nt">"dates"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
    </span><span class="nt">"start"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
      </span><span class="nt">"dateTime"</span><span class="p">:</span><span class="w"> </span><span class="s2">"2015-12-15T05:00:00.000+0000"</span><span class="p">,</span><span class="w">
      </span><span class="nt">"localDate"</span><span class="p">:</span><span class="w"> </span><span class="s2">"2015-12-15"</span><span class="p">,</span><span class="w">
      </span><span class="nt">"localTime"</span><span class="p">:</span><span class="w"> </span><span class="s2">"00:00:00"</span><span class="w">
    </span><span class="p">},</span><span class="w">
    </span><span class="nt">"end"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
      </span><span class="nt">"dateTime"</span><span class="p">:</span><span class="w"> </span><span class="s2">"2015-12-15T05:00:00.000+0000"</span><span class="p">,</span><span class="w">
      </span><span class="nt">"localDate"</span><span class="p">:</span><span class="w"> </span><span class="s2">"2015-12-15"</span><span class="p">,</span><span class="w">
      </span><span class="nt">"localTime"</span><span class="p">:</span><span class="w"> </span><span class="s2">"00:00:00"</span><span class="w">
    </span><span class="p">},</span><span class="w">
    </span><span class="nt">"timezone"</span><span class="p">:</span><span class="w"> </span><span class="s2">"America/New_York"</span><span class="p">,</span><span class="w">
    </span><span class="nt">"displayOptions"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
      </span><span class="nt">"range"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
        </span><span class="nt">"localStartDate"</span><span class="p">:</span><span class="w"> </span><span class="s2">"2015-12-15"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"localEndDate"</span><span class="p">:</span><span class="w"> </span><span class="s2">"2015-12-15"</span><span class="w">
      </span><span class="p">}</span><span class="w">
    </span><span class="p">},</span><span class="w">
    </span><span class="nt">"status"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
      </span><span class="nt">"code"</span><span class="p">:</span><span class="w"> </span><span class="s2">"active"</span><span class="w">
    </span><span class="p">}</span><span class="w">
  </span><span class="p">},</span><span class="w">
  </span><span class="nt">"test"</span><span class="p">:</span><span class="w"> </span><span class="kc">false</span><span class="p">,</span><span class="w">
  </span><span class="nt">"_links"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
    </span><span class="nt">"self"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
      </span><span class="nt">"href"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/discovery/v1/events/15004F83A3383A3E?locale=en-us&amp;domain=ticketmaster.com"</span><span class="w">
    </span><span class="p">},</span><span class="w">
    </span><span class="nt">"categories"</span><span class="p">:</span><span class="w">  </span><span class="p">[</span><span class="w">
       </span><span class="p">{</span><span class="w">
        </span><span class="nt">"href"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/discovery/v1/categories/10003?locale=en-us&amp;domain=ticketmaster.com"</span><span class="w">
      </span><span class="p">},</span><span class="w">
       </span><span class="p">{</span><span class="w">
        </span><span class="nt">"href"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/discovery/v1/categories/19?locale=en-us&amp;domain=ticketmaster.com"</span><span class="w">
      </span><span class="p">}</span><span class="w">
    </span><span class="p">],</span><span class="w">
    </span><span class="nt">"attractions"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
      </span><span class="nt">"href"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/discovery/v1/attractions/852425?locale=en-us&amp;domain=ticketmaster.com"</span><span class="w">
    </span><span class="p">},</span><span class="w">
    </span><span class="nt">"venue"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
      </span><span class="nt">"href"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/discovery/v1/venues/172095?locale=en-us&amp;domain=ticketmaster.com"</span><span class="w">
    </span><span class="p">}</span><span class="w">
  </span><span class="p">},</span><span class="w">
  </span><span class="nt">"id"</span><span class="p">:</span><span class="w"> </span><span class="s2">"15004F83A3383A3E"</span><span class="p">,</span><span class="w">
  </span><span class="nt">"_embedded"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
    </span><span class="nt">"venue"</span><span class="p">:</span><span class="w">  </span><span class="p">[</span><span class="w">
       </span><span class="p">{</span><span class="w">
        </span><span class="nt">"name"</span><span class="p">:</span><span class="w"> </span><span class="s2">"National Aquarium In Baltimore"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"marketId"</span><span class="p">:</span><span class="w">  </span><span class="p">[</span><span class="w">
          </span><span class="mi">47</span><span class="w">
        </span><span class="p">],</span><span class="w">
        </span><span class="nt">"country"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
          </span><span class="nt">"countryCode"</span><span class="p">:</span><span class="w"> </span><span class="s2">"US"</span><span class="w">
        </span><span class="p">},</span><span class="w">
        </span><span class="nt">"state"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
          </span><span class="nt">"stateCode"</span><span class="p">:</span><span class="w"> </span><span class="s2">"MD"</span><span class="w">
        </span><span class="p">},</span><span class="w">
        </span><span class="nt">"city"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
          </span><span class="nt">"name"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Baltimore"</span><span class="w">
        </span><span class="p">},</span><span class="w">
        </span><span class="nt">"location"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
          </span><span class="nt">"latitude"</span><span class="p">:</span><span class="w"> </span><span class="s2">"39.285497900"</span><span class="p">,</span><span class="w">
          </span><span class="nt">"longitude"</span><span class="p">:</span><span class="w"> </span><span class="s2">"-76.608331000"</span><span class="w">
        </span><span class="p">},</span><span class="w">
        </span><span class="nt">"postalCode"</span><span class="p">:</span><span class="w"> </span><span class="s2">"21202"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"address"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
          </span><span class="nt">"line1"</span><span class="p">:</span><span class="w"> </span><span class="s2">"501 East Pratt St."</span><span class="p">,</span><span class="w">
          </span><span class="nt">"line2"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Baltimore, MD"</span><span class="w">
        </span><span class="p">},</span><span class="w">
        </span><span class="nt">"timeZone"</span><span class="p">:</span><span class="w"> </span><span class="s2">"America/New_York"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"_links"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
          </span><span class="nt">"self"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
            </span><span class="nt">"href"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/discovery/v1/venues/172095?locale=en-us&amp;domain=ticketmaster.com"</span><span class="w">
          </span><span class="p">}</span><span class="w">
        </span><span class="p">},</span><span class="w">
        </span><span class="nt">"id"</span><span class="p">:</span><span class="w"> </span><span class="s2">"172095"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"type"</span><span class="p">:</span><span class="w"> </span><span class="s2">"venue"</span><span class="w">
      </span><span class="p">}</span><span class="w">
    </span><span class="p">],</span><span class="w">
    </span><span class="nt">"categories"</span><span class="p">:</span><span class="w">  </span><span class="p">[</span><span class="w">
       </span><span class="p">{</span><span class="w">
        </span><span class="nt">"name"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Family"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"level"</span><span class="p">:</span><span class="w"> </span><span class="mi">1</span><span class="p">,</span><span class="w">
        </span><span class="nt">"_links"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
          </span><span class="nt">"self"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
            </span><span class="nt">"href"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/discovery/v1/categories/10003?locale=en-us&amp;domain=ticketmaster.com"</span><span class="w">
          </span><span class="p">}</span><span class="w">
        </span><span class="p">},</span><span class="w">
        </span><span class="nt">"id"</span><span class="p">:</span><span class="w"> </span><span class="s2">"10003"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"type"</span><span class="p">:</span><span class="w"> </span><span class="s2">"category"</span><span class="w">
      </span><span class="p">},</span><span class="w">
       </span><span class="p">{</span><span class="w">
        </span><span class="nt">"name"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Family Attractions"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"level"</span><span class="p">:</span><span class="w"> </span><span class="mi">2</span><span class="p">,</span><span class="w">
        </span><span class="nt">"_links"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
          </span><span class="nt">"self"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
            </span><span class="nt">"href"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/discovery/v1/categories/19?locale=en-us&amp;domain=ticketmaster.com"</span><span class="w">
          </span><span class="p">}</span><span class="w">
        </span><span class="p">},</span><span class="w">
        </span><span class="nt">"id"</span><span class="p">:</span><span class="w"> </span><span class="s2">"19"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"type"</span><span class="p">:</span><span class="w"> </span><span class="s2">"category"</span><span class="w">
      </span><span class="p">}</span><span class="w">
    </span><span class="p">],</span><span class="w">
    </span><span class="nt">"attractions"</span><span class="p">:</span><span class="w">  </span><span class="p">[</span><span class="w">
       </span><span class="p">{</span><span class="w">
        </span><span class="nt">"url"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/National-Aquarium-In-Baltimore-tickets/artist/852425"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"image"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
          </span><span class="nt">"url"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/dbimages/45546a"</span><span class="w">
        </span><span class="p">},</span><span class="w">
        </span><span class="nt">"name"</span><span class="p">:</span><span class="w"> </span><span class="s2">"National Aquarium In Baltimore"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"_links"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
          </span><span class="nt">"self"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
            </span><span class="nt">"href"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/discovery/v1/attractions/852425?locale=en-us&amp;domain=ticketmaster.com"</span><span class="w">
          </span><span class="p">}</span><span class="w">
        </span><span class="p">},</span><span class="w">
        </span><span class="nt">"id"</span><span class="p">:</span><span class="w"> </span><span class="s2">"852425"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"type"</span><span class="p">:</span><span class="w"> </span><span class="s2">"attraction"</span><span class="w">
      </span><span class="p">}</span><span class="w">
    </span><span class="p">]</span><span class="w">
  </span><span class="p">},</span><span class="w">
  </span><span class="nt">"type"</span><span class="p">:</span><span class="w"> </span><span class="s2">"event"</span><span class="w">
</span><span class="p">}</span><span class="w">
</span><span class="err">}</span></code></pre></figure>

<h2 class="article console-link" id="event-img">Search Event Images</h2>

<p><strong>Method:</strong> GET.
Authentication required.
Returns all the images for an event by ID. If an event does not have an image for a supported resolution, the event’s classification image will be returned instead.</p>

<p class="code red">discovery/{version}/events/{id}/images.{format}</p>

<h3 id="url-parameters-2">URL parameters:</h3>

<table>
  <thead>
    <tr>
      <th style="text-align: left">Parameter</th>
      <th style="text-align: left">Description</th>
      <th style="text-align: left">Type</th>
      <th style="text-align: left">Default Value</th>
      <th style="text-align: left">Required</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align: left"><code class="highlighter-rouge">version</code></td>
      <td style="text-align: left">The API Version.</td>
      <td style="text-align: left">string</td>
      <td style="text-align: left">“v2”</td>
      <td style="text-align: left">Yes</td>
    </tr>
    <tr>
      <td style="text-align: left"><code class="highlighter-rouge">id</code></td>
      <td style="text-align: left">Event ID.</td>
      <td style="text-align: left">string</td>
      <td style="text-align: left">“1A4ZAZyGkeUYKaO”</td>
      <td style="text-align: left">Yes</td>
    </tr>
    <tr>
      <td style="text-align: left"><code class="highlighter-rouge">locale</code></td>
      <td style="text-align: left">The event locale, including country and localization. Values: “”, “en-us”, “en-gb”, “en-ca”, “es-us”, “en-mx”, “es-mx”, “en-au”, “en-nz”, “fr-fr”, “fr-ca”.</td>
      <td style="text-align: left">string</td>
      <td style="text-align: left">”en-us”</td>
      <td style="text-align: left">No</td>
    </tr>    
    <tr>
      <td style="text-align: left"><code class="highlighter-rouge">format</code></td>
      <td style="text-align: left">API Response Format.</td>
      <td style="text-align: left">string</td>
      <td style="text-align: left">“json”</td>
      <td style="text-align: left">Yes</td>
    </tr>    
  </tbody>
</table>

<h3 id="response-structure-2">Response structure:</h3>

<ul class="nested-list">
  <li><code class="highlighter-rouge">type</code> (string) - type of images set</li>
  <li><code class="highlighter-rouge">id</code> (string) - id of event</li>
  <li><code class="highlighter-rouge">images</code> (array) - images.
    <ul>
      <li><code class="highlighter-rouge"><span class="p">{</span><span class="err">array</span><span class="w"> </span><span class="err">item</span><span class="w"> </span><span class="err">object</span><span class="p">}</span></code> - image.
        <ul>
          <li><code class="highlighter-rouge">ratio</code> (string) - image ratio.</li>
          <li><code class="highlighter-rouge">url</code> (string) - image url.</li>
          <li><code class="highlighter-rouge">width</code> (string) - image width.</li>
          <li><code class="highlighter-rouge">height</code> (string) - image height.</li>
          <li><code class="highlighter-rouge">fallback</code> (boolean) - image fallback availability.</li>
        </ul>
      </li>
    </ul>
  </li>
  <li><code class="highlighter-rouge">_links</code> (object) - links to images data set.
    <ul>
      <li><code class="highlighter-rouge">self</code> (object) - link to this images set.
        <ul>
          <li><code class="highlighter-rouge">href</code> (string) - reference.</li>
        </ul>
      </li>
    </ul>
  </li>
</ul>

<blockquote class="aside lang-selector">
  <p><a href="#js">JavaScript</a>
<a href="#curl">cURL</a></p>
</blockquote>

<figure class="highlight"><pre><code class="language-js" data-lang="js"><span class="nx">$</span><span class="p">.</span><span class="nx">ajax</span><span class="p">({</span>
  <span class="na">type</span><span class="p">:</span><span class="s2">"GET"</span><span class="p">,</span>
  <span class="na">url</span><span class="p">:</span><span class="s2">"https://app.ticketmaster.com/discovery/v1/events/0B004F0401BD55E5/images.json?apikey={apikey}"</span><span class="p">,</span>
  <span class="na">async</span><span class="p">:</span><span class="kc">true</span><span class="p">,</span>
  <span class="na">dataType</span><span class="p">:</span> <span class="s2">"json"</span><span class="p">,</span>
  <span class="na">success</span><span class="p">:</span> <span class="kd">function</span><span class="p">(</span><span class="nx">json</span><span class="p">)</span> <span class="p">{</span>
              <span class="nx">console</span><span class="p">.</span><span class="nx">log</span><span class="p">(</span><span class="nx">json</span><span class="p">);</span>
              <span class="c1">// Parse the response.</span>
              <span class="c1">// Do other things.</span>
           <span class="p">},</span>
  <span class="na">error</span><span class="p">:</span> <span class="kd">function</span><span class="p">(</span><span class="nx">xhr</span><span class="p">,</span> <span class="nx">status</span><span class="p">,</span> <span class="nx">err</span><span class="p">)</span> <span class="p">{</span>
              <span class="c1">// This time, we do not end up here!</span>
           <span class="p">}</span>
<span class="p">});</span></code></pre></figure>

<figure class="highlight"><pre><code class="language-bash" data-lang="bash">curl <span class="se">\</span>
--include <span class="s1">'https://app.ticketmaster.com/discovery/v1/events/0B004F0401BD55E5/images.json?apikey={apikey}'</span></code></pre></figure>

<blockquote class="article reqres">
  <p><a href="#req">Request</a>
<a href="#res">Response</a></p>
</blockquote>

<figure class="highlight"><pre><code class="language-http" data-lang="http"><span class="nf">GET</span> <span class="nn">/discovery/v1/events/0B004F0401BD55E5/images.json?apikey=****</span> <span class="k">HTTP</span><span class="o">/</span><span class="m">1.1</span>
<span class="na">Host</span><span class="p">:</span> <span class="s">app.ticketmaster.com</span>
<span class="na">X-Target-URI</span><span class="p">:</span> <span class="s">https://app.ticketmaster.com</span>
<span class="na">Connection</span><span class="p">:</span> <span class="s">Keep-Alive</span></code></pre></figure>

<figure class="highlight"><pre><code class="language-http" data-lang="http"><span class="k">HTTP</span><span class="o">/</span><span class="m">1.1</span> <span class="m">200</span> <span class="ne">OK</span>
<span class="na">Content-Length</span><span class="p">:</span> <span class="s">1789</span>
<span class="na">Expires</span><span class="p">:</span> <span class="s">Tue, 01 Dec 2015 12:53:10 GMT</span>
<span class="na">Access-Control-Max-Age</span><span class="p">:</span> <span class="s">3628800</span>
<span class="na">Access-Control-Allow-Methods</span><span class="p">:</span> <span class="s">GET, PUT, POST, DELETE</span>
<span class="na">Connection</span><span class="p">:</span> <span class="s">keep-alive</span>
<span class="na">Server</span><span class="p">:</span> <span class="s">Apache-Coyote/1.1</span>
<span class="na">Cache-Control</span><span class="p">:</span> <span class="s">max-age=0, no-cache, no-store</span>
<span class="na">Pragma</span><span class="p">:</span> <span class="s">no-cache</span>
<span class="na">X-Varnish</span><span class="p">:</span> <span class="s">1715762</span>
<span class="na">Access-Control-Allow-Headers</span><span class="p">:</span> <span class="s">origin, x-requested-with, accept</span>
<span class="na">Date</span><span class="p">:</span> <span class="s">Tue, 01 Dec 2015 12:53:10 GMT</span>
<span class="na">Access-Control-Allow-Origin</span><span class="p">:</span> <span class="s">*</span>
<span class="na">X-Application-Context</span><span class="p">:</span> <span class="s">content-content-runtime-service:jash1,default:8080</span>
<span class="na">Content-Type</span><span class="p">:</span> <span class="s">application/json;charset=UTF-8</span>
<span class="na">Accept-Ranges</span><span class="p">:</span> <span class="s">bytes</span>
<span class="na">Set-Cookie</span><span class="p">:</span> <span class="s">****</span>

<span class="p">{</span><span class="w">
  </span><span class="nt">"type"</span><span class="p">:</span><span class="w"> </span><span class="s2">"event"</span><span class="p">,</span><span class="w">
  </span><span class="nt">"id"</span><span class="p">:</span><span class="w"> </span><span class="s2">"0B004F0401BD55E5"</span><span class="p">,</span><span class="w">
  </span><span class="nt">"images"</span><span class="p">:</span><span class="w">  </span><span class="p">[</span><span class="w">
     </span><span class="p">{</span><span class="w">
      </span><span class="nt">"ratio"</span><span class="p">:</span><span class="w"> </span><span class="s2">"16_9"</span><span class="p">,</span><span class="w">
      </span><span class="nt">"url"</span><span class="p">:</span><span class="w"> </span><span class="s2">"http://s1.ticketm.net/dam/a/2c3/0821e82a-6024-44ff-9a01-f850c38682c3_44411_RETINA_PORTRAIT_16_9.jpg"</span><span class="p">,</span><span class="w">
      </span><span class="nt">"width"</span><span class="p">:</span><span class="w"> </span><span class="mi">640</span><span class="p">,</span><span class="w">
      </span><span class="nt">"height"</span><span class="p">:</span><span class="w"> </span><span class="mi">360</span><span class="p">,</span><span class="w">
      </span><span class="nt">"fallback"</span><span class="p">:</span><span class="w"> </span><span class="kc">false</span><span class="w">
    </span><span class="p">},</span><span class="w">
     </span><span class="p">{</span><span class="w">
      </span><span class="nt">"ratio"</span><span class="p">:</span><span class="w"> </span><span class="s2">"16_9"</span><span class="p">,</span><span class="w">
      </span><span class="nt">"url"</span><span class="p">:</span><span class="w"> </span><span class="s2">"http://s1.ticketm.net/dam/a/2c3/0821e82a-6024-44ff-9a01-f850c38682c3_44411_RETINA_LANDSCAPE_16_9.jpg"</span><span class="p">,</span><span class="w">
      </span><span class="nt">"width"</span><span class="p">:</span><span class="w"> </span><span class="mi">1136</span><span class="p">,</span><span class="w">
      </span><span class="nt">"height"</span><span class="p">:</span><span class="w"> </span><span class="mi">639</span><span class="p">,</span><span class="w">
      </span><span class="nt">"fallback"</span><span class="p">:</span><span class="w"> </span><span class="kc">false</span><span class="w">
    </span><span class="p">},</span><span class="w">
     </span><span class="p">{</span><span class="w">
      </span><span class="nt">"ratio"</span><span class="p">:</span><span class="w"> </span><span class="s2">"16_9"</span><span class="p">,</span><span class="w">
      </span><span class="nt">"url"</span><span class="p">:</span><span class="w"> </span><span class="s2">"http://s1.ticketm.net/dam/a/2c3/0821e82a-6024-44ff-9a01-f850c38682c3_44411_TABLET_LANDSCAPE_LARGE_16_9.jpg"</span><span class="p">,</span><span class="w">
      </span><span class="nt">"width"</span><span class="p">:</span><span class="w"> </span><span class="mi">2048</span><span class="p">,</span><span class="w">
      </span><span class="nt">"height"</span><span class="p">:</span><span class="w"> </span><span class="mi">1152</span><span class="p">,</span><span class="w">
      </span><span class="nt">"fallback"</span><span class="p">:</span><span class="w"> </span><span class="kc">false</span><span class="w">
    </span><span class="p">},</span><span class="w">
     </span><span class="p">{</span><span class="w">
      </span><span class="nt">"ratio"</span><span class="p">:</span><span class="w"> </span><span class="s2">"4_3"</span><span class="p">,</span><span class="w">
      </span><span class="nt">"url"</span><span class="p">:</span><span class="w"> </span><span class="s2">"http://s1.ticketm.net/dam/a/2c3/0821e82a-6024-44ff-9a01-f850c38682c3_44411_CUSTOM.jpg"</span><span class="p">,</span><span class="w">
      </span><span class="nt">"width"</span><span class="p">:</span><span class="w"> </span><span class="mi">305</span><span class="p">,</span><span class="w">
      </span><span class="nt">"height"</span><span class="p">:</span><span class="w"> </span><span class="mi">225</span><span class="p">,</span><span class="w">
      </span><span class="nt">"fallback"</span><span class="p">:</span><span class="w"> </span><span class="kc">false</span><span class="w">
    </span><span class="p">},</span><span class="w">
     </span><span class="p">{</span><span class="w">
      </span><span class="nt">"ratio"</span><span class="p">:</span><span class="w"> </span><span class="s2">"3_2"</span><span class="p">,</span><span class="w">
      </span><span class="nt">"url"</span><span class="p">:</span><span class="w"> </span><span class="s2">"http://s1.ticketm.net/dam/a/2c3/0821e82a-6024-44ff-9a01-f850c38682c3_44411_TABLET_LANDSCAPE_3_2.jpg"</span><span class="p">,</span><span class="w">
      </span><span class="nt">"width"</span><span class="p">:</span><span class="w"> </span><span class="mi">1024</span><span class="p">,</span><span class="w">
      </span><span class="nt">"height"</span><span class="p">:</span><span class="w"> </span><span class="mi">683</span><span class="p">,</span><span class="w">
      </span><span class="nt">"fallback"</span><span class="p">:</span><span class="w"> </span><span class="kc">false</span><span class="w">
    </span><span class="p">},</span><span class="w">
     </span><span class="p">{</span><span class="w">
      </span><span class="nt">"ratio"</span><span class="p">:</span><span class="w"> </span><span class="s2">"16_9"</span><span class="p">,</span><span class="w">
      </span><span class="nt">"url"</span><span class="p">:</span><span class="w"> </span><span class="s2">"http://s1.ticketm.net/dam/a/2c3/0821e82a-6024-44ff-9a01-f850c38682c3_44411_TABLET_LANDSCAPE_16_9.jpg"</span><span class="p">,</span><span class="w">
      </span><span class="nt">"width"</span><span class="p">:</span><span class="w"> </span><span class="mi">1024</span><span class="p">,</span><span class="w">
      </span><span class="nt">"height"</span><span class="p">:</span><span class="w"> </span><span class="mi">576</span><span class="p">,</span><span class="w">
      </span><span class="nt">"fallback"</span><span class="p">:</span><span class="w"> </span><span class="kc">false</span><span class="w">
    </span><span class="p">},</span><span class="w">
     </span><span class="p">{</span><span class="w">
      </span><span class="nt">"ratio"</span><span class="p">:</span><span class="w"> </span><span class="s2">"3_2"</span><span class="p">,</span><span class="w">
      </span><span class="nt">"url"</span><span class="p">:</span><span class="w"> </span><span class="s2">"http://s1.ticketm.net/dam/a/2c3/0821e82a-6024-44ff-9a01-f850c38682c3_44411_ARTIST_PAGE_3_2.jpg"</span><span class="p">,</span><span class="w">
      </span><span class="nt">"width"</span><span class="p">:</span><span class="w"> </span><span class="mi">305</span><span class="p">,</span><span class="w">
      </span><span class="nt">"height"</span><span class="p">:</span><span class="w"> </span><span class="mi">203</span><span class="p">,</span><span class="w">
      </span><span class="nt">"fallback"</span><span class="p">:</span><span class="w"> </span><span class="kc">false</span><span class="w">
    </span><span class="p">},</span><span class="w">
     </span><span class="p">{</span><span class="w">
      </span><span class="nt">"ratio"</span><span class="p">:</span><span class="w"> </span><span class="s2">"16_9"</span><span class="p">,</span><span class="w">
      </span><span class="nt">"url"</span><span class="p">:</span><span class="w"> </span><span class="s2">"http://s1.ticketm.net/dam/a/2c3/0821e82a-6024-44ff-9a01-f850c38682c3_44411_RECOMENDATION_16_9.jpg"</span><span class="p">,</span><span class="w">
      </span><span class="nt">"width"</span><span class="p">:</span><span class="w"> </span><span class="mi">100</span><span class="p">,</span><span class="w">
      </span><span class="nt">"height"</span><span class="p">:</span><span class="w"> </span><span class="mi">56</span><span class="p">,</span><span class="w">
      </span><span class="nt">"fallback"</span><span class="p">:</span><span class="w"> </span><span class="kc">false</span><span class="w">
    </span><span class="p">},</span><span class="w">
     </span><span class="p">{</span><span class="w">
      </span><span class="nt">"ratio"</span><span class="p">:</span><span class="w"> </span><span class="s2">"3_2"</span><span class="p">,</span><span class="w">
      </span><span class="nt">"url"</span><span class="p">:</span><span class="w"> </span><span class="s2">"http://s1.ticketm.net/dam/a/2c3/0821e82a-6024-44ff-9a01-f850c38682c3_44411_RETINA_PORTRAIT_3_2.jpg"</span><span class="p">,</span><span class="w">
      </span><span class="nt">"width"</span><span class="p">:</span><span class="w"> </span><span class="mi">640</span><span class="p">,</span><span class="w">
      </span><span class="nt">"height"</span><span class="p">:</span><span class="w"> </span><span class="mi">427</span><span class="p">,</span><span class="w">
      </span><span class="nt">"fallback"</span><span class="p">:</span><span class="w"> </span><span class="kc">false</span><span class="w">
    </span><span class="p">},</span><span class="w">
     </span><span class="p">{</span><span class="w">
      </span><span class="nt">"ratio"</span><span class="p">:</span><span class="w"> </span><span class="s2">"16_9"</span><span class="p">,</span><span class="w">
      </span><span class="nt">"url"</span><span class="p">:</span><span class="w"> </span><span class="s2">"http://s1.ticketm.net/dam/a/2c3/0821e82a-6024-44ff-9a01-f850c38682c3_44411_EVENT_DETAIL_PAGE_16_9.jpg"</span><span class="p">,</span><span class="w">
      </span><span class="nt">"width"</span><span class="p">:</span><span class="w"> </span><span class="mi">205</span><span class="p">,</span><span class="w">
      </span><span class="nt">"height"</span><span class="p">:</span><span class="w"> </span><span class="mi">115</span><span class="p">,</span><span class="w">
      </span><span class="nt">"fallback"</span><span class="p">:</span><span class="w"> </span><span class="kc">false</span><span class="w">
    </span><span class="p">}</span><span class="w">
  </span><span class="p">],</span><span class="w">
  </span><span class="nt">"_links"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
    </span><span class="nt">"self"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
      </span><span class="nt">"href"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/discovery/v1/events/0B004F0401BD55E5/images.json"</span><span class="w">
    </span><span class="p">}</span><span class="w">
  </span><span class="p">}</span><span class="w">
</span><span class="p">}</span></code></pre></figure>

<h2 class="article console-link" id="search-attractions">Search Attractions</h2>

<p><strong>Method:</strong> GET.
Authentication required..
Search Attractions!</p>

<p class="code red">discovery/{version}/attractions.{format}</p>

<h3 id="url-parameters-3">URL parameters:</h3>

<table>
  <thead>
    <tr>
      <th style="text-align: left">Parameter</th>
      <th style="text-align: left">Description</th>
      <th style="text-align: left">Type</th>
      <th style="text-align: left">Default Value</th>
      <th style="text-align: left">Required</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align: left"><code class="highlighter-rouge">version</code></td>
      <td style="text-align: left">The API Version.</td>
      <td style="text-align: left">string</td>
      <td style="text-align: left">“v2”</td>
      <td style="text-align: left">Yes</td>
    </tr>
    <tr>
      <td style="text-align: left"><code class="highlighter-rouge">format</code></td>
      <td style="text-align: left">API Response Format.</td>
      <td style="text-align: left">string</td>
      <td style="text-align: left">“json”</td>
      <td style="text-align: left">Yes</td>
    </tr>
  </tbody>
</table>

<h3 id="query-parameters-2">Query parameters:</h3>

<table>
  <thead>
    <tr>
      <th style="text-align: left">Parameter</th>
      <th style="text-align: left">Description</th>
      <th style="text-align: left">Type</th>
      <th style="text-align: left">Default Value</th>
      <th style="text-align: left">Required</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align: left"><code class="highlighter-rouge">keyword</code></td>
      <td style="text-align: left">A string to search against attraction names.</td>
      <td style="text-align: left">string</td>
      <td style="text-align: left"> </td>
      <td style="text-align: left">No</td>
    </tr>
    <tr>
      <td style="text-align: left"><code class="highlighter-rouge">locale</code></td>
      <td style="text-align: left">The event locale, including country and localization. Values: “”, “en-us”, “en-gb”, “en-ca”, “es-us”, “en-mx”, “es-mx”, “en-au”, “en-nz”, “fr-fr”, “fr-ca”.</td>
      <td style="text-align: left">string</td>
      <td style="text-align: left"> </td>
      <td style="text-align: left">No</td>
    </tr>
    <tr>
      <td style="text-align: left"><code class="highlighter-rouge">size</code></td>
      <td style="text-align: left">The number of events returned in the API response.</td>
      <td style="text-align: left">string</td>
      <td style="text-align: left">“20”</td>
      <td style="text-align: left">No</td>
    </tr>
    <tr>
      <td style="text-align: left"><code class="highlighter-rouge">page</code></td>
      <td style="text-align: left">The page for paginating through the results.</td>
      <td style="text-align: left">string</td>
      <td style="text-align: left">“1”</td>
      <td style="text-align: left">No</td>
    </tr>
    <tr>
      <td style="text-align: left"><code class="highlighter-rouge">sort</code></td>
      <td style="text-align: left">The search sort criteria. Values: 'name,asc', 'name,desc'.</td>
      <td style="text-align: left">string</td>
      <td style="text-align: left"> </td>
      <td style="text-align: left">No</td>
    </tr>
  </tbody>
</table>

<h3 id="response-structure-3">Response structure:</h3>

<ul class="nested-list">
  <li><code class="highlighter-rouge">_embedded</code> (object) - container attractions.
    <ul>
      <li><code class="highlighter-rouge">attractions</code> (array) - attractions.
        <ul>
          <li><code class="highlighter-rouge"><span class="p">{</span><span class="err">array</span><span class="w"> </span><span class="err">item</span><span class="w"> </span><span class="err">object</span><span class="p">}</span></code> - attraction.
            <ul>
              <li><code class="highlighter-rouge">id</code> (string) - id of attraction.</li>
              <li><code class="highlighter-rouge">type</code> (string) - type of attraction.</li>
              <li><code class="highlighter-rouge">url</code> (string) - url to attraction.</li>
              <li><code class="highlighter-rouge">name</code> (string) - name of attraction.</li>
              <li><code class="highlighter-rouge">locale</code> (string) - locale of attraction.</li>
              <li><code class="highlighter-rouge">image</code> (object) - image for attraction.
                <ul>
                  <li><code class="highlighter-rouge">url</code> (string) - url to attraction image.</li>
                </ul>
              </li>
              <li><code class="highlighter-rouge">_links</code> (object) - links to attractions.
                <ul>
                  <li><code class="highlighter-rouge">self</code> (object) - link to this attraction.
                    <ul>
                      <li><code class="highlighter-rouge">href</code> (string) - reference.</li>
                    </ul>
                  </li>
                </ul>
              </li>
            </ul>
          </li>
        </ul>
      </li>
    </ul>
  </li>
  <li><code class="highlighter-rouge">_links</code> (object) - links to attractions data set.
    <ul>
      <li><code class="highlighter-rouge">self</code> (object) - link to this data set.
        <ul>
          <li><code class="highlighter-rouge">href</code> (string) - reference.</li>
          <li><code class="highlighter-rouge">templated</code> (boolean) - is templated.</li>
        </ul>
      </li>
      <li><code class="highlighter-rouge">next</code> (object) - link to the next data set.
        <ul>
          <li><code class="highlighter-rouge">href</code> (string) - reference.</li>
          <li><code class="highlighter-rouge">templated</code> (boolean) - is templated.</li>
        </ul>
      </li>
      <li><code class="highlighter-rouge">next</code> (object) - link to the next attraction.</li>
    </ul>
  </li>
  <li><code class="highlighter-rouge">page</code> (object) - information about current page in data source.
    <ul>
      <li><code class="highlighter-rouge">size</code> (number) - size of page.</li>
      <li><code class="highlighter-rouge">totalElements</code> (number) - total number of available elements in server.</li>
      <li><code class="highlighter-rouge">totalPages</code> (number) - total number of available pages in server.</li>
      <li><code class="highlighter-rouge">number</code> (number) - current page number counted from 0.</li>
    </ul>
  </li>
</ul>

<blockquote class="aside lang-selector">
  <p><a href="#js">JavaScript</a>
<a href="#curl">cURL</a></p>
</blockquote>

<figure class="highlight"><pre><code class="language-js" data-lang="js"><span class="nx">$</span><span class="p">.</span><span class="nx">ajax</span><span class="p">({</span>
  <span class="na">type</span><span class="p">:</span><span class="s2">"GET"</span><span class="p">,</span>
  <span class="na">url</span><span class="p">:</span><span class="s2">"https://app.ticketmaster.com/discovery/v1/attractions.json?apikey={apikey}"</span><span class="p">,</span>
  <span class="na">async</span><span class="p">:</span><span class="kc">true</span><span class="p">,</span>
  <span class="na">dataType</span><span class="p">:</span> <span class="s2">"json"</span><span class="p">,</span>
  <span class="na">success</span><span class="p">:</span> <span class="kd">function</span><span class="p">(</span><span class="nx">json</span><span class="p">)</span> <span class="p">{</span>
              <span class="nx">console</span><span class="p">.</span><span class="nx">log</span><span class="p">(</span><span class="nx">json</span><span class="p">);</span>
              <span class="c1">// Parse the response.</span>
              <span class="c1">// Do other things.</span>
           <span class="p">},</span>
  <span class="na">error</span><span class="p">:</span> <span class="kd">function</span><span class="p">(</span><span class="nx">xhr</span><span class="p">,</span> <span class="nx">status</span><span class="p">,</span> <span class="nx">err</span><span class="p">)</span> <span class="p">{</span>
              <span class="c1">// This time, we do not end up here!</span>
           <span class="p">}</span>
<span class="p">});</span></code></pre></figure>

<figure class="highlight"><pre><code class="language-bash" data-lang="bash">curl <span class="se">\</span>
--include <span class="s1">'https://app.ticketmaster.com/discovery/v1/attractions.json?apikey={apikey}'</span></code></pre></figure>

<blockquote class="article reqres">
  <p><a href="#req">Request</a>
<a href="#res">Response</a></p>
</blockquote>

<figure class="highlight"><pre><code class="language-http" data-lang="http"><span class="nf">GET</span> <span class="nn">/discovery/v1/attractions.json?apikey=****</span> <span class="k">HTTP</span><span class="o">/</span><span class="m">1.1</span>
<span class="na">Host</span><span class="p">:</span> <span class="s">app.ticketmaster.com</span>
<span class="na">X-Target-URI</span><span class="p">:</span> <span class="s">https://app.ticketmaster.com</span>
<span class="na">Connection</span><span class="p">:</span> <span class="s">Keep-Alive</span></code></pre></figure>

<figure class="highlight"><pre><code class="language-http" data-lang="http"><span class="k">HTTP</span><span class="o">/</span><span class="m">1.1</span> <span class="m">200</span> <span class="ne">OK</span>
<span class="na">Access-Control-Allow-Headers</span><span class="p">:</span> <span class="s">origin, x-requested-with, accept</span>
<span class="na">Access-Control-Allow-Origin</span><span class="p">:</span> <span class="s">*</span>
<span class="na">Date</span><span class="p">:</span> <span class="s">Tue, 01 Dec 2015 12:55:01 GMT</span>
<span class="na">Content-Length</span><span class="p">:</span> <span class="s">7606</span>
<span class="na">Access-Control-Max-Age</span><span class="p">:</span> <span class="s">3628800</span>
<span class="na">Access-Control-Allow-Methods</span><span class="p">:</span> <span class="s">GET, PUT, POST, DELETE</span>
<span class="na">X-Application-Context</span><span class="p">:</span> <span class="s">application:default,jetson4</span>
<span class="na">Connection</span><span class="p">:</span> <span class="s">keep-alive</span>
<span class="na">Content-Type</span><span class="p">:</span> <span class="s">application/json;charset=utf-8</span>
<span class="na">Server</span><span class="p">:</span> <span class="s">Apache-Coyote/1.1</span>
<span class="na">Set-Cookie</span><span class="p">:</span> <span class="s">****</span>

<span class="p">{</span><span class="w">
  </span><span class="nt">"_links"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
    </span><span class="nt">"self"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
      </span><span class="nt">"href"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/discovery/v1/attractions.json {?page,size,sort}"</span><span class="p">,</span><span class="w">
      </span><span class="nt">"templated"</span><span class="p">:</span><span class="w"> </span><span class="kc">true</span><span class="w">
    </span><span class="p">},</span><span class="w">
    </span><span class="nt">"next"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
      </span><span class="nt">"href"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/discovery/v1/attractions.json?page=1&amp;size=20 {&amp;sort}"</span><span class="p">,</span><span class="w">
      </span><span class="nt">"templated"</span><span class="p">:</span><span class="w"> </span><span class="kc">true</span><span class="w">
    </span><span class="p">}</span><span class="w">
  </span><span class="p">},</span><span class="w">
  </span><span class="nt">"_embedded"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
    </span><span class="nt">"attractions"</span><span class="p">:</span><span class="w">  </span><span class="p">[</span><span class="w">
       </span><span class="p">{</span><span class="w">
        </span><span class="nt">"url"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/artist/919340"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"image"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
          </span><span class="nt">"url"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/dam/a/418/aa73b994-9912-4535-ba21-4865ae93a418_41291_EVENT_DETAIL_PAGE_16_9.jpg"</span><span class="w">
        </span><span class="p">},</span><span class="w">
        </span><span class="nt">"name"</span><span class="p">:</span><span class="w"> </span><span class="s2">"!!!"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"locale"</span><span class="p">:</span><span class="w"> </span><span class="s2">"en-us"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"_links"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
          </span><span class="nt">"self"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
            </span><span class="nt">"href"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/discovery/v1/attractions/919340?locale=en-us&amp;domain=ticketmaster.com"</span><span class="w">
          </span><span class="p">}</span><span class="w">
        </span><span class="p">},</span><span class="w">
        </span><span class="nt">"id"</span><span class="p">:</span><span class="w"> </span><span class="s2">"919340"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"type"</span><span class="p">:</span><span class="w"> </span><span class="s2">"attraction"</span><span class="w">
      </span><span class="p">},</span><span class="w">
       </span><span class="p">{</span><span class="w">
        </span><span class="nt">"url"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/TEST-EVENT-NOT-FOR-SALE-tickets/artist/2188271"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"name"</span><span class="p">:</span><span class="w"> </span><span class="s2">"!!!! TEST EVENT. NOT FOR SALE. PURCHASES WILL BE VOIDED !!!!"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"locale"</span><span class="p">:</span><span class="w"> </span><span class="s2">"en-us"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"_links"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
          </span><span class="nt">"self"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
            </span><span class="nt">"href"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/discovery/v1/attractions/2188271?locale=en-us&amp;domain=ticketmaster.com"</span><span class="w">
          </span><span class="p">}</span><span class="w">
        </span><span class="p">},</span><span class="w">
        </span><span class="nt">"id"</span><span class="p">:</span><span class="w"> </span><span class="s2">"2188271"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"type"</span><span class="p">:</span><span class="w"> </span><span class="s2">"attraction"</span><span class="w">
      </span><span class="p">},</span><span class="w">
       </span><span class="p">{</span><span class="w">
        </span><span class="nt">"url"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/Hero-tickets/artist/883184"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"name"</span><span class="p">:</span><span class="w"> </span><span class="s2">"!Hero"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"locale"</span><span class="p">:</span><span class="w"> </span><span class="s2">"en-us"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"_links"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
          </span><span class="nt">"self"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
            </span><span class="nt">"href"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/discovery/v1/attractions/883184?locale=en-us&amp;domain=ticketmaster.com"</span><span class="w">
          </span><span class="p">}</span><span class="w">
        </span><span class="p">},</span><span class="w">
        </span><span class="nt">"id"</span><span class="p">:</span><span class="w"> </span><span class="s2">"883184"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"type"</span><span class="p">:</span><span class="w"> </span><span class="s2">"attraction"</span><span class="w">
      </span><span class="p">},</span><span class="w">
       </span><span class="p">{</span><span class="w">
        </span><span class="nt">"url"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/Tang-tickets/artist/1673094"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"name"</span><span class="p">:</span><span class="w"> </span><span class="s2">"!Tang"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"locale"</span><span class="p">:</span><span class="w"> </span><span class="s2">"en-us"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"_links"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
          </span><span class="nt">"self"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
            </span><span class="nt">"href"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/discovery/v1/attractions/1673094?locale=en-us&amp;domain=ticketmaster.com"</span><span class="w">
          </span><span class="p">}</span><span class="w">
        </span><span class="p">},</span><span class="w">
        </span><span class="nt">"id"</span><span class="p">:</span><span class="w"> </span><span class="s2">"1673094"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"type"</span><span class="p">:</span><span class="w"> </span><span class="s2">"attraction"</span><span class="w">
      </span><span class="p">},</span><span class="w">
       </span><span class="p">{</span><span class="w">
        </span><span class="nt">"url"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/Women-Art-Revolution-tickets/artist/1643423"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"name"</span><span class="p">:</span><span class="w"> </span><span class="s2">"!Women Art Revolution"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"locale"</span><span class="p">:</span><span class="w"> </span><span class="s2">"en-us"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"_links"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
          </span><span class="nt">"self"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
            </span><span class="nt">"href"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/discovery/v1/attractions/1643423?locale=en-us&amp;domain=ticketmaster.com"</span><span class="w">
          </span><span class="p">}</span><span class="w">
        </span><span class="p">},</span><span class="w">
        </span><span class="nt">"id"</span><span class="p">:</span><span class="w"> </span><span class="s2">"1643423"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"type"</span><span class="p">:</span><span class="w"> </span><span class="s2">"attraction"</span><span class="w">
      </span><span class="p">},</span><span class="w">
       </span><span class="p">{</span><span class="w">
        </span><span class="nt">"url"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/A-Choral-Holiday-tickets/artist/2178282"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"name"</span><span class="p">:</span><span class="w"> </span><span class="s2">""</span><span class="err">A</span><span class="w"> </span><span class="err">Choral</span><span class="w"> </span><span class="err">Holiday</span><span class="s2">""</span><span class="p">,</span><span class="w">
        </span><span class="nt">"locale"</span><span class="p">:</span><span class="w"> </span><span class="s2">"en-us"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"_links"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
          </span><span class="nt">"self"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
            </span><span class="nt">"href"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/discovery/v1/attractions/2178282?locale=en-us&amp;domain=ticketmaster.com"</span><span class="w">
          </span><span class="p">}</span><span class="w">
        </span><span class="p">},</span><span class="w">
        </span><span class="nt">"id"</span><span class="p">:</span><span class="w"> </span><span class="s2">"2178282"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"type"</span><span class="p">:</span><span class="w"> </span><span class="s2">"attraction"</span><span class="w">
      </span><span class="p">},</span><span class="w">
       </span><span class="p">{</span><span class="w">
        </span><span class="nt">"url"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/A-John-Denver-Christmas-Tribute-tickets/artist/2163030"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"name"</span><span class="p">:</span><span class="w"> </span><span class="s2">""</span><span class="err">A</span><span class="w"> </span><span class="err">John</span><span class="w"> </span><span class="err">Denver</span><span class="w"> </span><span class="err">Christmas</span><span class="w"> </span><span class="err">Tribute</span><span class="s2">" - Chris Collins &amp; Boulder Canyon"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"locale"</span><span class="p">:</span><span class="w"> </span><span class="s2">"en-us"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"_links"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
          </span><span class="nt">"self"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
            </span><span class="nt">"href"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/discovery/v1/attractions/2163030?locale=en-us&amp;domain=ticketmaster.com"</span><span class="w">
          </span><span class="p">}</span><span class="w">
        </span><span class="p">},</span><span class="w">
        </span><span class="nt">"id"</span><span class="p">:</span><span class="w"> </span><span class="s2">"2163030"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"type"</span><span class="p">:</span><span class="w"> </span><span class="s2">"attraction"</span><span class="w">
      </span><span class="p">},</span><span class="w">
       </span><span class="p">{</span><span class="w">
        </span><span class="nt">"url"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/A-Vivir-Con-Odin-Dupeyron-tickets/artist/2130498"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"image"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
          </span><span class="nt">"url"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/dbimages/212397a.jpg"</span><span class="w">
        </span><span class="p">},</span><span class="w">
        </span><span class="nt">"name"</span><span class="p">:</span><span class="w"> </span><span class="s2">""</span><span class="err">A</span><span class="w"> </span><span class="err">Vivir</span><span class="s2">" Con Odin Dupeyron"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"locale"</span><span class="p">:</span><span class="w"> </span><span class="s2">"en-us"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"_links"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
          </span><span class="nt">"self"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
            </span><span class="nt">"href"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/discovery/v1/attractions/2130498?locale=en-us&amp;domain=ticketmaster.com"</span><span class="w">
          </span><span class="p">}</span><span class="w">
        </span><span class="p">},</span><span class="w">
        </span><span class="nt">"id"</span><span class="p">:</span><span class="w"> </span><span class="s2">"2130498"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"type"</span><span class="p">:</span><span class="w"> </span><span class="s2">"attraction"</span><span class="w">
      </span><span class="p">},</span><span class="w">
       </span><span class="p">{</span><span class="w">
        </span><span class="nt">"url"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/A-Sides-tickets/artist/759799"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"name"</span><span class="p">:</span><span class="w"> </span><span class="s2">""</span><span class="err">A</span><span class="s2">" Sides"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"locale"</span><span class="p">:</span><span class="w"> </span><span class="s2">"en-us"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"_links"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
          </span><span class="nt">"self"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
            </span><span class="nt">"href"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/discovery/v1/attractions/759799?locale=en-us&amp;domain=ticketmaster.com"</span><span class="w">
          </span><span class="p">}</span><span class="w">
        </span><span class="p">},</span><span class="w">
        </span><span class="nt">"id"</span><span class="p">:</span><span class="w"> </span><span class="s2">"759799"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"type"</span><span class="p">:</span><span class="w"> </span><span class="s2">"attraction"</span><span class="w">
      </span><span class="p">},</span><span class="w">
       </span><span class="p">{</span><span class="w">
        </span><span class="nt">"url"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/BLUE-MAN-GROUP-tickets/artist/2168522"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"name"</span><span class="p">:</span><span class="w"> </span><span class="s2">""</span><span class="err">BLUE</span><span class="w"> </span><span class="err">MAN</span><span class="w"> </span><span class="err">GROUP</span><span class="s2">""</span><span class="p">,</span><span class="w">
        </span><span class="nt">"locale"</span><span class="p">:</span><span class="w"> </span><span class="s2">"en-us"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"_links"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
          </span><span class="nt">"self"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
            </span><span class="nt">"href"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/discovery/v1/attractions/2168522?locale=en-us&amp;domain=ticketmaster.com"</span><span class="w">
          </span><span class="p">}</span><span class="w">
        </span><span class="p">},</span><span class="w">
        </span><span class="nt">"id"</span><span class="p">:</span><span class="w"> </span><span class="s2">"2168522"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"type"</span><span class="p">:</span><span class="w"> </span><span class="s2">"attraction"</span><span class="w">
      </span><span class="p">},</span><span class="w">
       </span><span class="p">{</span><span class="w">
        </span><span class="nt">"url"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/Dee-tickets/artist/767040"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"name"</span><span class="p">:</span><span class="w"> </span><span class="s2">""</span><span class="err">Dee</span><span class="s2">""</span><span class="p">,</span><span class="w">
        </span><span class="nt">"locale"</span><span class="p">:</span><span class="w"> </span><span class="s2">"en-us"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"_links"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
          </span><span class="nt">"self"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
            </span><span class="nt">"href"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/discovery/v1/attractions/767040?locale=en-us&amp;domain=ticketmaster.com"</span><span class="w">
          </span><span class="p">}</span><span class="w">
        </span><span class="p">},</span><span class="w">
        </span><span class="nt">"id"</span><span class="p">:</span><span class="w"> </span><span class="s2">"767040"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"type"</span><span class="p">:</span><span class="w"> </span><span class="s2">"attraction"</span><span class="w">
      </span><span class="p">},</span><span class="w">
       </span><span class="p">{</span><span class="w">
        </span><span class="nt">"url"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/El-Cascanueces-Ballet-Ruso-de-Samara-tickets/artist/2182975"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"name"</span><span class="p">:</span><span class="w"> </span><span class="s2">""</span><span class="err">El</span><span class="w"> </span><span class="err">Cascanueces</span><span class="s2">" Ballet Ruso de Samara"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"locale"</span><span class="p">:</span><span class="w"> </span><span class="s2">"en-us"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"_links"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
          </span><span class="nt">"self"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
            </span><span class="nt">"href"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/discovery/v1/attractions/2182975?locale=en-us&amp;domain=ticketmaster.com"</span><span class="w">
          </span><span class="p">}</span><span class="w">
        </span><span class="p">},</span><span class="w">
        </span><span class="nt">"id"</span><span class="p">:</span><span class="w"> </span><span class="s2">"2182975"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"type"</span><span class="p">:</span><span class="w"> </span><span class="s2">"attraction"</span><span class="w">
      </span><span class="p">},</span><span class="w">
       </span><span class="p">{</span><span class="w">
        </span><span class="nt">"url"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/Givin-the-Dog-a-Bone-KY-tickets/artist/2174785"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"name"</span><span class="p">:</span><span class="w"> </span><span class="s2">""</span><span class="err">Givin'</span><span class="w"> </span><span class="err">the</span><span class="w"> </span><span class="err">Dog</span><span class="w"> </span><span class="err">a</span><span class="w"> </span><span class="err">Bone</span><span class="s2">" KY Humane Society benefit feat. Thunderstruck"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"locale"</span><span class="p">:</span><span class="w"> </span><span class="s2">"en-us"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"_links"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
          </span><span class="nt">"self"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
            </span><span class="nt">"href"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/discovery/v1/attractions/2174785?locale=en-us&amp;domain=ticketmaster.com"</span><span class="w">
          </span><span class="p">}</span><span class="w">
        </span><span class="p">},</span><span class="w">
        </span><span class="nt">"id"</span><span class="p">:</span><span class="w"> </span><span class="s2">"2174785"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"type"</span><span class="p">:</span><span class="w"> </span><span class="s2">"attraction"</span><span class="w">
      </span><span class="p">},</span><span class="w">
       </span><span class="p">{</span><span class="w">
        </span><span class="nt">"url"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/I-FEEL-GOOD-THE-JAMES-BROWN-tickets/artist/2083045"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"name"</span><span class="p">:</span><span class="w"> </span><span class="s2">""</span><span class="err">I</span><span class="w"> </span><span class="err">FEEL</span><span class="w"> </span><span class="err">GOOD</span><span class="s2">" THE JAMES BROWN STORY"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"locale"</span><span class="p">:</span><span class="w"> </span><span class="s2">"en-us"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"_links"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
          </span><span class="nt">"self"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
            </span><span class="nt">"href"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/discovery/v1/attractions/2083045?locale=en-us&amp;domain=ticketmaster.com"</span><span class="w">
          </span><span class="p">}</span><span class="w">
        </span><span class="p">},</span><span class="w">
        </span><span class="nt">"id"</span><span class="p">:</span><span class="w"> </span><span class="s2">"2083045"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"type"</span><span class="p">:</span><span class="w"> </span><span class="s2">"attraction"</span><span class="w">
      </span><span class="p">},</span><span class="w">
       </span><span class="p">{</span><span class="w">
        </span><span class="nt">"url"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/Its-a-Wonderful-Life-with-ZuzuA-tickets/artist/2154063"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"name"</span><span class="p">:</span><span class="w"> </span><span class="s2">""</span><span class="err">It's</span><span class="w"> </span><span class="err">a</span><span class="w"> </span><span class="err">Wonderful</span><span class="w"> </span><span class="err">Life</span><span class="w"> </span><span class="err">with</span><span class="w"> </span><span class="err">Zuzu</span><span class="s2">"-A Conversation with Karolyn Grimes"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"locale"</span><span class="p">:</span><span class="w"> </span><span class="s2">"en-us"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"_links"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
          </span><span class="nt">"self"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
            </span><span class="nt">"href"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/discovery/v1/attractions/2154063?locale=en-us&amp;domain=ticketmaster.com"</span><span class="w">
          </span><span class="p">}</span><span class="w">
        </span><span class="p">},</span><span class="w">
        </span><span class="nt">"id"</span><span class="p">:</span><span class="w"> </span><span class="s2">"2154063"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"type"</span><span class="p">:</span><span class="w"> </span><span class="s2">"attraction"</span><span class="w">
      </span><span class="p">},</span><span class="w">
       </span><span class="p">{</span><span class="w">
        </span><span class="nt">"url"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/LOVE-With-Andrey-Makarevich-tickets/artist/2170300"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"name"</span><span class="p">:</span><span class="w"> </span><span class="s2">""</span><span class="err">L.O.V.E.</span><span class="s2">" With Andrey Makarevich"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"locale"</span><span class="p">:</span><span class="w"> </span><span class="s2">"en-us"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"_links"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
          </span><span class="nt">"self"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
            </span><span class="nt">"href"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/discovery/v1/attractions/2170300?locale=en-us&amp;domain=ticketmaster.com"</span><span class="w">
          </span><span class="p">}</span><span class="w">
        </span><span class="p">},</span><span class="w">
        </span><span class="nt">"id"</span><span class="p">:</span><span class="w"> </span><span class="s2">"2170300"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"type"</span><span class="p">:</span><span class="w"> </span><span class="s2">"attraction"</span><span class="w">
      </span><span class="p">},</span><span class="w">
       </span><span class="p">{</span><span class="w">
        </span><span class="nt">"url"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/La-Reina-de-las-Nieves-Ballet-tickets/artist/2175716"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"name"</span><span class="p">:</span><span class="w"> </span><span class="s2">""</span><span class="err">La</span><span class="w"> </span><span class="err">Reina</span><span class="w"> </span><span class="err">de</span><span class="w"> </span><span class="err">las</span><span class="w"> </span><span class="err">Nieves</span><span class="s2">" Ballet Circo de Moscú"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"locale"</span><span class="p">:</span><span class="w"> </span><span class="s2">"en-us"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"_links"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
          </span><span class="nt">"self"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
            </span><span class="nt">"href"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/discovery/v1/attractions/2175716?locale=en-us&amp;domain=ticketmaster.com"</span><span class="w">
          </span><span class="p">}</span><span class="w">
        </span><span class="p">},</span><span class="w">
        </span><span class="nt">"id"</span><span class="p">:</span><span class="w"> </span><span class="s2">"2175716"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"type"</span><span class="p">:</span><span class="w"> </span><span class="s2">"attraction"</span><span class="w">
      </span><span class="p">},</span><span class="w">
       </span><span class="p">{</span><span class="w">
        </span><span class="nt">"url"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/Ladies-in-Love-A-Valentines-tickets/artist/2164933"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"name"</span><span class="p">:</span><span class="w"> </span><span class="s2">""</span><span class="err">Ladies</span><span class="w"> </span><span class="err">in</span><span class="w"> </span><span class="err">Love</span><span class="s2">" - A Valentine's Day Affair feat. SHERMA ANDREWS"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"locale"</span><span class="p">:</span><span class="w"> </span><span class="s2">"en-us"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"_links"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
          </span><span class="nt">"self"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
            </span><span class="nt">"href"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/discovery/v1/attractions/2164933?locale=en-us&amp;domain=ticketmaster.com"</span><span class="w">
          </span><span class="p">}</span><span class="w">
        </span><span class="p">},</span><span class="w">
        </span><span class="nt">"id"</span><span class="p">:</span><span class="w"> </span><span class="s2">"2164933"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"type"</span><span class="p">:</span><span class="w"> </span><span class="s2">"attraction"</span><span class="w">
      </span><span class="p">},</span><span class="w">
       </span><span class="p">{</span><span class="w">
        </span><span class="nt">"url"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/Mentiras-El-Musical-tickets/artist/1537157"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"name"</span><span class="p">:</span><span class="w"> </span><span class="s2">""</span><span class="err">Mentiras</span><span class="s2">" El Musical"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"locale"</span><span class="p">:</span><span class="w"> </span><span class="s2">"en-us"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"_links"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
          </span><span class="nt">"self"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
            </span><span class="nt">"href"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/discovery/v1/attractions/1537157?locale=en-us&amp;domain=ticketmaster.com"</span><span class="w">
          </span><span class="p">}</span><span class="w">
        </span><span class="p">},</span><span class="w">
        </span><span class="nt">"id"</span><span class="p">:</span><span class="w"> </span><span class="s2">"1537157"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"type"</span><span class="p">:</span><span class="w"> </span><span class="s2">"attraction"</span><span class="w">
      </span><span class="p">},</span><span class="w">
       </span><span class="p">{</span><span class="w">
        </span><span class="nt">"url"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/My-Spirit-Animal-is-A-Butch-tickets/artist/2140956"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"name"</span><span class="p">:</span><span class="w"> </span><span class="s2">""</span><span class="err">My</span><span class="w"> </span><span class="err">Spirit</span><span class="w"> </span><span class="err">Animal</span><span class="w"> </span><span class="err">is</span><span class="w"> </span><span class="err">A</span><span class="w"> </span><span class="err">Butch</span><span class="w"> </span><span class="err">Lesbian</span><span class="s2">" featuring Sampson"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"locale"</span><span class="p">:</span><span class="w"> </span><span class="s2">"en-us"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"_links"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
          </span><span class="nt">"self"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
            </span><span class="nt">"href"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/discovery/v1/attractions/2140956?locale=en-us&amp;domain=ticketmaster.com"</span><span class="w">
          </span><span class="p">}</span><span class="w">
        </span><span class="p">},</span><span class="w">
        </span><span class="nt">"id"</span><span class="p">:</span><span class="w"> </span><span class="s2">"2140956"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"type"</span><span class="p">:</span><span class="w"> </span><span class="s2">"attraction"</span><span class="w">
      </span><span class="p">}</span><span class="w">
    </span><span class="p">]</span><span class="w">
  </span><span class="p">},</span><span class="w">
  </span><span class="nt">"page"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
    </span><span class="nt">"size"</span><span class="p">:</span><span class="w"> </span><span class="mi">20</span><span class="p">,</span><span class="w">
    </span><span class="nt">"totalElements"</span><span class="p">:</span><span class="w"> </span><span class="mi">257006</span><span class="p">,</span><span class="w">
    </span><span class="nt">"totalPages"</span><span class="p">:</span><span class="w"> </span><span class="mi">12851</span><span class="p">,</span><span class="w">
    </span><span class="nt">"number"</span><span class="p">:</span><span class="w"> </span><span class="mi">0</span><span class="w">
  </span><span class="p">}</span><span class="w">
</span><span class="p">}</span><span class="w">
</span><span class="err">}</span></code></pre></figure>

<h2 class="article console-link" id="attraction-details">Get Attraction Details</h2>

<p><strong>Method:</strong> GET.
Authentication required.
Search Attractions!</p>

<p class="code red">discovery/{version}/attractions/{id}.{format}</p>

<h3 id="url-parameters-4">URL parameters:</h3>

<table>
  <thead>
    <tr>
      <th style="text-align: left">Parameter</th>
      <th style="text-align: left">Description</th>
      <th style="text-align: left">Type</th>
      <th style="text-align: left">Default Value</th>
      <th style="text-align: left">Required</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align: left"><code class="highlighter-rouge">version</code></td>
      <td style="text-align: left">The API Version.</td>
      <td style="text-align: left">string</td>
      <td style="text-align: left">“v2”</td>
      <td style="text-align: left">Yes</td>
    </tr>
    <tr>
      <td style="text-align: left"><code class="highlighter-rouge">id</code></td>
      <td style="text-align: left">Attraction ID.</td>
      <td style="text-align: left">string</td>
      <td style="text-align: left">“K8vZ917G7x0”</td>
      <td style="text-align: left">Yes</td>
    </tr>
    <tr>
      <td style="text-align: left"><code class="highlighter-rouge">format</code></td>
      <td style="text-align: left">API Response Format.</td>
      <td style="text-align: left">string</td>
      <td style="text-align: left">“json”</td>
      <td style="text-align: left">Yes</td>
    </tr>
  </tbody>
</table>

<h3 id="query-parameters-3">Query parameters:</h3>

<table>
  <thead>
    <tr>
      <th style="text-align: left">Parameter</th>
      <th style="text-align: left">Description</th>
      <th style="text-align: left">Type</th>
      <th style="text-align: left">Default Value</th>
      <th style="text-align: left">Required</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align: left"><code class="highlighter-rouge">locale</code></td>
      <td style="text-align: left">The event locale, including country and localization. Values: “”, “en-us”, “en-gb”, “en-ca”, “es-us”, “en-mx”, “es-mx”, “en-au”, “en-nz”, “fr-fr”, “fr-ca”.</td>
      <td style="text-align: left">string</td>
      <td style="text-align: left"> </td>
      <td style="text-align: left">No</td>
    </tr>
  </tbody>
</table>

<h3 id="response-structure-4">Response structure:</h3>

<ul class="nested-list">
  <li><code class="highlighter-rouge">url</code> (string) - url to attraction.</li>
  <li><code class="highlighter-rouge">name</code> (string) - name of attraction.</li>
  <li><code class="highlighter-rouge">locale</code> (string) - locale of attraction.</li>
  <li><code class="highlighter-rouge">image</code> (object) - image for attraction.
    <ul>
      <li><code class="highlighter-rouge">url</code> (string) - url to image.</li>
    </ul>
  </li>
  <li><code class="highlighter-rouge">_links</code> (object) - links to attractions.
    <ul>
      <li><code class="highlighter-rouge">self</code> (object) - link to this attraction.
        <ul>
          <li><code class="highlighter-rouge">href</code> (string) - reference.</li>
        </ul>
      </li>
    </ul>
  </li>
  <li><code class="highlighter-rouge">id</code> (string) - id of attraction.</li>
  <li><code class="highlighter-rouge">type</code> (string) - type of attraction.</li>
</ul>

<blockquote class="aside lang-selector">
  <p><a href="#js">JavaScript</a>
<a href="#curl">cURL</a></p>
</blockquote>

<figure class="highlight"><pre><code class="language-js" data-lang="js"><span class="nx">$</span><span class="p">.</span><span class="nx">ajax</span><span class="p">({</span>
  <span class="na">type</span><span class="p">:</span><span class="s2">"GET"</span><span class="p">,</span>
  <span class="na">url</span><span class="p">:</span><span class="s2">"https://app.ticketmaster.com/discovery/v1/attractions/768011.json?apikey={apikey}"</span><span class="p">,</span>
  <span class="na">async</span><span class="p">:</span><span class="kc">true</span><span class="p">,</span>
  <span class="na">dataType</span><span class="p">:</span> <span class="s2">"json"</span><span class="p">,</span>
  <span class="na">success</span><span class="p">:</span> <span class="kd">function</span><span class="p">(</span><span class="nx">json</span><span class="p">)</span> <span class="p">{</span>
              <span class="nx">console</span><span class="p">.</span><span class="nx">log</span><span class="p">(</span><span class="nx">json</span><span class="p">);</span>
              <span class="c1">// Parse the response.</span>
              <span class="c1">// Do other things.</span>
           <span class="p">},</span>
  <span class="na">error</span><span class="p">:</span> <span class="kd">function</span><span class="p">(</span><span class="nx">xhr</span><span class="p">,</span> <span class="nx">status</span><span class="p">,</span> <span class="nx">err</span><span class="p">)</span> <span class="p">{</span>
              <span class="c1">// This time, we do not end up here!</span>
           <span class="p">}</span>
<span class="p">});</span></code></pre></figure>

<figure class="highlight"><pre><code class="language-bash" data-lang="bash">curl <span class="se">\</span>
--include <span class="s1">'https://app.ticketmaster.com/discovery/v1/attractions/768011.json?apikey={apikey}'</span></code></pre></figure>

<blockquote class="article reqres">
  <p><a href="#req">Request</a>
<a href="#res">Response</a></p>
</blockquote>

<figure class="highlight"><pre><code class="language-http" data-lang="http"><span class="nf">GET</span> <span class="nn">/discovery/v1/attractions/768011.json?apikey=****</span> <span class="k">HTTP</span><span class="o">/</span><span class="m">1.1</span>
<span class="na">Host</span><span class="p">:</span> <span class="s">app.ticketmaster.com</span>
<span class="na">X-Target-URI</span><span class="p">:</span> <span class="s">https://app.ticketmaster.com</span>
<span class="na">Connection</span><span class="p">:</span> <span class="s">Keep-Alive</span></code></pre></figure>

<figure class="highlight"><pre><code class="language-http" data-lang="http"><span class="k">HTTP</span><span class="o">/</span><span class="m">1.1</span> <span class="m">200</span> <span class="ne">OK</span>
<span class="na">Access-Control-Allow-Headers</span><span class="p">:</span> <span class="s">origin, x-requested-with, accept</span>
<span class="na">Access-Control-Allow-Origin</span><span class="p">:</span> <span class="s">*</span>
<span class="na">Date</span><span class="p">:</span> <span class="s">Tue, 01 Dec 2015 12:58:55 GMT</span>
<span class="na">Content-Length</span><span class="p">:</span> <span class="s">445</span>
<span class="na">Access-Control-Max-Age</span><span class="p">:</span> <span class="s">3628800</span>
<span class="na">Access-Control-Allow-Methods</span><span class="p">:</span> <span class="s">GET, PUT, POST, DELETE</span>
<span class="na">X-Application-Context</span><span class="p">:</span> <span class="s">application:default,jetson4</span>
<span class="na">Connection</span><span class="p">:</span> <span class="s">keep-alive</span>
<span class="na">Content-Type</span><span class="p">:</span> <span class="s">application/json;charset=utf-8</span>
<span class="na">Server</span><span class="p">:</span> <span class="s">Apache-Coyote/1.1</span>
<span class="na">Set-Cookie</span><span class="p">:</span> <span class="s">****</span>

<span class="p">{</span><span class="w">
  </span><span class="nt">"url"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/Madonna-tickets/artist/768011"</span><span class="p">,</span><span class="w">
  </span><span class="nt">"image"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
    </span><span class="nt">"url"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/dbimages/213810a.jpg"</span><span class="w">
  </span><span class="p">},</span><span class="w">
  </span><span class="nt">"name"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Madonna"</span><span class="p">,</span><span class="w">
  </span><span class="nt">"locale"</span><span class="p">:</span><span class="w"> </span><span class="s2">"en-us"</span><span class="p">,</span><span class="w">
  </span><span class="nt">"_links"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
    </span><span class="nt">"self"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
      </span><span class="nt">"href"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/discovery/v1/attractions/768011?locale=en-us&amp;domain=ticketmaster.com"</span><span class="w">
    </span><span class="p">}</span><span class="w">
  </span><span class="p">},</span><span class="w">
  </span><span class="nt">"id"</span><span class="p">:</span><span class="w"> </span><span class="s2">"768011"</span><span class="p">,</span><span class="w">
  </span><span class="nt">"type"</span><span class="p">:</span><span class="w"> </span><span class="s2">"attraction"</span><span class="w">
</span><span class="p">}</span></code></pre></figure>

<h2 class="article console-link" id="search-categories">Search Categories</h2>

<p><strong>Method:</strong> GET.
Authentication required.
Search Classifications!</p>

<p class="code red">discovery/{version}/classifications.{format}</p>

<h3 id="url-parameters-5">URL parameters:</h3>

<table>
  <thead>
    <tr>
      <th style="text-align: left">Parameter</th>
      <th style="text-align: left">Description</th>
      <th style="text-align: left">Type</th>
      <th style="text-align: left">Default Value</th>
      <th style="text-align: left">Required</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align: left"><code class="highlighter-rouge">version</code></td>
      <td style="text-align: left">The API Version.</td>
      <td style="text-align: left">string</td>
      <td style="text-align: left">“v2”</td>
      <td style="text-align: left">Yes</td>
    </tr>
    <tr>
      <td style="text-align: left"><code class="highlighter-rouge">format</code></td>
      <td style="text-align: left">API Response Format.</td>
      <td style="text-align: left">string</td>
      <td style="text-align: left">“json”</td>
      <td style="text-align: left">Yes</td>
    </tr>
  </tbody>
</table>

<h3 id="query-parameters-4">Query parameters:</h3>

<table>
  <thead>
    <tr>
      <th style="text-align: left">Parameter</th>
      <th style="text-align: left">Description</th>
      <th style="text-align: left">Type</th>
      <th style="text-align: left">Default Value</th>
      <th style="text-align: left">Required</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align: left"><code class="highlighter-rouge">keyword</code></td>
      <td style="text-align: left">A string to search against classifications names</td>
      <td style="text-align: left">string</td>
      <td style="text-align: left"> </td>
      <td style="text-align: left">No</td>
    </tr>
    <tr>
      <td style="text-align: left"><code class="highlighter-rouge">size</code></td>
      <td style="text-align: left">The number of events returned in the API response.</td>
      <td style="text-align: left">string</td>
      <td style="text-align: left">“20”</td>
      <td style="text-align: left">No</td>
    </tr>
    <tr>
      <td style="text-align: left"><code class="highlighter-rouge">page</code></td>
      <td style="text-align: left">The page for paginating through the results.</td>
      <td style="text-align: left">string</td>
      <td style="text-align: left">“1”</td>
      <td style="text-align: left">No</td>
    </tr>
    <tr>
      <td style="text-align: left"><code class="highlighter-rouge">sort</code></td>
      <td style="text-align: left">The search sort criteria. Values: 'name,asc', 'name,desc'.</td>
      <td style="text-align: left">string</td>
      <td style="text-align: left"> </td>
      <td style="text-align: left">No</td>
    </tr>
  </tbody>
</table>

<h3 id="response-structure-5">Response structure:</h3>

<ul class="nested-list">
  <li><code class="highlighter-rouge">_embedded</code> (object) - container for categories.
    <ul>
      <li><code class="highlighter-rouge">categories</code> (array) - categories.
        <ul>
          <li><code class="highlighter-rouge"><span class="p">{</span><span class="err">array</span><span class="w"> </span><span class="err">item</span><span class="w"> </span><span class="err">object</span><span class="p">}</span></code> - category.
            <ul>
              <li><code class="highlighter-rouge">name</code> (string) - name of category.</li>
              <li><code class="highlighter-rouge">locale</code> (string) - locale of category.</li>
              <li><code class="highlighter-rouge">level</code> (number) - level of category.</li>
              <li><code class="highlighter-rouge">_links</code> (object) - links to categories.
                <ul>
                  <li><code class="highlighter-rouge">self</code> (object) - link to this category.
                    <ul>
                      <li><code class="highlighter-rouge">href</code> (string) - reference.</li>
                    </ul>
                  </li>
                  <li><code class="highlighter-rouge">parent</code> (object) - link to parent category.
                    <ul>
                      <li><code class="highlighter-rouge">href</code> (string) - reference.</li>
                    </ul>
                  </li>
                </ul>
              </li>
              <li><code class="highlighter-rouge">id</code> (string) - id of category.</li>
              <li><code class="highlighter-rouge">type</code> (string) - type of category.</li>
            </ul>
          </li>
        </ul>
      </li>
    </ul>
  </li>
  <li><code class="highlighter-rouge">_links</code> (object) - links to categories data sets.
    <ul>
      <li><code class="highlighter-rouge">self</code> (object) - link to this data set.
        <ul>
          <li><code class="highlighter-rouge">href</code> (string) - reference.</li>
          <li><code class="highlighter-rouge">templated</code> (boolean) - ability to be templated.</li>
        </ul>
      </li>
      <li><code class="highlighter-rouge">next</code> (object) - link to the next data set.
        <ul>
          <li><code class="highlighter-rouge">href</code> (string) - reference.</li>
          <li><code class="highlighter-rouge">templated</code> (boolean) - ability to be templated.</li>
        </ul>
      </li>
    </ul>
  </li>
  <li><code class="highlighter-rouge">page</code> (object) - information about current page in data source.
    <ul>
      <li><code class="highlighter-rouge">size</code> (number) - size of page.</li>
      <li><code class="highlighter-rouge">totalElements</code> (number) - total number of available elements in server.</li>
      <li><code class="highlighter-rouge">totalPages</code> (number) - total number of available pages in server.</li>
      <li><code class="highlighter-rouge">number</code> (number) - current page number counted from 0.</li>
    </ul>
  </li>
</ul>

<blockquote class="aside lang-selector">
  <p><a href="#js">JavaScript</a>
<a href="#curl">cURL</a></p>
</blockquote>

<figure class="highlight"><pre><code class="language-js" data-lang="js"><span class="nx">$</span><span class="p">.</span><span class="nx">ajax</span><span class="p">({</span>
  <span class="na">type</span><span class="p">:</span><span class="s2">"GET"</span><span class="p">,</span>
  <span class="na">url</span><span class="p">:</span><span class="s2">"https://app.ticketmaster.com/discovery/v1/categories.json?apikey={apikey}"</span><span class="p">,</span>
  <span class="na">async</span><span class="p">:</span><span class="kc">true</span><span class="p">,</span>
  <span class="na">dataType</span><span class="p">:</span> <span class="s2">"json"</span><span class="p">,</span>
  <span class="na">success</span><span class="p">:</span> <span class="kd">function</span><span class="p">(</span><span class="nx">json</span><span class="p">)</span> <span class="p">{</span>
              <span class="nx">console</span><span class="p">.</span><span class="nx">log</span><span class="p">(</span><span class="nx">json</span><span class="p">);</span>
              <span class="c1">// Parse the response.</span>
              <span class="c1">// Do other things.</span>
           <span class="p">},</span>
  <span class="na">error</span><span class="p">:</span> <span class="kd">function</span><span class="p">(</span><span class="nx">xhr</span><span class="p">,</span> <span class="nx">status</span><span class="p">,</span> <span class="nx">err</span><span class="p">)</span> <span class="p">{</span>
              <span class="c1">// This time, we do not end up here!</span>
           <span class="p">}</span>
<span class="p">});</span></code></pre></figure>

<figure class="highlight"><pre><code class="language-bash" data-lang="bash">curl <span class="se">\</span>
--include <span class="s1">'https://app.ticketmaster.com/discovery/v1/categories.json?apikey={apikey}'</span></code></pre></figure>

<blockquote class="article reqres">
  <p><a href="#req">Request</a>
<a href="#res">Response</a></p>
</blockquote>

<figure class="highlight"><pre><code class="language-http" data-lang="http"><span class="nf">GET</span> <span class="nn">/discovery/v1/categories.json?apikey=****</span> <span class="k">HTTP</span><span class="o">/</span><span class="m">1.1</span>
<span class="na">Host</span><span class="p">:</span> <span class="s">app.ticketmaster.com</span>
<span class="na">X-Target-URI</span><span class="p">:</span> <span class="s">https://app.ticketmaster.com</span>
<span class="na">Connection</span><span class="p">:</span> <span class="s">Keep-Alive</span></code></pre></figure>

<figure class="highlight"><pre><code class="language-http" data-lang="http"><span class="k">HTTP</span><span class="o">/</span><span class="m">1.1</span> <span class="m">200</span> <span class="ne">OK</span>
<span class="na">Access-Control-Allow-Headers</span><span class="p">:</span> <span class="s">origin, x-requested-with, accept</span>
<span class="na">Access-Control-Allow-Origin</span><span class="p">:</span> <span class="s">*</span>
<span class="na">Date</span><span class="p">:</span> <span class="s">Tue, 01 Dec 2015 13:02:18 GMT</span>
<span class="na">Content-Length</span><span class="p">:</span> <span class="s">8336</span>
<span class="na">Access-Control-Max-Age</span><span class="p">:</span> <span class="s">3628800</span>
<span class="na">Access-Control-Allow-Methods</span><span class="p">:</span> <span class="s">GET, PUT, POST, DELETE</span>
<span class="na">X-Application-Context</span><span class="p">:</span> <span class="s">application:default,jetson4</span>
<span class="na">Connection</span><span class="p">:</span> <span class="s">keep-alive</span>
<span class="na">Content-Type</span><span class="p">:</span> <span class="s">application/json;charset=utf-8</span>
<span class="na">Server</span><span class="p">:</span> <span class="s">Apache-Coyote/1.1</span>
<span class="na">Set-Cookie</span><span class="p">:</span> <span class="s">****</span>

<span class="p">{</span><span class="w">
  </span><span class="nt">"_links"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
    </span><span class="nt">"self"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
      </span><span class="nt">"href"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/discovery/v1/categories.json {?page,size,sort}"</span><span class="p">,</span><span class="w">
      </span><span class="nt">"templated"</span><span class="p">:</span><span class="w"> </span><span class="kc">true</span><span class="w">
    </span><span class="p">},</span><span class="w">
    </span><span class="nt">"next"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
      </span><span class="nt">"href"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/discovery/v1/categories.json?page=1&amp;size=20 {&amp;sort}"</span><span class="p">,</span><span class="w">
      </span><span class="nt">"templated"</span><span class="p">:</span><span class="w"> </span><span class="kc">true</span><span class="w">
    </span><span class="p">}</span><span class="w">
  </span><span class="p">},</span><span class="w">
  </span><span class="nt">"_embedded"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
    </span><span class="nt">"categories"</span><span class="p">:</span><span class="w">  </span><span class="p">[</span><span class="w">
       </span><span class="p">{</span><span class="w">
        </span><span class="nt">"name"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Plays"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"locale"</span><span class="p">:</span><span class="w"> </span><span class="s2">"en-us"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"level"</span><span class="p">:</span><span class="w"> </span><span class="mi">2</span><span class="p">,</span><span class="w">
        </span><span class="nt">"_links"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
          </span><span class="nt">"self"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
            </span><span class="nt">"href"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/discovery/v1/categories/32?locale=en-us&amp;domain=ticketmaster.com"</span><span class="w">
          </span><span class="p">},</span><span class="w">
          </span><span class="nt">"parent"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
            </span><span class="nt">"href"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/discovery/v1/categories/10002?locale=en-us&amp;domain=ticketmaster.com"</span><span class="w">
          </span><span class="p">}</span><span class="w">
        </span><span class="p">},</span><span class="w">
        </span><span class="nt">"id"</span><span class="p">:</span><span class="w"> </span><span class="s2">"32"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"type"</span><span class="p">:</span><span class="w"> </span><span class="s2">"category"</span><span class="w">
      </span><span class="p">},</span><span class="w">
       </span><span class="p">{</span><span class="w">
        </span><span class="nt">"name"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Classical"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"locale"</span><span class="p">:</span><span class="w"> </span><span class="s2">"en-us"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"level"</span><span class="p">:</span><span class="w"> </span><span class="mi">2</span><span class="p">,</span><span class="w">
        </span><span class="nt">"_links"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
          </span><span class="nt">"self"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
            </span><span class="nt">"href"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/discovery/v1/categories/203?locale=en-us&amp;domain=ticketmaster.com"</span><span class="w">
          </span><span class="p">},</span><span class="w">
          </span><span class="nt">"parent"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
            </span><span class="nt">"href"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/discovery/v1/categories/10002?locale=en-us&amp;domain=ticketmaster.com"</span><span class="w">
          </span><span class="p">}</span><span class="w">
        </span><span class="p">},</span><span class="w">
        </span><span class="nt">"id"</span><span class="p">:</span><span class="w"> </span><span class="s2">"203"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"type"</span><span class="p">:</span><span class="w"> </span><span class="s2">"category"</span><span class="w">
      </span><span class="p">},</span><span class="w">
       </span><span class="p">{</span><span class="w">
        </span><span class="nt">"name"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Ballet and Dance"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"locale"</span><span class="p">:</span><span class="w"> </span><span class="s2">"en-us"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"level"</span><span class="p">:</span><span class="w"> </span><span class="mi">2</span><span class="p">,</span><span class="w">
        </span><span class="nt">"_links"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
          </span><span class="nt">"self"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
            </span><span class="nt">"href"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/discovery/v1/categories/12?locale=en-us&amp;domain=ticketmaster.com"</span><span class="w">
          </span><span class="p">},</span><span class="w">
          </span><span class="nt">"parent"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
            </span><span class="nt">"href"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/discovery/v1/categories/10002?locale=en-us&amp;domain=ticketmaster.com"</span><span class="w">
          </span><span class="p">}</span><span class="w">
        </span><span class="p">},</span><span class="w">
        </span><span class="nt">"id"</span><span class="p">:</span><span class="w"> </span><span class="s2">"12"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"type"</span><span class="p">:</span><span class="w"> </span><span class="s2">"category"</span><span class="w">
      </span><span class="p">},</span><span class="w">
       </span><span class="p">{</span><span class="w">
        </span><span class="nt">"name"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Opera"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"locale"</span><span class="p">:</span><span class="w"> </span><span class="s2">"en-us"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"level"</span><span class="p">:</span><span class="w"> </span><span class="mi">2</span><span class="p">,</span><span class="w">
        </span><span class="nt">"_links"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
          </span><span class="nt">"self"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
            </span><span class="nt">"href"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/discovery/v1/categories/13?locale=en-us&amp;domain=ticketmaster.com"</span><span class="w">
          </span><span class="p">},</span><span class="w">
          </span><span class="nt">"parent"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
            </span><span class="nt">"href"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/discovery/v1/categories/10002?locale=en-us&amp;domain=ticketmaster.com"</span><span class="w">
          </span><span class="p">}</span><span class="w">
        </span><span class="p">},</span><span class="w">
        </span><span class="nt">"id"</span><span class="p">:</span><span class="w"> </span><span class="s2">"13"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"type"</span><span class="p">:</span><span class="w"> </span><span class="s2">"category"</span><span class="w">
      </span><span class="p">},</span><span class="w">
       </span><span class="p">{</span><span class="w">
        </span><span class="nt">"name"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Museums and Exhibits"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"locale"</span><span class="p">:</span><span class="w"> </span><span class="s2">"en-us"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"level"</span><span class="p">:</span><span class="w"> </span><span class="mi">2</span><span class="p">,</span><span class="w">
        </span><span class="nt">"_links"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
          </span><span class="nt">"self"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
            </span><span class="nt">"href"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/discovery/v1/categories/14?locale=en-us&amp;domain=ticketmaster.com"</span><span class="w">
          </span><span class="p">},</span><span class="w">
          </span><span class="nt">"parent"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
            </span><span class="nt">"href"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/discovery/v1/categories/10002?locale=en-us&amp;domain=ticketmaster.com"</span><span class="w">
          </span><span class="p">}</span><span class="w">
        </span><span class="p">},</span><span class="w">
        </span><span class="nt">"id"</span><span class="p">:</span><span class="w"> </span><span class="s2">"14"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"type"</span><span class="p">:</span><span class="w"> </span><span class="s2">"category"</span><span class="w">
      </span><span class="p">},</span><span class="w">
       </span><span class="p">{</span><span class="w">
        </span><span class="nt">"name"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Musicals"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"locale"</span><span class="p">:</span><span class="w"> </span><span class="s2">"en-us"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"level"</span><span class="p">:</span><span class="w"> </span><span class="mi">2</span><span class="p">,</span><span class="w">
        </span><span class="nt">"_links"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
          </span><span class="nt">"self"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
            </span><span class="nt">"href"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/discovery/v1/categories/207?locale=en-us&amp;domain=ticketmaster.com"</span><span class="w">
          </span><span class="p">},</span><span class="w">
          </span><span class="nt">"parent"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
            </span><span class="nt">"href"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/discovery/v1/categories/10002?locale=en-us&amp;domain=ticketmaster.com"</span><span class="w">
          </span><span class="p">}</span><span class="w">
        </span><span class="p">},</span><span class="w">
        </span><span class="nt">"id"</span><span class="p">:</span><span class="w"> </span><span class="s2">"207"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"type"</span><span class="p">:</span><span class="w"> </span><span class="s2">"category"</span><span class="w">
      </span><span class="p">},</span><span class="w">
       </span><span class="p">{</span><span class="w">
        </span><span class="nt">"name"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Broadway"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"locale"</span><span class="p">:</span><span class="w"> </span><span class="s2">"en-us"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"level"</span><span class="p">:</span><span class="w"> </span><span class="mi">2</span><span class="p">,</span><span class="w">
        </span><span class="nt">"_links"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
          </span><span class="nt">"self"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
            </span><span class="nt">"href"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/discovery/v1/categories/16?locale=en-us&amp;domain=ticketmaster.com"</span><span class="w">
          </span><span class="p">},</span><span class="w">
          </span><span class="nt">"parent"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
            </span><span class="nt">"href"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/discovery/v1/categories/10002?locale=en-us&amp;domain=ticketmaster.com"</span><span class="w">
          </span><span class="p">}</span><span class="w">
        </span><span class="p">},</span><span class="w">
        </span><span class="nt">"id"</span><span class="p">:</span><span class="w"> </span><span class="s2">"16"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"type"</span><span class="p">:</span><span class="w"> </span><span class="s2">"category"</span><span class="w">
      </span><span class="p">},</span><span class="w">
       </span><span class="p">{</span><span class="w">
        </span><span class="nt">"name"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Audio Tours"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"locale"</span><span class="p">:</span><span class="w"> </span><span class="s2">"en-us"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"level"</span><span class="p">:</span><span class="w"> </span><span class="mi">2</span><span class="p">,</span><span class="w">
        </span><span class="nt">"_links"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
          </span><span class="nt">"self"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
            </span><span class="nt">"href"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/discovery/v1/categories/240?locale=en-us&amp;domain=ticketmaster.com"</span><span class="w">
          </span><span class="p">},</span><span class="w">
          </span><span class="nt">"parent"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
            </span><span class="nt">"href"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/discovery/v1/categories/10005?locale=en-us&amp;domain=ticketmaster.com"</span><span class="w">
          </span><span class="p">}</span><span class="w">
        </span><span class="p">},</span><span class="w">
        </span><span class="nt">"id"</span><span class="p">:</span><span class="w"> </span><span class="s2">"240"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"type"</span><span class="p">:</span><span class="w"> </span><span class="s2">"category"</span><span class="w">
      </span><span class="p">},</span><span class="w">
       </span><span class="p">{</span><span class="w">
        </span><span class="nt">"name"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Off-Broadway"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"locale"</span><span class="p">:</span><span class="w"> </span><span class="s2">"en-us"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"level"</span><span class="p">:</span><span class="w"> </span><span class="mi">2</span><span class="p">,</span><span class="w">
        </span><span class="nt">"_links"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
          </span><span class="nt">"self"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
            </span><span class="nt">"href"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/discovery/v1/categories/17?locale=en-us&amp;domain=ticketmaster.com"</span><span class="w">
          </span><span class="p">},</span><span class="w">
          </span><span class="nt">"parent"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
            </span><span class="nt">"href"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/discovery/v1/categories/10002?locale=en-us&amp;domain=ticketmaster.com"</span><span class="w">
          </span><span class="p">}</span><span class="w">
        </span><span class="p">},</span><span class="w">
        </span><span class="nt">"id"</span><span class="p">:</span><span class="w"> </span><span class="s2">"17"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"type"</span><span class="p">:</span><span class="w"> </span><span class="s2">"category"</span><span class="w">
      </span><span class="p">},</span><span class="w">
       </span><span class="p">{</span><span class="w">
        </span><span class="nt">"name"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Magic Shows"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"locale"</span><span class="p">:</span><span class="w"> </span><span class="s2">"en-us"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"level"</span><span class="p">:</span><span class="w"> </span><span class="mi">2</span><span class="p">,</span><span class="w">
        </span><span class="nt">"_links"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
          </span><span class="nt">"self"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
            </span><span class="nt">"href"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/discovery/v1/categories/209?locale=en-us&amp;domain=ticketmaster.com"</span><span class="w">
          </span><span class="p">},</span><span class="w">
          </span><span class="nt">"parent"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
            </span><span class="nt">"href"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/discovery/v1/categories/10003?locale=en-us&amp;domain=ticketmaster.com"</span><span class="w">
          </span><span class="p">}</span><span class="w">
        </span><span class="p">},</span><span class="w">
        </span><span class="nt">"id"</span><span class="p">:</span><span class="w"> </span><span class="s2">"209"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"type"</span><span class="p">:</span><span class="w"> </span><span class="s2">"category"</span><span class="w">
      </span><span class="p">},</span><span class="w">
       </span><span class="p">{</span><span class="w">
        </span><span class="nt">"name"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Arts &amp; Theater"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"locale"</span><span class="p">:</span><span class="w"> </span><span class="s2">"en-us"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"level"</span><span class="p">:</span><span class="w"> </span><span class="mi">1</span><span class="p">,</span><span class="w">
        </span><span class="nt">"_links"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
          </span><span class="nt">"self"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
            </span><span class="nt">"href"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/discovery/v1/categories/10002?locale=en-us&amp;domain=ticketmaster.com"</span><span class="w">
          </span><span class="p">}</span><span class="w">
        </span><span class="p">},</span><span class="w">
        </span><span class="nt">"id"</span><span class="p">:</span><span class="w"> </span><span class="s2">"10002"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"type"</span><span class="p">:</span><span class="w"> </span><span class="s2">"category"</span><span class="w">
      </span><span class="p">},</span><span class="w">
       </span><span class="p">{</span><span class="w">
        </span><span class="nt">"name"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Comedy"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"locale"</span><span class="p">:</span><span class="w"> </span><span class="s2">"en-us"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"level"</span><span class="p">:</span><span class="w"> </span><span class="mi">2</span><span class="p">,</span><span class="w">
        </span><span class="nt">"_links"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
          </span><span class="nt">"self"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
            </span><span class="nt">"href"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/discovery/v1/categories/51?locale=en-us&amp;domain=ticketmaster.com"</span><span class="w">
          </span><span class="p">},</span><span class="w">
          </span><span class="nt">"parent"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
            </span><span class="nt">"href"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/discovery/v1/categories/10002?locale=en-us&amp;domain=ticketmaster.com"</span><span class="w">
          </span><span class="p">}</span><span class="w">
        </span><span class="p">},</span><span class="w">
        </span><span class="nt">"id"</span><span class="p">:</span><span class="w"> </span><span class="s2">"51"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"type"</span><span class="p">:</span><span class="w"> </span><span class="s2">"category"</span><span class="w">
      </span><span class="p">},</span><span class="w">
       </span><span class="p">{</span><span class="w">
        </span><span class="nt">"name"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Family"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"locale"</span><span class="p">:</span><span class="w"> </span><span class="s2">"en-us"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"level"</span><span class="p">:</span><span class="w"> </span><span class="mi">1</span><span class="p">,</span><span class="w">
        </span><span class="nt">"_links"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
          </span><span class="nt">"self"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
            </span><span class="nt">"href"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/discovery/v1/categories/10003?locale=en-us&amp;domain=ticketmaster.com"</span><span class="w">
          </span><span class="p">}</span><span class="w">
        </span><span class="p">},</span><span class="w">
        </span><span class="nt">"id"</span><span class="p">:</span><span class="w"> </span><span class="s2">"10003"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"type"</span><span class="p">:</span><span class="w"> </span><span class="s2">"category"</span><span class="w">
      </span><span class="p">},</span><span class="w">
       </span><span class="p">{</span><span class="w">
        </span><span class="nt">"name"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Family Attractions"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"locale"</span><span class="p">:</span><span class="w"> </span><span class="s2">"en-us"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"level"</span><span class="p">:</span><span class="w"> </span><span class="mi">2</span><span class="p">,</span><span class="w">
        </span><span class="nt">"_links"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
          </span><span class="nt">"self"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
            </span><span class="nt">"href"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/discovery/v1/categories/19?locale=en-us&amp;domain=ticketmaster.com"</span><span class="w">
          </span><span class="p">},</span><span class="w">
          </span><span class="nt">"parent"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
            </span><span class="nt">"href"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/discovery/v1/categories/10003?locale=en-us&amp;domain=ticketmaster.com"</span><span class="w">
          </span><span class="p">}</span><span class="w">
        </span><span class="p">},</span><span class="w">
        </span><span class="nt">"id"</span><span class="p">:</span><span class="w"> </span><span class="s2">"19"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"type"</span><span class="p">:</span><span class="w"> </span><span class="s2">"category"</span><span class="w">
      </span><span class="p">},</span><span class="w">
       </span><span class="p">{</span><span class="w">
        </span><span class="nt">"name"</span><span class="p">:</span><span class="w"> </span><span class="s2">"More Arts and Theater"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"locale"</span><span class="p">:</span><span class="w"> </span><span class="s2">"en-us"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"level"</span><span class="p">:</span><span class="w"> </span><span class="mi">2</span><span class="p">,</span><span class="w">
        </span><span class="nt">"_links"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
          </span><span class="nt">"self"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
            </span><span class="nt">"href"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/discovery/v1/categories/53?locale=en-us&amp;domain=ticketmaster.com"</span><span class="w">
          </span><span class="p">},</span><span class="w">
          </span><span class="nt">"parent"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
            </span><span class="nt">"href"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/discovery/v1/categories/10002?locale=en-us&amp;domain=ticketmaster.com"</span><span class="w">
          </span><span class="p">}</span><span class="w">
        </span><span class="p">},</span><span class="w">
        </span><span class="nt">"id"</span><span class="p">:</span><span class="w"> </span><span class="s2">"53"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"type"</span><span class="p">:</span><span class="w"> </span><span class="s2">"category"</span><span class="w">
      </span><span class="p">},</span><span class="w">
       </span><span class="p">{</span><span class="w">
        </span><span class="nt">"name"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Miscellaneous"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"locale"</span><span class="p">:</span><span class="w"> </span><span class="s2">"en-us"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"level"</span><span class="p">:</span><span class="w"> </span><span class="mi">1</span><span class="p">,</span><span class="w">
        </span><span class="nt">"_links"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
          </span><span class="nt">"self"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
            </span><span class="nt">"href"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/discovery/v1/categories/10005?locale=en-us&amp;domain=ticketmaster.com"</span><span class="w">
          </span><span class="p">}</span><span class="w">
        </span><span class="p">},</span><span class="w">
        </span><span class="nt">"id"</span><span class="p">:</span><span class="w"> </span><span class="s2">"10005"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"type"</span><span class="p">:</span><span class="w"> </span><span class="s2">"category"</span><span class="w">
      </span><span class="p">},</span><span class="w">
       </span><span class="p">{</span><span class="w">
        </span><span class="nt">"name"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Fairs and Festivals"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"locale"</span><span class="p">:</span><span class="w"> </span><span class="s2">"en-us"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"level"</span><span class="p">:</span><span class="w"> </span><span class="mi">2</span><span class="p">,</span><span class="w">
        </span><span class="nt">"_links"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
          </span><span class="nt">"self"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
            </span><span class="nt">"href"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/discovery/v1/categories/54?locale=en-us&amp;domain=ticketmaster.com"</span><span class="w">
          </span><span class="p">},</span><span class="w">
          </span><span class="nt">"parent"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
            </span><span class="nt">"href"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/discovery/v1/categories/10003?locale=en-us&amp;domain=ticketmaster.com"</span><span class="w">
          </span><span class="p">}</span><span class="w">
        </span><span class="p">},</span><span class="w">
        </span><span class="nt">"id"</span><span class="p">:</span><span class="w"> </span><span class="s2">"54"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"type"</span><span class="p">:</span><span class="w"> </span><span class="s2">"category"</span><span class="w">
      </span><span class="p">},</span><span class="w">
       </span><span class="p">{</span><span class="w">
        </span><span class="nt">"name"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Ice Shows"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"locale"</span><span class="p">:</span><span class="w"> </span><span class="s2">"en-us"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"level"</span><span class="p">:</span><span class="w"> </span><span class="mi">2</span><span class="p">,</span><span class="w">
        </span><span class="nt">"_links"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
          </span><span class="nt">"self"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
            </span><span class="nt">"href"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/discovery/v1/categories/22?locale=en-us&amp;domain=ticketmaster.com"</span><span class="w">
          </span><span class="p">},</span><span class="w">
          </span><span class="nt">"parent"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
            </span><span class="nt">"href"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/discovery/v1/categories/10003?locale=en-us&amp;domain=ticketmaster.com"</span><span class="w">
          </span><span class="p">}</span><span class="w">
        </span><span class="p">},</span><span class="w">
        </span><span class="nt">"id"</span><span class="p">:</span><span class="w"> </span><span class="s2">"22"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"type"</span><span class="p">:</span><span class="w"> </span><span class="s2">"category"</span><span class="w">
      </span><span class="p">},</span><span class="w">
       </span><span class="p">{</span><span class="w">
        </span><span class="nt">"name"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Children's Music and Theater"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"locale"</span><span class="p">:</span><span class="w"> </span><span class="s2">"en-us"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"level"</span><span class="p">:</span><span class="w"> </span><span class="mi">2</span><span class="p">,</span><span class="w">
        </span><span class="nt">"_links"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
          </span><span class="nt">"self"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
            </span><span class="nt">"href"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/discovery/v1/categories/23?locale=en-us&amp;domain=ticketmaster.com"</span><span class="w">
          </span><span class="p">},</span><span class="w">
          </span><span class="nt">"parent"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
            </span><span class="nt">"href"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/discovery/v1/categories/10003?locale=en-us&amp;domain=ticketmaster.com"</span><span class="w">
          </span><span class="p">}</span><span class="w">
        </span><span class="p">},</span><span class="w">
        </span><span class="nt">"id"</span><span class="p">:</span><span class="w"> </span><span class="s2">"23"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"type"</span><span class="p">:</span><span class="w"> </span><span class="s2">"category"</span><span class="w">
      </span><span class="p">},</span><span class="w">
       </span><span class="p">{</span><span class="w">
        </span><span class="nt">"name"</span><span class="p">:</span><span class="w"> </span><span class="s2">"More Family"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"locale"</span><span class="p">:</span><span class="w"> </span><span class="s2">"en-us"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"level"</span><span class="p">:</span><span class="w"> </span><span class="mi">2</span><span class="p">,</span><span class="w">
        </span><span class="nt">"_links"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
          </span><span class="nt">"self"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
            </span><span class="nt">"href"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/discovery/v1/categories/55?locale=en-us&amp;domain=ticketmaster.com"</span><span class="w">
          </span><span class="p">},</span><span class="w">
          </span><span class="nt">"parent"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
            </span><span class="nt">"href"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/discovery/v1/categories/10003?locale=en-us&amp;domain=ticketmaster.com"</span><span class="w">
          </span><span class="p">}</span><span class="w">
        </span><span class="p">},</span><span class="w">
        </span><span class="nt">"id"</span><span class="p">:</span><span class="w"> </span><span class="s2">"55"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"type"</span><span class="p">:</span><span class="w"> </span><span class="s2">"category"</span><span class="w">
      </span><span class="p">},</span><span class="w">
       </span><span class="p">{</span><span class="w">
        </span><span class="nt">"name"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Circus"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"locale"</span><span class="p">:</span><span class="w"> </span><span class="s2">"en-us"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"level"</span><span class="p">:</span><span class="w"> </span><span class="mi">2</span><span class="p">,</span><span class="w">
        </span><span class="nt">"_links"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
          </span><span class="nt">"self"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
            </span><span class="nt">"href"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/discovery/v1/categories/29?locale=en-us&amp;domain=ticketmaster.com"</span><span class="w">
          </span><span class="p">},</span><span class="w">
          </span><span class="nt">"parent"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
            </span><span class="nt">"href"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/discovery/v1/categories/10003?locale=en-us&amp;domain=ticketmaster.com"</span><span class="w">
          </span><span class="p">}</span><span class="w">
        </span><span class="p">},</span><span class="w">
        </span><span class="nt">"id"</span><span class="p">:</span><span class="w"> </span><span class="s2">"29"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"type"</span><span class="p">:</span><span class="w"> </span><span class="s2">"category"</span><span class="w">
      </span><span class="p">}</span><span class="w">
    </span><span class="p">]</span><span class="w">
  </span><span class="p">},</span><span class="w">
  </span><span class="nt">"page"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
    </span><span class="nt">"size"</span><span class="p">:</span><span class="w"> </span><span class="mi">20</span><span class="p">,</span><span class="w">
    </span><span class="nt">"totalElements"</span><span class="p">:</span><span class="w"> </span><span class="mi">76</span><span class="p">,</span><span class="w">
    </span><span class="nt">"totalPages"</span><span class="p">:</span><span class="w"> </span><span class="mi">4</span><span class="p">,</span><span class="w">
    </span><span class="nt">"number"</span><span class="p">:</span><span class="w"> </span><span class="mi">0</span><span class="w">
  </span><span class="p">}</span><span class="w">
</span><span class="p">}</span></code></pre></figure>

<h2 class="article console-link" id="category-details">Get Classification Details</h2>

<p><strong>Method:</strong> GET.
Authentication required.
Returns the classification detail by ID.</p>

<p class="code red">discovery/{version}/classifications/{id}.{format}</p>

<h3 id="url-parameters-6">URL parameters:</h3>

<table>
  <thead>
    <tr>
      <th style="text-align: left">Parameter</th>
      <th style="text-align: left">Description</th>
      <th style="text-align: left">Type</th>
      <th style="text-align: left">Default Value</th>
      <th style="text-align: left">Required</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align: left"><code class="highlighter-rouge">version</code></td>
      <td style="text-align: left">The API Version.</td>
      <td style="text-align: left">string</td>
      <td style="text-align: left">“v2”</td>
      <td style="text-align: left">Yes</td>
    </tr>
    <tr>
      <td style="text-align: left"><code class="highlighter-rouge">id</code></td>
      <td style="text-align: left">Category ID.</td>
      <td style="text-align: left">string</td>
      <td style="text-align: left">“KZFzniwnSyZfZ7v7na”</td>
      <td style="text-align: left">Yes</td>
    </tr>
    <tr>
      <td style="text-align: left"><code class="highlighter-rouge">format</code></td>
      <td style="text-align: left">API Response Format.</td>
      <td style="text-align: left">string</td>
      <td style="text-align: left">“json”</td>
      <td style="text-align: left">Yes</td>
    </tr>
  </tbody>
</table>

<h3 id="query-parameters-5">Query parameters:</h3>

<table>
  <thead>
    <tr>
      <th style="text-align: left">Parameter</th>
      <th style="text-align: left">Description</th>
      <th style="text-align: left">Type</th>
      <th style="text-align: left">Default Value</th>
      <th style="text-align: left">Required</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align: left"><code class="highlighter-rouge">locale</code></td>
      <td style="text-align: left">The event locale, including country and localization. Values: “”, “en-us”, “en-gb”, “en-ca”, “es-us”, “en-mx”, “es-mx”, “en-au”, “en-nz”, “fr-fr”, “fr-ca”.</td>
      <td style="text-align: left">string</td>
      <td style="text-align: left"> </td>
      <td style="text-align: left">No</td>
    </tr>
  </tbody>
</table>

<h3 id="response-structure-6">Response structure:</h3>

<ul class="nested-list">
  <li><code class="highlighter-rouge">name</code> (string) - name of category.</li>
  <li><code class="highlighter-rouge">locale</code> (string) - locale of category.</li>
  <li><code class="highlighter-rouge">level</code> (number) - level of category.</li>
  <li><code class="highlighter-rouge">_links</code> (object) - links to categories.
    <ul>
      <li><code class="highlighter-rouge">self</code> (object) - link to this category.
        <ul>
          <li><code class="highlighter-rouge">href</code> (string) - reference.</li>
        </ul>
      </li>
      <li><code class="highlighter-rouge">parent</code> (object) - link to parent category.
        <ul>
          <li><code class="highlighter-rouge">href</code> (string) - reference.</li>
        </ul>
      </li>
    </ul>
  </li>
  <li><code class="highlighter-rouge">id</code> (string) - id of category.</li>
  <li><code class="highlighter-rouge">type</code> (string) - type of category.</li>
</ul>

<blockquote class="aside lang-selector">
  <p><a href="#js">JavaScript</a>
<a href="#curl">cURL</a></p>
</blockquote>

<figure class="highlight"><pre><code class="language-js" data-lang="js"><span class="nx">$</span><span class="p">.</span><span class="nx">ajax</span><span class="p">({</span>
  <span class="na">type</span><span class="p">:</span><span class="s2">"GET"</span><span class="p">,</span>
  <span class="na">url</span><span class="p">:</span><span class="s2">"https://app.ticketmaster.com/discovery/v1/categories/203.json?apikey={apikey}"</span><span class="p">,</span>
  <span class="na">async</span><span class="p">:</span><span class="kc">true</span><span class="p">,</span>
  <span class="na">dataType</span><span class="p">:</span> <span class="s2">"json"</span><span class="p">,</span>
  <span class="na">success</span><span class="p">:</span> <span class="kd">function</span><span class="p">(</span><span class="nx">json</span><span class="p">)</span> <span class="p">{</span>
              <span class="nx">console</span><span class="p">.</span><span class="nx">log</span><span class="p">(</span><span class="nx">json</span><span class="p">);</span>
              <span class="c1">// Parse the response.</span>
              <span class="c1">// Do other things.</span>
           <span class="p">},</span>
  <span class="na">error</span><span class="p">:</span> <span class="kd">function</span><span class="p">(</span><span class="nx">xhr</span><span class="p">,</span> <span class="nx">status</span><span class="p">,</span> <span class="nx">err</span><span class="p">)</span> <span class="p">{</span>
              <span class="c1">// This time, we do not end up here!</span>
           <span class="p">}</span>
<span class="p">});</span></code></pre></figure>

<figure class="highlight"><pre><code class="language-bash" data-lang="bash">curl <span class="se">\</span>
--include <span class="s1">'https://app.ticketmaster.com/discovery/v1/categories/203.json?apikey={apikey}'</span></code></pre></figure>

<blockquote class="article reqres">
  <p><a href="#req">Request</a>
<a href="#res">Response</a></p>
</blockquote>

<figure class="highlight"><pre><code class="language-http" data-lang="http"><span class="nf">GET</span> <span class="nn">/discovery/v1/categories/203.json?apikey=****</span> <span class="k">HTTP</span><span class="o">/</span><span class="m">1.1</span>
<span class="na">Host</span><span class="p">:</span> <span class="s">app.ticketmaster.com</span>
<span class="na">X-Target-URI</span><span class="p">:</span> <span class="s">https://app.ticketmaster.com</span>
<span class="na">Connection</span><span class="p">:</span> <span class="s">Keep-Alive</span></code></pre></figure>

<figure class="highlight"><pre><code class="language-http" data-lang="http"><span class="k">HTTP</span><span class="o">/</span><span class="m">1.1</span> <span class="m">200</span> <span class="ne">OK</span>
<span class="na">Access-Control-Allow-Headers</span><span class="p">:</span> <span class="s">origin, x-requested-with, accept</span>
<span class="na">Access-Control-Allow-Origin</span><span class="p">:</span> <span class="s">*</span>
<span class="na">Date</span><span class="p">:</span> <span class="s">Tue, 01 Dec 2015 13:03:29 GMT</span>
<span class="na">Content-Length</span><span class="p">:</span> <span class="s">568</span>
<span class="na">Access-Control-Max-Age</span><span class="p">:</span> <span class="s">3628800</span>
<span class="na">Access-Control-Allow-Methods</span><span class="p">:</span> <span class="s">GET, PUT, POST, DELETE</span>
<span class="na">X-Application-Context</span><span class="p">:</span> <span class="s">application:default,jetson1</span>
<span class="na">Connection</span><span class="p">:</span> <span class="s">keep-alive</span>
<span class="na">Content-Type</span><span class="p">:</span> <span class="s">application/json;charset=utf-8</span>
<span class="na">Server</span><span class="p">:</span> <span class="s">Apache-Coyote/1.1</span>
<span class="na">Set-Cookie</span><span class="p">:</span> <span class="s">****</span>

<span class="p">{</span><span class="w">
  </span><span class="nt">"name"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Classical"</span><span class="p">,</span><span class="w">
  </span><span class="nt">"locale"</span><span class="p">:</span><span class="w"> </span><span class="s2">"en-us"</span><span class="p">,</span><span class="w">
  </span><span class="nt">"level"</span><span class="p">:</span><span class="w"> </span><span class="mi">2</span><span class="p">,</span><span class="w">
  </span><span class="nt">"_links"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
    </span><span class="nt">"self"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
      </span><span class="nt">"href"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/discovery/v1/categories/203?locale=en-us&amp;domain=ticketmaster.com"</span><span class="w">
    </span><span class="p">},</span><span class="w">
    </span><span class="nt">"parent"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
      </span><span class="nt">"href"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/discovery/v1/categories/10002?locale=en-us&amp;domain=ticketmaster.com"</span><span class="w">
    </span><span class="p">}</span><span class="w">
  </span><span class="p">},</span><span class="w">
  </span><span class="nt">"id"</span><span class="p">:</span><span class="w"> </span><span class="s2">"203"</span><span class="p">,</span><span class="w">
  </span><span class="nt">"type"</span><span class="p">:</span><span class="w"> </span><span class="s2">"category"</span><span class="w">
</span><span class="p">}</span></code></pre></figure>

<h2 class="article console-link" id="search-venues">Search Venues</h2>

<p><strong>Method:</strong> GET.
Authentication required.
Search Venues!</p>

<p class="code red">discovery/{version}/venues.{format}</p>

<h3 id="url-parameters-7">URL parameters:</h3>

<table>
  <thead>
    <tr>
      <th style="text-align: left">Parameter</th>
      <th style="text-align: left">Description</th>
      <th style="text-align: left">Type</th>
      <th style="text-align: left">Default Value</th>
      <th style="text-align: left">Required</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align: left"><code class="highlighter-rouge">version</code></td>
      <td style="text-align: left">The API Version.</td>
      <td style="text-align: left">string</td>
      <td style="text-align: left">“v2”</td>
      <td style="text-align: left">Yes</td>
    </tr>
    <tr>
      <td style="text-align: left"><code class="highlighter-rouge">format</code></td>
      <td style="text-align: left">API Response Format.</td>
      <td style="text-align: left">string</td>
      <td style="text-align: left">“json”</td>
      <td style="text-align: left">Yes</td>
    </tr>
  </tbody>
</table>

<h3 id="query-parameters-6">Query parameters:</h3>

<table>
  <thead>
    <tr>
      <th style="text-align: left">Parameter</th>
      <th style="text-align: left">Description</th>
      <th style="text-align: left">Type</th>
      <th style="text-align: left">Default Value</th>
      <th style="text-align: left">Required</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align: left"><code class="highlighter-rouge">keyword</code></td>
      <td style="text-align: left">A string to search against venue names.</td>
      <td style="text-align: left">string</td>
      <td style="text-align: left"> </td>
      <td style="text-align: left">No</td>
    </tr>
    <tr>
      <td style="text-align: left"><code class="highlighter-rouge">locale</code></td>
      <td style="text-align: left">The event locale, including country and localization. Values: “”, “en-us”, “en-gb”, “en-ca”, “es-us”, “en-mx”, “es-mx”, “en-au”, “en-nz”, “fr-fr”, “fr-ca”.</td>
      <td style="text-align: left">string</td>
      <td style="text-align: left"> </td>
      <td style="text-align: left">No</td>
    </tr>
    <tr>
      <td style="text-align: left"><code class="highlighter-rouge">size</code></td>
      <td style="text-align: left">The number of events returned in the API response.</td>
      <td style="text-align: left">string</td>
      <td style="text-align: left">“20”</td>
      <td style="text-align: left">No</td>
    </tr>
    <tr>
      <td style="text-align: left"><code class="highlighter-rouge">page</code></td>
      <td style="text-align: left">The page for paginating through the results.</td>
      <td style="text-align: left">string</td>
      <td style="text-align: left">“1”</td>
      <td style="text-align: left">No</td>
    </tr>
    <tr>
      <td style="text-align: left"><code class="highlighter-rouge">sort</code></td>
      <td style="text-align: left">The search sort criteria. Values: 'name,desc', 'name,asc'.</td>
      <td style="text-align: left">string</td>
      <td style="text-align: left"> </td>
      <td style="text-align: left">No</td>
    </tr>
  </tbody>
</table>

<h3 id="response-structure-7">Response structure:</h3>

<ul class="nested-list">
  <li><code class="highlighter-rouge">_embedded</code> (object) - container for venues.
    <ul>
      <li><code class="highlighter-rouge">venues</code> (array) - venues.
        <ul>
          <li><code class="highlighter-rouge"><span class="p">{</span><span class="err">array</span><span class="w"> </span><span class="err">item</span><span class="w"> </span><span class="err">object</span><span class="p">}</span></code> - venue.
            <ul>
              <li><code class="highlighter-rouge">name</code> (string) - name of venue.</li>
              <li><code class="highlighter-rouge">locale</code> (string) - locale of venue.</li>
              <li><code class="highlighter-rouge">marketId</code> (array of numbers) - id of supported markets.</li>
              <li><code class="highlighter-rouge">country</code> (string) - country code.</li>
              <li><code class="highlighter-rouge">state</code> (object) - state of venue.
                <ul>
                  <li><code class="highlighter-rouge">stateCode</code> (string) - code of state.</li>
                </ul>
              </li>
              <li><code class="highlighter-rouge">city</code> (object) - citiy of venue.
                <ul>
                  <li><code class="highlighter-rouge">name</code> (string) - name of city.</li>
                </ul>
              </li>
              <li><code class="highlighter-rouge">postalCode</code> (string) - postal code of venue.</li>
              <li><code class="highlighter-rouge">address</code> (object) - address of venue.
                <ul>
                  <li><code class="highlighter-rouge">line1</code> (string) - address line 1.</li>
                  <li><code class="highlighter-rouge">line2</code> (string) - address line 2.</li>
                </ul>
              </li>
              <li><code class="highlighter-rouge">timeZone</code> (string) - time zone of venue.</li>
              <li><code class="highlighter-rouge">_links</code> (object) - links to venues.
                <ul>
                  <li><code class="highlighter-rouge">self</code> (object) - link to this venue.
                    <ul>
                      <li><code class="highlighter-rouge">href</code> (string) - reference.</li>
                    </ul>
                  </li>
                </ul>
              </li>
              <li><code class="highlighter-rouge">id</code> (string) - id of venue.</li>
              <li><code class="highlighter-rouge">type</code> (string) - type of venue.</li>
            </ul>
          </li>
        </ul>
      </li>
    </ul>
  </li>
  <li><code class="highlighter-rouge">_links</code> (object) - links to venues data set.
    <ul>
      <li><code class="highlighter-rouge">self</code> (object) - link to this data set.
        <ul>
          <li><code class="highlighter-rouge">href</code> (string) - reference.</li>
          <li><code class="highlighter-rouge">templated</code> (boolean) - is templated.</li>
        </ul>
      </li>
    </ul>
  </li>
  <li><code class="highlighter-rouge">page</code> (object) - information about current page in data source.
    <ul>
      <li><code class="highlighter-rouge">size</code> (number) - page size.</li>
      <li><code class="highlighter-rouge">totalElements</code> (number) - total number of available elements in server.</li>
      <li><code class="highlighter-rouge">totalPages</code> (number) - total number of available pages in server.</li>
      <li><code class="highlighter-rouge">number</code> (number) - current page number counted from 0.</li>
    </ul>
  </li>
</ul>

<blockquote class="aside lang-selector">
  <p><a href="#js">JavaScript</a>
<a href="#curl">cURL</a></p>
</blockquote>

<figure class="highlight"><pre><code class="language-js" data-lang="js"><span class="nx">$</span><span class="p">.</span><span class="nx">ajax</span><span class="p">({</span>
  <span class="na">type</span><span class="p">:</span><span class="s2">"GET"</span><span class="p">,</span>
  <span class="na">url</span><span class="p">:</span><span class="s2">"https://app.ticketmaster.com/discovery/v1/venues.json?keyword=UCV&amp;apikey={apikey}"</span><span class="p">,</span>
  <span class="na">async</span><span class="p">:</span><span class="kc">true</span><span class="p">,</span>
  <span class="na">dataType</span><span class="p">:</span> <span class="s2">"json"</span><span class="p">,</span>
  <span class="na">success</span><span class="p">:</span> <span class="kd">function</span><span class="p">(</span><span class="nx">json</span><span class="p">)</span> <span class="p">{</span>
              <span class="nx">console</span><span class="p">.</span><span class="nx">log</span><span class="p">(</span><span class="nx">json</span><span class="p">);</span>
              <span class="c1">// Parse the response.</span>
              <span class="c1">// Do other things.</span>
           <span class="p">},</span>
  <span class="na">error</span><span class="p">:</span> <span class="kd">function</span><span class="p">(</span><span class="nx">xhr</span><span class="p">,</span> <span class="nx">status</span><span class="p">,</span> <span class="nx">err</span><span class="p">)</span> <span class="p">{</span>
              <span class="c1">// This time, we do not end up here!</span>
           <span class="p">}</span>
<span class="p">});</span></code></pre></figure>

<figure class="highlight"><pre><code class="language-bash" data-lang="bash">curl <span class="se">\</span>
--include <span class="s1">'https://app.ticketmaster.com/discovery/v1/venues.json?keyword=UCV&amp;apikey={apikey}'</span></code></pre></figure>

<blockquote class="article reqres">
  <p><a href="#req">Request</a>
<a href="#res">Response</a></p>
</blockquote>

<figure class="highlight"><pre><code class="language-http" data-lang="http"><span class="nf">GET</span> <span class="nn">/discovery/v1/venues.json?apikey=****&amp;keyword=UCV</span> <span class="k">HTTP</span><span class="o">/</span><span class="m">1.1</span>
<span class="na">Host</span><span class="p">:</span> <span class="s">app.ticketmaster.com</span>
<span class="na">X-Target-URI</span><span class="p">:</span> <span class="s">http://app.ticketmaster.com</span>
<span class="na">Connection</span><span class="p">:</span> <span class="s">Keep-Alive</span></code></pre></figure>

<figure class="highlight"><pre><code class="language-http" data-lang="http"><span class="k">HTTP</span><span class="o">/</span><span class="m">1.1</span> <span class="m">200</span> <span class="ne">OK</span>
<span class="na">Access-Control-Allow-Headers</span><span class="p">:</span> <span class="s">origin, x-requested-with, accept</span>
<span class="na">Access-Control-Allow-Origin</span><span class="p">:</span> <span class="s">*</span>
<span class="na">Date</span><span class="p">:</span> <span class="s">Tue, 01 Dec 2015 13:04:50 GMT</span>
<span class="na">Content-Length</span><span class="p">:</span> <span class="s">1646</span>
<span class="na">Access-Control-Max-Age</span><span class="p">:</span> <span class="s">3628800</span>
<span class="na">Access-Control-Allow-Methods</span><span class="p">:</span> <span class="s">GET, PUT, POST, DELETE</span>
<span class="na">X-Application-Context</span><span class="p">:</span> <span class="s">application:default,jetson1</span>
<span class="na">Connection</span><span class="p">:</span> <span class="s">keep-alive</span>
<span class="na">Content-Type</span><span class="p">:</span> <span class="s">application/json;charset=utf-8</span>
<span class="na">Server</span><span class="p">:</span> <span class="s">Apache-Coyote/1.1</span>
<span class="na">Set-Cookie</span><span class="p">:</span> <span class="s">****</span>

<span class="p">{</span><span class="w">
  </span><span class="nt">"_links"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
    </span><span class="nt">"self"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
      </span><span class="nt">"href"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/discovery/v1/venues.json?keyword=UCV {&amp;page,size,sort}"</span><span class="p">,</span><span class="w">
      </span><span class="nt">"templated"</span><span class="p">:</span><span class="w"> </span><span class="kc">true</span><span class="w">
    </span><span class="p">}</span><span class="w">
  </span><span class="p">},</span><span class="w">
  </span><span class="nt">"_embedded"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
    </span><span class="nt">"venues"</span><span class="p">:</span><span class="w">  </span><span class="p">[</span><span class="w">
       </span><span class="p">{</span><span class="w">
        </span><span class="nt">"name"</span><span class="p">:</span><span class="w"> </span><span class="s2">"#1 Please do not use, left over from UCV initial acct set up"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"locale"</span><span class="p">:</span><span class="w"> </span><span class="s2">"en-us"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"marketId"</span><span class="p">:</span><span class="w">  </span><span class="p">[</span><span class="w">
          </span><span class="mi">103</span><span class="w">
        </span><span class="p">],</span><span class="w">
        </span><span class="nt">"country"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
          </span><span class="nt">"countryCode"</span><span class="p">:</span><span class="w"> </span><span class="s2">"CA"</span><span class="w">
        </span><span class="p">},</span><span class="w">
        </span><span class="nt">"state"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
          </span><span class="nt">"stateCode"</span><span class="p">:</span><span class="w"> </span><span class="s2">"ON"</span><span class="w">
        </span><span class="p">},</span><span class="w">
        </span><span class="nt">"city"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
          </span><span class="nt">"name"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Morrisburg"</span><span class="w">
        </span><span class="p">},</span><span class="w">
        </span><span class="nt">"postalCode"</span><span class="p">:</span><span class="w"> </span><span class="s2">"K0C1X0"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"address"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
          </span><span class="nt">"line1"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Crysler Park Marina, 13480 County Rd 2"</span><span class="p">,</span><span class="w">
          </span><span class="nt">"line2"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Morrisburg, ON"</span><span class="w">
        </span><span class="p">},</span><span class="w">
        </span><span class="nt">"timeZone"</span><span class="p">:</span><span class="w"> </span><span class="s2">"America/Toronto"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"_links"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
          </span><span class="nt">"self"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
            </span><span class="nt">"href"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/discovery/v1/venues/341396?locale=en-us&amp;domain=ticketmaster.com"</span><span class="w">
          </span><span class="p">}</span><span class="w">
        </span><span class="p">},</span><span class="w">
        </span><span class="nt">"id"</span><span class="p">:</span><span class="w"> </span><span class="s2">"341396"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"type"</span><span class="p">:</span><span class="w"> </span><span class="s2">"venue"</span><span class="w">
      </span><span class="p">},</span><span class="w">
       </span><span class="p">{</span><span class="w">
        </span><span class="nt">"name"</span><span class="p">:</span><span class="w"> </span><span class="s2">"#2 Please do not use, left over from UCV initial acct set up"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"locale"</span><span class="p">:</span><span class="w"> </span><span class="s2">"en-us"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"marketId"</span><span class="p">:</span><span class="w">  </span><span class="p">[</span><span class="w">
          </span><span class="mi">103</span><span class="w">
        </span><span class="p">],</span><span class="w">
        </span><span class="nt">"country"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
          </span><span class="nt">"countryCode"</span><span class="p">:</span><span class="w"> </span><span class="s2">"CA"</span><span class="w">
        </span><span class="p">},</span><span class="w">
        </span><span class="nt">"state"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
          </span><span class="nt">"stateCode"</span><span class="p">:</span><span class="w"> </span><span class="s2">"ON"</span><span class="w">
        </span><span class="p">},</span><span class="w">
        </span><span class="nt">"city"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
          </span><span class="nt">"name"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Morrisburg"</span><span class="w">
        </span><span class="p">},</span><span class="w">
        </span><span class="nt">"postalCode"</span><span class="p">:</span><span class="w"> </span><span class="s2">"K0C1X0"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"address"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
          </span><span class="nt">"line1"</span><span class="p">:</span><span class="w"> </span><span class="s2">"13740 County Road 2"</span><span class="p">,</span><span class="w">
          </span><span class="nt">"line2"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Morrisburg, ON"</span><span class="w">
        </span><span class="p">},</span><span class="w">
        </span><span class="nt">"timeZone"</span><span class="p">:</span><span class="w"> </span><span class="s2">"America/Toronto"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"_links"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
          </span><span class="nt">"self"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
            </span><span class="nt">"href"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/discovery/v1/venues/341395?locale=en-us&amp;domain=ticketmaster.com"</span><span class="w">
          </span><span class="p">}</span><span class="w">
        </span><span class="p">},</span><span class="w">
        </span><span class="nt">"id"</span><span class="p">:</span><span class="w"> </span><span class="s2">"341395"</span><span class="p">,</span><span class="w">
        </span><span class="nt">"type"</span><span class="p">:</span><span class="w"> </span><span class="s2">"venue"</span><span class="w">
      </span><span class="p">}</span><span class="w">
    </span><span class="p">]</span><span class="w">
  </span><span class="p">},</span><span class="w">
  </span><span class="nt">"page"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
    </span><span class="nt">"size"</span><span class="p">:</span><span class="w"> </span><span class="mi">20</span><span class="p">,</span><span class="w">
    </span><span class="nt">"totalElements"</span><span class="p">:</span><span class="w"> </span><span class="mi">2</span><span class="p">,</span><span class="w">
    </span><span class="nt">"totalPages"</span><span class="p">:</span><span class="w"> </span><span class="mi">1</span><span class="p">,</span><span class="w">
    </span><span class="nt">"number"</span><span class="p">:</span><span class="w"> </span><span class="mi">0</span><span class="w">
  </span><span class="p">}</span><span class="w">
</span><span class="p">}</span></code></pre></figure>

<h2 class="article console-link" id="venue-details">Get Venue Details</h2>

<p><strong>Method:</strong> GET.
Authentication required.
Returns the venue detail by ID.</p>

<p class="code red">discovery/{version}/venues/{id}.{format}</p>

<h3 id="url-parameters-8">URL parameters:</h3>

<table>
  <thead>
    <tr>
      <th style="text-align: left">Parameter</th>
      <th style="text-align: left">Description</th>
      <th style="text-align: left">Type</th>
      <th style="text-align: left">Default Value</th>
      <th style="text-align: left">Required</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align: left"><code class="highlighter-rouge">version</code></td>
      <td style="text-align: left">The API Version.</td>
      <td style="text-align: left">string</td>
      <td style="text-align: left">“v2”</td>
      <td style="text-align: left">Yes</td>
    </tr>
    <tr>
      <td style="text-align: left"><code class="highlighter-rouge">id</code></td>
      <td style="text-align: left">Venue ID.</td>
      <td style="text-align: left">string</td>
      <td style="text-align: left">“KovZpZAFnIEA”</td>
      <td style="text-align: left">Yes</td>
    </tr>
    <tr>
      <td style="text-align: left"><code class="highlighter-rouge">format</code></td>
      <td style="text-align: left">API Response Format.</td>
      <td style="text-align: left">string</td>
      <td style="text-align: left">“json”</td>
      <td style="text-align: left">Yes</td>
    </tr>
  </tbody>
</table>

<h3 id="query-parameters-7">Query parameters:</h3>

<table>
  <thead>
    <tr>
      <th style="text-align: left">Parameter</th>
      <th style="text-align: left">Description</th>
      <th style="text-align: left">Type</th>
      <th style="text-align: left">Default Value</th>
      <th style="text-align: left">Required</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align: left"><code class="highlighter-rouge">locale</code></td>
      <td style="text-align: left">The event locale, including country and localization. Values: “”, “en-us”, “en-gb”, “en-ca”, “es-us”, “en-mx”, “es-mx”, “en-au”, “en-nz”, “fr-fr”, “fr-ca”.</td>
      <td style="text-align: left">string</td>
      <td style="text-align: left"> </td>
      <td style="text-align: left">No</td>
    </tr>
  </tbody>
</table>

<h3 id="response-structure-8">Response structure:</h3>

<ul class="nested-list">
  <li><code class="highlighter-rouge">name</code> (string) - name of venue.</li>
  <li><code class="highlighter-rouge">locale</code> (string) - locale of venue.</li>
  <li><code class="highlighter-rouge">marketId</code> (array of numbers) - id of supported markets.</li>
  <li><code class="highlighter-rouge">country</code> (string) - country code.</li>
  <li><code class="highlighter-rouge">state</code> (object) - state of venue.
    <ul>
      <li><code class="highlighter-rouge">stateCode</code> (string) - code of state.</li>
    </ul>
  </li>
  <li><code class="highlighter-rouge">city</code> (object) - citiy of venue.
    <ul>
      <li><code class="highlighter-rouge">name</code> (string) - name of city.</li>
    </ul>
  </li>
  <li><code class="highlighter-rouge">postalCode</code> (string) - postal code of venue.</li>
  <li><code class="highlighter-rouge">address</code> (object) - address of venue.
    <ul>
      <li><code class="highlighter-rouge">line1</code> (string) - address line 1.</li>
      <li><code class="highlighter-rouge">line2</code> (string) - address line 2.</li>
    </ul>
  </li>
  <li><code class="highlighter-rouge">timeZone</code> (string) - time zone of venue.</li>
  <li><code class="highlighter-rouge">_links</code> (object) - links to venues.
    <ul>
      <li><code class="highlighter-rouge">self</code> (object) - link to this venue.
        <ul>
          <li><code class="highlighter-rouge">href</code> (string) - reference.</li>
        </ul>
      </li>
    </ul>
  </li>
  <li><code class="highlighter-rouge">id</code> (string) - id of venue.</li>
  <li><code class="highlighter-rouge">type</code> (string) - type of venue.</li>
</ul>

<blockquote class="aside lang-selector">
  <p><a href="#js">JavaScript</a>
<a href="#curl">cURL</a></p>
</blockquote>

<figure class="highlight"><pre><code class="language-js" data-lang="js"><span class="nx">$</span><span class="p">.</span><span class="nx">ajax</span><span class="p">({</span>
  <span class="na">type</span><span class="p">:</span><span class="s2">"GET"</span><span class="p">,</span>
  <span class="na">url</span><span class="p">:</span><span class="s2">"https://app.ticketmaster.com/discovery/v1/venues/90150.json?apikey={apikey}"</span><span class="p">,</span>
  <span class="na">async</span><span class="p">:</span><span class="kc">true</span><span class="p">,</span>
  <span class="na">dataType</span><span class="p">:</span> <span class="s2">"json"</span><span class="p">,</span>
  <span class="na">success</span><span class="p">:</span> <span class="kd">function</span><span class="p">(</span><span class="nx">json</span><span class="p">)</span> <span class="p">{</span>
              <span class="nx">console</span><span class="p">.</span><span class="nx">log</span><span class="p">(</span><span class="nx">json</span><span class="p">);</span>
              <span class="c1">// Parse the response.</span>
              <span class="c1">// Do other things.</span>
           <span class="p">},</span>
  <span class="na">error</span><span class="p">:</span> <span class="kd">function</span><span class="p">(</span><span class="nx">xhr</span><span class="p">,</span> <span class="nx">status</span><span class="p">,</span> <span class="nx">err</span><span class="p">)</span> <span class="p">{</span>
              <span class="c1">// This time, we do not end up here!</span>
           <span class="p">}</span>
<span class="p">});</span></code></pre></figure>

<figure class="highlight"><pre><code class="language-bash" data-lang="bash">curl <span class="se">\</span>
--include <span class="s1">'https://app.ticketmaster.com/discovery/v1/venues/90150.json?apikey={apikey}'</span></code></pre></figure>

<blockquote class="article reqres">
  <p><a href="#req">Request</a>
<a href="#res">Response</a></p>
</blockquote>

<figure class="highlight"><pre><code class="language-http" data-lang="http"><span class="nf">GET</span> <span class="nn">/discovery/v1/venues/90150.json?apikey=****</span> <span class="k">HTTP</span><span class="o">/</span><span class="m">1.1</span>
<span class="na">Host</span><span class="p">:</span> <span class="s">app.ticketmaster.com</span>
<span class="na">X-Target-URI</span><span class="p">:</span> <span class="s">https://app.ticketmaster.com</span>
<span class="na">Connection</span><span class="p">:</span> <span class="s">Keep-Alive</span></code></pre></figure>

<figure class="highlight"><pre><code class="language-http" data-lang="http"><span class="k">HTTP</span><span class="o">/</span><span class="m">1.1</span> <span class="m">200</span> <span class="ne">OK</span>
<span class="na">Access-Control-Allow-Headers</span><span class="p">:</span> <span class="s">origin, x-requested-with, accept</span>
<span class="na">Access-Control-Allow-Origin</span><span class="p">:</span> <span class="s">*</span>
<span class="na">Date</span><span class="p">:</span> <span class="s">Tue, 01 Dec 2015 13:07:04 GMT</span>
<span class="na">Content-Length</span><span class="p">:</span> <span class="s">641</span>
<span class="na">Access-Control-Max-Age</span><span class="p">:</span> <span class="s">3628800</span>
<span class="na">Access-Control-Allow-Methods</span><span class="p">:</span> <span class="s">GET, PUT, POST, DELETE</span>
<span class="na">X-Application-Context</span><span class="p">:</span> <span class="s">application:default,jetson1</span>
<span class="na">Connection</span><span class="p">:</span> <span class="s">keep-alive</span>
<span class="na">Content-Type</span><span class="p">:</span> <span class="s">application/json;charset=utf-8</span>
<span class="na">Server</span><span class="p">:</span> <span class="s">Apache-Coyote/1.1</span>
<span class="na">Set-Cookie</span><span class="p">:</span> <span class="s">****</span>

<span class="p">{</span><span class="w">
  </span><span class="nt">"name"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Hollywood Bowl"</span><span class="p">,</span><span class="w">
  </span><span class="nt">"locale"</span><span class="p">:</span><span class="w"> </span><span class="s2">"en-us"</span><span class="p">,</span><span class="w">
  </span><span class="nt">"marketId"</span><span class="p">:</span><span class="w">  </span><span class="p">[</span><span class="w">
    </span><span class="mi">27</span><span class="w">
  </span><span class="p">],</span><span class="w">
  </span><span class="nt">"country"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
    </span><span class="nt">"countryCode"</span><span class="p">:</span><span class="w"> </span><span class="s2">"US"</span><span class="w">
  </span><span class="p">},</span><span class="w">
  </span><span class="nt">"state"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
    </span><span class="nt">"stateCode"</span><span class="p">:</span><span class="w"> </span><span class="s2">"CA"</span><span class="w">
  </span><span class="p">},</span><span class="w">
  </span><span class="nt">"city"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
    </span><span class="nt">"name"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Hollywood"</span><span class="w">
  </span><span class="p">},</span><span class="w">
  </span><span class="nt">"postalCode"</span><span class="p">:</span><span class="w"> </span><span class="s2">"90068"</span><span class="p">,</span><span class="w">
  </span><span class="nt">"address"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
    </span><span class="nt">"line1"</span><span class="p">:</span><span class="w"> </span><span class="s2">"2301 N Highland Ave"</span><span class="p">,</span><span class="w">
    </span><span class="nt">"line2"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Hollywood, CA"</span><span class="w">
  </span><span class="p">},</span><span class="w">
  </span><span class="nt">"timeZone"</span><span class="p">:</span><span class="w"> </span><span class="s2">"America/Los_Angeles"</span><span class="p">,</span><span class="w">
  </span><span class="nt">"_links"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
    </span><span class="nt">"self"</span><span class="p">:</span><span class="w">  </span><span class="p">{</span><span class="w">
      </span><span class="nt">"href"</span><span class="p">:</span><span class="w"> </span><span class="s2">"/discovery/v1/venues/90150?locale=en-us&amp;domain=ticketmaster.com"</span><span class="w">
    </span><span class="p">}</span><span class="w">
  </span><span class="p">},</span><span class="w">
  </span><span class="nt">"id"</span><span class="p">:</span><span class="w"> </span><span class="s2">"90150"</span><span class="p">,</span><span class="w">
  </span><span class="nt">"type"</span><span class="p">:</span><span class="w"> </span><span class="s2">"venue"</span><span class="w">
</span><span class="p">}</span></code></pre></figure>

<h2 class="article" id="supported-markets">Supported Markets</h2>

<h4 id="usa">USA</h4>

<table>
  <thead>
    <tr>
      <th style="text-align: left">ID</th>
      <th style="text-align: left">Market</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align: left">1</td>
      <td style="text-align: left">Birmingham &amp; More</td>
    </tr>
    <tr>
      <td style="text-align: left">2</td>
      <td style="text-align: left">Charlotte</td>
    </tr>
    <tr>
      <td style="text-align: left">3</td>
      <td style="text-align: left">Chicagoland &amp; Northern IL</td>
    </tr>
    <tr>
      <td style="text-align: left">4</td>
      <td style="text-align: left">Cincinnati &amp; Dayton</td>
    </tr>
    <tr>
      <td style="text-align: left">5</td>
      <td style="text-align: left">Dallas - Fort Worth &amp; More</td>
    </tr>
    <tr>
      <td style="text-align: left">6</td>
      <td style="text-align: left">Denver &amp; More</td>
    </tr>
    <tr>
      <td style="text-align: left">7</td>
      <td style="text-align: left">Detroit, Toledo &amp; More</td>
    </tr>
    <tr>
      <td style="text-align: left">8</td>
      <td style="text-align: left">El Paso &amp; New Mexico</td>
    </tr>
    <tr>
      <td style="text-align: left">9</td>
      <td style="text-align: left">Grand Rapids &amp; More</td>
    </tr>
    <tr>
      <td style="text-align: left">10</td>
      <td style="text-align: left">Greater Atlanta Area</td>
    </tr>
    <tr>
      <td style="text-align: left">11</td>
      <td style="text-align: left">Greater Boston Area</td>
    </tr>
    <tr>
      <td style="text-align: left">12</td>
      <td style="text-align: left">Cleveland, Youngstown &amp; More</td>
    </tr>
    <tr>
      <td style="text-align: left">13</td>
      <td style="text-align: left">Greater Columbus Area</td>
    </tr>
    <tr>
      <td style="text-align: left">14</td>
      <td style="text-align: left">Greater Las Vegas Area</td>
    </tr>
    <tr>
      <td style="text-align: left">15</td>
      <td style="text-align: left">Greater Miami Area</td>
    </tr>
    <tr>
      <td style="text-align: left">16</td>
      <td style="text-align: left">Minneapolis/St. Paul &amp; More</td>
    </tr>
    <tr>
      <td style="text-align: left">17</td>
      <td style="text-align: left">Greater Orlando Area</td>
    </tr>
    <tr>
      <td style="text-align: left">18</td>
      <td style="text-align: left">Greater Philadelphia Area</td>
    </tr>
    <tr>
      <td style="text-align: left">19</td>
      <td style="text-align: left">Greater Pittsburgh Area</td>
    </tr>
    <tr>
      <td style="text-align: left">20</td>
      <td style="text-align: left">Greater San Diego Area</td>
    </tr>
    <tr>
      <td style="text-align: left">21</td>
      <td style="text-align: left">Greater Tampa Area</td>
    </tr>
    <tr>
      <td style="text-align: left">22</td>
      <td style="text-align: left">Houston &amp; More</td>
    </tr>
    <tr>
      <td style="text-align: left">23</td>
      <td style="text-align: left">Indianapolis &amp; More</td>
    </tr>
    <tr>
      <td style="text-align: left">24</td>
      <td style="text-align: left">Iowa</td>
    </tr>
    <tr>
      <td style="text-align: left">25</td>
      <td style="text-align: left">Jacksonville &amp; More</td>
    </tr>
    <tr>
      <td style="text-align: left">26</td>
      <td style="text-align: left">Kansas City &amp; More</td>
    </tr>
    <tr>
      <td style="text-align: left">27</td>
      <td style="text-align: left">Greater Los Angeles Area</td>
    </tr>
    <tr>
      <td style="text-align: left">28</td>
      <td style="text-align: left">Louisville &amp; Lexington</td>
    </tr>
    <tr>
      <td style="text-align: left">29</td>
      <td style="text-align: left">Memphis, Little Rock &amp; More</td>
    </tr>
    <tr>
      <td style="text-align: left">30</td>
      <td style="text-align: left">Milwaukee &amp; WI</td>
    </tr>
    <tr>
      <td style="text-align: left">31</td>
      <td style="text-align: left">Nashville, Knoxville &amp; More</td>
    </tr>
    <tr>
      <td style="text-align: left">32</td>
      <td style="text-align: left">United States</td>
    </tr>
    <tr>
      <td style="text-align: left">33</td>
      <td style="text-align: left">New England</td>
    </tr>
    <tr>
      <td style="text-align: left">34</td>
      <td style="text-align: left">New Orleans &amp; More</td>
    </tr>
    <tr>
      <td style="text-align: left">35</td>
      <td style="text-align: left">New York/Tri-State Area</td>
    </tr>
    <tr>
      <td style="text-align: left">36</td>
      <td style="text-align: left">Phoenix &amp; Tucson</td>
    </tr>
    <tr>
      <td style="text-align: left">37</td>
      <td style="text-align: left">Portland &amp; More</td>
    </tr>
    <tr>
      <td style="text-align: left">38</td>
      <td style="text-align: left">Raleigh &amp; Durham</td>
    </tr>
    <tr>
      <td style="text-align: left">39</td>
      <td style="text-align: left">Saint Louis &amp; More</td>
    </tr>
    <tr>
      <td style="text-align: left">40</td>
      <td style="text-align: left">San Antonio &amp; Austin</td>
    </tr>
    <tr>
      <td style="text-align: left">41</td>
      <td style="text-align: left">N. California/N. Nevada</td>
    </tr>
    <tr>
      <td style="text-align: left">42</td>
      <td style="text-align: left">Greater Seattle Area</td>
    </tr>
    <tr>
      <td style="text-align: left">43</td>
      <td style="text-align: left">North &amp; South Dakota</td>
    </tr>
    <tr>
      <td style="text-align: left">44</td>
      <td style="text-align: left">Upstate New York</td>
    </tr>
    <tr>
      <td style="text-align: left">45</td>
      <td style="text-align: left">Utah &amp; Montana</td>
    </tr>
    <tr>
      <td style="text-align: left">46</td>
      <td style="text-align: left">Virginia</td>
    </tr>
    <tr>
      <td style="text-align: left">47</td>
      <td style="text-align: left">Washington, DC and Maryland</td>
    </tr>
    <tr>
      <td style="text-align: left">48</td>
      <td style="text-align: left">West Virginia</td>
    </tr>
    <tr>
      <td style="text-align: left">49</td>
      <td style="text-align: left">Hawaii</td>
    </tr>
    <tr>
      <td style="text-align: left">50</td>
      <td style="text-align: left">Alaska</td>
    </tr>
    <tr>
      <td style="text-align: left">51</td>
      <td style="text-align: left">All of US</td>
    </tr>
    <tr>
      <td style="text-align: left">52</td>
      <td style="text-align: left">Nebraska</td>
    </tr>
    <tr>
      <td style="text-align: left">53</td>
      <td style="text-align: left">Springfield</td>
    </tr>
    <tr>
      <td style="text-align: left">54</td>
      <td style="text-align: left">Central Illinois</td>
    </tr>
    <tr>
      <td style="text-align: left">55</td>
      <td style="text-align: left">Northern New Jersey</td>
    </tr>
    <tr>
      <td style="text-align: left">121</td>
      <td style="text-align: left">South Carolina</td>
    </tr>
    <tr>
      <td style="text-align: left">122</td>
      <td style="text-align: left">South Texas</td>
    </tr>
    <tr>
      <td style="text-align: left">123</td>
      <td style="text-align: left">Beaumont</td>
    </tr>
    <tr>
      <td style="text-align: left">124</td>
      <td style="text-align: left">Connecticut</td>
    </tr>
    <tr>
      <td style="text-align: left">125</td>
      <td style="text-align: left">Oklahoma</td>
    </tr>
  </tbody>
</table>

<h4 id="canada">Canada</h4>

<table>
  <thead>
    <tr>
      <th style="text-align: left">ID</th>
      <th style="text-align: left">Market</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align: left">101</td>
      <td style="text-align: left">All of Canada</td>
    </tr>
    <tr>
      <td style="text-align: left">102</td>
      <td style="text-align: left">Toronto, Hamilton &amp; Area</td>
    </tr>
    <tr>
      <td style="text-align: left">103</td>
      <td style="text-align: left">Ottawa &amp; Eastern Ontario</td>
    </tr>
    <tr>
      <td style="text-align: left">106</td>
      <td style="text-align: left">Manitoba</td>
    </tr>
    <tr>
      <td style="text-align: left">107</td>
      <td style="text-align: left">Edmonton &amp; Northern Alberta</td>
    </tr>
    <tr>
      <td style="text-align: left">108</td>
      <td style="text-align: left">Calgary &amp; Southern Alberta</td>
    </tr>
    <tr>
      <td style="text-align: left">110</td>
      <td style="text-align: left">B.C. Interior</td>
    </tr>
    <tr>
      <td style="text-align: left">111</td>
      <td style="text-align: left">Vancouver &amp; Area</td>
    </tr>
    <tr>
      <td style="text-align: left">112</td>
      <td style="text-align: left">Saskatchewan</td>
    </tr>
    <tr>
      <td style="text-align: left">120</td>
      <td style="text-align: left">Montréal &amp; Area</td>
    </tr>
  </tbody>
</table>

<h4 id="europe">Europe</h4>

<table>
  <thead>
    <tr>
      <th style="text-align: left">ID</th>
      <th style="text-align: left">Market</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align: left">201</td>
      <td style="text-align: left">All of United Kingdom</td>
    </tr>
    <tr>
      <td style="text-align: left">202</td>
      <td style="text-align: left">London</td>
    </tr>
    <tr>
      <td style="text-align: left">203</td>
      <td style="text-align: left">South</td>
    </tr>
    <tr>
      <td style="text-align: left">204</td>
      <td style="text-align: left">Midlands and Central</td>
    </tr>
    <tr>
      <td style="text-align: left">205</td>
      <td style="text-align: left">Wales and North West</td>
    </tr>
    <tr>
      <td style="text-align: left">206</td>
      <td style="text-align: left">North and North East</td>
    </tr>
    <tr>
      <td style="text-align: left">207</td>
      <td style="text-align: left">Scotland</td>
    </tr>
    <tr>
      <td style="text-align: left">208</td>
      <td style="text-align: left">Ireland</td>
    </tr>
    <tr>
      <td style="text-align: left">209</td>
      <td style="text-align: left">Northern Ireland</td>
    </tr>
    <tr>
      <td style="text-align: left">210</td>
      <td style="text-align: left">Germany</td>
    </tr>
    <tr>
      <td style="text-align: left">211</td>
      <td style="text-align: left">Netherlands</td>
    </tr>
    <tr>
      <td style="text-align: left">500</td>
      <td style="text-align: left">Sweden</td>
    </tr>
    <tr>
      <td style="text-align: left">501</td>
      <td style="text-align: left">Todas las poblaciones</td>
    </tr>
    <tr>
      <td style="text-align: left">502</td>
      <td style="text-align: left">Barcelona</td>
    </tr>
    <tr>
      <td style="text-align: left">503</td>
      <td style="text-align: left">Madrid</td>
    </tr>
    <tr>
      <td style="text-align: left">600</td>
      <td style="text-align: left">Turkey</td>
    </tr>
  </tbody>
</table>

<h4 id="australia-and-new-zealand">Australia and New Zealand</h4>

<table>
  <thead>
    <tr>
      <th style="text-align: left">ID</th>
      <th style="text-align: left">Market</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align: left">301</td>
      <td style="text-align: left">All of Australia</td>
    </tr>
    <tr>
      <td style="text-align: left">302</td>
      <td style="text-align: left">New South Wales/Australian Capital Territory</td>
    </tr>
    <tr>
      <td style="text-align: left">303</td>
      <td style="text-align: left">Queensland</td>
    </tr>
    <tr>
      <td style="text-align: left">304</td>
      <td style="text-align: left">Western Australi</td>
    </tr>
    <tr>
      <td style="text-align: left">305</td>
      <td style="text-align: left">Victoria/Tasmania</td>
    </tr>
    <tr>
      <td style="text-align: left">306</td>
      <td style="text-align: left">Western Australia</td>
    </tr>
    <tr>
      <td style="text-align: left">350</td>
      <td style="text-align: left">All of New Zealand</td>
    </tr>
    <tr>
      <td style="text-align: left">351</td>
      <td style="text-align: left">North Island</td>
    </tr>
    <tr>
      <td style="text-align: left">352</td>
      <td style="text-align: left">South Island</td>
    </tr>
  </tbody>
</table>

<h4 id="mexico">Mexico</h4>

<table>
  <thead>
    <tr>
      <th style="text-align: left">ID</th>
      <th style="text-align: left">Market</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align: left">401</td>
      <td style="text-align: left">All of Mexico</td>
    </tr>
    <tr>
      <td style="text-align: left">402</td>
      <td style="text-align: left">Mexico City and Metropolitan Area</td>
    </tr>
    <tr>
      <td style="text-align: left">403</td>
      <td style="text-align: left">Monterrey</td>
    </tr>
    <tr>
      <td style="text-align: left">404</td>
      <td style="text-align: left">Guadalajara</td>
    </tr>
  </tbody>
</table>


<h2 class="article" id="supported-sources">Supported Sources</h2>

<table>
  <thead>
    <tr>
      <th style="text-align: left">Source</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align: left">ticketmaster</td>
    </tr>
    <tr>
      <td style="text-align: left">universe</td>
    </tr>
    <tr>
      <td style="text-align: left">ticketweb</td>
    </tr>
  </tbody>
</table>

<h2 class="article" id="supported-locales">Supported Locales</h2>

<table>
  <thead>
    <tr>
      <th style="text-align: left">Locale</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align: left">en-us</td>
    </tr>
    <tr>
      <td style="text-align: left">en-au</td>
    </tr>
    <tr>
      <td style="text-align: left">en-gb</td>
    </tr>
    <tr>
      <td style="text-align: left">en-nz</td>
    </tr>
    <tr>
      <td style="text-align: left">en-mx</td>
    </tr>
    <tr>
      <td style="text-align: left">en-ca</td>
    </tr>
    <tr>
      <td style="text-align: left">es-us</td>
    </tr>
    <tr>
      <td style="text-align: left">es-mx</td>
    </tr>
    <tr>
      <td style="text-align: left">fr-fr</td>
    </tr>
    <tr>
      <td style="text-align: left">fr-ca</td>
    </tr>
  </tbody>
</table>

                </div>
            </div>
        </div>
    </div>

</div>

<div id="footer" class="xs-center slice-top-left">
<div class="row footer-nav">
    <div class="row-container">
        <div class="col-xs-12 col-sm-2">
            <a href="/products-and-docs/"><h4 class="white">Products & Docs</h4></a>
            <ul>
                <li><a href="/products-and-docs/apis/getting-started/">APIs</a></li>
                <li><a href="/products-and-docs/sdks/">SDKs</a></li>
                <li><a href="/products-and-docs/widgets/">Widgets</a></li>
            </ul>
        </div>
        <div class="col-xs-12 col-sm-2">
            <a href="/partners/"><h4 class="white">Partners</h4></a>
            <ul>
                <li><a href="/partners/distribution-partners/">Distribution Partners</a></li>
                <li><a href="/partners/certified-partners/">Certified Partners </a></li>
                <li><a href="https://darwin.affiliatewindow.com/login">Affiliates</a></li>
                <li><a href="/partners/startups-and-developers/">Startups & Developers</a></li>
            </ul>
        </div>
        <div class="col-xs-12 col-sm-2">
            <a href="/support/"><h4 class="white">Support</h4></a>
            <ul>
                <li><a href="/support/faq/">FAQ</a></li>
                <li><a href="http://stackoverflow.com/questions/tagged/ticketmaster-api/ ">Forums</a></li>
                <li><a href="/support/terms-of-use/">General Terms of Use</a></li>
                <li><a href="/support/terms-of-use/partner/">Partner API Terms of Use</a></li>
                <li><a href="/support/branding-guide/">Branding Guide</a></li>
            </ul>
        </div>
        <div class="col-xs-12 col-sm-2">
            <a href="/blogs/"><h4 class="white">Blogs</h4></a>
            <ul>
                <li><a href="http://tech.ticketmaster.com/">Tech Blog</a></li>
                <li><a href="https://medium.com/ticketmaster-tech/">Medium Publication</a></li>
            </ul>
        </div>
        <div class="col-xs-12 col-sm-2">
            <a href="/events/"><h4 class="white">Events</h4></a>
            <ul>
                <li><a href="/events/#hackathon">hackatons</a></li>
                <li><a href="/events/#devjam">devjam</a></li>
            </ul>
        </div>
        <div class="col-xs-12 col-sm-2">
            <a href="http://code.ticketmaster.com/"><h4 class="white">Open Source</h4></a>
            <ul>
                <li><a href="http://code.ticketmaster.com/#android-projects">Android</a></li>
                <li><a href="http://code.ticketmaster.com/#backend-projects">Backend</a></li>
                <li><a href="http://code.ticketmaster.com/#iOS-projects">iOS</a></li>
                <li><a href="http://code.ticketmaster.com/#web-projects">Web</a></li>
            </ul>
        </div>
    </div>
</div>
<div class="row bottom-logo" style="margin-bottom: 10px;">
    <div class="row-container">
        <div class="col-xs-12">
            <a href="/">
            <img alt="Ticketmaster logo" src="/assets/img/footer/ticketmaster-logo-white.svg">
            </a>
            <span>© 1976–2016 Ticketmaster. All rights reserved.</span>
        </div>
    </div>
</div>
</div>


<div class="modal fs-modal modal-langs" tabindex="-1" role="dialog" aria-labelledby="search-events">
    <div class="modal-dialog">
        <div class="modal-content">
            <div class="modal-header">
                <button aria-label="Close" data-dismiss="modal" class="close" type="button"><span aria-hidden="true">×</span></button>
                <h4 id="modal-title" class="modal-title"></h4>
            </div>
            <div class="modal-body">
                <div class="highlight"></div>
            </div>
        </div>
    </div>
    <textarea name="copy-clip" id="copy-clip" class="copy-clip"></textarea>
</div>

<script src="/scripts/components/parser.js"></script>
<script src="/scripts/vendors/clipboard.js"></script>
<script src="/scripts/vendors/user-scroll-disabler.js"></script>
<script src="/scripts/components/pd-side-menu.js"></script>
<script src="/scripts/components/menu-highlight.js"></script>
<script src="/scripts/components/request-response.js"></script>
<script src="/scripts/components/table-collapse.js"></script>
<script src="/scripts/vendors/jstree.min.js"></script>
<script src="/scripts/components/list-collapse.js"></script>


<script>
    new Clipboard('.copy-btn');
</script>

        <div id="back-top">
            <a href="javascript:void(0)"><span></span></a>
        </div>
        <script>
            (function(i,s,o,g,r,a,m){i['GoogleAnalyticsObject']=r;i[r]=i[r]||function(){
                    (i[r].q=i[r].q||[]).push(arguments)},i[r].l=1*new Date();a=s.createElement(o),
                  m=s.getElementsByTagName(o)[0];a.async=1;a.src=g;m.parentNode.insertBefore(a,m)
            })(window,document,'script','//www.google-analytics.com/analytics.js','ga');
            ga('create', 'UA-72344127-1', 'auto');
            ga('send', 'pageview');
        </script>
        <script src="/scripts/components/scroll-top.js"></script>
        <script src="/scripts/vendors/bootstrap.min.js"></script>
        

<div class="modal fade" id="feedback-modal" tabindex="-1" role="dialog">
  <div class="modal-dialog">
    <div class="modal-content">
      <div class="modal-header">
        <button type="button" class="close" data-dismiss="modal" aria-label="Close"></button>
        <h3 class="modal-title col-lg-12">Leave Your Feedback</h3>
      </div>
      <div class="modal-body">

        <form id="js_feedback_form" accept-charset="UTF-8" action="http://getsimpleform.com/messages/ajax?form_api_token=d9878ccc8e22c7253d057015617f82cd" method="POST">
          <div class="col-lg-6">
            <label for="name">Your name</label>
            <input required type="text" id="name" name="name" maxlength="255" autofocus >
          </div>
          <div class="col-lg-6">
            <label for="email">Your email</label>
            <input type="email" id="email" name="email" required pattern="[A-Za-z0-9._%+-]+@[A-Za-z0-9.-]+\.[A-Za-z]{2,3}$">
          </div>
          <div class="col-lg-12">
            <label for="subject">Subject</label>
            <div class="js_custom_select custom_select">
              <select required class="custom_select__field" name="subject" id="subject">
                <option value="General feedback">General feedback</option>
                <option value="Current workflow of the portal">Current workflow of the portal</option>
                <option value="Technical issues">Technical issues</option>
              </select>
              <input class="custom_select__placeholder" type="text" value="General feedback" readonly>
              <ul class="custom_select__list">
                <li class="custom_select__item" data-value="General feedback">General feedback</li>
                <li class="custom_select__item" data-value="Current workflow of the portal">Current workflow of the portal</li>
                <li class="custom_select__item" data-value="Technical issues">Technical issues</li>
              </ul>
            </div>
          </div>
          <div class="col-lg-12">
            <label for="description">Description</label>
            <textarea required rows="3" name="description" id="description"></textarea>
          </div>
        </form>

      </div>
      <div class="modal-footer">
        <button id="js_feedback_btn" type="button" class="btn btn-submit">send</button>
      </div>



    </div><!-- /.modal-content -->
  </div><!-- /.modal-dialog -->
</div><!-- /.modal -->



<!-- Button trigger modal -->
<button id="js_feedback_open" type="button" class="btn feedback-btn" data-toggle="modal" data-target="#feedback-modal">feedback</button>


<!-- Modal alert-->
<div id="feedback-alert-modal" class="modal fade" role="dialog">
  <div class="modal-dialog">

    <!-- Modal content-->
    <div class="modal-content">
      <div class="modal-body">
        <h3 class="modal-title col-lg-12 text-center">Thank you for contacting us!</h3>
        <p class="text-center">We will review and respond promptly.</p>
        <div class="modal-footer">
          <button id="js_feedback_btn_alert_ok" type="button" class="btn btn-submit text-center">Ok</button>
        </div>
      </div>
    </div>

  </div>
</div>
<!-- Modal alert end-->
        <script src="/scripts/components/custom-select.js"></script>
        <script src="/scripts/components/feedback.js"></script>

    </body>
</html>
