# api documentation for  [webshot (v0.18.0)](https://github.com/brenden/node-webshot)  [![npm package](https://img.shields.io/npm/v/npmdoc-webshot.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-webshot) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-webshot.svg)](https://travis-ci.org/npmdoc/node-npmdoc-webshot)
#### Easy website screenshots

[![NPM](https://nodei.co/npm/webshot.png?downloads=true)](https://www.npmjs.com/package/webshot)

[![apidoc](https://npmdoc.github.io/node-npmdoc-webshot/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-webshot_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-webshot/build..beta..travis-ci.org/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-webshot/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-webshot/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Brenden Kokoszka"
    },
    "bugs": {
        "url": "https://github.com/brenden/node-webshot/issues"
    },
    "contributors": [
        {
            "name": "Brenden Kokoszka",
            "email": "brenden.kokoszka@gmail.com"
        },
        {
            "name": "Matthew Chase Whittemore",
            "email": "mcwhittemore@gmail.com"
        }
    ],
    "dependencies": {
        "cross-spawn": "^0.2.3",
        "graceful-fs": "~3.0.4",
        "phantomjs-prebuilt": "^2.1.3",
        "tmp": "~0.0.25"
    },
    "description": "Easy website screenshots",
    "devDependencies": {
        "imagemagick": "git://github.com/rsms/node-imagemagick.git",
        "mocha": "*",
        "should": "*"
    },
    "directories": {},
    "dist": {
        "shasum": "057e6925bc3970ae97eed56fc23118578cbcfdc3",
        "tarball": "https://registry.npmjs.org/webshot/-/webshot-0.18.0.tgz"
    },
    "engine": [
        "node >=0.7.00"
    ],
    "homepage": "https://github.com/brenden/node-webshot",
    "keywords": [
        "screenshot",
        "screengrab"
    ],
    "license": "MIT",
    "main": "./lib/webshot.js",
    "maintainers": [
        {
            "name": "bkokoszka",
            "email": "bkokoszk@nd.edu"
        }
    ],
    "name": "webshot",
    "optionalDependencies": {
        "phantomjs-prebuilt": "^2.1.3"
    },
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+ssh://git@github.com/brenden/node-webshot.git"
    },
    "scripts": {
        "test": "mocha --ui bdd --reporter spec --require should ./test/core.js ./test/options/*"
    },
    "version": "0.18.0"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module webshot](#apidoc.module.webshot)
1.  object <span class="apidocSignatureSpan">webshot.</span>options

#### [module webshot.options](#apidoc.module.webshot.options)
1.  [function <span class="apidocSignatureSpan">webshot.options.</span>filterObject (obj, keys)](#apidoc.element.webshot.options.filterObject)
1.  [function <span class="apidocSignatureSpan">webshot.options.</span>mergeObjects (a, b)](#apidoc.element.webshot.options.mergeObjects)
1.  object <span class="apidocSignatureSpan">webshot.options.</span>caller
1.  object <span class="apidocSignatureSpan">webshot.options.</span>phantom
1.  object <span class="apidocSignatureSpan">webshot.options.</span>phantomCallback
1.  object <span class="apidocSignatureSpan">webshot.options.</span>phantomPage



# <a name="apidoc.module.webshot"></a>[module webshot](#apidoc.module.webshot)



# <a name="apidoc.module.webshot.options"></a>[module webshot.options](#apidoc.module.webshot.options)

#### <a name="apidoc.element.webshot.options.filterObject"></a>[function <span class="apidocSignatureSpan">webshot.options.</span>filterObject (obj, keys)](#apidoc.element.webshot.options.filterObject)
- description and source-code
```javascript
function filterObject(obj, keys) {
  var filtered = {};

  keys.forEach(function(key) {
    if (obj[key]) filtered[key] = obj[key];
  });

  return filtered;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webshot.options.mergeObjects"></a>[function <span class="apidocSignatureSpan">webshot.options.</span>mergeObjects (a, b)](#apidoc.element.webshot.options.mergeObjects)
- description and source-code
```javascript
function mergeObjects(a, b) {
  var merged = {};

  Object.keys(a).forEach(function(key) {
    merged[key] = toString.call(a[key]) === '[object Object]'
      ? mergeObjects(a[key], b[key] || {})
      : a[key] || b[key];
  });

  Object.keys(b).forEach(function(key) {
    if (merged.hasOwnProperty(key)) return;
    merged[key] = b[key];
  });

  return merged;
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
