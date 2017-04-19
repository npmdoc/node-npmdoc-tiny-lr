# npmdoc-tiny-lr

#### api documentation for  [tiny-lr (v1.0.3)](https://github.com/mklabs/tiny-lr)  [![npm package](https://img.shields.io/npm/v/npmdoc-tiny-lr.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-tiny-lr) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-tiny-lr.svg)](https://travis-ci.org/npmdoc/node-npmdoc-tiny-lr)

#### Tiny LiveReload server, background-friendly

[![NPM](https://nodei.co/npm/tiny-lr.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/tiny-lr)

- [https://npmdoc.github.io/node-npmdoc-tiny-lr/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-tiny-lr/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-tiny-lr/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-tiny-lr/build/apidoc.html)

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
            "name": "elwayman02"
        },
        {
            "name": "mklabs"
        },
        {
            "name": "shama"
        }
    ],
    "name": "tiny-lr",
    "optionalDependencies": {},
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



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
