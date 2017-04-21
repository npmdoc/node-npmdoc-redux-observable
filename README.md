# npmdoc-redux-observable

#### api documentation for  [redux-observable (v0.14.1)](https://github.com/redux-observable/redux-observable#README.md)  [![npm package](https://img.shields.io/npm/v/npmdoc-redux-observable.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-redux-observable) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-redux-observable.svg)](https://travis-ci.org/npmdoc/node-npmdoc-redux-observable)

#### RxJS based middleware for Redux. Compose and cancel async actions and more.

[![NPM](https://nodei.co/npm/redux-observable.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/redux-observable)

- [https://npmdoc.github.io/node-npmdoc-redux-observable/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-redux-observable/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-redux-observable/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-redux-observable/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-redux-observable/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-redux-observable/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "name": "redux-observable",
    "version": "0.14.1",
    "description": "RxJS based middleware for Redux. Compose and cancel async actions and more.",
    "module": "lib/es/index.js",
    "main": "lib/cjs/index.js",
    "scripts": {
        "lint": "eslint src && eslint test",
        "build": "npm run build:es && npm run build:cjs && npm run build:umd && npm run build:umd:min",
        "build:es": "gulp build:es",
        "build:cjs": "babel src -d lib/cjs",
        "build:umd": "cross-env NODE_ENV=development webpack src/index.js dist/redux-observable.js",
        "build:umd:min": "cross-env NODE_ENV=production webpack src/index.js dist/redux-observable.min.js",
        "build:tests": "rm -rf temp && babel test -d temp",
        "clean": "rimraf lib temp dist",
        "check": "npm run lint && npm run test",
        "test": "npm run lint && npm run build && npm run build:tests && mocha temp && npm run test:typings",
        "test:typings": "tsc --noImplicitAny index.d.ts test/typings.ts --outDir temp --target ES5 --moduleResolution node && cd temp && node typings.js",
        "shipit": "npm run clean && npm run build && npm run lint && npm test && scripts/preprepublish.sh && npm publish",
        "docs:clean": "rimraf _book",
        "docs:prepare": "gitbook install",
        "docs:build": "npm run docs:prepare && gitbook build -g redux-observable/redux-observable && cp logo/favicon.ico _book/gitbook/images",
        "docs:watch": "gitbook serve",
        "docs:publish": "npm run docs:clean && npm run docs:build && cp CNAME _book && cd _book && git init && git commit --allow-empty -m 'update book' && git checkout -b gh-pages && touch .nojekyll && git add . && git commit -am 'update book' && git push git@github.com:redux-observable/redux-observable gh-pages --force"
    },
    "typings": "./index.d.ts",
    "files": [
        "dist",
        "lib",
        "index.d.ts",
        "README.md",
        "LICENSE"
    ],
    "repository": {
        "type": "git",
        "url": "git+https://github.com/redux-observable/redux-observable.git"
    },
    "keywords": [
        "Rx",
        "Ducks",
        "Reducks",
        "Redux",
        "middleware",
        "observable",
        "thunk",
        "async",
        "cancel",
        "action"
    ],
    "contributors": [
        {
            "name": "Ben Lesh"
        },
        {
            "name": "Jay Phelps"
        }
    ],
    "license": "MIT",
    "bugs": {
        "url": "https://github.com/redux-observable/redux-observable/issues"
    },
    "homepage": "https://github.com/redux-observable/redux-observable#README.md",
    "peerDependencies": {
        "redux": "3.*",
        "rxjs": "^5.0.0"
    },
    "devDependencies": {
        "@types/chai": "^3.4.34",
        "@types/es6-shim": "^0.31.32",
        "@types/mocha": "^2.2.33",
        "@types/sinon": "^1.16.32",
        "babel-cli": "^6.11.4",
        "babel-eslint": "^7.0.0",
        "babel-loader": "^6.2.4",
        "babel-plugin-transform-es2015-modules-commonjs": "^6.11.5",
        "babel-plugin-transform-function-bind": "^6.8.0",
        "babel-plugin-transform-object-rest-spread": "^6.8.0",
        "babel-polyfill": "^6.13.0",
        "babel-preset-es2015": "^6.13.2",
        "babel-register": "^6.11.6",
        "chai": "^3.5.0",
        "conventional-changelog-cli": "1.2.0",
        "cross-env": "^3.1.0",
        "eslint": "^3.2.2",
        "gitbook-cli": "^2.3.0",
        "gitbook-plugin-addcssjs": "^1.0.2",
        "gitbook-plugin-anker-enable": "^0.0.4",
        "gitbook-plugin-edit-link": "^2.0.2",
        "gitbook-plugin-github": "^3.0.0",
        "gitbook-plugin-prism": "^2.0.1",
        "gitbook-plugin-theme-default": "^1.0.5",
        "gulp": "^3.9.1",
        "gulp-babel": "^6.1.2",
        "json-server": "^0.9.0",
        "mocha": "^3.0.1",
        "redux": "^3.5.2",
        "rimraf": "^2.5.4",
        "rxjs": "^5.0.0",
        "sinon": "1.17.7",
        "typescript": "^2.1.4",
        "webpack": "^2.2.1",
        "webpack-rxjs-externals": "~1.0.0"
    }
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
