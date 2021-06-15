# mymail
com.my.mail
#
/*

 *****************************************************************************

    Copyright (c) Microsoft Corporation.

    Permission to use, copy, modify, and/or distribute this software for any

    purpose with or without fee is hereby granted.

    THE SOFTWARE IS PROVIDED "AS IS" AND THE AUTHOR DISCLAIMS ALL WARRANTIES WITH

    REGARD TO THIS SOFTWARE INCLUDING ALL IMPLIED WARRANTIES OF MERCHANTABILITY

    AND FITNESS. IN NO EVENT SHALL THE AUTHOR BE LIABLE FOR ANY SPECIAL, DIRECT,

    INDIRECT, OR CONSEQUENTIAL DAMAGES OR ANY DAMAGES WHATSOEVER RESULTING FROM

    LOSS OF USE, DATA OR PROFITS, WHETHER IN AN ACTION OF CONTRACT, NEGLIGENCE OR

    OTHER TORTIOUS ACTION, ARISING OUT OF OR IN CONNECTION WITH THE USE OR

    PERFORMANCE OF THIS SOFTWARE.

**************************************************************************** *****************************************************************************

    Copyright (c) Microsoft Corporation. All rights reserved.

    Licensed under the Apache License, Version 2.0 (the "License"); you may not use

    this file except in compliance with the License. You may obtain a copy of the

    License at http://www.apache.org/licenses/LICENSE-2.0

    THIS CODE IS PROVIDED ON AN *AS IS* BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY

    KIND, EITHER EXPRESS OR IMPLIED, INCLUDING WITHOUT LIMITATION ANY IMPLIED

    WARRANTIES OR CONDITIONS OF TITLE, FITNESS FOR A PARTICULAR PURPOSE,

    MERCHANTABLITY OR NON-INFRINGEMENT.

    See the Apache Version 2.0 License for specific language governing permissions

    and limitations under the License.

*****************************************************************************/

var $jscomp=$jscomp||{};$jscomp.scope={};$jscomp.ASSUME_ES5=!1;$jscomp.ASSUME_NO_NATIVE_MAP=!1;$jscomp.ASSUME_NO_NATIVE_SET=!1;$jscomp.defineProperty=$jscomp.ASSUME_ES5||"function"==typeof Object.defineProperties?Object.defineProperty:function(a,d,e){a!=Array.prototype&&a!=Object.prototype&&(a[d]=e.value)};$jscomp.getGlobal=function(a){return"undefined"!=typeof window&&window===a?a:"undefined"!=typeof global&&null!=global?global:a};$jscomp.global=$jscomp.getGlobal(this);

$jscomp.polyfill=function(a,d,e,h){if(d){e=$jscomp.global;a=a.split(".");for(h=0;h<a.length-1;h++){var g=a[h];g in e||(e[g]={});e=e[g]}a=a[a.length-1];h=e[a];d=d(h);d!=h&&null!=d&&$jscomp.defineProperty(e,a,{configurable:!0,writable:!0,value:d})}};$jscomp.underscoreProtoCanBeSet=function(){var a={a:!0},d={};try{return d.__proto__=a,d.a}catch(e){}return!1};

$jscomp.setPrototypeOf="function"==typeof Object.setPrototypeOf?Object.setPrototypeOf:$jscomp.underscoreProtoCanBeSet()?function(a,d){a.__proto__=d;if(a.__proto__!==d)throw new TypeError(a+" is not extensible");return a}:null;$jscomp.polyfill("Object.setPrototypeOf",function(a){return a||$jscomp.setPrototypeOf},"es6","es5");$jscomp.owns=function(a,d){return Object.prototype.hasOwnProperty.call(a,d)};

$jscomp.polyfill("Object.assign",function(a){return a?a:function(a,e){for(var d=1;d<arguments.length;d++){var g=arguments[d];if(g)for(var k in g)$jscomp.owns(g,k)&&(a[k]=g[k])}return a}},"es6","es3");$jscomp.checkStringArgs=function(a,d,e){if(null==a)throw new TypeError("The 'this' value for String.prototype."+e+" must not be null or undefined");if(d instanceof RegExp)throw new TypeError("First argument to String.prototype."+e+" must not be a regular expression");return a+""};

$jscomp.polyfill("String.prototype.startsWith",function(a){return a?a:function(a,e){var d=$jscomp.checkStringArgs(this,a,"startsWith");a+="";var g=d.length,k=a.length;e=Math.max(0,Math.min(e|0,d.length));for(var l=0;l<k&&e<g;)if(d[e++]!=a[l++])return!1;return l>=k}},"es6","es3");$jscomp.SYMBOL_PREFIX="jscomp_symbol_";$jscomp.initSymbol=function(){$jscomp.initSymbol=function(){};$jscomp.global.Symbol||($jscomp.global.Symbol=$jscomp.Symbol)};

$jscomp.Symbol=function(){var a=0;return function(d){return $jscomp.SYMBOL_PREFIX+(d||"")+a++}}();$jscomp.initSymbolIterator=function(){$jscomp.initSymbol();var a=$jscomp.global.Symbol.iterator;a||(a=$jscomp.global.Symbol.iterator=$jscomp.global.Symbol("iterator"));"function"!=typeof Array.prototype[a]&&$jscomp.defineProperty(Array.prototype,a,{configurable:!0,writable:!0,value:function(){return $jscomp.arrayIterator(this)}});$jscomp.initSymbolIterator=function(){}};

$jscomp.arrayIterator=function(a){var d=0;return $jscomp.iteratorPrototype(function(){return d<a.length?{done:!1,value:a[d++]}:{done:!0}})};$jscomp.iteratorPrototype=function(a){$jscomp.initSymbolIterator();a={next:a};a[$jscomp.global.Symbol.iterator]=function(){return this};return a};

$jscomp.iteratorFromArray=function(a,d){$jscomp.initSymbolIterator();a instanceof String&&(a+="");var e=0,h={next:function(){if(e<a.length){var g=e++;return{value:d(g,a[g]),done:!1}}h.next=function(){return{done:!0,value:void 0}};return h.next()}};h[Symbol.iterator]=function(){return h};return h};$jscomp.polyfill("Array.prototype.keys",function(a){return a?a:function(){return $jscomp.iteratorFromArray(this,function(a){return a})}},"es6","es3");

(function(a,d){"object"===typeof exports&&"undefined"!==typeof module?d(exports):"function"===typeof define&&define.amd?define(["exports"],d):(a="undefined"!==typeof globalThis?globalThis:a||self,d(a["@mail/amp-viewer"]={}))})(this,function(a){function d(a,b){function c(){this.constructor=a}g(a,b);a.prototype=null===b?Object.create(b):(c.prototype=b.prototype,new c)}function e(){for(var a=0,b=0,c=arguments.length;b<c;b++)a+=arguments[b].length;a=Array(a);var f=0;for(b=0;b<c;b++)for(var d=arguments[b],

e=0,g=d.length;e<g;e++,f++)a[f]=d[e];return a}function h(a){return Object.keys(a).map(function(b){return encodeURIComponent(b)+"="+encodeURIComponent(a[b])}).join("&")}var g=function(a,b){g=Object.setPrototypeOf||{__proto__:[]}instanceof Array&&function(a,b){a.__proto__=b}||function(a,b){for(var c in b)Object.prototype.hasOwnProperty.call(b,c)&&(a[c]=b[c])};return g(a,b)},k=function(){k=Object.assign||function(a){for(var b,c=1,f=arguments.length;c<f;c++){b=arguments[c];for(var d in b)Object.prototype.hasOwnProperty.call(b,

d)&&(a[d]=b[d])}return a};return k.apply(this,arguments)},l=function(a,b){return b={exports:{}},a(b,b.exports),b.exports}(function(a,b){function c(a,b){function c(){this.constructor=a}g(a,b);a.prototype=null===b?Object.create(b):(c.prototype=b.prototype,new c)}function f(a,b,c){var q=a.prototype[b],m="function"===typeof q;a.prototype[b]=function(){c.apply(this,arguments);if(m)return q.apply(this,arguments)}}Object.defineProperty(b,"__esModule",{value:!0});var d=function(){function a(a,b,c){this.state=

a;this.signal=b;this.implementation=c}a.prototype.onConditionsMet=function(a){};a.prototype.onConditionsUnmet=function(a){};return a}(),e=function(){function a(a){this.transitions=a;this.currentState="initial";this.possibleTransitions=[]}Object.defineProperty(a.prototype,"state",{get:function(){return this.currentState},enumerable:!0,configurable:!0});a.prototype.transition=function(a){for(var b=[],c=1;c<arguments.length;c++)b[c-1]=arguments[c];c=this.findTransitions(a);for(var d=this.state,m=0;m<

c.length&&(this.doTransition.apply(this,[c[m].implementation].concat(b)),d===this.state);m++);};a.prototype.reset=function(){this.doTransition("initial")};a.prototype.doTransition=function(a){for(var c=this,b=[],d=1;d<arguments.length;d++)b[d-1]=arguments[d];this.possibleTransitions.forEach(function(a){return a.onConditionsUnmet(c)});this.currentState="function"===typeof a?a.apply(void 0,[this].concat(b)):a;this.possibleTransitions=this.getPossibleTransitions();this.possibleTransitions.forEach(function(a){return a.onConditionsMet(c)})};

a.prototype.getPossibleTransitions=function(){var a=this;return this.transitions.filter(function(c){return c.state===a.state})};a.prototype.findTransitions=function(a){return this.getPossibleTransitions().filter(function(c){return c.signal===a||void 0===c.signal})};return a}(),g=function(a,c){g=Object.setPrototypeOf||{__proto__:[]}instanceof Array&&function(a,c){a.__proto__=c}||function(a,c){for(var b in c)c.hasOwnProperty(b)&&(a[b]=c[b])};return g(a,c)},t=function(a){function b(c,d,f){c=a.call(this,

c,b.signal(f),d)||this;c.ms=f;return c}c(b,a);b.signal=function(a){return"_$timer"+a};b.prototype.onConditionsMet=function(c){a.prototype.onConditionsMet.call(this,c);this.timer=setTimeout(this.handleTimer.bind(this,c),this.ms)};b.prototype.onConditionsUnmet=function(c){a.prototype.onConditionsUnmet.call(this,c);clearTimeout(this.timer)};b.prototype.handleTimer=function(a){a.transition(b.signal(this.ms))};return b}(d),h=function(a){function b(c,b,d){return a.call(this,c,b,function(){for(var a=[],

b=0;b<arguments.length;b++)a[b]=arguments[b];d.apply(void 0,a);return c})||this}c(b,a);return b}(d),k=function(a){function b(b){var c=a.call(this,b.transitions||[])||this;c.component=b;c.handlers={};return c}c(b,a);b.prototype.signal=function(a){var b=this,c=String(a);this.handlers[c]||(this.handlers[c]=function(c){b.transition(a,c)});return this.handlers[c]};b.prototype.transition=function(c){for(var b=[],d=1;d<arguments.length;d++)b[d-1]=arguments[d];var f;a.prototype.transition.apply(this,[c].concat(b));

"string"===typeof this.mapToState&&this.component.state[this.mapToState]!==this.state&&this.component.setState((f={},f[this.mapToState]=this.state,f))};b.prototype.doTransition=function(c){for(var b=this,d=[],f=1;f<arguments.length;f++)d[f-1]=arguments[f];if("function"!==typeof c)return a.prototype.doTransition.call(this,c);a.prototype.doTransition.call(this,function(){return c.apply(void 0,[b.component].concat(d))},d)};return b}(e);a=function(a){var b=function(d){return"function"===typeof d?b({})(d):

function(b){b=function(b){function f(){for(var c=[],f=0;f<arguments.length;f++)c[f]=arguments[f];c=b.apply(this,c)||this;a.onConstruct(c,d);return c}c(f,b);return f}(b);a.onPatch(b,d);return b}};return b}({onPatch:function(a,b){b=b.catching;f(a,"componentDidMount",function(){this.automaton.transition("mount")});f(a,"componentDidUpdate",function(a,b){this.automaton.transition("update",a,b)});f(a,"componentWillUnmount",function(){this.automaton.transition("unmount");this.automaton.reset()});b&&f(a,

"componentDidCatch",function(a,b){this.automaton.transition("catch",a,b)})},onConstruct:function(a,b){a.automaton=new k(a);a.automaton.transition("create",a);"string"===typeof b.mapToState&&(a.state||(a.state={}),a.state[b.mapToState]=a.automaton.state,a.automaton.mapToState=b.mapToState)}});b.INITIAL="initial";b.transition=function(a,b,c){return"function"===typeof b?new d(a,void 0,b):new d(a,b,c)};b.automaton=function(a){return new e(a)};b.Automaton=e;b.Transition=d;b.timer=function(a,b,c){return new t(a,

c,b)};b.sideEffect=function(a,b,c){"function"===typeof b&&(c=b,b=void 0);return new h(a,b,c)};b.CATCH="catch";b.CREATE="create";b.MOUNT="mount";b.UNMOUNT="unmount";b.UPDATE="update";b.withAutomaton=a;b.automatonOf=function(a){return a.automaton};b.asSignal=function(a,b){return a.automaton.signal(b)}});(function(a){return a&&a.__esModule&&Object.prototype.hasOwnProperty.call(a,"default")?a["default"]:a})(l);var n=l.transition,v=l.automaton,r=l.timer,p=l.sideEffect;l=function(){function a(){this.handlers=

{}}a.prototype.on=function(a,c){this.handlers[a]=this.handlers[a]||[];this.handlers[a].push(c)};a.prototype.off=function(a,c){this.handlers[a]&&(this.handlers[a]=this.handlers[a].filter(function(a){return c!==a}))};a.prototype.emit=function(a,c){(this.handlers[a]||[]).forEach(function(a){return a(c)})};return a}();var w=/^(https?:\/\/)?(.*\.)?(imgs|dev)?mail\.ru$/,x=/^(https?:\/\/)?localhost:?/,y=function(a){function b(c){var d=a.call(this)||this;d.id=b.lastId++;d.options=k({},c);d.id=c.id||d.id;

d.handleMessage=d.handleMessage.bind(d);return d}d(b,a);b.prototype.setup=function(){this.options.selfWindow.addEventListener("message",this.handleMessage)};b.prototype.teardown=function(){this.options.selfWindow.removeEventListener("message",this.handleMessage)};b.prototype.sendMessage=function(a){var b=a.type;this.options.debug&&console.warn("[SEND]",b,a);this.options.targetWindow.postMessage(this.id+"@@mail-amp-postMessage$"+JSON.stringify(a),this.options.targetOrigin||"*")};b.prototype.setDebug=

function(a){this.options.debug=a};b.prototype.setTargetWindow=function(a){this.options.targetWindow=a};b.prototype.setTargetOrigin=function(a){this.options.targetOrigin=a};b.prototype.setId=function(a){this.id=a};b.prototype.getId=function(){return this.id};b.prototype.handleMessage=function(a){var b=this.options.originRegexp;if(b&&!b.test(a.origin))this.options.debug&&console.error("[RECEIVE] Received message from prohibited origin:",a.origin);else{try{var c=""+this.id+"@@mail-amp-postMessage$";

if(String(a.data).startsWith(c))var d=JSON.parse(a.data.slice(c.length));else return}catch(u){console.error(u);return}this.options.debug&&console.warn("[RECEIVE]",d.type,d);this.emit(d.type,d)}};b.lastId=0;return b}(l),z=function(a){function b(b){var c=a.call(this)||this;c.options=k({},b);var d=w;x.test(window.location.href)&&(d=void 0);c.transport=new y(k({selfWindow:window,originRegexp:d,debug:b.debug},b.transport));return c}d(b,a);b.prototype.setup=function(){this.initializeController();this.transport.setup();

this.transport.on("ready",this.asSignal("ready"));this.transport.on("configured",this.asSignal("configured"));this.transport.on("resize",this.asSignal("resize"));this.transport.on("navigate",this.asSignal("navigate"));this.transport.on("radar",this.asSignal("radar"));this.transport.on("error",this.asSignal("error"));this.automaton.transition(void 0)};b.prototype.teardown=function(){this.automaton.reset();this.transport.teardown()};b.prototype.loadLetter=function(a){this.letter=a;"ready"===this.automaton.state&&

this.transport.sendMessage({type:"content",data:this.letter})};b.prototype.errorReporter=function(a,b){var c=this;return function(){c.emit("error",{type:a,error:b});return"error"}};b.prototype.asSignal=function(a){var b=this;return function(c){b.automaton.transition(a,c)}};b.prototype.initializeController=function(){var a=this;this.automaton=v(e([n("initial","create","creation"),n("creation",function(){var b=a.options.iframeSrc;a.iframe=a.options.iframe||document.createElement("IFRAME");a.iframe.setAttribute("scrolling",

"no");a.iframe.setAttribute("allowfullscreen","false");a.iframe.setAttribute("sandbox","allow-scripts allow-forms allow-same-origin");a.iframe.setAttribute("allow","accelerometer 'none';autoplay 'none';camera 'none';document-domain 'none';encrypted-media 'none';fullscreen 'none';geolocation 'none';gyroscope 'none';magnetometer 'none';microphone 'none';midi 'none';payment 'none';picture-in-picture 'none';sync-xhr 'none';usb 'none';xr-spatial-tracking 'none';");a.iframe.src=b+"#?__mrg_frame_id="+a.transport.getId()+

"&"+h({origin:window.location.origin,prerenderSize:0,visibilityState:"visible",viewportType:a.options.mobileSafari?"natural":"natural-ios-embed",paddingTop:0,history:1,p2r:0,storage:0,development:0,log:1,cap:"xhrInterceptor,viewerRenderTemplate",csi:0});/^https?:\/\//.test(b)&&(b=b.split("/"),a.transport.setTargetOrigin(b[0]+"//"+b[2]));a.iframe.onerror=a.asSignal("event-error");return"loading"}),r("loading",this.options.timeout,this.errorReporter("timeout","Iframe loading timed out")),n("loading",

"ready",function(){a.transport.setTargetWindow(a.iframe.contentWindow);a.transport.sendMessage({type:"configure",data:a.options});return"configuring"}),r("configuring",this.options.timeout,this.errorReporter("timeout","Iframe configuring timed out")),n("configuring","configured",function(){a.letter&&a.transport.sendMessage({type:"content",data:a.letter});a.emit("ready",void 0);return"ready"}),p("ready","resize",function(b,c){a.iframe.style.height=c.data.height+"px";a.emit("resize",c.data)}),p("ready",

"navigate",function(b,c){a.emit("navigate",c.data)})],["initial","loading","configuring","ready","error"].map(function(b){return p(b,"radar",function(b,c){a.emit("radar",c.data)})}),["initial","loading","configuring","ready"].map(function(b){return n(b,"error",function(c,d){if("timeout"===d.data.type||"validation"===d.data.type||"lib_untrusted"===d.data.type)return a.emit("error",d.data),"error";a.emit("warning",d.data);return b})})));this.automaton.transition("create")};return b}(l);a.createAmpViewer=

function(a){return new z(a)};Object.defineProperty(a,"__esModule",{value:!0})});

