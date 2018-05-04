

```python
from bs4 import BeautifulSoup
import requests
import pymongo
```


```python
url = 'https://mars.nasa.gov/news/'
response = requests.get(url)
soup = BeautifulSoup(response.text, 'html.parser')
```


```python
print(soup.prettify())
```

    <!DOCTYPE html>
    <!--[if lte IE 9]> <p class="browsehappy">You are using an <strong>outdated</strong> browser. Please <a href="http://browsehappy.com/">upgrade your browser</a> to improve your experience.</p> <![endif]-->
    <html lang="en" xml:lang="en" xmlns="http://www.w3.org/1999/xhtml">
     <head>
      <meta content="text/html; charset=utf-8" http-equiv="Content-Type"/>
      <!-- Always force latest IE rendering engine or request Chrome Frame -->
      <meta content="IE=edge,chrome=1" http-equiv="X-UA-Compatible"/>
      <script type="text/javascript">
       window.NREUM||(NREUM={});NREUM.info={"beacon":"bam.nr-data.net","errorBeacon":"bam.nr-data.net","licenseKey":"5e33925808","applicationID":"59562082","transactionName":"JVcPR0MLWApSRU1eAQVVEhxSC1oSUlkWbBMHXwRAHhdcCUA=","queueTime":0,"applicationTime":153,"agent":""}
      </script>
      <script type="text/javascript">
       (window.NREUM||(NREUM={})).loader_config={xpid:"VQcPUlZTDxAFXVRUBQEPVA=="};window.NREUM||(NREUM={}),__nr_require=function(t,n,e){function r(e){if(!n[e]){var o=n[e]={exports:{}};t[e][0].call(o.exports,function(n){var o=t[e][1][n];return r(o||n)},o,o.exports)}return n[e].exports}if("function"==typeof __nr_require)return __nr_require;for(var o=0;o<e.length;o++)r(e[o]);return r}({1:[function(t,n,e){function r(t){try{s.console&&console.log(t)}catch(n){}}var o,i=t("ee"),a=t(15),s={};try{o=localStorage.getItem("__nr_flags").split(","),console&&"function"==typeof console.log&&(s.console=!0,o.indexOf("dev")!==-1&&(s.dev=!0),o.indexOf("nr_dev")!==-1&&(s.nrDev=!0))}catch(c){}s.nrDev&&i.on("internal-error",function(t){r(t.stack)}),s.dev&&i.on("fn-err",function(t,n,e){r(e.stack)}),s.dev&&(r("NR AGENT IN DEVELOPMENT MODE"),r("flags: "+a(s,function(t,n){return t}).join(", ")))},{}],2:[function(t,n,e){function r(t,n,e,r,s){try{p?p-=1:o(s||new UncaughtException(t,n,e),!0)}catch(f){try{i("ierr",[f,c.now(),!0])}catch(d){}}return"function"==typeof u&&u.apply(this,a(arguments))}function UncaughtException(t,n,e){this.message=t||"Uncaught error with no additional information",this.sourceURL=n,this.line=e}function o(t,n){var e=n?null:c.now();i("err",[t,e])}var i=t("handle"),a=t(16),s=t("ee"),c=t("loader"),f=t("gos"),u=window.onerror,d=!1,l="nr@seenError",p=0;c.features.err=!0,t(1),window.onerror=r;try{throw new Error}catch(h){"stack"in h&&(t(8),t(7),"addEventListener"in window&&t(5),c.xhrWrappable&&t(9),d=!0)}s.on("fn-start",function(t,n,e){d&&(p+=1)}),s.on("fn-err",function(t,n,e){d&&!e[l]&&(f(e,l,function(){return!0}),this.thrown=!0,o(e))}),s.on("fn-end",function(){d&&!this.thrown&&p>0&&(p-=1)}),s.on("internal-error",function(t){i("ierr",[t,c.now(),!0])})},{}],3:[function(t,n,e){t("loader").features.ins=!0},{}],4:[function(t,n,e){function r(t){}if(window.performance&&window.performance.timing&&window.performance.getEntriesByType){var o=t("ee"),i=t("handle"),a=t(8),s=t(7),c="learResourceTimings",f="addEventListener",u="resourcetimingbufferfull",d="bstResource",l="resource",p="-start",h="-end",m="fn"+p,w="fn"+h,v="bstTimer",y="pushState",g=t("loader");g.features.stn=!0,t(6);var b=NREUM.o.EV;o.on(m,function(t,n){var e=t[0];e instanceof b&&(this.bstStart=g.now())}),o.on(w,function(t,n){var e=t[0];e instanceof b&&i("bst",[e,n,this.bstStart,g.now()])}),a.on(m,function(t,n,e){this.bstStart=g.now(),this.bstType=e}),a.on(w,function(t,n){i(v,[n,this.bstStart,g.now(),this.bstType])}),s.on(m,function(){this.bstStart=g.now()}),s.on(w,function(t,n){i(v,[n,this.bstStart,g.now(),"requestAnimationFrame"])}),o.on(y+p,function(t){this.time=g.now(),this.startPath=location.pathname+location.hash}),o.on(y+h,function(t){i("bstHist",[location.pathname+location.hash,this.startPath,this.time])}),f in window.performance&&(window.performance["c"+c]?window.performance[f](u,function(t){i(d,[window.performance.getEntriesByType(l)]),window.performance["c"+c]()},!1):window.performance[f]("webkit"+u,function(t){i(d,[window.performance.getEntriesByType(l)]),window.performance["webkitC"+c]()},!1)),document[f]("scroll",r,{passive:!0}),document[f]("keypress",r,!1),document[f]("click",r,!1)}},{}],5:[function(t,n,e){function r(t){for(var n=t;n&&!n.hasOwnProperty(u);)n=Object.getPrototypeOf(n);n&&o(n)}function o(t){s.inPlace(t,[u,d],"-",i)}function i(t,n){return t[1]}var a=t("ee").get("events"),s=t(18)(a,!0),c=t("gos"),f=XMLHttpRequest,u="addEventListener",d="removeEventListener";n.exports=a,"getPrototypeOf"in Object?(r(document),r(window),r(f.prototype)):f.prototype.hasOwnProperty(u)&&(o(window),o(f.prototype)),a.on(u+"-start",function(t,n){var e=t[1],r=c(e,"nr@wrapped",function(){function t(){if("function"==typeof e.handleEvent)return e.handleEvent.apply(e,arguments)}var n={object:t,"function":e}[typeof e];return n?s(n,"fn-",null,n.name||"anonymous"):e});this.wrapped=t[1]=r}),a.on(d+"-start",function(t){t[1]=this.wrapped||t[1]})},{}],6:[function(t,n,e){var r=t("ee").get("history"),o=t(18)(r);n.exports=r,o.inPlace(window.history,["pushState","replaceState"],"-")},{}],7:[function(t,n,e){var r=t("ee").get("raf"),o=t(18)(r),i="equestAnimationFrame";n.exports=r,o.inPlace(window,["r"+i,"mozR"+i,"webkitR"+i,"msR"+i],"raf-"),r.on("raf-start",function(t){t[0]=o(t[0],"fn-")})},{}],8:[function(t,n,e){function r(t,n,e){t[0]=a(t[0],"fn-",null,e)}function o(t,n,e){this.method=e,this.timerDuration=isNaN(t[1])?0:+t[1],t[0]=a(t[0],"fn-",this,e)}var i=t("ee").get("timer"),a=t(18)(i),s="setTimeout",c="setInterval",f="clearTimeout",u="-start",d="-";n.exports=i,a.inPlace(window,[s,"setImmediate"],s+d),a.inPlace(window,[c],c+d),a.inPlace(window,[f,"clearImmediate"],f+d),i.on(c+u,r),i.on(s+u,o)},{}],9:[function(t,n,e){function r(t,n){d.inPlace(n,["onreadystatechange"],"fn-",s)}function o(){var t=this,n=u.context(t);t.readyState>3&&!n.resolved&&(n.resolved=!0,u.emit("xhr-resolved",[],t)),d.inPlace(t,y,"fn-",s)}function i(t){g.push(t),h&&(x?x.then(a):w?w(a):(E=-E,O.data=E))}function a(){for(var t=0;t<g.length;t++)r([],g[t]);g.length&&(g=[])}function s(t,n){return n}function c(t,n){for(var e in t)n[e]=t[e];return n}t(5);var f=t("ee"),u=f.get("xhr"),d=t(18)(u),l=NREUM.o,p=l.XHR,h=l.MO,m=l.PR,w=l.SI,v="readystatechange",y=["onload","onerror","onabort","onloadstart","onloadend","onprogress","ontimeout"],g=[];n.exports=u;var b=window.XMLHttpRequest=function(t){var n=new p(t);try{u.emit("new-xhr",[n],n),n.addEventListener(v,o,!1)}catch(e){try{u.emit("internal-error",[e])}catch(r){}}return n};if(c(p,b),b.prototype=p.prototype,d.inPlace(b.prototype,["open","send"],"-xhr-",s),u.on("send-xhr-start",function(t,n){r(t,n),i(n)}),u.on("open-xhr-start",r),h){var x=m&&m.resolve();if(!w&&!m){var E=1,O=document.createTextNode(E);new h(a).observe(O,{characterData:!0})}}else f.on("fn-end",function(t){t[0]&&t[0].type===v||a()})},{}],10:[function(t,n,e){function r(t){var n=this.params,e=this.metrics;if(!this.ended){this.ended=!0;for(var r=0;r<d;r++)t.removeEventListener(u[r],this.listener,!1);if(!n.aborted){if(e.duration=a.now()-this.startTime,4===t.readyState){n.status=t.status;var i=o(t,this.lastSize);if(i&&(e.rxSize=i),this.sameOrigin){var c=t.getResponseHeader("X-NewRelic-App-Data");c&&(n.cat=c.split(", ").pop())}}else n.status=0;e.cbTime=this.cbTime,f.emit("xhr-done",[t],t),s("xhr",[n,e,this.startTime])}}}function o(t,n){var e=t.responseType;if("json"===e&&null!==n)return n;var r="arraybuffer"===e||"blob"===e||"json"===e?t.response:t.responseText;return h(r)}function i(t,n){var e=c(n),r=t.params;r.host=e.hostname+":"+e.port,r.pathname=e.pathname,t.sameOrigin=e.sameOrigin}var a=t("loader");if(a.xhrWrappable){var s=t("handle"),c=t(11),f=t("ee"),u=["load","error","abort","timeout"],d=u.length,l=t("id"),p=t(14),h=t(13),m=window.XMLHttpRequest;a.features.xhr=!0,t(9),f.on("new-xhr",function(t){var n=this;n.totalCbs=0,n.called=0,n.cbTime=0,n.end=r,n.ended=!1,n.xhrGuids={},n.lastSize=null,p&&(p>34||p<10)||window.opera||t.addEventListener("progress",function(t){n.lastSize=t.loaded},!1)}),f.on("open-xhr-start",function(t){this.params={method:t[0]},i(this,t[1]),this.metrics={}}),f.on("open-xhr-end",function(t,n){"loader_config"in NREUM&&"xpid"in NREUM.loader_config&&this.sameOrigin&&n.setRequestHeader("X-NewRelic-ID",NREUM.loader_config.xpid)}),f.on("send-xhr-start",function(t,n){var e=this.metrics,r=t[0],o=this;if(e&&r){var i=h(r);i&&(e.txSize=i)}this.startTime=a.now(),this.listener=function(t){try{"abort"===t.type&&(o.params.aborted=!0),("load"!==t.type||o.called===o.totalCbs&&(o.onloadCalled||"function"!=typeof n.onload))&&o.end(n)}catch(e){try{f.emit("internal-error",[e])}catch(r){}}};for(var s=0;s<d;s++)n.addEventListener(u[s],this.listener,!1)}),f.on("xhr-cb-time",function(t,n,e){this.cbTime+=t,n?this.onloadCalled=!0:this.called+=1,this.called!==this.totalCbs||!this.onloadCalled&&"function"==typeof e.onload||this.end(e)}),f.on("xhr-load-added",function(t,n){var e=""+l(t)+!!n;this.xhrGuids&&!this.xhrGuids[e]&&(this.xhrGuids[e]=!0,this.totalCbs+=1)}),f.on("xhr-load-removed",function(t,n){var e=""+l(t)+!!n;this.xhrGuids&&this.xhrGuids[e]&&(delete this.xhrGuids[e],this.totalCbs-=1)}),f.on("addEventListener-end",function(t,n){n instanceof m&&"load"===t[0]&&f.emit("xhr-load-added",[t[1],t[2]],n)}),f.on("removeEventListener-end",function(t,n){n instanceof m&&"load"===t[0]&&f.emit("xhr-load-removed",[t[1],t[2]],n)}),f.on("fn-start",function(t,n,e){n instanceof m&&("onload"===e&&(this.onload=!0),("load"===(t[0]&&t[0].type)||this.onload)&&(this.xhrCbStart=a.now()))}),f.on("fn-end",function(t,n){this.xhrCbStart&&f.emit("xhr-cb-time",[a.now()-this.xhrCbStart,this.onload,n],n)})}},{}],11:[function(t,n,e){n.exports=function(t){var n=document.createElement("a"),e=window.location,r={};n.href=t,r.port=n.port;var o=n.href.split("://");!r.port&&o[1]&&(r.port=o[1].split("/")[0].split("@").pop().split(":")[1]),r.port&&"0"!==r.port||(r.port="https"===o[0]?"443":"80"),r.hostname=n.hostname||e.hostname,r.pathname=n.pathname,r.protocol=o[0],"/"!==r.pathname.charAt(0)&&(r.pathname="/"+r.pathname);var i=!n.protocol||":"===n.protocol||n.protocol===e.protocol,a=n.hostname===document.domain&&n.port===e.port;return r.sameOrigin=i&&(!n.hostname||a),r}},{}],12:[function(t,n,e){function r(){}function o(t,n,e){return function(){return i(t,[f.now()].concat(s(arguments)),n?null:this,e),n?void 0:this}}var i=t("handle"),a=t(15),s=t(16),c=t("ee").get("tracer"),f=t("loader"),u=NREUM;"undefined"==typeof window.newrelic&&(newrelic=u);var d=["setPageViewName","setCustomAttribute","setErrorHandler","finished","addToTrace","inlineHit","addRelease"],l="api-",p=l+"ixn-";a(d,function(t,n){u[n]=o(l+n,!0,"api")}),u.addPageAction=o(l+"addPageAction",!0),u.setCurrentRouteName=o(l+"routeName",!0),n.exports=newrelic,u.interaction=function(){return(new r).get()};var h=r.prototype={createTracer:function(t,n){var e={},r=this,o="function"==typeof n;return i(p+"tracer",[f.now(),t,e],r),function(){if(c.emit((o?"":"no-")+"fn-start",[f.now(),r,o],e),o)try{return n.apply(this,arguments)}catch(t){throw c.emit("fn-err",[arguments,this,t],e),t}finally{c.emit("fn-end",[f.now()],e)}}}};a("setName,setAttribute,save,ignore,onEnd,getContext,end,get".split(","),function(t,n){h[n]=o(p+n)}),newrelic.noticeError=function(t){"string"==typeof t&&(t=new Error(t)),i("err",[t,f.now()])}},{}],13:[function(t,n,e){n.exports=function(t){if("string"==typeof t&&t.length)return t.length;if("object"==typeof t){if("undefined"!=typeof ArrayBuffer&&t instanceof ArrayBuffer&&t.byteLength)return t.byteLength;if("undefined"!=typeof Blob&&t instanceof Blob&&t.size)return t.size;if(!("undefined"!=typeof FormData&&t instanceof FormData))try{return JSON.stringify(t).length}catch(n){return}}}},{}],14:[function(t,n,e){var r=0,o=navigator.userAgent.match(/Firefox[\/\s](\d+\.\d+)/);o&&(r=+o[1]),n.exports=r},{}],15:[function(t,n,e){function r(t,n){var e=[],r="",i=0;for(r in t)o.call(t,r)&&(e[i]=n(r,t[r]),i+=1);return e}var o=Object.prototype.hasOwnProperty;n.exports=r},{}],16:[function(t,n,e){function r(t,n,e){n||(n=0),"undefined"==typeof e&&(e=t?t.length:0);for(var r=-1,o=e-n||0,i=Array(o<0?0:o);++r<o;)i[r]=t[n+r];return i}n.exports=r},{}],17:[function(t,n,e){n.exports={exists:"undefined"!=typeof window.performance&&window.performance.timing&&"undefined"!=typeof window.performance.timing.navigationStart}},{}],18:[function(t,n,e){function r(t){return!(t&&t instanceof Function&&t.apply&&!t[a])}var o=t("ee"),i=t(16),a="nr@original",s=Object.prototype.hasOwnProperty,c=!1;n.exports=function(t,n){function e(t,n,e,o){function nrWrapper(){var r,a,s,c;try{a=this,r=i(arguments),s="function"==typeof e?e(r,a):e||{}}catch(f){l([f,"",[r,a,o],s])}u(n+"start",[r,a,o],s);try{return c=t.apply(a,r)}catch(d){throw u(n+"err",[r,a,d],s),d}finally{u(n+"end",[r,a,c],s)}}return r(t)?t:(n||(n=""),nrWrapper[a]=t,d(t,nrWrapper),nrWrapper)}function f(t,n,o,i){o||(o="");var a,s,c,f="-"===o.charAt(0);for(c=0;c<n.length;c++)s=n[c],a=t[s],r(a)||(t[s]=e(a,f?s+o:o,i,s))}function u(e,r,o){if(!c||n){var i=c;c=!0;try{t.emit(e,r,o,n)}catch(a){l([a,e,r,o])}c=i}}function d(t,n){if(Object.defineProperty&&Object.keys)try{var e=Object.keys(t);return e.forEach(function(e){Object.defineProperty(n,e,{get:function(){return t[e]},set:function(n){return t[e]=n,n}})}),n}catch(r){l([r])}for(var o in t)s.call(t,o)&&(n[o]=t[o]);return n}function l(n){try{t.emit("internal-error",n)}catch(e){}}return t||(t=o),e.inPlace=f,e.flag=a,e}},{}],ee:[function(t,n,e){function r(){}function o(t){function n(t){return t&&t instanceof r?t:t?c(t,s,i):i()}function e(e,r,o,i){if(!l.aborted||i){t&&t(e,r,o);for(var a=n(o),s=h(e),c=s.length,f=0;f<c;f++)s[f].apply(a,r);var d=u[y[e]];return d&&d.push([g,e,r,a]),a}}function p(t,n){v[t]=h(t).concat(n)}function h(t){return v[t]||[]}function m(t){return d[t]=d[t]||o(e)}function w(t,n){f(t,function(t,e){n=n||"feature",y[e]=n,n in u||(u[n]=[])})}var v={},y={},g={on:p,emit:e,get:m,listeners:h,context:n,buffer:w,abort:a,aborted:!1};return g}function i(){return new r}function a(){(u.api||u.feature)&&(l.aborted=!0,u=l.backlog={})}var s="nr@context",c=t("gos"),f=t(15),u={},d={},l=n.exports=o();l.backlog=u},{}],gos:[function(t,n,e){function r(t,n,e){if(o.call(t,n))return t[n];var r=e();if(Object.defineProperty&&Object.keys)try{return Object.defineProperty(t,n,{value:r,writable:!0,enumerable:!1}),r}catch(i){}return t[n]=r,r}var o=Object.prototype.hasOwnProperty;n.exports=r},{}],handle:[function(t,n,e){function r(t,n,e,r){o.buffer([t],r),o.emit(t,n,e)}var o=t("ee").get("handle");n.exports=r,r.ee=o},{}],id:[function(t,n,e){function r(t){var n=typeof t;return!t||"object"!==n&&"function"!==n?-1:t===window?0:a(t,i,function(){return o++})}var o=1,i="nr@id",a=t("gos");n.exports=r},{}],loader:[function(t,n,e){function r(){if(!x++){var t=b.info=NREUM.info,n=l.getElementsByTagName("script")[0];if(setTimeout(u.abort,3e4),!(t&&t.licenseKey&&t.applicationID&&n))return u.abort();f(y,function(n,e){t[n]||(t[n]=e)}),c("mark",["onload",a()+b.offset],null,"api");var e=l.createElement("script");e.src="https://"+t.agent,n.parentNode.insertBefore(e,n)}}function o(){"complete"===l.readyState&&i()}function i(){c("mark",["domContent",a()+b.offset],null,"api")}function a(){return E.exists&&performance.now?Math.round(performance.now()):(s=Math.max((new Date).getTime(),s))-b.offset}var s=(new Date).getTime(),c=t("handle"),f=t(15),u=t("ee"),d=window,l=d.document,p="addEventListener",h="attachEvent",m=d.XMLHttpRequest,w=m&&m.prototype;NREUM.o={ST:setTimeout,SI:d.setImmediate,CT:clearTimeout,XHR:m,REQ:d.Request,EV:d.Event,PR:d.Promise,MO:d.MutationObserver};var v=""+location,y={beacon:"bam.nr-data.net",errorBeacon:"bam.nr-data.net",agent:"js-agent.newrelic.com/nr-1071.min.js"},g=m&&w&&w[p]&&!/CriOS/.test(navigator.userAgent),b=n.exports={offset:s,now:a,origin:v,features:{},xhrWrappable:g};t(12),l[p]?(l[p]("DOMContentLoaded",i,!1),d[p]("load",r,!1)):(l[h]("onreadystatechange",o),d[h]("onload",r)),c("mark",["firstbyte",s],null,"api");var x=0,E=t(17)},{}]},{},["loader",2,10,4,3]);
      </script>
      <!-- Responsiveness -->
      <meta content="width=device-width, initial-scale=1.0" name="viewport"/>
      <!-- Favicon -->
      <link href="/apple-touch-icon.png" rel="apple-touch-icon" sizes="180x180"/>
      <link href="/favicon-32x32.png" rel="icon" sizes="32x32" type="image/png"/>
      <link href="/favicon-16x16.png" rel="icon" sizes="16x16" type="image/png"/>
      <link href="/manifest.json" rel="manifest"/>
      <link color="#e48b55" href="/safari-pinned-tab.svg" rel="mask-icon"/>
      <meta content="#000000" name="theme-color"/>
      <meta content="authenticity_token" name="csrf-param">
       <meta content="Oso/0fgTb5asaXalkgeNO73sd1mhB4aCWfvx9VNGeGk=" name="csrf-token">
        <title>
         NASA’s Mars Exploration Program : News
        </title>
        <meta content="NASA’s Mars Exploration Program " property="og:site_name"/>
        <meta content="mars.nasa.gov" name="author"/>
        <meta content="Mars, missions, NASA, rover, Curiosity, Opportunity, InSight, Mars Reconnaissance Orbiter, facts" name="keywords"/>
        <meta content="NASA’s real-time portal for Mars exploration, featuring the last news, images, and discoveries from the Red Planet." name="description"/>
        <meta content="NASA’s real-time portal for Mars exploration, featuring the last news, images, and discoveries from the Red Planet." property="og:description"/>
        <meta content="NASA’s Mars Exploration Program : News " property="og:title"/>
        <meta content="https://mars.nasa.gov/news" property="og:url"/>
        <meta content="article" property="og:type"/>
        <meta content="2017-09-22 19:53:22 UTC" property="og:updated_time"/>
        <meta content="https://mars.nasa.gov/system/site_config_values/meta_share_images/1_142497main_PIA03154-200.jpg" property="og:image"/>
        <link href="https://mars.nasa.gov/system/site_config_values/meta_share_images/1_142497main_PIA03154-200.jpg" rel="image_src"/>
        <link href="https://fonts.googleapis.com/css?family=Montserrat:200,300,400,500,600,700|Raleway:300,400" rel="stylesheet"/>
        <link href="/assets/public_manifest-574a8376577ebdeea854fd2967ce0bef2e7d5cfd38633c33e8d92aed83e81c3a.css" media="all" rel="stylesheet">
         <link href="/assets/gulp/vendor/jquery.fancybox-364352e03618ba5a8da007665b1f0be31795293b22bc4d7c5974891d4976a137.css" media="screen" rel="stylesheet">
          <link href="/assets/gulp/print-240f8bfaa7f6402dfd6c49ee3c1ffea57a89ddd4c8c90e2f2a5c7d63c5753e32.css" media="print" rel="stylesheet">
           <script src="/assets/public_manifest-eed54cbc0cf59efc6cd5645db8873a28b8feb4489dd1ea1c3842a65c1a1d5dee.js">
           </script>
           <!--[if gt IE 8]><!-->
           <script src="/assets/not_ie8_manifest.js">
           </script>
           <!--[if !IE]>-->
           <script src="/assets/not_ie8_manifest.js">
           </script>
           <!--<![endif]-->
           <script src="/assets/vendor/jquery.fancybox-9d361e5f98a5c0f233a25df9252dbadea6897af1c0ef221d7465e1205941ea0d.js">
           </script>
           <script src="/assets/mb_manifest-beb93a6fa0c9c378ceac4ff575efdfe599ad319d75eef30bf6c6cd48e1ccfc26.js">
           </script>
           <!-- /twitter cards -->
           <meta content="summary_large_image" name="twitter:card"/>
           <meta content="News " name="twitter:title"/>
           <meta content="NASA’s real-time portal for Mars exploration, featuring the last news, images, and discoveries from the Red Planet." name="twitter:description"/>
           <meta content="https://mars.nasa.gov/system/site_config_values/meta_share_images/1_142497main_PIA03154-200.jpg" name="twitter:image"/>
          </link>
         </link>
        </link>
       </meta>
      </meta>
     </head>
     <body id="news">
      <div id="main_container">
       <div id="site_body">
        <div class="site_header_area">
         <header class="site_header">
          <div class="brand_area">
           <div class="brand1">
            <a class="nasa_logo" href="http://www.nasa.gov" target="_blank" title="visit nasa.gov">
             NASA
            </a>
           </div>
           <div class="brand2">
            <a class="top_logo" href="https://science.nasa.gov/" target="_blank" title="Explore NASA Science">
             NASA Science
            </a>
            <a class="sub_logo" href="/mars-exploration/#" title="Mars">
             Mars Exploration Program
            </a>
           </div>
           <img alt="" class="print_only print_logo" src="/assets/logo_nasa_trio_black@2x.png"/>
          </div>
          <a class="visuallyhidden focusable" href="#page">
           Skip Navigation
          </a>
          <div class="right_header_container">
           <a class="menu_button" href="javascript:void(0);" id="menu_button">
            <span class="menu_icon">
             menu
            </span>
           </a>
           <a class="modal_close" id="modal_close">
            <span class="modal_close_icon">
            </span>
           </a>
          </div>
          <div class="nav_area">
           <div id="site_nav_container">
            <nav class="site_nav">
             <ul class="nav">
              <li>
               <div class="arrow_box">
                <span class="arrow_down">
                </span>
               </div>
               <div class="nav_title">
                <a class="main_nav_item" href="/#red_planet" target="_self">
                 The Red Planet
                </a>
               </div>
               <div class="global_subnav_container">
                <ul class="subnav">
                 <li>
                  <a href="/#red_planet/0" target="_self">
                   Dashboard
                  </a>
                 </li>
                 <li>
                  <a href="/#red_planet/1" target="_self">
                   Science Goals
                  </a>
                 </li>
                 <li>
                  <a href="/#red_planet/2" target="_self">
                   The Planet
                  </a>
                 </li>
                 <li>
                  <a href="/#red_planet/3" target="_self">
                   Atmosphere
                  </a>
                 </li>
                 <li>
                  <a href="/#red_planet/4" target="_self">
                   Astrobiology
                  </a>
                 </li>
                 <li>
                  <a href="/#red_planet/5" target="_self">
                   Past, Present, Future, Timeline
                  </a>
                 </li>
                </ul>
               </div>
               <div class="gradient_line">
               </div>
              </li>
              <li>
               <div class="arrow_box">
                <span class="arrow_down">
                </span>
               </div>
               <div class="nav_title">
                <a class="main_nav_item" href="/#mars_exploration_program" target="_self">
                 The Program
                </a>
               </div>
               <div class="global_subnav_container">
                <ul class="subnav">
                 <li>
                  <a href="/#mars_exploration_program/0" target="_self">
                   Mission Statement
                  </a>
                 </li>
                 <li>
                  <a href="/#mars_exploration_program/1" target="_self">
                   About the Program
                  </a>
                 </li>
                 <li>
                  <a href="/#mars_exploration_program/2" target="_self">
                   Organization
                  </a>
                 </li>
                 <li>
                  <a href="/#mars_exploration_program/3" target="_self">
                   Why Mars?
                  </a>
                 </li>
                 <li>
                  <a href="/#mars_exploration_program/4" target="_self">
                   Research Programs
                  </a>
                 </li>
                 <li>
                  <a href="/#mars_exploration_program/5" target="_self">
                   Planetary Resources
                  </a>
                 </li>
                 <li>
                  <a href="/#mars_exploration_program/6" target="_self">
                   Technologies
                  </a>
                 </li>
                </ul>
               </div>
               <div class="gradient_line">
               </div>
              </li>
              <li>
               <div class="arrow_box">
                <span class="arrow_down">
                </span>
               </div>
               <div class="nav_title">
                <a class="main_nav_item" href="/#news_and_events" target="_self">
                 News &amp; Events
                </a>
               </div>
               <div class="global_subnav_container">
                <ul class="subnav">
                 <li class="current">
                  <a href="/news" target="_self">
                   News
                  </a>
                 </li>
                 <li>
                  <a href="/events" target="_self">
                   Events
                  </a>
                 </li>
                </ul>
               </div>
               <div class="gradient_line">
               </div>
              </li>
              <li>
               <div class="arrow_box">
                <span class="arrow_down">
                </span>
               </div>
               <div class="nav_title">
                <a class="main_nav_item" href="/#multimedia" target="_self">
                 Multimedia
                </a>
               </div>
               <div class="global_subnav_container">
                <ul class="subnav">
                 <li>
                  <a href="/multimedia/images/" target="_self">
                   Images
                  </a>
                 </li>
                 <li>
                  <a href="/multimedia/videos/" target="_self">
                   Videos
                  </a>
                 </li>
                </ul>
               </div>
               <div class="gradient_line">
               </div>
              </li>
              <li>
               <div class="arrow_box">
                <span class="arrow_down">
                </span>
               </div>
               <div class="nav_title">
                <a class="main_nav_item" href="/#missions" target="_self">
                 Missions
                </a>
               </div>
               <div class="global_subnav_container">
                <ul class="subnav">
                 <li>
                  <a href="/mars-exploration/missions/?category=167" target="_self">
                   Past
                  </a>
                 </li>
                 <li>
                  <a href="/mars-exploration/missions/?category=170" target="_self">
                   Present
                  </a>
                 </li>
                 <li>
                  <a href="/mars-exploration/missions/?category=171" target="_self">
                   Future
                  </a>
                 </li>
                 <li>
                  <a href="/mars-exploration/partners" target="_self">
                   International Partners
                  </a>
                 </li>
                </ul>
               </div>
               <div class="gradient_line">
               </div>
              </li>
              <li>
               <div class="nav_title">
                <a class="main_nav_item" href="/#more" target="_self">
                 More
                </a>
               </div>
               <div class="gradient_line">
               </div>
              </li>
              <li>
               <div class="nav_title">
                <a class="main_nav_item" href="/legacy" target="_self">
                 Legacy Site
                </a>
               </div>
               <div class="gradient_line">
               </div>
              </li>
             </ul>
             <form action="https://mars.nasa.gov/search/" class="overlay_search nav_search">
              <label class="search_label">
               Search
              </label>
              <input class="search_field" name="q" type="text" value=""/>
              <div class="search_submit">
              </div>
             </form>
            </nav>
           </div>
          </div>
         </header>
        </div>
        <div id="sticky_nav_spacer">
        </div>
        <div id="page">
         <!-- title to go in the page_header -->
         <div class="header_mask">
         </div>
         <div class="react_grid_list" data-react-class="GridListPage" data-react-props='{"left_column":false,"class_name":"","default_view":"list_view","model":"news_items","view_toggle":false,"search":true,"list_item":"News","title":"News","categories":["19,165,184,204"],"order":"publish_date desc,created_at desc","no_items_text":"There are no items matching these criteria.","per_page":null,"filters":"[ [ \"date\", [ [ \"2018\", \"2018\" ], [ \"2017\", \"2017\" ], [ \"2016\", \"2016\" ], [ \"2015\", \"2015\" ], [ \"2014\", \"2014\" ], [ \"2013\", \"2013\" ], [ \"2012\", \"2012\" ], [ \"2011\", \"2011\" ], [ \"2010\", \"2010\" ], [ \"2009\", \"2009\" ], [ \"2008\", \"2008\" ], [ \"2007\", \"2007\" ], [ \"2006\", \"2006\" ], [ \"2005\", \"2005\" ], [ \"2004\", \"2004\" ], [ \"2003\", \"2003\" ], [ \"2002\", \"2002\" ], [ \"2001\", \"2001\" ], [ \"2000\", \"2000\" ] ], [ \"Latest\", \"\" ], false ], [ \"categories\", [ [ \"Feature Stories\", 165 ], [ \"Press Releases\", 19 ], [ \"Spotlights\", 184 ], [ \"Status Reports\", 204 ] ], [ \"All Categories\", \"\" ], false ] ]","conditions":null,"scope_in_title":true,"options":{"blank_scope":"Latest"},"results_in_title":false}'>
         </div>
         <section class="module suggested_features">
          <div class="grid_layout">
           <header>
            <h2 class="module_title">
             You Might Also Like
            </h2>
           </header>
           <section>
            <script>
             $(document).ready(function(){
        $(".features").slick({
          dots: false,
          infinite: true,
          speed: 300,
          slide: '.features .slide',
          slidesToShow: 3,
          slidesToScroll: 3,
          lazyLoad: 'ondemand',
          centerMode: false,
          arrows: true,
          appendArrows: '.features .slick-nav',
          appendDots: ".features .slick-nav",
          responsive: [{"breakpoint":953,"settings":{"slidesToShow":2,"slidesToScroll":2,"centerMode":false}},{"breakpoint":480,"settings":{"slidesToShow":1,"slidesToScroll":1,"centerMode":true,"arrows":false,"centerPadding":"25px"}}]
        });
      });
            </script>
            <div class="features">
             <div class="slide">
              <div class="image_and_description_container">
               <a href="/news/8326/nasa-invests-in-visionary-technology/">
                <div class="rollover_description">
                 <div class="rollover_description_inner">
                  NASA is investing in technology concepts, including several from JPL, that may one day be used for future space exploration missions.
                 </div>
                 <div class="overlay_arrow">
                  <img alt="More" src="/assets/overlay-arrow.png"/>
                 </div>
                </div>
                <img alt="NASA Invests in Visionary Technology " class="img-lazy" data-lazy="/system/news_items/list_view_images/8326_niac320.jpg" src="/assets/loading_320x240.png"/>
               </a>
              </div>
              <div class="content_title">
               <a href="/news/8326/nasa-invests-in-visionary-technology/">
                NASA Invests in Visionary Technology
               </a>
              </div>
             </div>
             <div class="slide">
              <div class="image_and_description_container">
               <a href="/news/8325/nasa-is-ready-to-study-the-heart-of-mars/">
                <div class="rollover_description">
                 <div class="rollover_description_inner">
                  NASA is about to go on a journey to study the center of Mars.
                 </div>
                 <div class="overlay_arrow">
                  <img alt="More" src="/assets/overlay-arrow.png"/>
                 </div>
                </div>
                <img alt="NASA is Ready to Study the Heart of Mars" class="img-lazy" data-lazy="/system/news_items/list_view_images/8325_insight20180329b_320.jpg" src="/assets/loading_320x240.png"/>
               </a>
              </div>
              <div class="content_title">
               <a href="/news/8325/nasa-is-ready-to-study-the-heart-of-mars/">
                NASA is Ready to Study the Heart of Mars
               </a>
              </div>
             </div>
             <div class="slide">
              <div class="image_and_description_container">
               <a href="/news/8322/nasa-briefing-on-first-mission-to-study-mars-interior/">
                <div class="rollover_description">
                 <div class="rollover_description_inner">
                  NASA’s next mission to Mars will be the topic of a media briefing Thursday, March 29, at JPL. The briefing will air live on NASA Television and the agency’s website.
                 </div>
                 <div class="overlay_arrow">
                  <img alt="More" src="/assets/overlay-arrow.png"/>
                 </div>
                </div>
                <img alt="NASA Briefing on First Mission to Study Mars Interior" class="img-lazy" data-lazy="/system/news_items/list_view_images/8322_PIA22228_320.jpg" src="/assets/loading_320x240.png"/>
               </a>
              </div>
              <div class="content_title">
               <a href="/news/8322/nasa-briefing-on-first-mission-to-study-mars-interior/">
                NASA Briefing on First Mission to Study Mars Interior
               </a>
              </div>
             </div>
             <div class="slide">
              <div class="image_and_description_container">
               <a href="/news/8321/new-ar-mobile-app-features-3-d-nasa-spacecraft/">
                <div class="rollover_description">
                 <div class="rollover_description_inner">
                  NASA spacecraft travel to far-off destinations in space, but a new mobile app produced by NASA's Jet Propulsion Laboratory, Pasadena, California, brings spacecraft to users.
                 </div>
                 <div class="overlay_arrow">
                  <img alt="More" src="/assets/overlay-arrow.png"/>
                 </div>
                </div>
                <img alt="New 'AR' Mobile App Features 3-D NASA Spacecraft" class="img-lazy" data-lazy="/system/news_items/list_view_images/8321_list_image.jpg" src="/assets/loading_320x240.png"/>
               </a>
              </div>
              <div class="content_title">
               <a href="/news/8321/new-ar-mobile-app-features-3-d-nasa-spacecraft/">
                New 'AR' Mobile App Features 3-D NASA Spacecraft
               </a>
              </div>
             </div>
             <div class="slide">
              <div class="image_and_description_container">
               <a href="/news/8317/witness-first-mars-launch-from-west-coast/">
                <div class="rollover_description">
                 <div class="rollover_description_inner">
                  NASA invites digital creators to apply for social media credentials to cover the launch of the InSight mission to Mars, May 3-5, at California's Vandenberg Air Force Base.
                 </div>
                 <div class="overlay_arrow">
                  <img alt="More" src="/assets/overlay-arrow.png"/>
                 </div>
                </div>
                <img alt="Witness First Mars Launch from West Coast" class="img-lazy" data-lazy="/system/news_items/list_view_images/8317_list_image.jpg" src="/assets/loading_320x240.png"/>
               </a>
              </div>
              <div class="content_title">
               <a href="/news/8317/witness-first-mars-launch-from-west-coast/">
                Witness First Mars Launch from West Coast
               </a>
              </div>
             </div>
             <div class="slide">
              <div class="image_and_description_container">
               <a href="/news/8315/nasa-insight-mission-to-mars-arrives-at-launch-site/">
                <div class="rollover_description">
                 <div class="rollover_description_inner">
                  NASA's InSight spacecraft has arrived at Vandenberg Air Force Base in central California to begin final preparations for a launch this May.
                 </div>
                 <div class="overlay_arrow">
                  <img alt="More" src="/assets/overlay-arrow.png"/>
                 </div>
                </div>
                <img alt="NASA InSight Mission to Mars Arrives at Launch Site" class="img-lazy" data-lazy="/system/news_items/list_view_images/8315_list_image.jpg" src="/assets/loading_320x240.png"/>
               </a>
              </div>
              <div class="content_title">
               <a href="/news/8315/nasa-insight-mission-to-mars-arrives-at-launch-site/">
                NASA InSight Mission to Mars Arrives at Launch Site
               </a>
              </div>
             </div>
             <div class="grid_layout">
              <div class="slick-nav_container">
               <div class="slick-nav">
               </div>
              </div>
             </div>
            </div>
           </section>
          </div>
         </section>
        </div>
        <footer id="site_footer">
         <div class="grid_layout">
          <section class="upper_footer">
           <div class="share">
            <h2>
             Follow the Journey
            </h2>
            <div class="social_icons">
             <!-- AddThis Button BEGIN -->
             <div class="addthis_toolbox addthis_default_style addthis_32x32_style">
              <a addthis:userid="NASABeAMartian" class="addthis_button_twitter_follow icon">
               <img alt="twitter" src="/assets/twitter_icon@2x.png"/>
              </a>
              <a addthis:userid="NASABEAM" class="addthis_button_facebook_follow icon">
               <img alt="facebook" src="/assets/facebook_icon@2x.png"/>
              </a>
              <a addthis:userid="nasa" class="addthis_button_instagram_follow icon">
               <img alt="instagram" src="/assets/instagram_icon@2x.png"/>
              </a>
              <a addthis:url="https://mars.nasa.gov/rss/api/?feed=news&amp;category=all&amp;feedtype=rss" class="addthis_button_rss_follow icon">
               <img alt="rss" src="/assets/rss_icon@2x.png"/>
              </a>
             </div>
             <script>
              addthis_loader.init("//s7.addthis.com/js/300/addthis_widget.js#pubid=ra-5a690e4c1320e328", {follow: true})
             </script>
             <!-- AddThis Button END -->
            </div>
           </div>
           <div class="gradient_line">
           </div>
          </section>
          <section class="sitemap">
           <div class="sitemap_directory" id="sitemap_directory">
            <div class="sitemap_block">
             <div class="footer_sitemap_item">
              <h3 class="sitemap_title">
               <a href="/#red_planet">
                The Red Planet
               </a>
              </h3>
              <ul>
               <li>
                <div class="global_subnav_container">
                 <ul class="subnav">
                  <li>
                   <a href="/#red_planet/0" target="_self">
                    Dashboard
                   </a>
                  </li>
                  <li>
                   <a href="/#red_planet/1" target="_self">
                    Science Goals
                   </a>
                  </li>
                  <li>
                   <a href="/#red_planet/2" target="_self">
                    The Planet
                   </a>
                  </li>
                  <li>
                   <a href="/#red_planet/3" target="_self">
                    Atmosphere
                   </a>
                  </li>
                  <li>
                   <a href="/#red_planet/4" target="_self">
                    Astrobiology
                   </a>
                  </li>
                  <li>
                   <a href="/#red_planet/5" target="_self">
                    Past, Present, Future, Timeline
                   </a>
                  </li>
                 </ul>
                </div>
               </li>
              </ul>
             </div>
            </div>
            <div class="sitemap_block">
             <div class="footer_sitemap_item">
              <h3 class="sitemap_title">
               <a href="/#mars_exploration_program">
                The Program
               </a>
              </h3>
              <ul>
               <li>
                <div class="global_subnav_container">
                 <ul class="subnav">
                  <li>
                   <a href="/#mars_exploration_program/0" target="_self">
                    Mission Statement
                   </a>
                  </li>
                  <li>
                   <a href="/#mars_exploration_program/1" target="_self">
                    About the Program
                   </a>
                  </li>
                  <li>
                   <a href="/#mars_exploration_program/2" target="_self">
                    Organization
                   </a>
                  </li>
                  <li>
                   <a href="/#mars_exploration_program/3" target="_self">
                    Why Mars?
                   </a>
                  </li>
                  <li>
                   <a href="/#mars_exploration_program/4" target="_self">
                    Research Programs
                   </a>
                  </li>
                  <li>
                   <a href="/#mars_exploration_program/5" target="_self">
                    Planetary Resources
                   </a>
                  </li>
                  <li>
                   <a href="/#mars_exploration_program/6" target="_self">
                    Technologies
                   </a>
                  </li>
                 </ul>
                </div>
               </li>
              </ul>
             </div>
            </div>
            <div class="sitemap_block">
             <div class="footer_sitemap_item">
              <h3 class="sitemap_title">
               <a href="/#news_and_events">
                News &amp; Events
               </a>
              </h3>
              <ul>
               <li>
                <div class="global_subnav_container">
                 <ul class="subnav">
                  <li class="current">
                   <a href="/news" target="_self">
                    News
                   </a>
                  </li>
                  <li>
                   <a href="/events" target="_self">
                    Events
                   </a>
                  </li>
                 </ul>
                </div>
               </li>
              </ul>
             </div>
            </div>
            <div class="sitemap_block">
             <div class="footer_sitemap_item">
              <h3 class="sitemap_title">
               <a href="/#multimedia">
                Multimedia
               </a>
              </h3>
              <ul>
               <li>
                <div class="global_subnav_container">
                 <ul class="subnav">
                  <li>
                   <a href="/multimedia/images/" target="_self">
                    Images
                   </a>
                  </li>
                  <li>
                   <a href="/multimedia/videos/" target="_self">
                    Videos
                   </a>
                  </li>
                 </ul>
                </div>
               </li>
              </ul>
             </div>
            </div>
            <div class="sitemap_block">
             <div class="footer_sitemap_item">
              <h3 class="sitemap_title">
               <a href="/#missions">
                Missions
               </a>
              </h3>
              <ul>
               <li>
                <div class="global_subnav_container">
                 <ul class="subnav">
                  <li>
                   <a href="/mars-exploration/missions/?category=167" target="_self">
                    Past
                   </a>
                  </li>
                  <li>
                   <a href="/mars-exploration/missions/?category=170" target="_self">
                    Present
                   </a>
                  </li>
                  <li>
                   <a href="/mars-exploration/missions/?category=171" target="_self">
                    Future
                   </a>
                  </li>
                  <li>
                   <a href="/mars-exploration/partners" target="_self">
                    International Partners
                   </a>
                  </li>
                 </ul>
                </div>
               </li>
              </ul>
             </div>
            </div>
            <div class="sitemap_block">
             <div class="footer_sitemap_item">
              <h3 class="sitemap_title">
               <a href="/#more">
                More
               </a>
              </h3>
              <ul>
               <li>
                <div class="global_subnav_container">
                 <ul class="subnav">
                 </ul>
                </div>
               </li>
              </ul>
             </div>
            </div>
            <div class="sitemap_block">
             <div class="footer_sitemap_item">
              <h3 class="sitemap_title">
               <a href="/legacy">
                Legacy Site
               </a>
              </h3>
              <ul>
               <li>
                <div class="global_subnav_container">
                 <ul class="subnav">
                  <li>
                   <a class="" href="/legacy" target="_self">
                    Legacy Site
                   </a>
                  </li>
                 </ul>
                </div>
               </li>
              </ul>
             </div>
            </div>
           </div>
           <div class="gradient_line">
           </div>
          </section>
          <section class="lower_footer">
           <div class="nav_container">
            <nav>
             <ul>
              <li>
               <a href="http://science.nasa.gov/" target="_blank">
                NASA Science Mission Directorate
               </a>
              </li>
              <li>
               <a href="https://www.jpl.nasa.gov/copyrights.php" target="_blank">
                Privacy
               </a>
              </li>
              <li>
               <a href="http://www.jpl.nasa.gov/imagepolicy/" target="_blank">
                Image Policy
               </a>
              </li>
              <li>
               <a href="https://mars.nasa.gov/feedback/" target="_self">
                Feedback
               </a>
              </li>
              <li>
               <a href="http://mars.nasa.gov/legacy" target="_blank">
                Legacy Mars Site
               </a>
              </li>
             </ul>
            </nav>
           </div>
           <div class="credits">
            <div class="footer_brands_top">
             <p>
              Managed by the Mars Exploration Program and the Jet Propulsion Laboratory for NASA’s Science Mission Directorate
             </p>
            </div>
            <!-- .footer_brands -->
            <!-- %a.jpl{href: "", target: "_blank"}Institution -->
            <!-- -->
            <!-- %a.caltech{href: "", target: "_blank"}Institution -->
            <!-- .staff -->
            <!-- %p -->
            <!-- - get_staff_for_category(get_field_from_admin_config(:web_staff_category_id)) -->
            <!-- - @staff.each_with_index do |staff, idx| -->
            <!-- - unless staff.is_in_footer == 0 -->
            <!-- = staff.title + ": " -->
            <!-- - if staff.contact_link =~ /@/ -->
            <!-- = mail_to staff.contact_link, staff.name, :subject => "[#{@site_title}]" -->
            <!-- - elsif staff.contact_link.present? -->
            <!-- = link_to staff.name, staff.contact_link -->
            <!-- - else -->
            <!-- = staff.name -->
            <!-- - unless (idx + 1 == @staff.size) -->
            <!-- %br -->
           </div>
          </section>
         </div>
        </footer>
       </div>
      </div>
      <script id="_fed_an_ua_tag" src="https://dap.digitalgov.gov/Universal-Federated-Analytics-Min.js?agency=NASA&amp;subagency=JPL-Mars-MEPJPL&amp;pua=UA-9453474-9,UA-118212757-11&amp;dclink=true&amp;sp=searchbox&amp;exts=tif,tiff,wav" type="text/javascript">
      </script>
     </body>
    </html>
    
    


```python
results = soup.find_all('li', class_="list_text")
```


```python
for result in results:
    # Error handling
    try:
        title = result.find('a', class_="content_title").text
        link = result.a['href']

#         if (title):
#             print('-------------')
        print(title)
    except Exception as e:
        print(e)
```
