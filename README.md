# test coverage for  [pixi.js (v4.5.0)](http://goodboydigital.com/)  [![npm package](https://img.shields.io/npm/v/npmtest-pixi.js.svg?style=flat-square)](https://www.npmjs.org/package/npmtest-pixi.js) [![travis-ci.org build-status](https://api.travis-ci.org/npmtest/node-npmtest-pixi.js.svg)](https://travis-ci.org/npmtest/node-npmtest-pixi.js)
#### Pixi.js is a fast lightweight 2D library that works across all devices.

[![NPM](https://nodei.co/npm/pixi.js.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/pixi.js)

| git-branch : | [alpha](https://github.com/npmtest/node-npmtest-pixi.js/tree/alpha)|
|--:|:--|
| coverage : | [![istanbul-coverage](https://npmtest.github.io/node-npmtest-pixi.js/build/coverage.badge.svg)](https://npmtest.github.io/node-npmtest-pixi.js/build/coverage.html/index.html)|
| test-report : | [![test-report](https://npmtest.github.io/node-npmtest-pixi.js/build/test-report.badge.svg)](https://npmtest.github.io/node-npmtest-pixi.js/build/test-report.html)|
| build-artifacts : | [![build-artifacts](https://npmtest.github.io/node-npmtest-pixi.js/glyphicons_144_folder_open.png)](https://github.com/npmtest/node-npmtest-pixi.js/tree/gh-pages/build)|

- [https://npmtest.github.io/node-npmtest-pixi.js/build/coverage.html/index.html](https://npmtest.github.io/node-npmtest-pixi.js/build/coverage.html/index.html)

[![istanbul-coverage](https://npmtest.github.io/node-npmtest-pixi.js/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fcoverage.lib.html.png)](https://npmtest.github.io/node-npmtest-pixi.js/build/coverage.html/index.html)

- [https://npmtest.github.io/node-npmtest-pixi.js/build/test-report.html](https://npmtest.github.io/node-npmtest-pixi.js/build/test-report.html)

[![test-report](https://npmtest.github.io/node-npmtest-pixi.js/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Ftest-report.html.png)](https://npmtest.github.io/node-npmtest-pixi.js/build/test-report.html)

- [https://npmdoc.github.io/node-npmdoc-pixi.js/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-pixi.js/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-pixi.js/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-pixi.js/build/apidoc.html)

![npmPackageListing](https://npmtest.github.io/node-npmtest-pixi.js/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmtest.github.io/node-npmtest-pixi.js/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Mat Groves"
    },
    "bugs": {
        "url": "https://github.com/pixijs/pixi.js/issues"
    },
    "contributors": [
        {
            "name": "Ivan Popelyshev"
        },
        {
            "name": "Matt Karl"
        },
        {
            "name": "Chad Engler"
        },
        {
            "name": "Richard Davey"
        }
    ],
    "dependencies": {
        "bit-twiddle": "^1.0.2",
        "earcut": "^2.0.7",
        "eventemitter3": "^2.0.0",
        "ismobilejs": "^0.4.0",
        "object-assign": "^4.0.1",
        "pixi-gl-core": "^1.0.3",
        "resource-loader": "^2.0.6"
    },
    "description": "Pixi.js is a fast lightweight 2D library that works across all devices.",
    "devDependencies": {
        "babel-cli": "^6.18.0",
        "babel-plugin-static-fs": "^1.1.0",
        "babel-plugin-version-inline": "^1.0.0",
        "babel-preset-es2015": "^6.14.0",
        "babelify": "^7.3.0",
        "del": "^2.2.0",
        "electron": "^1.4.15",
        "eslint": "^3.5.0",
        "floss": "^2.0.1",
        "jaguarjs-jsdoc": "^1.0.1",
        "js-md5": "^0.4.1",
        "jsdoc": "^3.4.2",
        "minimist": "^1.2.0",
        "mkdirp": "^0.5.1",
        "parallelshell": "^2.0.0",
        "pixify": "^1.7.0",
        "rimraf": "^2.5.3",
        "watch": "^0.19.1"
    },
    "directories": {},
    "dist": {
        "shasum": "4fffd66e4dd30b350ccae9965d2831bc885dee5b",
        "tarball": "https://registry.npmjs.org/pixi.js/-/pixi.js-4.5.0.tgz"
    },
    "files": [
        "dist/",
        "lib/",
        "CONTRIBUTING.md",
        "LICENSE",
        "package.json",
        "README.md"
    ],
    "gitHead": "2fb5c997d0d9da01f5f59780b5f74194d603c5a6",
    "homepage": "http://goodboydigital.com/",
    "license": "MIT",
    "main": "./lib/index.js",
    "maintainers": [
        {
            "name": "doormat23"
        },
        {
            "name": "englercj"
        }
    ],
    "name": "pixi.js",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git+https://github.com/pixijs/pixi.js.git"
    },
    "scripts": {
        "build": "npm run dist",
        "clean": "rimraf dist lib && mkdirp dist && mkdir lib",
        "coverage": "npm test -- -c dist/pixi.js -s -h",
        "dist": "pixify -d dist -n PIXI -o pixi -t babelify",
        "docs": "jsdoc -c scripts/jsdoc.conf.json -R README.md",
        "lib": "babel src --out-dir lib -s",
        "lint": "eslint scripts src test --max-warnings 0",
        "lintfix": "npm run lint --fix",
        "postpublish": "git push && git push --tags",
        "postversion": "npm run clean && npm run build && npm run lib && npm test",
        "prebuild": "npm run lint",
        "precoverage": "rimraf coverage",
        "predist": "rimraf dist/**",
        "predocs": "rimraf docs/**",
        "prelib": "rimraf lib/**",
        "prerenders": "npm --prefix scripts/renders i scripts/renders",
        "prestart": "npm run clean",
        "publish:major": "npm version major && npm publish",
        "publish:minor": "npm version minor && npm publish",
        "publish:patch": "npm version patch && npm publish",
        "renders": "electron scripts/renders",
        "start": "parallelshell \"npm run watch\" \"npm run watch:lint\" \"npm run watch:lib\"",
        "test": "floss --path test/index.js",
        "test:debug": "npm test -- --debug",
        "watch": "npm run dist -- --watch",
        "watch:lib": "npm run lib -- --watch",
        "watch:lint": "watch \"eslint scripts src test || exit 0\" src"
    },
    "version": "4.5.0"
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
