# api documentation for  [nightmare (v2.10.0)](https://github.com/segmentio/nightmare#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-nightmare.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-nightmare) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-nightmare.svg)](https://travis-ci.org/npmdoc/node-npmdoc-nightmare)
#### A high-level browser automation library.

[![NPM](https://nodei.co/npm/nightmare.png?downloads=true)](https://www.npmjs.com/package/nightmare)

[![apidoc](https://npmdoc.github.io/node-npmdoc-nightmare/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-nightmare_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-nightmare/build..beta..travis-ci.org/apidoc.html)

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
            "name": "bdentino",
            "email": "brian.dentino@gmail.com"
        },
        {
            "name": "mattmueller",
            "email": "mattmuelle@gmail.com"
        },
        {
            "name": "reinpk",
            "email": "reinpk@gmail.com"
        },
        {
            "name": "rosshinkley",
            "email": "rosshinkley@gmail.com"
        },
        {
            "name": "segment-admin",
            "email": "tools+npm@segment.com"
        },
        {
            "name": "stephenmathieson",
            "email": "me@stephenmathieson.com"
        }
    ],
    "name": "nightmare",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
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
1.  [function <span class="apidocSignatureSpan">nightmare.</span>Promise ()](#apidoc.element.nightmare.Promise)
1.  [function <span class="apidocSignatureSpan">nightmare.</span>action ()](#apidoc.element.nightmare.action)
1.  [function <span class="apidocSignatureSpan">nightmare.</span>frame_manager (window)](#apidoc.element.nightmare.frame_manager)
1.  object <span class="apidocSignatureSpan">nightmare.</span>actions
1.  object <span class="apidocSignatureSpan">nightmare.</span>childActions
1.  object <span class="apidocSignatureSpan">nightmare.</span>javascript
1.  object <span class="apidocSignatureSpan">nightmare.</span>namespaces
1.  string <span class="apidocSignatureSpan">nightmare.</span>version

#### [module nightmare.actions](#apidoc.module.nightmare.actions)
1.  [function <span class="apidocSignatureSpan">nightmare.actions.</span>authentication (login, password, done)](#apidoc.element.nightmare.actions.authentication)
1.  [function <span class="apidocSignatureSpan">nightmare.actions.</span>back (done)](#apidoc.element.nightmare.actions.back)
1.  [function <span class="apidocSignatureSpan">nightmare.actions.</span>check (selector, done)](#apidoc.element.nightmare.actions.check)
1.  [function <span class="apidocSignatureSpan">nightmare.actions.</span>click (selector, done)](#apidoc.element.nightmare.actions.click)
1.  [function <span class="apidocSignatureSpan">nightmare.actions.</span>engineVersions (done)](#apidoc.element.nightmare.actions.engineVersions)
1.  [function <span class="apidocSignatureSpan">nightmare.actions.</span>evaluate (fn)](#apidoc.element.nightmare.actions.evaluate)
1.  [function <span class="apidocSignatureSpan">nightmare.actions.</span>exists (selector, done)](#apidoc.element.nightmare.actions.exists)
1.  [function <span class="apidocSignatureSpan">nightmare.actions.</span>forward (done)](#apidoc.element.nightmare.actions.forward)
1.  [function <span class="apidocSignatureSpan">nightmare.actions.</span>html (path, saveType, done)](#apidoc.element.nightmare.actions.html)
1.  [function <span class="apidocSignatureSpan">nightmare.actions.</span>inject (type, file, done)](#apidoc.element.nightmare.actions.inject)
1.  [function <span class="apidocSignatureSpan">nightmare.actions.</span>insert (selector, text, done)](#apidoc.element.nightmare.actions.insert)
1.  [function <span class="apidocSignatureSpan">nightmare.actions.</span>mousedown (selector, done)](#apidoc.element.nightmare.actions.mousedown)
1.  [function <span class="apidocSignatureSpan">nightmare.actions.</span>mouseover (selector, done)](#apidoc.element.nightmare.actions.mouseover)
1.  [function <span class="apidocSignatureSpan">nightmare.actions.</span>mouseup (selector, done)](#apidoc.element.nightmare.actions.mouseup)
1.  [function <span class="apidocSignatureSpan">nightmare.actions.</span>path (done)](#apidoc.element.nightmare.actions.path)
1.  [function <span class="apidocSignatureSpan">nightmare.actions.</span>pdf (path, options, done)](#apidoc.element.nightmare.actions.pdf)
1.  [function <span class="apidocSignatureSpan">nightmare.actions.</span>refresh (done)](#apidoc.element.nightmare.actions.refresh)
1.  [function <span class="apidocSignatureSpan">nightmare.actions.</span>screenshot (path, clip, done)](#apidoc.element.nightmare.actions.screenshot)
1.  [function <span class="apidocSignatureSpan">nightmare.actions.</span>scrollTo (y, x, done)](#apidoc.element.nightmare.actions.scrollTo)
1.  [function <span class="apidocSignatureSpan">nightmare.actions.</span>select (selector, option, done)](#apidoc.element.nightmare.actions.select)
1.  [function <span class="apidocSignatureSpan">nightmare.actions.</span>title (done)](#apidoc.element.nightmare.actions.title)
1.  [function <span class="apidocSignatureSpan">nightmare.actions.</span>type ()](#apidoc.element.nightmare.actions.type)
1.  [function <span class="apidocSignatureSpan">nightmare.actions.</span>uncheck (selector, done)](#apidoc.element.nightmare.actions.uncheck)
1.  [function <span class="apidocSignatureSpan">nightmare.actions.</span>url (done)](#apidoc.element.nightmare.actions.url)
1.  [function <span class="apidocSignatureSpan">nightmare.actions.</span>useragent (useragent, done)](#apidoc.element.nightmare.actions.useragent)
1.  [function <span class="apidocSignatureSpan">nightmare.actions.</span>viewport (width, height, done)](#apidoc.element.nightmare.actions.viewport)
1.  [function <span class="apidocSignatureSpan">nightmare.actions.</span>visible (selector, done)](#apidoc.element.nightmare.actions.visible)
1.  [function <span class="apidocSignatureSpan">nightmare.actions.</span>wait ()](#apidoc.element.nightmare.actions.wait)
1.  object <span class="apidocSignatureSpan">nightmare.actions.</span>cookies

#### [module nightmare.frame_manager](#apidoc.module.nightmare.frame_manager)
1.  [function <span class="apidocSignatureSpan">nightmare.</span>frame_manager (window)](#apidoc.element.nightmare.frame_manager.frame_manager)
1.  [function <span class="apidocSignatureSpan">nightmare.frame_manager.</span>super_ ()](#apidoc.element.nightmare.frame_manager.super_)

#### [module nightmare.javascript](#apidoc.module.nightmare.javascript)
1.  [function <span class="apidocSignatureSpan">nightmare.javascript.</span>execute (obj )](#apidoc.element.nightmare.javascript.execute)
1.  [function <span class="apidocSignatureSpan">nightmare.javascript.</span>inject (obj )](#apidoc.element.nightmare.javascript.inject)



# <a name="apidoc.module.nightmare"></a>[module nightmare](#apidoc.module.nightmare)

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

#### <a name="apidoc.element.nightmare.frame_manager"></a>[function <span class="apidocSignatureSpan">nightmare.</span>frame_manager (window)](#apidoc.element.nightmare.frame_manager)
- description and source-code
```javascript
function FrameManager(window) {
  if (!(this instanceof FrameManager)) return new FrameManager(window);

  EventEmitter.call(this);
  var subscribed = false;
  var requestedFrame = false;
  var frameRequestTimeout;
  var self = this;

  this.on('newListener', subscribe);
  this.on('removeListener', unsubscribe);

  function subscribe(eventName) {
    if (!subscribed && eventName === 'data') {
      parent.emit('log', 'subscribing to browser window frames');
      window.webContents.beginFrameSubscription(receiveFrame);
    }
  }

  function unsubscribe() {
    if (!self.listenerCount('data')) {
      parent.emit('log', 'unsubscribing from browser window frames')
      window.webContents.endFrameSubscription();
      subscribed = false;
    }
  }

  function receiveFrame(buffer) {
    requestedFrame = false;
    clearTimeout(frameRequestTimeout);
    self.emit('data', buffer);
  }

<span class="apidocCodeCommentSpan">  /**
   * In addition to listening for events, calling 'requestFrame' will ensure
   * that a frame is queued up to render (instead of just waiting for the next
   * time the browser chooses to draw a frame).
   * @param {Function} [callback] Called when the frame is rendered.
   * @param {Number} [timeout=1000] If no frame has been rendered after this
       many milliseconds, run the callback anyway. In this case, The
       callback's first argument, an image buffer, will be 'null'.
   */
</span>  this.requestFrame = function(callback, timeout) {
    timeout = (timeout == undefined) ? 1000 : timeout;

    if (callback) {
      this.once('data', callback);
    }

    if (!requestedFrame) {
      requestedFrame = true;

      // Force the browser to render new content by using the debugger to
      // highlight a portion of the page. This way, we can guarantee a change
      // that both requires rendering a frame and does not actually affect
      // the content of the page.
      if (!window.webContents.debugger.isAttached()) {
        try {
          window.webContents.debugger.attach();
        }
        catch (error) {
          parent.emit('log', 'Failed to attach to debugger for frame subscriptions: ${error}');
          this.emit('data', null);
          return;
        }
      }

      if (timeout) {
        frameRequestTimeout = setTimeout(function() {
          parent.emit('log', 'FrameManager timing out after ${timeout} ms with no new rendered frames');
          self.emit('data', null)
        }, timeout);
      }

      parent.emit('log', 'Highlighting page to trigger rendering.');
      window.webContents.debugger.sendCommand('DOM.enable')
      window.webContents.debugger.sendCommand(
        'DOM.highlightRect', HIGHLIGHT_STYLE, function(error) {
          window.webContents.debugger.sendCommand('DOM.hideHighlight');
          window.webContents.debugger.detach();
        });
    }
  };
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.nightmare.actions"></a>[module nightmare.actions](#apidoc.module.nightmare.actions)

#### <a name="apidoc.element.nightmare.actions.authentication"></a>[function <span class="apidocSignatureSpan">nightmare.actions.</span>authentication (login, password, done)](#apidoc.element.nightmare.actions.authentication)
- description and source-code
```javascript
authentication = function (login, password, done) {
  debug('.authentication()');
  this.child.call('authentication', login, password, done);
}
```
- example usage
```shell
...

#### .engineVersions()
Gets the versions for Electron and Chromium.

#### .useragent(useragent)
Set the 'useragent' used by electron.

#### .authentication(user, password)
Set the 'user' and 'password' for accessing a web page using basic authentication. Be sure to set it before calling '.goto(url)'.

#### .end()
Complete any queue operations, disconnect and close the electron process.  Note that if you're using promises, '.then()' must be
 called after '.end()' to run the '.end()' task.  Also note that if using a '.end()' callback, the '.end()' call is equivalent to
 calling '.end()' followed by '.then(fn)'.  Consider:

'''js
nightmare
...
```

#### <a name="apidoc.element.nightmare.actions.back"></a>[function <span class="apidocSignatureSpan">nightmare.actions.</span>back (done)](#apidoc.element.nightmare.actions.back)
- description and source-code
```javascript
back = function (done) {
  debug('.back()');
  this.evaluate_now(function() {
    window.history.back();
  }, done);
}
```
- example usage
```shell
...
- 'details': A string with additional details about the error. This may be null or an empty string.
- 'url': The URL that failed to load

Note that any valid response from a server is considered “successful.” That means things like 404 “not found” errors are successful
 results for 'goto'. Only things that would cause no page to appear in the browser window, such as no server responding at the given
 address, the server hanging up in the middle of a response, or invalid URLs, are errors.

You can also adjust how long 'goto' will wait before timing out by setting the ['gotoTimeout' option](#gototimeout-default-30s)
on the Nightmare constructor.

#### .back()
Go back to the previous page.

#### .forward()
Go forward to the next page.

#### .refresh()
Refresh the current page.
...
```

#### <a name="apidoc.element.nightmare.actions.check"></a>[function <span class="apidocSignatureSpan">nightmare.actions.</span>check (selector, done)](#apidoc.element.nightmare.actions.check)
- description and source-code
```javascript
check = function (selector, done) {
  debug('.check() ' + selector);
  this.evaluate_now(function(selector) {
    var element = document.querySelector(selector);
    var event = document.createEvent('HTMLEvents');
    element.checked = true;
    event.initEvent('change', true, true);
    element.dispatchEvent(event);
  }, done, selector);
}
```
- example usage
```shell
...
> If you don't need the keyboard events, consider using '.insert()' instead as it will be faster and more robust.

#### .insert(selector[, text])
Similar to '.type()'. '.insert()' enters the 'text' provided into the 'selector' element.  Empty or falsey values provided for '
text' will clear the selector's value.

'.insert()' is faster than '.type()' but does not trigger the keyboard events.

#### .check(selector)
checks the 'selector' checkbox element.

#### .uncheck(selector)
unchecks the 'selector' checkbox element.

#### .select(selector, option)
Changes the 'selector' dropdown element to the option with attribute [value='option']
...
```

#### <a name="apidoc.element.nightmare.actions.click"></a>[function <span class="apidocSignatureSpan">nightmare.actions.</span>click (selector, done)](#apidoc.element.nightmare.actions.click)
- description and source-code
```javascript
click = function (selector, done) {
  debug('.click() on ' + selector);
  this.evaluate_now(function (selector) {
    document.activeElement.blur();
    var element = document.querySelector(selector);
    if (!element) {
      throw new Error('Unable to find element by selector: ' + selector);
    }
    var event = document.createEvent('MouseEvent');
    event.initEvent('click', true, true);
    element.dispatchEvent(event);
  }, done, selector);
}
```
- example usage
```shell
...
'''js
var Nightmare = require('nightmare');		
var nightmare = Nightmare({ show: true });

nightmare
.goto('https://duckduckgo.com')
.type('#search_form_input_homepage', 'github nightmare')
.click('#search_button_homepage')
.wait('#zero_click_wrapper .c-info__title a')
.evaluate(function () {
  return document.querySelector('#zero_click_wrapper .c-info__title a').href;
})
.end()
.then(function (result) {
  console.log(result);
...
```

#### <a name="apidoc.element.nightmare.actions.engineVersions"></a>[function <span class="apidocSignatureSpan">nightmare.actions.</span>engineVersions (done)](#apidoc.element.nightmare.actions.engineVersions)
- description and source-code
```javascript
engineVersions = function (done){
  debug('.engineVersions()');
  done(null, this.engineVersions);
}
```
- example usage
```shell
...
Defines the number of times to retry an authentication when set up with '.authenticate()'.
'''js
var nightmare = Nightmare({
  maxAuthRetries: 3
});
'''

#### .engineVersions()
Gets the versions for Electron and Chromium.

#### .useragent(useragent)
Set the 'useragent' used by electron.

#### .authentication(user, password)
Set the 'user' and 'password' for accessing a web page using basic authentication. Be sure to set it before calling '.goto(url)'.
...
```

#### <a name="apidoc.element.nightmare.actions.evaluate"></a>[function <span class="apidocSignatureSpan">nightmare.actions.</span>evaluate (fn)](#apidoc.element.nightmare.actions.evaluate)
- description and source-code
```javascript
evaluate = function (fn) {
  var args = sliced(arguments);
  var done = args[args.length-1];
  var self = this;
  var newDone = function(){
    clearTimeout(timeoutTimer);
    done.apply(self, arguments);
  };
  var newArgs = [fn, newDone].concat(args.slice(1,-1));
  if (typeof fn !== 'function') {
    return done(new Error('.evaluate() fn should be a function'));
  }
  debug('.evaluate() fn on the page');
  var timeoutTimer = setTimeout(function(){
    done(new Error('Evaluation timed out after ${self.options.executionTimeout}msec.  Are you calling done() or resolving your promises
?'));
  }, self.options.executionTimeout);
  this.evaluate_now.apply(this, newArgs);
}
```
- example usage
```shell
...
var nightmare = Nightmare({ show: true });

nightmare
.goto('https://duckduckgo.com')
.type('#search_form_input_homepage', 'github nightmare')
.click('#search_button_homepage')
.wait('#zero_click_wrapper .c-info__title a')
.evaluate(function () {
  return document.querySelector('#zero_click_wrapper .c-info__title a').href;
})
.end()
.then(function (result) {
  console.log(result);
})
.catch(function (error) {
...
```

#### <a name="apidoc.element.nightmare.actions.exists"></a>[function <span class="apidocSignatureSpan">nightmare.actions.</span>exists (selector, done)](#apidoc.element.nightmare.actions.exists)
- description and source-code
```javascript
exists = function (selector, done) {
  debug('.exists() for ' + selector);
  this.evaluate_now(function(selector) {
    return (document.querySelector(selector)!==null);
  }, done, selector);
}
```
- example usage
```shell
...
Wait until the 'fn' evaluated on the page with 'arg1, arg2,...' returns 'true'. All the 'args' are optional. See '.evaluate()' for
 usage.

#### .header([header, value])
Add a header override for all HTTP requests.  If 'header' is undefined, the header overrides will be reset.

### Extract from the Page

#### .exists(selector)
Returns whether the selector exists or not on the page.

#### .visible(selector)
Returns whether the selector is visible or not

#### .on(event, callback)
Capture page events with the callback. You have to call '.on()' before calling '.goto()'. Supported events are [documented here](
http://electron.atom.io/docs/api/web-contents/#instance-events).
...
```

#### <a name="apidoc.element.nightmare.actions.forward"></a>[function <span class="apidocSignatureSpan">nightmare.actions.</span>forward (done)](#apidoc.element.nightmare.actions.forward)
- description and source-code
```javascript
forward = function (done) {
  debug('.forward()');
  this.evaluate_now(function() {
    window.history.forward();
  }, done);
}
```
- example usage
```shell
...
Note that any valid response from a server is considered “successful.” That means things like 404 “not found” errors are successful
 results for 'goto'. Only things that would cause no page to appear in the browser window, such as no server responding at the given
 address, the server hanging up in the middle of a response, or invalid URLs, are errors.

You can also adjust how long 'goto' will wait before timing out by setting the ['gotoTimeout' option](#gototimeout-default-30s)
on the Nightmare constructor.

#### .back()
Go back to the previous page.

#### .forward()
Go forward to the next page.

#### .refresh()
Refresh the current page.

#### .click(selector)
Clicks the 'selector' element once.
...
```

#### <a name="apidoc.element.nightmare.actions.html"></a>[function <span class="apidocSignatureSpan">nightmare.actions.</span>html (path, saveType, done)](#apidoc.element.nightmare.actions.html)
- description and source-code
```javascript
html = function (path, saveType, done) {
  debug('.html()');
  if (typeof path === 'function' && !saveType && !done) {
    done = path;
    saveType = undefined;
    path = undefined;
  } else if (typeof path === 'object' && typeof saveType === 'function' && !done) {
    done = saveType;
    saveType = path;
    path = undefined;
  } else if (typeof saveType === 'function' && !done) {
    done = saveType;
    saveType = undefined;
  }
  this.child.call('html', path, saveType, function (error) {
    if (error) debug(error);
    done(error);
  });
}
```
- example usage
```shell
...

#### .removeListener(event, callback)
Removes a given listener callback for an event.

#### .screenshot([path][, clip])
Takes a screenshot of the current page. Useful for debugging. The output is always a 'png'. Both arguments are optional. If 'path
' is provided, it saves the image to the disk. Otherwise it returns a 'Buffer' of the image data. If 'clip' is provided (as [documented
 here](https://github.com/atom/electron/blob/master/docs/api/browser-window.md#wincapturepagerect-callback)), the image will be
clipped to the rectangle.

#### .html(path, saveType)
Save the current page as html as files to disk at the given path. Save type options are [here](https://github.com/atom/electron/
blob/master/docs/api/web-contents.md#webcontentssavepagefullpath-savetype-callback).

#### .pdf(path, options)
Saves a PDF to the specified 'path'. Options are [here](https://github.com/electron/electron/blob/v1.4.4/docs/api/web-contents.md
#contentsprinttopdfoptions-callback).

#### .title()
Returns the title of the current page.
...
```

#### <a name="apidoc.element.nightmare.actions.inject"></a>[function <span class="apidocSignatureSpan">nightmare.actions.</span>inject (type, file, done)](#apidoc.element.nightmare.actions.inject)
- description and source-code
```javascript
inject = function (type, file, done) {
  debug('.inject()-ing a file');
  if (type === 'js') {
    var js = fs.readFileSync(file, { encoding: 'utf-8' });
    this._inject(js, done);
  }
  else if (type === 'css') {
    var css = fs.readFileSync(file, { encoding: 'utf-8' });
    this.child.call('css', css, done);
  }
  else {
    debug('unsupported file type in .inject()');
    done();
  }
}
```
- example usage
```shell
...
#### .scrollTo(top, left)
Scrolls the page to desired position. 'top' and 'left' are always relative to the top left corner of the document.

#### .viewport(width, height)

Set the viewport size.

#### .inject(type, file)
Inject a local 'file' onto the current page. The file 'type' must be either 'js' or 'css'.

#### .evaluate(fn[, arg1, arg2,...])
Invokes 'fn' on the page with 'arg1, arg2,...'. All the 'args' are optional. On completion it returns the return value of 'fn'.
Useful for extracting information from the page. Here's an example:

'''js
var selector = 'h1';
...
```

#### <a name="apidoc.element.nightmare.actions.insert"></a>[function <span class="apidocSignatureSpan">nightmare.actions.</span>insert (selector, text, done)](#apidoc.element.nightmare.actions.insert)
- description and source-code
```javascript
insert = function (selector, text, done) {
  if (arguments.length === 2) {
    done = text
    text = null
  }

  debug('.insert() %s into %s', text, selector);
  var child = this.child;

  focusSelector.bind(this)(function(err) {
    if(err) {
      debug('Unable to .insert() into non-existent selector %s', selector);
      return done(err);
    }

    var blurDone = blurSelector.bind(this, done, selector);
    if ((text || '') == '') {
      this.evaluate_now(function(selector) {
        document.querySelector(selector).value = '';
      }, blurDone, selector);
    } else {
      child.call('insert', text, blurDone);
    }
  }, selector);
}
```
- example usage
```shell
...
#### .type(selector[, text])
Enters the 'text' provided into the 'selector' element.  Empty or falsey values provided for 'text' will clear the selector's value
.

'.type()' mimics a user typing in a textbox and will emit the proper keyboard events

Key presses can also be fired using Unicode values with '.type()'. For example, if you wanted to fire an enter key press, you would
  write '.type('body', '\u000d')'.

> If you don't need the keyboard events, consider using '.insert()' instead as it will be faster and more robust.

#### .insert(selector[, text])
Similar to '.type()'. '.insert()' enters the 'text' provided into the 'selector' element.  Empty or falsey values provided for '
text' will clear the selector's value.

'.insert()' is faster than '.type()' but does not trigger the keyboard events.

#### .check(selector)
...
```

#### <a name="apidoc.element.nightmare.actions.mousedown"></a>[function <span class="apidocSignatureSpan">nightmare.actions.</span>mousedown (selector, done)](#apidoc.element.nightmare.actions.mousedown)
- description and source-code
```javascript
mousedown = function (selector, done) {
  debug('.mousedown() on ' + selector);
  this.evaluate_now(function (selector) {
    var element = document.querySelector(selector);
    if (!element) {
      throw new Error('Unable to find element by selector: ' + selector);
    }
    var event = document.createEvent('MouseEvent');
    event.initEvent('mousedown', true, true);
    element.dispatchEvent(event);
  }, done, selector);
}
```
- example usage
```shell
...

#### .refresh()
Refresh the current page.

#### .click(selector)
Clicks the 'selector' element once.

#### .mousedown(selector)
Mousedown the 'selector' element once.

#### .mouseup(selector)
Mouseup the 'selector' element once.

#### .mouseover(selector)
Mouseover the 'selector' element once.
...
```

#### <a name="apidoc.element.nightmare.actions.mouseover"></a>[function <span class="apidocSignatureSpan">nightmare.actions.</span>mouseover (selector, done)](#apidoc.element.nightmare.actions.mouseover)
- description and source-code
```javascript
mouseover = function (selector, done) {
  debug('.mouseover() on ' + selector);
  this.evaluate_now(function (selector) {
    var element = document.querySelector(selector);
    if (!element) {
      throw new Error('Unable to find element by selector: ' + selector);
    }
    var event = document.createEvent('MouseEvent');
    event.initMouseEvent('mouseover', true, true);
    element.dispatchEvent(event);
  }, done, selector);
}
```
- example usage
```shell
...

#### .mousedown(selector)
Mousedown the 'selector' element once.

#### .mouseup(selector)
Mouseup the 'selector' element once.

#### .mouseover(selector)
Mouseover the 'selector' element once.

#### .type(selector[, text])
Enters the 'text' provided into the 'selector' element.  Empty or falsey values provided for 'text' will clear the selector's value
.

'.type()' mimics a user typing in a textbox and will emit the proper keyboard events
...
```

#### <a name="apidoc.element.nightmare.actions.mouseup"></a>[function <span class="apidocSignatureSpan">nightmare.actions.</span>mouseup (selector, done)](#apidoc.element.nightmare.actions.mouseup)
- description and source-code
```javascript
mouseup = function (selector, done) {
  debug('.mouseup() on ' + selector);
  this.evaluate_now(function (selector) {
    var element = document.querySelector(selector);
    if (!element) {
      throw new Error('Unable to find element by selector: ' + selector);
    }
    var event = document.createEvent('MouseEvent');
    event.initEvent('mouseup', true, true);
    element.dispatchEvent(event);
  }, done, selector);
}
```
- example usage
```shell
...

#### .click(selector)
Clicks the 'selector' element once.

#### .mousedown(selector)
Mousedown the 'selector' element once.

#### .mouseup(selector)
Mouseup the 'selector' element once.

#### .mouseover(selector)
Mouseover the 'selector' element once.

#### .type(selector[, text])
Enters the 'text' provided into the 'selector' element.  Empty or falsey values provided for 'text' will clear the selector's value
.
...
```

#### <a name="apidoc.element.nightmare.actions.path"></a>[function <span class="apidocSignatureSpan">nightmare.actions.</span>path (done)](#apidoc.element.nightmare.actions.path)
- description and source-code
```javascript
path = function (done) {
  debug('.path() getting it');
  this.evaluate_now(function() {
    return document.location.pathname;
  }, done);
}
```
- example usage
```shell
...

#### .title()
Returns the title of the current page.

#### .url()
Returns the url of the current page.

#### .path()
Returns the path name of the current page.

### Cookies

#### .cookies.get(name)

Get a cookie by it's 'name'. The url will be the current url.
...
```

#### <a name="apidoc.element.nightmare.actions.pdf"></a>[function <span class="apidocSignatureSpan">nightmare.actions.</span>pdf (path, options, done)](#apidoc.element.nightmare.actions.pdf)
- description and source-code
```javascript
pdf = function (path, options, done) {
  debug('.pdf()');
  if (typeof path === 'function' && !options && !done) {
    done = path;
    options = undefined;
    path = undefined;
  } else if (typeof path === 'object' && typeof options === 'function' && !done){
    done = options;
    options = path;
    path = undefined;
  } else if (typeof options === 'function' && !done) {
    done = options;
    options = undefined;
  }
  this.child.call('pdf', path, options, function (error, pdf) {
    if (error) debug(error);
    var buf = new Buffer(pdf.data);
    debug('.pdf() captured with length %s', buf.length);
    path ? fs.writeFile(path, buf, done) : done(null, buf);
  });
}
```
- example usage
```shell
...

#### .screenshot([path][, clip])
Takes a screenshot of the current page. Useful for debugging. The output is always a 'png'. Both arguments are optional. If 'path
' is provided, it saves the image to the disk. Otherwise it returns a 'Buffer' of the image data. If 'clip' is provided (as [documented
 here](https://github.com/atom/electron/blob/master/docs/api/browser-window.md#wincapturepagerect-callback)), the image will be
clipped to the rectangle.

#### .html(path, saveType)
Save the current page as html as files to disk at the given path. Save type options are [here](https://github.com/atom/electron/
blob/master/docs/api/web-contents.md#webcontentssavepagefullpath-savetype-callback).

#### .pdf(path, options)
Saves a PDF to the specified 'path'. Options are [here](https://github.com/electron/electron/blob/v1.4.4/docs/api/web-contents.md
#contentsprinttopdfoptions-callback).

#### .title()
Returns the title of the current page.

#### .url()
Returns the url of the current page.
...
```

#### <a name="apidoc.element.nightmare.actions.refresh"></a>[function <span class="apidocSignatureSpan">nightmare.actions.</span>refresh (done)](#apidoc.element.nightmare.actions.refresh)
- description and source-code
```javascript
refresh = function (done) {
  debug('.refresh()');
  this.evaluate_now(function() {
    window.location.reload();
  }, done);
}
```
- example usage
```shell
...

#### .back()
Go back to the previous page.

#### .forward()
Go forward to the next page.

#### .refresh()
Refresh the current page.

#### .click(selector)
Clicks the 'selector' element once.

#### .mousedown(selector)
Mousedown the 'selector' element once.
...
```

#### <a name="apidoc.element.nightmare.actions.screenshot"></a>[function <span class="apidocSignatureSpan">nightmare.actions.</span>screenshot (path, clip, done)](#apidoc.element.nightmare.actions.screenshot)
- description and source-code
```javascript
screenshot = function (path, clip, done) {
  debug('.screenshot()');
  if (typeof path === 'function') {
    done = path;
    clip = undefined;
    path = undefined;
  } else if (typeof clip === 'function') {
    done = clip;
    clip = (typeof path === 'string') ? undefined : path;
    path = (typeof path === 'string') ? path : undefined;
  }
  this.child.call('screenshot', path, clip, function (error, img) {
    var buf = new Buffer(img.data);
    debug('.screenshot() captured with length %s', buf.length);
    path ? fs.writeFile(path, buf, done) : done(null, buf);
  });
}
```
- example usage
```shell
...

#### .once(event, callback)
Similar to '.on()', but captures page events with the callback one time.

#### .removeListener(event, callback)
Removes a given listener callback for an event.

#### .screenshot([path][, clip])
Takes a screenshot of the current page. Useful for debugging. The output is always a 'png'. Both arguments are optional. If 'path
' is provided, it saves the image to the disk. Otherwise it returns a 'Buffer' of the image data. If 'clip' is provided (as [documented
 here](https://github.com/atom/electron/blob/master/docs/api/browser-window.md#wincapturepagerect-callback)), the image will be
clipped to the rectangle.

#### .html(path, saveType)
Save the current page as html as files to disk at the given path. Save type options are [here](https://github.com/atom/electron/
blob/master/docs/api/web-contents.md#webcontentssavepagefullpath-savetype-callback).

#### .pdf(path, options)
Saves a PDF to the specified 'path'. Options are [here](https://github.com/electron/electron/blob/v1.4.4/docs/api/web-contents.md
#contentsprinttopdfoptions-callback).
...
```

#### <a name="apidoc.element.nightmare.actions.scrollTo"></a>[function <span class="apidocSignatureSpan">nightmare.actions.</span>scrollTo (y, x, done)](#apidoc.element.nightmare.actions.scrollTo)
- description and source-code
```javascript
scrollTo = function (y, x, done) {
  debug('.scrollTo()');
  this.evaluate_now(function (y, x) {
    window.scrollTo(x, y);
  }, done, y, x);
}
```
- example usage
```shell
...

#### .uncheck(selector)
unchecks the 'selector' checkbox element.

#### .select(selector, option)
Changes the 'selector' dropdown element to the option with attribute [value='option']

#### .scrollTo(top, left)
Scrolls the page to desired position. 'top' and 'left' are always relative to the top left corner of the document.

#### .viewport(width, height)

Set the viewport size.

#### .inject(type, file)
...
```

#### <a name="apidoc.element.nightmare.actions.select"></a>[function <span class="apidocSignatureSpan">nightmare.actions.</span>select (selector, option, done)](#apidoc.element.nightmare.actions.select)
- description and source-code
```javascript
select = function (selector, option, done) {
  debug('.select() ' + selector);
  this.evaluate_now(function(selector, option) {
    var element = document.querySelector(selector);
    var event = document.createEvent('HTMLEvents');
    element.value = option;
    event.initEvent('change', true, true);
    element.dispatchEvent(event);
  }, done, selector, option);
}
```
- example usage
```shell
...

#### .check(selector)
checks the 'selector' checkbox element.

#### .uncheck(selector)
unchecks the 'selector' checkbox element.

#### .select(selector, option)
Changes the 'selector' dropdown element to the option with attribute [value='option']

#### .scrollTo(top, left)
Scrolls the page to desired position. 'top' and 'left' are always relative to the top left corner of the document.

#### .viewport(width, height)
...
```

#### <a name="apidoc.element.nightmare.actions.title"></a>[function <span class="apidocSignatureSpan">nightmare.actions.</span>title (done)](#apidoc.element.nightmare.actions.title)
- description and source-code
```javascript
title = function (done) {
  debug('.title() getting it');
  this.evaluate_now(function() {
    return document.title;
  }, done);
}
```
- example usage
```shell
...

#### .html(path, saveType)
Save the current page as html as files to disk at the given path. Save type options are [here](https://github.com/atom/electron/
blob/master/docs/api/web-contents.md#webcontentssavepagefullpath-savetype-callback).

#### .pdf(path, options)
Saves a PDF to the specified 'path'. Options are [here](https://github.com/electron/electron/blob/v1.4.4/docs/api/web-contents.md
#contentsprinttopdfoptions-callback).

#### .title()
Returns the title of the current page.

#### .url()
Returns the url of the current page.

#### .path()
Returns the path name of the current page.
...
```

#### <a name="apidoc.element.nightmare.actions.type"></a>[function <span class="apidocSignatureSpan">nightmare.actions.</span>type ()](#apidoc.element.nightmare.actions.type)
- description and source-code
```javascript
type = function () {
  var selector = arguments[0], text, done;
  if(arguments.length == 2) {
    done = arguments[1];
  } else {
    text = arguments[1];
    done = arguments[2];
  }

  debug('.type() %s into %s', text, selector);
  var self = this;

  focusSelector.bind(this)(function(err) {
    if(err) {
      debug('Unable to .type() into non-existent selector %s', selector);
      return done(err);
    }

    var blurDone = blurSelector.bind(this, done, selector);
    if ((text || '') == '') {
      this.evaluate_now(function(selector) {
        document.querySelector(selector).value = '';
      }, blurDone, selector);
    } else {
      self.child.call('type', text, blurDone);
    }
  }, selector);
}
```
- example usage
```shell
...

'''js
var Nightmare = require('nightmare');		
var nightmare = Nightmare({ show: true });

nightmare
.goto('https://duckduckgo.com')
.type('#search_form_input_homepage', 'github nightmare')
.click('#search_button_homepage')
.wait('#zero_click_wrapper .c-info__title a')
.evaluate(function () {
  return document.querySelector('#zero_click_wrapper .c-info__title a').href;
})
.end()
.then(function (result) {
...
```

#### <a name="apidoc.element.nightmare.actions.uncheck"></a>[function <span class="apidocSignatureSpan">nightmare.actions.</span>uncheck (selector, done)](#apidoc.element.nightmare.actions.uncheck)
- description and source-code
```javascript
uncheck = function (selector, done){
  debug('.uncheck() ' + selector);
  this.evaluate_now(function(selector) {
      var element = document.querySelector(selector);
      var event = document.createEvent('HTMLEvents');
      element.checked = null;
      event.initEvent('change', true, true);
      element.dispatchEvent(event);
    }, done, selector);
}
```
- example usage
```shell
...
Similar to '.type()'. '.insert()' enters the 'text' provided into the 'selector' element.  Empty or falsey values provided for '
text' will clear the selector's value.

'.insert()' is faster than '.type()' but does not trigger the keyboard events.

#### .check(selector)
checks the 'selector' checkbox element.

#### .uncheck(selector)
unchecks the 'selector' checkbox element.

#### .select(selector, option)
Changes the 'selector' dropdown element to the option with attribute [value='option']

#### .scrollTo(top, left)
Scrolls the page to desired position. 'top' and 'left' are always relative to the top left corner of the document.
...
```

#### <a name="apidoc.element.nightmare.actions.url"></a>[function <span class="apidocSignatureSpan">nightmare.actions.</span>url (done)](#apidoc.element.nightmare.actions.url)
- description and source-code
```javascript
url = function (done) {
  debug('.url() getting it');
  this.evaluate_now(function() {
    return document.location.href;
  }, done);
}
```
- example usage
```shell
...

#### .pdf(path, options)
Saves a PDF to the specified 'path'. Options are [here](https://github.com/electron/electron/blob/v1.4.4/docs/api/web-contents.md
#contentsprinttopdfoptions-callback).

#### .title()
Returns the title of the current page.

#### .url()
Returns the url of the current page.

#### .path()
Returns the path name of the current page.

### Cookies
...
```

#### <a name="apidoc.element.nightmare.actions.useragent"></a>[function <span class="apidocSignatureSpan">nightmare.actions.</span>useragent (useragent, done)](#apidoc.element.nightmare.actions.useragent)
- description and source-code
```javascript
useragent = function (useragent, done) {
  debug('.useragent() to ' + useragent);
  this.child.call('useragent', useragent, done);
}
```
- example usage
```shell
...
  maxAuthRetries: 3
});
'''

#### .engineVersions()
Gets the versions for Electron and Chromium.

#### .useragent(useragent)
Set the 'useragent' used by electron.

#### .authentication(user, password)
Set the 'user' and 'password' for accessing a web page using basic authentication. Be sure to set it before calling '.goto(url)'.

#### .end()
Complete any queue operations, disconnect and close the electron process.  Note that if you're using promises, '.then()' must be
 called after '.end()' to run the '.end()' task.  Also note that if using a '.end()' callback, the '.end()' call is equivalent to
 calling '.end()' followed by '.then(fn)'.  Consider:
...
```

#### <a name="apidoc.element.nightmare.actions.viewport"></a>[function <span class="apidocSignatureSpan">nightmare.actions.</span>viewport (width, height, done)](#apidoc.element.nightmare.actions.viewport)
- description and source-code
```javascript
viewport = function (width, height, done) {
  debug('.viewport()');
  this.child.call('size', width, height, done);
}
```
- example usage
```shell
...

#### .select(selector, option)
Changes the 'selector' dropdown element to the option with attribute [value='option']

#### .scrollTo(top, left)
Scrolls the page to desired position. 'top' and 'left' are always relative to the top left corner of the document.

#### .viewport(width, height)

Set the viewport size.

#### .inject(type, file)
Inject a local 'file' onto the current page. The file 'type' must be either 'js' or 'css'.

#### .evaluate(fn[, arg1, arg2,...])
...
```

#### <a name="apidoc.element.nightmare.actions.visible"></a>[function <span class="apidocSignatureSpan">nightmare.actions.</span>visible (selector, done)](#apidoc.element.nightmare.actions.visible)
- description and source-code
```javascript
visible = function (selector, done) {
  debug('.visible() for ' + selector);
  this.evaluate_now(function(selector) {
    var elem = document.querySelector(selector);
    if (elem) return (elem.offsetWidth > 0 && elem.offsetHeight > 0);
    else return false;
  }, done, selector);
}
```
- example usage
```shell
...
Add a header override for all HTTP requests.  If 'header' is undefined, the header overrides will be reset.

### Extract from the Page

#### .exists(selector)
Returns whether the selector exists or not on the page.

#### .visible(selector)
Returns whether the selector is visible or not

#### .on(event, callback)
Capture page events with the callback. You have to call '.on()' before calling '.goto()'. Supported events are [documented here](
http://electron.atom.io/docs/api/web-contents/#instance-events).

##### Additional "page" events
...
```

#### <a name="apidoc.element.nightmare.actions.wait"></a>[function <span class="apidocSignatureSpan">nightmare.actions.</span>wait ()](#apidoc.element.nightmare.actions.wait)
- description and source-code
```javascript
wait = function () {
  var args = sliced(arguments);
  var done = args[args.length-1];
  if (args.length < 2) {
    debug('Not enough arguments for .wait()');
    return done();
  }

  var arg = args[0];
  if (typeof arg === 'number') {
    debug('.wait() for ' + arg + 'ms');
    if(arg < this.options.waitTimeout){
      waitms(arg, done);
    } else {
      waitms(this.options.waitTimeout, function(){
        done(new Error('.wait() timed out after '+this.options.waitTimeout+'msec'));
      }.bind(this));
    }
  }
  else if (typeof arg === 'string') {
    var timeout = null;
    if (typeof args[1] === 'number') {
      timeout = args[1];
    }
    debug('.wait() for '+arg+' element'+(timeout ? ' or '+timeout+'msec' : ''));
    waitelem.apply({ timeout: timeout }, [this, arg, done]);
  }
  else if (typeof arg === 'function') {
    debug('.wait() for fn');
    args.unshift(this);
    waitfn.apply(this, args);
  }
  else {
    done();
  }
}
```
- example usage
```shell
...
var Nightmare = require('nightmare');		
var nightmare = Nightmare({ show: true });

nightmare
.goto('https://duckduckgo.com')
.type('#search_form_input_homepage', 'github nightmare')
.click('#search_button_homepage')
.wait('#zero_click_wrapper .c-info__title a')
.evaluate(function () {
  return document.querySelector('#zero_click_wrapper .c-info__title a').href;
})
.end()
.then(function (result) {
  console.log(result);
})
...
```



# <a name="apidoc.module.nightmare.frame_manager"></a>[module nightmare.frame_manager](#apidoc.module.nightmare.frame_manager)

#### <a name="apidoc.element.nightmare.frame_manager.frame_manager"></a>[function <span class="apidocSignatureSpan">nightmare.</span>frame_manager (window)](#apidoc.element.nightmare.frame_manager.frame_manager)
- description and source-code
```javascript
function FrameManager(window) {
  if (!(this instanceof FrameManager)) return new FrameManager(window);

  EventEmitter.call(this);
  var subscribed = false;
  var requestedFrame = false;
  var frameRequestTimeout;
  var self = this;

  this.on('newListener', subscribe);
  this.on('removeListener', unsubscribe);

  function subscribe(eventName) {
    if (!subscribed && eventName === 'data') {
      parent.emit('log', 'subscribing to browser window frames');
      window.webContents.beginFrameSubscription(receiveFrame);
    }
  }

  function unsubscribe() {
    if (!self.listenerCount('data')) {
      parent.emit('log', 'unsubscribing from browser window frames')
      window.webContents.endFrameSubscription();
      subscribed = false;
    }
  }

  function receiveFrame(buffer) {
    requestedFrame = false;
    clearTimeout(frameRequestTimeout);
    self.emit('data', buffer);
  }

<span class="apidocCodeCommentSpan">  /**
   * In addition to listening for events, calling 'requestFrame' will ensure
   * that a frame is queued up to render (instead of just waiting for the next
   * time the browser chooses to draw a frame).
   * @param {Function} [callback] Called when the frame is rendered.
   * @param {Number} [timeout=1000] If no frame has been rendered after this
       many milliseconds, run the callback anyway. In this case, The
       callback's first argument, an image buffer, will be 'null'.
   */
</span>  this.requestFrame = function(callback, timeout) {
    timeout = (timeout == undefined) ? 1000 : timeout;

    if (callback) {
      this.once('data', callback);
    }

    if (!requestedFrame) {
      requestedFrame = true;

      // Force the browser to render new content by using the debugger to
      // highlight a portion of the page. This way, we can guarantee a change
      // that both requires rendering a frame and does not actually affect
      // the content of the page.
      if (!window.webContents.debugger.isAttached()) {
        try {
          window.webContents.debugger.attach();
        }
        catch (error) {
          parent.emit('log', 'Failed to attach to debugger for frame subscriptions: ${error}');
          this.emit('data', null);
          return;
        }
      }

      if (timeout) {
        frameRequestTimeout = setTimeout(function() {
          parent.emit('log', 'FrameManager timing out after ${timeout} ms with no new rendered frames');
          self.emit('data', null)
        }, timeout);
      }

      parent.emit('log', 'Highlighting page to trigger rendering.');
      window.webContents.debugger.sendCommand('DOM.enable')
      window.webContents.debugger.sendCommand(
        'DOM.highlightRect', HIGHLIGHT_STYLE, function(error) {
          window.webContents.debugger.sendCommand('DOM.hideHighlight');
          window.webContents.debugger.detach();
        });
    }
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.nightmare.frame_manager.super_"></a>[function <span class="apidocSignatureSpan">nightmare.frame_manager.</span>super_ ()](#apidoc.element.nightmare.frame_manager.super_)
- description and source-code
```javascript
function EventEmitter() {
  EventEmitter.init.call(this);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.nightmare.javascript"></a>[module nightmare.javascript](#apidoc.module.nightmare.javascript)

#### <a name="apidoc.element.nightmare.javascript.execute"></a>[function <span class="apidocSignatureSpan">nightmare.javascript.</span>execute (obj )](#apidoc.element.nightmare.javascript.execute)
- description and source-code
```javascript
function anonymous(obj ) {

  function escape(html) {
    return String(html)
      .replace(/&/g, '&amp;')
      .replace(/"/g, '&quot;')
      .replace(/</g, '&lt;')
      .replace(/>/g, '&gt;');
  };

  function section(obj, prop, negate, thunk) {
    var val = obj[prop];
    if (Array.isArray(val)) return val.map(thunk).join('');
    if ('function' == typeof val) return val.call(obj, thunk(obj));
    if (negate) val = !val;
    if (val) return thunk(obj);
    return '';
  };

  return "\n(function javascript () {\n  var ipc = (window.__nightmare ? __nightmare.ipc : window[''].nightmare.ipc);\n  try {\n
    var fn = (" + obj.src + "),\n      response, \n      args = [];\n\n    " + section(obj, "args", false, function(obj){ return "args.push(" + obj.argument + ");" }) + "\n\n    if(fn.length - 1 == args.length) {\n      args.push(((err, v) => {\n          if(err) {\n            ipc.send('error', err.message || err.toString());\n          }\n          ipc.send('response', v);\n        }));\n      fn.apply(null, args);\n    } \n    else {\n      response = fn.apply(null, args);\n      if(response && response.then) {\n        response.then((v) => {\n          ipc.send('response', v);\n        })\n        .catch((err) => {\n          ipc.send('error', err)\n        });\n      } else {\n        ipc.send('response', response);\n      }\n    }\n  } catch (err) {\n    ipc.send('error', err.message);\n  }\n})()\n"
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.nightmare.javascript.inject"></a>[function <span class="apidocSignatureSpan">nightmare.javascript.</span>inject (obj )](#apidoc.element.nightmare.javascript.inject)
- description and source-code
```javascript
function anonymous(obj ) {

  function escape(html) {
    return String(html)
      .replace(/&/g, '&amp;')
      .replace(/"/g, '&quot;')
      .replace(/</g, '&lt;')
      .replace(/>/g, '&gt;');
  };

  function section(obj, prop, negate, thunk) {
    var val = obj[prop];
    if (Array.isArray(val)) return val.map(thunk).join('');
    if ('function' == typeof val) return val.call(obj, thunk(obj));
    if (negate) val = !val;
    if (val) return thunk(obj);
    return '';
  };

  return "\n(function javascript () {\n  var ipc = (window.__nightmare ? __nightmare.ipc : window[''].nightmare.ipc);\n  try {\n
    var response = (function () { " + obj.src + "\n})()\n    ipc.send('response', response);\n  } catch (e) {\n    ipc.send('error', e.message);\n  }\n})()\n"
}
```
- example usage
```shell
...
#### .scrollTo(top, left)
Scrolls the page to desired position. 'top' and 'left' are always relative to the top left corner of the document.

#### .viewport(width, height)

Set the viewport size.

#### .inject(type, file)
Inject a local 'file' onto the current page. The file 'type' must be either 'js' or 'css'.

#### .evaluate(fn[, arg1, arg2,...])
Invokes 'fn' on the page with 'arg1, arg2,...'. All the 'args' are optional. On completion it returns the return value of 'fn'.
Useful for extracting information from the page. Here's an example:

'''js
var selector = 'h1';
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
