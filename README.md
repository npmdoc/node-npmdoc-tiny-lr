# api documentation for  [tiny-lr (v1.0.3)](https://github.com/mklabs/tiny-lr)  [![npm package](https://img.shields.io/npm/v/npmdoc-tiny-lr.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-tiny-lr) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-tiny-lr.svg)](https://travis-ci.org/npmdoc/node-npmdoc-tiny-lr)
#### Tiny LiveReload server, background-friendly

[![NPM](https://nodei.co/npm/tiny-lr.png?downloads=true)](https://www.npmjs.com/package/tiny-lr)

[![apidoc](https://npmdoc.github.io/node-npmdoc-tiny-lr/build/screenCapture.buildNpmdoc.browser.%252Fhome%252Ftravis%252Fbuild%252Fnpmdoc%252Fnode-npmdoc-tiny-lr%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-tiny-lr/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-tiny-lr/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-tiny-lr/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "mklabs"
    },
    "bugs": {
        "url": "https://github.com/mklabs/tiny-lr/issues"
    },
    "config": {
        "test_port": "9001"
    },
    "contributors": [
        {
            "name": "Kyle Robinson Young",
            "url": "https://github.com/shama"
        },
        {
            "name": "Jordan Hawker",
            "url": "https://github.com/elwayman02"
        },
        {
            "name": "Hemanth.hm",
            "url": "https://github.com/hemanth"
        },
        {
            "name": "Mickael Daniel",
            "url": "https://github.com/mklabs"
        }
    ],
    "dependencies": {
        "body": "^5.1.0",
        "debug": "~2.2.0",
        "faye-websocket": "~0.10.0",
        "livereload-js": "^2.2.2",
        "object-assign": "^4.1.0",
        "qs": "^6.2.0"
    },
    "description": "Tiny LiveReload server, background-friendly",
    "devDependencies": {
        "babel-cli": "^6.9.0",
        "babel-plugin-add-module-exports": "^0.2.1",
        "babel-plugin-transform-regenerator": "^6.9.0",
        "babel-preset-es2015": "^6.9.0",
        "eslint": "^2.11.1",
        "eslint-config-standard": "^5.3.1",
        "eslint-plugin-promise": "^1.1.0",
        "eslint-plugin-standard": "^1.3.2",
        "express": "^4.1.1",
        "gaze": "^1.1.2",
        "mocha": "^2.3.3",
        "npm-watch": "^0.1.6",
        "standard-version": "^2.2.1",
        "supertest": "^1.2.0"
    },
    "directories": {},
    "dist": {
        "shasum": "386731170ce521263a9d337f769ee8f11e88eb04",
        "tarball": "https://registry.npmjs.org/tiny-lr/-/tiny-lr-1.0.3.tgz"
    },
    "gitHead": "bb3f575c221113108d29879ffa6b85ea48dd9119",
    "homepage": "https://github.com/mklabs/tiny-lr",
    "license": "MIT",
    "main": "./src",
    "maintainers": [
        {
            "name": "elwayman02",
            "email": "hawker.jordan@gmail.com"
        },
        {
            "name": "mklabs",
            "email": "daniel.mickael@gmail.com"
        },
        {
            "name": "shama",
            "email": "kyle@dontkry.com"
        }
    ],
    "name": "tiny-lr",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git://github.com/mklabs/tiny-lr.git"
    },
    "scripts": {
        "babel": "babel lib/ -d src && babel test/ -d src_test/",
        "eslint": "eslint . --debug",
        "get-change": "curl http://localhost:35729/changed?files=site.css",
        "mocha": "npm run babel && mocha --reporter spec src_test/",
        "post-change": "sh scripts/post-change",
        "prepublish:": "npm run babel",
        "test": "npm run eslint && npm run mocha",
        "test-debug": "DEBUG=tinylr:* mocha --reporter list",
        "test-debug-all": "DEBUG=* mocha --reporter list",
        "watch": "npm-watch"
    },
    "version": "1.0.3",
    "watch": {
        "babel": "{lib,test}/**/*.js"
    }
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module tiny-lr](#apidoc.module.tiny-lr)
1.  [function <span class="apidocSignatureSpan">tiny-lr.</span>Client (req, socket, head)](#apidoc.element.tiny-lr.Client)
1.  [function <span class="apidocSignatureSpan">tiny-lr.</span>Server ()](#apidoc.element.tiny-lr.Server)
1.  [function <span class="apidocSignatureSpan">tiny-lr.</span>changed (done)](#apidoc.element.tiny-lr.changed)
1.  [function <span class="apidocSignatureSpan">tiny-lr.</span>middleware (opts)](#apidoc.element.tiny-lr.middleware)



# <a name="apidoc.module.tiny-lr"></a>[module tiny-lr](#apidoc.module.tiny-lr)

#### <a name="apidoc.element.tiny-lr.Client"></a>[function <span class="apidocSignatureSpan">tiny-lr.</span>Client (req, socket, head)](#apidoc.element.tiny-lr.Client)
- description and source-code
```javascript
function Client(req, socket, head) {
  var options = arguments.length > 3 && arguments[3] !== undefined ? arguments[3] : {};

  _classCallCheck(this, Client);

  var _this = _possibleConstructorReturn(this, (Client.__proto__ || Object.getPrototypeOf(Client)).call(this));

  _this.options = options;
  _this.ws = new _fayeWebsocket2.default(req, socket, head);
  _this.ws.onmessage = _this.message.bind(_this);
  _this.ws.onclose = _this.close.bind(_this);
  _this.id = _this.uniqueId('ws');
  return _this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.tiny-lr.Server"></a>[function <span class="apidocSignatureSpan">tiny-lr.</span>Server ()](#apidoc.element.tiny-lr.Server)
- description and source-code
```javascript
function Server() {
  var options = arguments.length > 0 && arguments[0] !== undefined ? arguments[0] : {};

  _classCallCheck(this, Server);

  var _this = _possibleConstructorReturn(this, (Server.__proto__ || Object.getPrototypeOf(Server)).call(this));

  _this.options = options;

  options.livereload = options.livereload || require.resolve('livereload-js/dist/livereload.js');

  // todo: change falsy check to allow 0 for random port
  options.port = parseInt(options.port || 35729, 10);

  if (options.errorListener) {
    _this.errorListener = options.errorListener;
  }

  _this.clients = {};
  _this.configure(options.app);
  _this.routes(options.app);
  return _this;
}
```
- example usage
```shell
...

'''js
var tinylr = require('tiny-lr');

// standard LiveReload port
var port = 35729;

// tinylr(opts) => new tinylr.Server(opts);
tinylr().listen(port, function() {
  console.log('... Listening on %s ...', port);
})
'''

You can define your own route and listen for a specific request:
...
```

#### <a name="apidoc.element.tiny-lr.changed"></a>[function <span class="apidocSignatureSpan">tiny-lr.</span>changed (done)](#apidoc.element.tiny-lr.changed)
- description and source-code
```javascript
function changed(done) {
  var files = [].slice.call(arguments);
  if (files[files.length - 1] === 'function') done = files.pop();
  done = typeof done === 'function' ? done : function () {};
  debug('Notifying %d servers - Files: ', servers.length, files);
  servers.forEach(function (srv) {
    var params = { params: { files: files } };
    srv && srv.changed(params);
  });
  done();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.tiny-lr.middleware"></a>[function <span class="apidocSignatureSpan">tiny-lr.</span>middleware (opts)](#apidoc.element.tiny-lr.middleware)
- description and source-code
```javascript
function middleware(opts) {
  var srv = new _server2.default(opts);
  servers.push(srv);
  return function tinylr(req, res, next) {
    srv.handler(req, res, next);
  };
}
```
- example usage
```shell
...

var app = express();

// This binds both express app and tinylr on the same port

app
  .use(body())
  .use(tinylr.middleware({ app: app }))
  .use(express.static(path.resolve('./')))
  .listen(port, function() {
    console.log('listening on %d', port);
  });
'''

The port you listen on is important, and tinylr should **always** listen on
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
