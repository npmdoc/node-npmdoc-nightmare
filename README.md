# api documentation for  [nightmare (v2.10.0)](https://github.com/segmentio/nightmare#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-nightmare.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-nightmare) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-nightmare.svg)](https://travis-ci.org/npmdoc/node-npmdoc-nightmare)
#### A high-level browser automation library.

[![NPM](https://nodei.co/npm/nightmare.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/nightmare)

[![apidoc](https://npmdoc.github.io/node-npmdoc-nightmare/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-nightmare/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-nightmare/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-nightmare/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Segment"
    },
    "bugs": {
        "url": "https://github.com/segmentio/nightmare/issues"
    },
    "dependencies": {
        "debug": "^2.2.0",
        "deep-defaults": "^1.0.3",
        "defaults": "^1.0.2",
        "electron": "^1.4.4",
        "enqueue": "^1.0.2",
        "function-source": "^0.1.0",
        "jsesc": "^0.5.0",
        "minstache": "^1.2.0",
        "mkdirp": "^0.5.1",
        "once": "^1.3.3",
        "rimraf": "^2.4.3",
        "sliced": "1.0.1",
        "split2": "^2.0.1"
    },
    "description": "A high-level browser automation library.",
    "devDependencies": {
        "basic-auth": "^1.0.3",
        "basic-auth-connect": "^1.0.0",
        "bluebird": "^3.4.0",
        "chai": "^3.4.1",
        "chai-as-promised": "^5.3.0",
        "express": "^4.13.3",
        "mocha": "^2.3.0",
        "mocha-generators": "^1.2.0",
        "multer": "1.1.0",
        "pngjs": "^2.2.0",
        "serve-static": "^1.10.0",
        "split": "^1.0.0"
    },
    "directories": {},
    "dist": {
        "shasum": "e9c5d590bb296f59685fd48218c2fbac44767b21",
        "tarball": "https://registry.npmjs.org/nightmare/-/nightmare-2.10.0.tgz"
    },
    "engines": {
        "node": ">=4.0.0"
    },
    "gitHead": "e8c4ad3919bcb1d6440106baf57eafdee09d92ff",
    "homepage": "https://github.com/segmentio/nightmare#readme",
    "keywords": [
        "nightmare",
        "electron"
    ],
    "license": "MIT",
    "main": "lib/nightmare.js",
    "maintainers": [
        {
            "name": "bdentino"
        },
        {
            "name": "mattmueller"
        },
        {
            "name": "reinpk"
        },
        {
            "name": "rosshinkley"
        },
        {
            "name": "segment-admin"
        },
        {
            "name": "stephenmathieson"
        }
    ],
    "name": "nightmare",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git+https://github.com/segmentio/nightmare.git"
    },
    "scripts": {
        "test": "make test"
    },
    "version": "2.10.0"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module nightmare](#apidoc.module.nightmare)
1.  [function <span class="apidocSignatureSpan"></span>nightmare (options)](#apidoc.element.nightmare.nightmare)
1.  [function <span class="apidocSignatureSpan">nightmare.</span>Promise ()](#apidoc.element.nightmare.Promise)
1.  [function <span class="apidocSignatureSpan">nightmare.</span>action ()](#apidoc.element.nightmare.action)
1.  [function <span class="apidocSignatureSpan">nightmare.</span>toString ()](#apidoc.element.nightmare.toString)
1.  object <span class="apidocSignatureSpan">nightmare.</span>childActions
1.  object <span class="apidocSignatureSpan">nightmare.</span>namespaces
1.  string <span class="apidocSignatureSpan">nightmare.</span>version



# <a name="apidoc.module.nightmare"></a>[module nightmare](#apidoc.module.nightmare)

#### <a name="apidoc.element.nightmare.nightmare"></a>[function <span class="apidocSignatureSpan"></span>nightmare (options)](#apidoc.element.nightmare.nightmare)
- description and source-code
```javascript
function Nightmare(options) {
  if (!(this instanceof Nightmare)) return new Nightmare(options);
  options = options || {};
  var electronArgs = {};
  var self = this;

  options.waitTimeout = options.waitTimeout || DEFAULT_WAIT_TIMEOUT;
  options.gotoTimeout = options.gotoTimeout || DEFAULT_GOTO_TIMEOUT;
  options.pollInterval = options.pollInterval || DEFAULT_POLL_INTERVAL;

  options.typeInterval = options.typeInterval || DEFAULT_TYPE_INTERVAL;
  options.executionTimeout = options.executionTimeout || DEFAULT_EXECUTION_TIMEOUT;
  options.webPreferences = options.webPreferences || {};

  // null is a valid value, which will result in the use of the electron default behavior, which is to persist storage.
  // The default behavior for nightmare will be to use non-persistent storage.
  // http://electron.atom.io/docs/api/browser-window/#new-browserwindowoptions
  options.webPreferences.partition = options.webPreferences.partition !== undefined ? options.webPreferences.partition : DEFAULT_PARTITION
;

  options.Promise = options.Promise || Nightmare.Promise || Promise;

  var electron_path = options.electronPath || default_electron_path

  if (options.paths) {
    electronArgs.paths = options.paths;
  }

  if (options.switches) {
    electronArgs.switches = options.switches;
  }
  options.maxAuthRetries = options.maxAuthRetries || MAX_AUTH_RETRIES;

  electronArgs.loadTimeout = options.loadTimeout;
  if(options.loadTimeout && options.gotoTimeout && options.loadTimeout < options.gotoTimeout){
    debug('WARNING:  load timeout of ${options.loadTimeout} is shorter than goto timeout of ${options.gotoTimeout}');
  }

  electronArgs.dock = options.dock || false;

  attachToProcess(this);

  // initial state
  this.state = 'initial';
  this.running = false;
  this.ending = false;
  this.ended = false;
  this._queue = [];
  this._headers = {};
  this.options = options;

  debug('queuing process start');
  this.queue((done) => {

    this.proc = proc.spawn(electron_path, [runner].concat(JSON.stringify(electronArgs)), {
      stdio: [null, null, null, 'ipc'],
      env: defaults(options.env || {}, process.env)
    });

    this.proc.stdout.pipe(split2()).on('data', (data) => {
      electronLog.stdout(data);
    });

    this.proc.stderr.pipe(split2()).on('data', (data) => {
      electronLog.stderr(data);
    });

    this.proc.on('close', (code) => {
      if(!self.ended){
        handleExit(code, self, noop);
      }
    });

    this.child = child(this.proc);

    this.child.once('die', function(err){
      debug('dying: ' + err);
      self.die = err;
    });

    // propagate console.log(...) through
    this.child.on('log', function() {
      log.apply(log, arguments);
    });

    this.child.on('uncaughtException', function(stack) {
      console.error('Nightmare runner error:\n\n%s\n', '\t' + stack.replace(/\n/g, '\n\t'));
      endInstance(self, noop);
      process.exit(1);
    });

    this.child.on('page', function(type) {
      log.apply(null, ['page-' + type].concat(sliced(arguments, 1)));
    });

    // propogate events through to debugging
    this.child.on('did-finish-load', function () { log('did-finish-load', JSON.stringify(Array.prototype.slice.call(arguments))); });
    this.child.on('did-fail-load', function () { log('did-fail-load', JSON.stringify(Array.prototype.slice.call(arguments))); });
    this.child.on('did-fail-provisional-load', function () { log('did-fail-provisional-load', JSON.stringify(Array.prototype.slice
.call(arguments))); });
    this.child.on('did-frame-finish-load', function () { log('did-frame-finish-load', JSON.stringify(Array.prototype.slice.call(
arguments))); });
    this.child.on('did-start-loading', function () { log('did-start-loading', JSON.stringify(Array.prototype.slice.call(arguments
))); });
    this.child.on('did-stop-loading', function () { log('did-stop-loading', JSON.stringify(Array.prototype.slice.call(arguments))); });
    this.child.on('did-get-response-details', function () { log('did-get-response-details', JSON.stringify(Array.prototype.slice
.call(arguments))); }); ...
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.nightmare.Promise"></a>[function <span class="apidocSignatureSpan">nightmare.</span>Promise ()](#apidoc.element.nightmare.Promise)
- description and source-code
```javascript
function Promise() { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.nightmare.action"></a>[function <span class="apidocSignatureSpan">nightmare.</span>action ()](#apidoc.element.nightmare.action)
- description and source-code
```javascript
action = function () {
  var name = arguments[0], childfn, parentfn;
  if(arguments.length === 2) {
    parentfn = arguments[1];
  } else {
    parentfn = arguments[2];
    childfn = arguments[1];
  }

  // support functions and objects
  // if it's an object, wrap it's
  // properties in the queue function

  if(parentfn) {
    if (typeof parentfn === 'function') {
      Nightmare.prototype[name] = queued(name, parentfn);
    } else {
      if (!~Nightmare.namespaces.indexOf(name)) {
        Nightmare.namespaces.push(name);
      }
      Nightmare.prototype[name] = function() {
        var self = this;
        return keys(parentfn).reduce(function (obj, key) {
          obj[key] = queued(name, parentfn[key]).bind(self)
        return obj;
        }, {});
      }
    }
  }

  if(childfn) {
    if (typeof childfn === 'function') {
     Nightmare.childActions[name] = childfn;
    } else {
      for(var key in childfn){
        Nightmare.childActions[name+'.'+key] = childfn;
      }
    }
  }
}
```
- example usage
```shell
...
var Promise = require('bluebird');

var nightmare = Nightmare({ Promise });
'''

### Extending Nightmare

#### Nightmare.action(name, [electronAction|electronNamespace], action|namespace)

You can add your own custom actions to the Nightmare prototype. Here's an example:

'''js
Nightmare.action('size', function (done) {
this.evaluate_now(function() {
  var w = Math.max(document.documentElement.clientWidth, window.innerWidth || 0)
...
```

#### <a name="apidoc.element.nightmare.toString"></a>[function <span class="apidocSignatureSpan">nightmare.</span>toString ()](#apidoc.element.nightmare.toString)
- description and source-code
```javascript
toString = function () {
    return toString;
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
