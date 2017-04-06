# api documentation for  [asynquence (v0.10.0)](http://github.com/getify/asynquence)  [![npm package](https://img.shields.io/npm/v/npmdoc-asynquence.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-asynquence) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-asynquence.svg)](https://travis-ci.org/npmdoc/node-npmdoc-asynquence)
#### promise-style async sequence flow-control

[![NPM](https://nodei.co/npm/asynquence.png?downloads=true)](https://www.npmjs.com/package/asynquence)

[![apidoc](https://npmdoc.github.io/node-npmdoc-asynquence/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-asynquence_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-asynquence/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-asynquence/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-asynquence/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Kyle Simpson",
        "email": "getify@gmail.com"
    },
    "bugs": {
        "url": "https://github.com/getify/asynquence/issues",
        "email": "getify@gmail.com"
    },
    "dependencies": {},
    "description": "promise-style async sequence flow-control",
    "devDependencies": {
        "babel-core": "~5.8.12",
        "es-feature-tests": "latest",
        "native-promise-only": "latest",
        "uglify-js": "~2.4.24"
    },
    "directories": {},
    "dist": {
        "shasum": "4ec766a3876016ec3d14f7ba834f660d589f7c31",
        "tarball": "https://registry.npmjs.org/asynquence/-/asynquence-0.10.0.tgz"
    },
    "gitHead": "54a7afae5bf118b5d1af9bf482b46f5428d3d580",
    "homepage": "http://github.com/getify/asynquence",
    "keywords": [
        "async",
        "flow-control",
        "sequences",
        "promise",
        "iterator",
        "generator"
    ],
    "license": "MIT",
    "main": "./asq.src.js",
    "maintainers": [
        {
            "name": "getify",
            "email": "getify@gmail.com"
        }
    ],
    "name": "asynquence",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git://github.com/getify/asynquence.git"
    },
    "scripts": {
        "build": "npm run build-core",
        "build-core": "./build-core.js",
        "prepublish": "npm run build-core",
        "test": "./node-tests.js"
    },
    "version": "0.10.0"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module asynquence](#apidoc.module.asynquence)
1.  [function <span class="apidocSignatureSpan">asynquence.</span>__schedule (fn)](#apidoc.element.asynquence.__schedule)
1.  [function <span class="apidocSignatureSpan">asynquence.</span>__tapSequence (def)](#apidoc.element.asynquence.__tapSequence)
1.  [function <span class="apidocSignatureSpan">asynquence.</span>asq ()](#apidoc.element.asynquence.asq)
1.  [function <span class="apidocSignatureSpan">asynquence.</span>clone ()](#apidoc.element.asynquence.clone)
1.  [function <span class="apidocSignatureSpan">asynquence.</span>extend (name, build)](#apidoc.element.asynquence.extend)
1.  [function <span class="apidocSignatureSpan">asynquence.</span>failed ()](#apidoc.element.asynquence.failed)
1.  [function <span class="apidocSignatureSpan">asynquence.</span>isMessageWrapper (val)](#apidoc.element.asynquence.isMessageWrapper)
1.  [function <span class="apidocSignatureSpan">asynquence.</span>isSequence (val)](#apidoc.element.asynquence.isSequence)
1.  [function <span class="apidocSignatureSpan">asynquence.</span>messages ()](#apidoc.element.asynquence.messages)
1.  [function <span class="apidocSignatureSpan">asynquence.</span>noConflict ()](#apidoc.element.asynquence.noConflict)
1.  [function <span class="apidocSignatureSpan">asynquence.</span>unpause (sq)](#apidoc.element.asynquence.unpause)

#### [module asynquence.asq](#apidoc.module.asynquence.asq)
1.  [function <span class="apidocSignatureSpan">asynquence.</span>asq ()](#apidoc.element.asynquence.asq.asq)
1.  [function <span class="apidocSignatureSpan">asynquence.asq.</span>__schedule (e)](#apidoc.element.asynquence.asq.__schedule)
1.  [function <span class="apidocSignatureSpan">asynquence.asq.</span>__tapSequence (e)](#apidoc.element.asynquence.asq.__tapSequence)
1.  [function <span class="apidocSignatureSpan">asynquence.asq.</span>clone ()](#apidoc.element.asynquence.asq.clone)
1.  [function <span class="apidocSignatureSpan">asynquence.asq.</span>extend (e, n)](#apidoc.element.asynquence.asq.extend)
1.  [function <span class="apidocSignatureSpan">asynquence.asq.</span>failed ()](#apidoc.element.asynquence.asq.failed)
1.  [function <span class="apidocSignatureSpan">asynquence.asq.</span>isMessageWrapper (e)](#apidoc.element.asynquence.asq.isMessageWrapper)
1.  [function <span class="apidocSignatureSpan">asynquence.asq.</span>isSequence (e)](#apidoc.element.asynquence.asq.isSequence)
1.  [function <span class="apidocSignatureSpan">asynquence.asq.</span>messages ()](#apidoc.element.asynquence.asq.messages)
1.  [function <span class="apidocSignatureSpan">asynquence.asq.</span>noConflict ()](#apidoc.element.asynquence.asq.noConflict)
1.  [function <span class="apidocSignatureSpan">asynquence.asq.</span>unpause (e)](#apidoc.element.asynquence.asq.unpause)



# <a name="apidoc.module.asynquence"></a>[module asynquence](#apidoc.module.asynquence)

#### <a name="apidoc.element.asynquence.__schedule"></a>[function <span class="apidocSignatureSpan">asynquence.</span>__schedule (fn)](#apidoc.element.asynquence.__schedule)
- description and source-code
```javascript
function schedule(fn) {
		scheduling_queue.add(fn);
		if (!cycle) {
			cycle = timer(scheduling_queue.drain);
		}
	}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.asynquence.__tapSequence"></a>[function <span class="apidocSignatureSpan">asynquence.</span>__tapSequence (def)](#apidoc.element.asynquence.__tapSequence)
- description and source-code
```javascript
function tapSequence(def) {
		// temporary 'trigger' which, if called before being replaced
		// above, creates replacement proxy sequence with the
		// success/error message(s) pre-injected
		function trigger() {
			def.seq = createSequence.apply(ø,arguments).defer();
		}

		// fail trigger
		trigger.fail = function $$trigger$fail() {
			var args = ARRAY_SLICE.call(arguments);
			def.seq = createSequence(function $$create$sequence(done){
				done.fail.apply(ø,args);
			})
			.defer();
		};

		// listen for signals from the sequence
		def.seq
		// note: cannot use 'seq.pipe(trigger)' because we
		// need to be able to update the shared closure
		// to change 'trigger'
		.val(function $$val(){
			trigger.apply(ø,arguments);
			return ASQmessages.apply(ø,arguments);
		})
		.or(function $$or(){
			trigger.fail.apply(ø,arguments);
		});

		// make a sequence to act as a proxy to the original
		// sequence
		def.seq = createSequence(function $$create$sequence(done){
			// replace the temporary trigger (created below)
			// with this proxy's trigger
			trigger = done;
		})
		.defer();
	}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.asynquence.asq"></a>[function <span class="apidocSignatureSpan">asynquence.</span>asq ()](#apidoc.element.asynquence.asq)
- description and source-code
```javascript
function createSequence(){function scheduleSequenceTick(){r?sequenceTick():e||(e=schedule(sequenceTick))}function throwSequenceErrors
(){throw 1===$.length?$[0]:$}function sequenceTick(){var a,c;if(e=null,delete d.unpause,r)clearTimeout(e),e=null,s.length=p.length
=g.length=$.length=0;else if(n)for(0!==p.length||t||(t=!0,throwSequenceErrors());p.length;){t=!0,a=p.shift();try{a.apply(h,$)}catch
(i){l(i)?$=$.concat(i):($.push(i),i.stack&&$.push(i.stack)),0===p.length&&throwSequenceErrors()}}else if(u&&s.length>0){u=!1,a=s
.shift(),c=g.slice(),g.length=0,c.unshift(createStepCompletion());try{a.apply(h,c)}catch(i){l(i)?$=$.concat(i):$.push(i),n=!0,scheduleSequenceTick
()}}}function createStepCompletion(){function done(){n||r||u||e||(e=!0,u=!0,g.push.apply(g,arguments),$.length=0,scheduleSequenceTick
())}done.fail=function $$step$fail(){n||r||u||e||(n=!0,g.length=0,$.push.apply($,arguments),scheduleSequenceTick())},done.abort=
function $$step$abort(){n||r||(u=!1,r=!0,g.length=$.length=0,scheduleSequenceTick())},done.errfcb=function $$step$errfcb(e){e?done
.fail(e):done.apply(h,f.call(arguments,1))};var e=!1;return done}function createGate(e,t,u){function resetGate(){clearTimeout(s),
s=d=m=o=null}function scheduleGateTick(){return g?gateTick():void(s||(s=schedule(gateTick)))}function gateTick(){if(!(n||r||$)){
var t=[];s=null,p?(e.fail.apply(h,o),resetGate()):g?(e.abort(),resetGate()):checkGate()&&($=!0,d.forEach(function $$each(e,n){t.
push(m["s"+n])}),e.apply(h,t),resetGate())}}function checkGate(){if(0!==d.length){var e=!0;return d.some(function $$some(n){return
 null===n?(e=!1,!0):void 0}),e}}function createSegmentCompletion(){function done(){if(!(n||r||p||g||$||d[e])){var t=c.apply(h,arguments
);m["s"+e]=t.length>1?t:t[0],d[e]=!0,scheduleGateTick()}}var e=d.length;return done.fail=function $$segment$fail(){n||r||p||g||$||
d[e]||(p=!0,o=f.call(arguments),scheduleGateTick())},done.abort=function $$segment$abort(){n||r||p||g||$||(g=!0,gateTick())},done
.errfcb=function $$segment$errfcb(e){e?done.fail(e):done.apply(h,f.call(arguments,1))},d[e]=null,done}var a,i,o,s,p=!1,g=!1,$=!1
,d=[],m={};t.some(function $$some(e){if(p||g)return!0;a=u.slice(),a.unshift(createSegmentCompletion());try{e.apply(h,a)}catch(n){
return i=n,p=!0,!0}}),i&&(l(i)?e.fail.apply(h,i):e.fail(i))}function then(){return n||r||0===arguments.length?d:(wrapArgs(arguments
,thenWrapper).forEach(function $$each(e){i(e)?seq(e):s.push(e)}),scheduleSequenceTick(),d)}function or(){return r||0===arguments
.length?d:(p.push.apply(p,arguments),scheduleSequenceTick(),d)}function gate(){if(n||r||0===arguments.length)return d;var e=f.call
(arguments).map(function $$map(e){var n;return i(e)?(n={seq:e},tapSequence(n),function $$segment(e){n.seq.pipe(e)}):e});return then
(function $$then(n){var t=f.call(arguments,1);createGate(n,e,t)}),d}function pipe(){return r||0===arguments.length?d:(f.call(arguments
).forEach(function $$each(e){then(function $$then(n){e.apply(h,f.call(arguments,1)),n()}).or(e.fail)}),d)}function seq(){return
n||r||0===arguments.length?d:(f.call(arguments).forEach(function $$each(e){var n={seq:e};i(e)&&tapSequence(n),then(function $$then
(e){var t=n.seq;i(t)||(t=n.seq.apply(h,f.call(arguments,1))),t.pipe(e)})}),d)}function val(){return n||r||0===arguments.length?d
:(f.call(wrapArgs(arguments,valWrapper)).forEach(function $$each(e){then(function $$then(n){var t=e.apply(h,f.call(arguments,1));
l(t)||(t=c(t)),n.apply(h,t)})}),d)}function promise(){function wrap(e){return function $$fn(){e.apply(h,l(arguments[0])?arguments
[0]:arguments)}}return n||r||0===arguments.length?d:(f.call(arguments).forEach(function $$each(e){then(function $$then(n){var t=
e;"function"==typeof e&&"function"!=typeof e.then&&(t=e.apply(h,f.call(arguments,1))),t.then(wrap(n),wrap(n.fail))})}),d)}function
 fork(){var e;return val(function $$val(){return e?e.apply(h,arguments):e=createSequence.apply(h,arguments).defer(),c.apply(h,arguments
)}),or(function $$or(){if(e)e.fail.apply(h,arguments);else{var n=f.call(arguments);e=createSequence().then(function $$then(e){e.
fail.apply(h,n)}).def ...
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.asynquence.clone"></a>[function <span class="apidocSignatureSpan">asynquence.</span>clone ()](#apidoc.element.asynquence.clone)
- description and source-code
```javascript
function $$public$clone() {
		return DEF(name,context);
	}
```
- example usage
```shell
...

'ASQ.iterable(..)' is added by the 'iterable-sequence' contrib plugin. See [Iterable Sequences](#iterable-sequences) below for more
 information.

'ASQ.unpause(..)' is a helper for dealing with "paused" (aka, *just* duplicated) sequences (see 'duplicate()' above).

'ASQ.noConflict()' rolls back the global 'ASQ' identifier and returns the current API instance to you. This can be used to keep
your global namespace clean, or it can be used to have multiple simultaneous libraries (including separate versions/copies of *asynquence
*!) in the same program without conflicts over the 'ASQ' global identifier.

'ASQ.clone()' creates a fresh, clean copy of *asynquence*. This is primarily useful if you want to have different *asynquence* copies
 which are each extended with different plugins (see below).

**Note:** In node.js, if you load contrib bundle(s) from the standard top-level package location ('./node_modules/asynquence-contrib
/a-bundle-file.js'), it will automatically look for and load (if found) the peer *asynquence* top-level package ('./node_modules
/asynquence/') and return it. So as a shortcut, you could simply do: 'var ASQ = require("asynquence-contrib")' instead of loading
 both packages separately.

However, if you load contrib bundle(s) that cannot find a peer *asynquence* top-level package to load and use, a dependency-injection
 function is instead returned, which expects to be called with either an *asynquence* instance, or a relative path specifying where
 to load it.

In node, we can use the npm package 'freshy' to let us reload the *asynquence* package to get a fresh copy of it, for each bundle
 to attach to:
...
```

#### <a name="apidoc.element.asynquence.extend"></a>[function <span class="apidocSignatureSpan">asynquence.</span>extend (name, build)](#apidoc.element.asynquence.extend)
- description and source-code
```javascript
function $$public$extend(name, build) {
		extensions[name] = build;

		return createSequence;
	}
```
- example usage
```shell
...

<script>ASQ = ASQ2;</script>
<script src="./path/to/bundle2.js"></script>
'''

### Plugin Extensions

'ASQ.extend( {name}, {build} )' allows you to specify an API extension, giving it a 'name' and a 'build' function callback that
should return the implementation of your API extension. The 'build' callback is provided two parameters, the sequence 'api' instance
, and an 'internals(..)' method, which lets you get or set values of various internal properties (generally, don't use this if you
 can avoid it).

Example:

'''js
// "foobar" plugin, which injects message "foobar!"
// into the sequence stream
ASQ.extend("foobar",function __build__(api,internals){
...
```

#### <a name="apidoc.element.asynquence.failed"></a>[function <span class="apidocSignatureSpan">asynquence.</span>failed ()](#apidoc.element.asynquence.failed)
- description and source-code
```javascript
function $$public$failed() {
		var args = ASQmessages.apply(ø,arguments);
		return createSequence(function $$failed(){ throw args; }).defer();
	}
```
- example usage
```shell
...

    'ASQ(function(done){ somethingAsync(done.errfcb); })' is sugar short-hand for 'ASQ(function(done){ somethingAsync(function(err
){ if (err) done.fail(err); else done.apply(null,[].slice.call(arguments,1))}); })'.

You can also 'abort()' a sequence at any time, which will prevent any further actions from occurring on that sequence (all callbacks
 will be ignored). The call to 'abort()' can happen on the sequence API itself, or using the 'abort' flag on a completion trigger
 in any step (see example below).

#### API Static Functions

'ASQ.failed(..)' produces a sequence which is already in the failed state. If you pass messages along to 'failed(..)', they will
 be the error messages for the sequence.

'ASQ.messages(..)' wraps a set of values as a ASQ-branded array, making it easier to pass multiple messages at once, and also to
 make it easier to distinguish a normal array (a value) from a value-messages container array, using 'ASQ.isMessageWrapper(..)'.

If you want to test if any arbitrary object is an *asynquence* sequence instance, use 'ASQ.isSequence(..)'.

'ASQ.iterable(..)' is added by the 'iterable-sequence' contrib plugin. See [Iterable Sequences](#iterable-sequences) below for more
 information.
...
```

#### <a name="apidoc.element.asynquence.isMessageWrapper"></a>[function <span class="apidocSignatureSpan">asynquence.</span>isMessageWrapper (val)](#apidoc.element.asynquence.isMessageWrapper)
- description and source-code
```javascript
function $$public$isMessageWrapper(val) {
		return checkBranding(val) && Array.isArray(val);
	}
```
- example usage
```shell
...

You can also 'abort()' a sequence at any time, which will prevent any further actions from occurring on that sequence (all callbacks
 will be ignored). The call to 'abort()' can happen on the sequence API itself, or using the 'abort' flag on a completion trigger
 in any step (see example below).

#### API Static Functions

'ASQ.failed(..)' produces a sequence which is already in the failed state. If you pass messages along to 'failed(..)', they will
 be the error messages for the sequence.

'ASQ.messages(..)' wraps a set of values as a ASQ-branded array, making it easier to pass multiple messages at once, and also to
 make it easier to distinguish a normal array (a value) from a value-messages container array, using 'ASQ.isMessageWrapper(..)'.

If you want to test if any arbitrary object is an *asynquence* sequence instance, use 'ASQ.isSequence(..)'.

'ASQ.iterable(..)' is added by the 'iterable-sequence' contrib plugin. See [Iterable Sequences](#iterable-sequences) below for more
 information.

'ASQ.unpause(..)' is a helper for dealing with "paused" (aka, *just* duplicated) sequences (see 'duplicate()' above).
...
```

#### <a name="apidoc.element.asynquence.isSequence"></a>[function <span class="apidocSignatureSpan">asynquence.</span>isSequence (val)](#apidoc.element.asynquence.isSequence)
- description and source-code
```javascript
function $$public$isSequence(val) {
		return checkBranding(val) && !Array.isArray(val);
	}
```
- example usage
```shell
...

#### API Static Functions

'ASQ.failed(..)' produces a sequence which is already in the failed state. If you pass messages along to 'failed(..)', they will
 be the error messages for the sequence.

'ASQ.messages(..)' wraps a set of values as a ASQ-branded array, making it easier to pass multiple messages at once, and also to
 make it easier to distinguish a normal array (a value) from a value-messages container array, using 'ASQ.isMessageWrapper(..)'.

If you want to test if any arbitrary object is an *asynquence* sequence instance, use 'ASQ.isSequence(..)'.

'ASQ.iterable(..)' is added by the 'iterable-sequence' contrib plugin. See [Iterable Sequences](#iterable-sequences) below for more
 information.

'ASQ.unpause(..)' is a helper for dealing with "paused" (aka, *just* duplicated) sequences (see 'duplicate()' above).

'ASQ.noConflict()' rolls back the global 'ASQ' identifier and returns the current API instance to you. This can be used to keep
your global namespace clean, or it can be used to have multiple simultaneous libraries (including separate versions/copies of *asynquence
*!) in the same program without conflicts over the 'ASQ' global identifier.
...
```

#### <a name="apidoc.element.asynquence.messages"></a>[function <span class="apidocSignatureSpan">asynquence.</span>messages ()](#apidoc.element.asynquence.messages)
- description and source-code
```javascript
function $$public$messages() {
		var ret = ARRAY_SLICE.call(arguments);
		// brand the message wrapper so we can detect
		return brandIt(ret);
	}
```
- example usage
```shell
...

You can also 'abort()' a sequence at any time, which will prevent any further actions from occurring on that sequence (all callbacks
 will be ignored). The call to 'abort()' can happen on the sequence API itself, or using the 'abort' flag on a completion trigger
 in any step (see example below).

#### API Static Functions

'ASQ.failed(..)' produces a sequence which is already in the failed state. If you pass messages along to 'failed(..)', they will
 be the error messages for the sequence.

'ASQ.messages(..)' wraps a set of values as a ASQ-branded array, making it easier to pass multiple messages at once, and also to
 make it easier to distinguish a normal array (a value) from a value-messages container array, using 'ASQ.isMessageWrapper(..)'.

If you want to test if any arbitrary object is an *asynquence* sequence instance, use 'ASQ.isSequence(..)'.

'ASQ.iterable(..)' is added by the 'iterable-sequence' contrib plugin. See [Iterable Sequences](#iterable-sequences) below for more
 information.

'ASQ.unpause(..)' is a helper for dealing with "paused" (aka, *just* duplicated) sequences (see 'duplicate()' above).
...
```

#### <a name="apidoc.element.asynquence.noConflict"></a>[function <span class="apidocSignatureSpan">asynquence.</span>noConflict ()](#apidoc.element.asynquence.noConflict)
- description and source-code
```javascript
function $$public$noConflict() {
		if (context) {
			context[name] = old_public_api;
		}
		return createSequence;
	}
```
- example usage
```shell
...

If you want to test if any arbitrary object is an *asynquence* sequence instance, use 'ASQ.isSequence(..)'.

'ASQ.iterable(..)' is added by the 'iterable-sequence' contrib plugin. See [Iterable Sequences](#iterable-sequences) below for more
 information.

'ASQ.unpause(..)' is a helper for dealing with "paused" (aka, *just* duplicated) sequences (see 'duplicate()' above).

'ASQ.noConflict()' rolls back the global 'ASQ' identifier and returns the current API instance to you. This can be used to keep
your global namespace clean, or it can be used to have multiple simultaneous libraries (including separate versions/copies of *asynquence
*!) in the same program without conflicts over the 'ASQ' global identifier.

'ASQ.clone()' creates a fresh, clean copy of *asynquence*. This is primarily useful if you want to have different *asynquence* copies
 which are each extended with different plugins (see below).

**Note:** In node.js, if you load contrib bundle(s) from the standard top-level package location ('./node_modules/asynquence-contrib
/a-bundle-file.js'), it will automatically look for and load (if found) the peer *asynquence* top-level package ('./node_modules
/asynquence/') and return it. So as a shortcut, you could simply do: 'var ASQ = require("asynquence-contrib")' instead of loading
 both packages separately.

However, if you load contrib bundle(s) that cannot find a peer *asynquence* top-level package to load and use, a dependency-injection
 function is instead returned, which expects to be called with either an *asynquence* instance, or a relative path specifying where
 to load it.
...
```

#### <a name="apidoc.element.asynquence.unpause"></a>[function <span class="apidocSignatureSpan">asynquence.</span>unpause (sq)](#apidoc.element.asynquence.unpause)
- description and source-code
```javascript
function $$public$unpause(sq) {
		if (sq.unpause) sq.unpause();
		return sq;
	}
```
- example usage
```shell
...

**Note:** Unlike most other API methods, 'fork()' returns a new sequence instance, so chaining after 'fork()' would not be chaining
 off of the main sequence but off the forked sequence.

'Sq.fork()' is (sort-of) sugar short-hand for 'ASQ().seq(Sq)'.

* 'duplicate()' creates a separate copy of the current sequence (as it is at that moment). The duplicated sequence is "paused",
meaning it won't automatically run, even if the original sequence is already running.

To unpause the paused sequence-copy, call 'unpause()' on it. The other option is to call the helper 'ASQ.unpause(..)' and pass in
 a sequence. If the sequence is paused, it will be unpaused (and if not, just passes through safely).

**Note:** Technically, 'unpause()' schedules the sequence to be unpaused as the next "tick", so it doesn't really unpause *immediately
* (synchronously). This is consistent with all other calls to the API ('ASQ()', 'then()', 'gate()', etc), which all schedule procession
 of the sequence on the next "tick".

The instance form of 'unpause(..)' (not 'ASQ.unpause(..)') will accept any arguments sent to it and pass them along as messages
to the first step of the sequence, each time it's invoked. This allows you to setup different templated (duplicated) sequences with
 distinct initial message states, if necessary.

'unpause()' is only present on a sequence API in this initial paused state after it was duplicated from another sequence. It is
removed as soon as that next "tick" actually unpauses the sequence. It is safe to call multiple times until that next "tick", though
 that's not recommended. The 'ASQ.unpause(..)' helper is always present, and it first checks for an 'unpause()' on the specified
 sequence instance before calling it, so that's safer.
...
```



# <a name="apidoc.module.asynquence.asq"></a>[module asynquence.asq](#apidoc.module.asynquence.asq)

#### <a name="apidoc.element.asynquence.asq.asq"></a>[function <span class="apidocSignatureSpan">asynquence.</span>asq ()](#apidoc.element.asynquence.asq.asq)
- description and source-code
```javascript
function createSequence(){function scheduleSequenceTick(){r?sequenceTick():e||(e=schedule(sequenceTick))}function throwSequenceErrors
(){throw 1===$.length?$[0]:$}function sequenceTick(){var a,c;if(e=null,delete d.unpause,r)clearTimeout(e),e=null,s.length=p.length
=g.length=$.length=0;else if(n)for(0!==p.length||t||(t=!0,throwSequenceErrors());p.length;){t=!0,a=p.shift();try{a.apply(h,$)}catch
(i){l(i)?$=$.concat(i):($.push(i),i.stack&&$.push(i.stack)),0===p.length&&throwSequenceErrors()}}else if(u&&s.length>0){u=!1,a=s
.shift(),c=g.slice(),g.length=0,c.unshift(createStepCompletion());try{a.apply(h,c)}catch(i){l(i)?$=$.concat(i):$.push(i),n=!0,scheduleSequenceTick
()}}}function createStepCompletion(){function done(){n||r||u||e||(e=!0,u=!0,g.push.apply(g,arguments),$.length=0,scheduleSequenceTick
())}done.fail=function $$step$fail(){n||r||u||e||(n=!0,g.length=0,$.push.apply($,arguments),scheduleSequenceTick())},done.abort=
function $$step$abort(){n||r||(u=!1,r=!0,g.length=$.length=0,scheduleSequenceTick())},done.errfcb=function $$step$errfcb(e){e?done
.fail(e):done.apply(h,f.call(arguments,1))};var e=!1;return done}function createGate(e,t,u){function resetGate(){clearTimeout(s),
s=d=m=o=null}function scheduleGateTick(){return g?gateTick():void(s||(s=schedule(gateTick)))}function gateTick(){if(!(n||r||$)){
var t=[];s=null,p?(e.fail.apply(h,o),resetGate()):g?(e.abort(),resetGate()):checkGate()&&($=!0,d.forEach(function $$each(e,n){t.
push(m["s"+n])}),e.apply(h,t),resetGate())}}function checkGate(){if(0!==d.length){var e=!0;return d.some(function $$some(n){return
 null===n?(e=!1,!0):void 0}),e}}function createSegmentCompletion(){function done(){if(!(n||r||p||g||$||d[e])){var t=c.apply(h,arguments
);m["s"+e]=t.length>1?t:t[0],d[e]=!0,scheduleGateTick()}}var e=d.length;return done.fail=function $$segment$fail(){n||r||p||g||$||
d[e]||(p=!0,o=f.call(arguments),scheduleGateTick())},done.abort=function $$segment$abort(){n||r||p||g||$||(g=!0,gateTick())},done
.errfcb=function $$segment$errfcb(e){e?done.fail(e):done.apply(h,f.call(arguments,1))},d[e]=null,done}var a,i,o,s,p=!1,g=!1,$=!1
,d=[],m={};t.some(function $$some(e){if(p||g)return!0;a=u.slice(),a.unshift(createSegmentCompletion());try{e.apply(h,a)}catch(n){
return i=n,p=!0,!0}}),i&&(l(i)?e.fail.apply(h,i):e.fail(i))}function then(){return n||r||0===arguments.length?d:(wrapArgs(arguments
,thenWrapper).forEach(function $$each(e){i(e)?seq(e):s.push(e)}),scheduleSequenceTick(),d)}function or(){return r||0===arguments
.length?d:(p.push.apply(p,arguments),scheduleSequenceTick(),d)}function gate(){if(n||r||0===arguments.length)return d;var e=f.call
(arguments).map(function $$map(e){var n;return i(e)?(n={seq:e},tapSequence(n),function $$segment(e){n.seq.pipe(e)}):e});return then
(function $$then(n){var t=f.call(arguments,1);createGate(n,e,t)}),d}function pipe(){return r||0===arguments.length?d:(f.call(arguments
).forEach(function $$each(e){then(function $$then(n){e.apply(h,f.call(arguments,1)),n()}).or(e.fail)}),d)}function seq(){return
n||r||0===arguments.length?d:(f.call(arguments).forEach(function $$each(e){var n={seq:e};i(e)&&tapSequence(n),then(function $$then
(e){var t=n.seq;i(t)||(t=n.seq.apply(h,f.call(arguments,1))),t.pipe(e)})}),d)}function val(){return n||r||0===arguments.length?d
:(f.call(wrapArgs(arguments,valWrapper)).forEach(function $$each(e){then(function $$then(n){var t=e.apply(h,f.call(arguments,1));
l(t)||(t=c(t)),n.apply(h,t)})}),d)}function promise(){function wrap(e){return function $$fn(){e.apply(h,l(arguments[0])?arguments
[0]:arguments)}}return n||r||0===arguments.length?d:(f.call(arguments).forEach(function $$each(e){then(function $$then(n){var t=
e;"function"==typeof e&&"function"!=typeof e.then&&(t=e.apply(h,f.call(arguments,1))),t.then(wrap(n),wrap(n.fail))})}),d)}function
 fork(){var e;return val(function $$val(){return e?e.apply(h,arguments):e=createSequence.apply(h,arguments).defer(),c.apply(h,arguments
)}),or(function $$or(){if(e)e.fail.apply(h,arguments);else{var n=f.call(arguments);e=createSequence().then(function $$then(e){e.
fail.apply(h,n)}).def ...
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.asynquence.asq.__schedule"></a>[function <span class="apidocSignatureSpan">asynquence.asq.</span>__schedule (e)](#apidoc.element.asynquence.asq.__schedule)
- description and source-code
```javascript
function schedule(e){r.add(e),t||(t=u(r.drain))}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.asynquence.asq.__tapSequence"></a>[function <span class="apidocSignatureSpan">asynquence.asq.</span>__tapSequence (e)](#apidoc.element.asynquence.asq.__tapSequence)
- description and source-code
```javascript
function tapSequence(e){function trigger(){e.seq=createSequence.apply(h,arguments).defer()}trigger.fail=function $$trigger$fail(){
var n=f.call(arguments);e.seq=createSequence(function $$create$sequence(e){e.fail.apply(h,n)}).defer()},e.seq.val(function $$val
(){return trigger.apply(h,arguments),c.apply(h,arguments)}).or(function $$or(){trigger.fail.apply(h,arguments)}),e.seq=createSequence
(function $$create$sequence(e){trigger=e}).defer()}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.asynquence.asq.clone"></a>[function <span class="apidocSignatureSpan">asynquence.asq.</span>clone ()](#apidoc.element.asynquence.asq.clone)
- description and source-code
```javascript
function $$public$clone(){return DEF(e,n)}
```
- example usage
```shell
...

'ASQ.iterable(..)' is added by the 'iterable-sequence' contrib plugin. See [Iterable Sequences](#iterable-sequences) below for more
 information.

'ASQ.unpause(..)' is a helper for dealing with "paused" (aka, *just* duplicated) sequences (see 'duplicate()' above).

'ASQ.noConflict()' rolls back the global 'ASQ' identifier and returns the current API instance to you. This can be used to keep
your global namespace clean, or it can be used to have multiple simultaneous libraries (including separate versions/copies of *asynquence
*!) in the same program without conflicts over the 'ASQ' global identifier.

'ASQ.clone()' creates a fresh, clean copy of *asynquence*. This is primarily useful if you want to have different *asynquence* copies
 which are each extended with different plugins (see below).

**Note:** In node.js, if you load contrib bundle(s) from the standard top-level package location ('./node_modules/asynquence-contrib
/a-bundle-file.js'), it will automatically look for and load (if found) the peer *asynquence* top-level package ('./node_modules
/asynquence/') and return it. So as a shortcut, you could simply do: 'var ASQ = require("asynquence-contrib")' instead of loading
 both packages separately.

However, if you load contrib bundle(s) that cannot find a peer *asynquence* top-level package to load and use, a dependency-injection
 function is instead returned, which expects to be called with either an *asynquence* instance, or a relative path specifying where
 to load it.

In node, we can use the npm package 'freshy' to let us reload the *asynquence* package to get a fresh copy of it, for each bundle
 to attach to:
...
```

#### <a name="apidoc.element.asynquence.asq.extend"></a>[function <span class="apidocSignatureSpan">asynquence.asq.</span>extend (e, n)](#apidoc.element.asynquence.asq.extend)
- description and source-code
```javascript
function $$public$extend(e, n){return o[e]=n,createSequence}
```
- example usage
```shell
...

<script>ASQ = ASQ2;</script>
<script src="./path/to/bundle2.js"></script>
'''

### Plugin Extensions

'ASQ.extend( {name}, {build} )' allows you to specify an API extension, giving it a 'name' and a 'build' function callback that
should return the implementation of your API extension. The 'build' callback is provided two parameters, the sequence 'api' instance
, and an 'internals(..)' method, which lets you get or set values of various internal properties (generally, don't use this if you
 can avoid it).

Example:

'''js
// "foobar" plugin, which injects message "foobar!"
// into the sequence stream
ASQ.extend("foobar",function __build__(api,internals){
...
```

#### <a name="apidoc.element.asynquence.asq.failed"></a>[function <span class="apidocSignatureSpan">asynquence.asq.</span>failed ()](#apidoc.element.asynquence.asq.failed)
- description and source-code
```javascript
function $$public$failed(){var e=c.apply(h,arguments);return createSequence(function $$failed(){throw e}).defer()}
```
- example usage
```shell
...

    'ASQ(function(done){ somethingAsync(done.errfcb); })' is sugar short-hand for 'ASQ(function(done){ somethingAsync(function(err
){ if (err) done.fail(err); else done.apply(null,[].slice.call(arguments,1))}); })'.

You can also 'abort()' a sequence at any time, which will prevent any further actions from occurring on that sequence (all callbacks
 will be ignored). The call to 'abort()' can happen on the sequence API itself, or using the 'abort' flag on a completion trigger
 in any step (see example below).

#### API Static Functions

'ASQ.failed(..)' produces a sequence which is already in the failed state. If you pass messages along to 'failed(..)', they will
 be the error messages for the sequence.

'ASQ.messages(..)' wraps a set of values as a ASQ-branded array, making it easier to pass multiple messages at once, and also to
 make it easier to distinguish a normal array (a value) from a value-messages container array, using 'ASQ.isMessageWrapper(..)'.

If you want to test if any arbitrary object is an *asynquence* sequence instance, use 'ASQ.isSequence(..)'.

'ASQ.iterable(..)' is added by the 'iterable-sequence' contrib plugin. See [Iterable Sequences](#iterable-sequences) below for more
 information.
...
```

#### <a name="apidoc.element.asynquence.asq.isMessageWrapper"></a>[function <span class="apidocSignatureSpan">asynquence.asq.</span>isMessageWrapper (e)](#apidoc.element.asynquence.asq.isMessageWrapper)
- description and source-code
```javascript
function $$public$isMessageWrapper(e){return checkBranding(e)&&Array.isArray(e)}
```
- example usage
```shell
...

You can also 'abort()' a sequence at any time, which will prevent any further actions from occurring on that sequence (all callbacks
 will be ignored). The call to 'abort()' can happen on the sequence API itself, or using the 'abort' flag on a completion trigger
 in any step (see example below).

#### API Static Functions

'ASQ.failed(..)' produces a sequence which is already in the failed state. If you pass messages along to 'failed(..)', they will
 be the error messages for the sequence.

'ASQ.messages(..)' wraps a set of values as a ASQ-branded array, making it easier to pass multiple messages at once, and also to
 make it easier to distinguish a normal array (a value) from a value-messages container array, using 'ASQ.isMessageWrapper(..)'.

If you want to test if any arbitrary object is an *asynquence* sequence instance, use 'ASQ.isSequence(..)'.

'ASQ.iterable(..)' is added by the 'iterable-sequence' contrib plugin. See [Iterable Sequences](#iterable-sequences) below for more
 information.

'ASQ.unpause(..)' is a helper for dealing with "paused" (aka, *just* duplicated) sequences (see 'duplicate()' above).
...
```

#### <a name="apidoc.element.asynquence.asq.isSequence"></a>[function <span class="apidocSignatureSpan">asynquence.asq.</span>isSequence (e)](#apidoc.element.asynquence.asq.isSequence)
- description and source-code
```javascript
function $$public$isSequence(e){return checkBranding(e)&&!Array.isArray(e)}
```
- example usage
```shell
...

#### API Static Functions

'ASQ.failed(..)' produces a sequence which is already in the failed state. If you pass messages along to 'failed(..)', they will
 be the error messages for the sequence.

'ASQ.messages(..)' wraps a set of values as a ASQ-branded array, making it easier to pass multiple messages at once, and also to
 make it easier to distinguish a normal array (a value) from a value-messages container array, using 'ASQ.isMessageWrapper(..)'.

If you want to test if any arbitrary object is an *asynquence* sequence instance, use 'ASQ.isSequence(..)'.

'ASQ.iterable(..)' is added by the 'iterable-sequence' contrib plugin. See [Iterable Sequences](#iterable-sequences) below for more
 information.

'ASQ.unpause(..)' is a helper for dealing with "paused" (aka, *just* duplicated) sequences (see 'duplicate()' above).

'ASQ.noConflict()' rolls back the global 'ASQ' identifier and returns the current API instance to you. This can be used to keep
your global namespace clean, or it can be used to have multiple simultaneous libraries (including separate versions/copies of *asynquence
*!) in the same program without conflicts over the 'ASQ' global identifier.
...
```

#### <a name="apidoc.element.asynquence.asq.messages"></a>[function <span class="apidocSignatureSpan">asynquence.asq.</span>messages ()](#apidoc.element.asynquence.asq.messages)
- description and source-code
```javascript
function $$public$messages(){var e=f.call(arguments);return brandIt(e)}
```
- example usage
```shell
...

You can also 'abort()' a sequence at any time, which will prevent any further actions from occurring on that sequence (all callbacks
 will be ignored). The call to 'abort()' can happen on the sequence API itself, or using the 'abort' flag on a completion trigger
 in any step (see example below).

#### API Static Functions

'ASQ.failed(..)' produces a sequence which is already in the failed state. If you pass messages along to 'failed(..)', they will
 be the error messages for the sequence.

'ASQ.messages(..)' wraps a set of values as a ASQ-branded array, making it easier to pass multiple messages at once, and also to
 make it easier to distinguish a normal array (a value) from a value-messages container array, using 'ASQ.isMessageWrapper(..)'.

If you want to test if any arbitrary object is an *asynquence* sequence instance, use 'ASQ.isSequence(..)'.

'ASQ.iterable(..)' is added by the 'iterable-sequence' contrib plugin. See [Iterable Sequences](#iterable-sequences) below for more
 information.

'ASQ.unpause(..)' is a helper for dealing with "paused" (aka, *just* duplicated) sequences (see 'duplicate()' above).
...
```

#### <a name="apidoc.element.asynquence.asq.noConflict"></a>[function <span class="apidocSignatureSpan">asynquence.asq.</span>noConflict ()](#apidoc.element.asynquence.asq.noConflict)
- description and source-code
```javascript
function $$public$noConflict(){return n&&(n[e]=s),createSequence}
```
- example usage
```shell
...

If you want to test if any arbitrary object is an *asynquence* sequence instance, use 'ASQ.isSequence(..)'.

'ASQ.iterable(..)' is added by the 'iterable-sequence' contrib plugin. See [Iterable Sequences](#iterable-sequences) below for more
 information.

'ASQ.unpause(..)' is a helper for dealing with "paused" (aka, *just* duplicated) sequences (see 'duplicate()' above).

'ASQ.noConflict()' rolls back the global 'ASQ' identifier and returns the current API instance to you. This can be used to keep
your global namespace clean, or it can be used to have multiple simultaneous libraries (including separate versions/copies of *asynquence
*!) in the same program without conflicts over the 'ASQ' global identifier.

'ASQ.clone()' creates a fresh, clean copy of *asynquence*. This is primarily useful if you want to have different *asynquence* copies
 which are each extended with different plugins (see below).

**Note:** In node.js, if you load contrib bundle(s) from the standard top-level package location ('./node_modules/asynquence-contrib
/a-bundle-file.js'), it will automatically look for and load (if found) the peer *asynquence* top-level package ('./node_modules
/asynquence/') and return it. So as a shortcut, you could simply do: 'var ASQ = require("asynquence-contrib")' instead of loading
 both packages separately.

However, if you load contrib bundle(s) that cannot find a peer *asynquence* top-level package to load and use, a dependency-injection
 function is instead returned, which expects to be called with either an *asynquence* instance, or a relative path specifying where
 to load it.
...
```

#### <a name="apidoc.element.asynquence.asq.unpause"></a>[function <span class="apidocSignatureSpan">asynquence.asq.</span>unpause (e)](#apidoc.element.asynquence.asq.unpause)
- description and source-code
```javascript
function $$public$unpause(e){return e.unpause&&e.unpause(),e}
```
- example usage
```shell
...

**Note:** Unlike most other API methods, 'fork()' returns a new sequence instance, so chaining after 'fork()' would not be chaining
 off of the main sequence but off the forked sequence.

'Sq.fork()' is (sort-of) sugar short-hand for 'ASQ().seq(Sq)'.

* 'duplicate()' creates a separate copy of the current sequence (as it is at that moment). The duplicated sequence is "paused",
meaning it won't automatically run, even if the original sequence is already running.

To unpause the paused sequence-copy, call 'unpause()' on it. The other option is to call the helper 'ASQ.unpause(..)' and pass in
 a sequence. If the sequence is paused, it will be unpaused (and if not, just passes through safely).

**Note:** Technically, 'unpause()' schedules the sequence to be unpaused as the next "tick", so it doesn't really unpause *immediately
* (synchronously). This is consistent with all other calls to the API ('ASQ()', 'then()', 'gate()', etc), which all schedule procession
 of the sequence on the next "tick".

The instance form of 'unpause(..)' (not 'ASQ.unpause(..)') will accept any arguments sent to it and pass them along as messages
to the first step of the sequence, each time it's invoked. This allows you to setup different templated (duplicated) sequences with
 distinct initial message states, if necessary.

'unpause()' is only present on a sequence API in this initial paused state after it was duplicated from another sequence. It is
removed as soon as that next "tick" actually unpauses the sequence. It is safe to call multiple times until that next "tick", though
 that's not recommended. The 'ASQ.unpause(..)' helper is always present, and it first checks for an 'unpause()' on the specified
 sequence instance before calling it, so that's safer.
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
