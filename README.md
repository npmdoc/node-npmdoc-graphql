# npmdoc-graphql

#### api documentation for  [graphql (v0.9.3)](https://github.com/graphql/graphql-js)  [![npm package](https://img.shields.io/npm/v/npmdoc-graphql.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-graphql) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-graphql.svg)](https://travis-ci.org/npmdoc/node-npmdoc-graphql)

#### A Query Language and Runtime which can target any service.

[![NPM](https://nodei.co/npm/graphql.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/graphql)

- [https://npmdoc.github.io/node-npmdoc-graphql/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-graphql/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-graphql/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-graphql/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-graphql/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-graphql/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "bugs": {
        "url": "https://github.com/graphql/graphql-js/issues"
    },
    "contributors": [
        {
            "name": "Lee Byron",
            "url": "http://leebyron.com/"
        },
        {
            "name": "Nicholas Schrock"
        },
        {
            "name": "Daniel Schafer"
        }
    ],
    "dependencies": {
        "iterall": "1.0.3"
    },
    "description": "A Query Language and Runtime which can target any service.",
    "devDependencies": {
        "babel-cli": "6.24.1",
        "babel-eslint": "7.2.2",
        "babel-plugin-check-es2015-constants": "6.22.0",
        "babel-plugin-syntax-async-functions": "6.13.0",
        "babel-plugin-transform-class-properties": "6.24.1",
        "babel-plugin-transform-es2015-arrow-functions": "6.22.0",
        "babel-plugin-transform-es2015-block-scoped-functions": "6.22.0",
        "babel-plugin-transform-es2015-block-scoping": "6.24.1",
        "babel-plugin-transform-es2015-classes": "6.24.1",
        "babel-plugin-transform-es2015-computed-properties": "6.24.1",
        "babel-plugin-transform-es2015-destructuring": "6.23.0",
        "babel-plugin-transform-es2015-duplicate-keys": "6.24.1",
        "babel-plugin-transform-es2015-function-name": "6.24.1",
        "babel-plugin-transform-es2015-literals": "6.22.0",
        "babel-plugin-transform-es2015-modules-commonjs": "6.24.1",
        "babel-plugin-transform-es2015-object-super": "6.24.1",
        "babel-plugin-transform-es2015-parameters": "6.24.1",
        "babel-plugin-transform-es2015-shorthand-properties": "6.24.1",
        "babel-plugin-transform-es2015-spread": "6.22.0",
        "babel-plugin-transform-es2015-template-literals": "6.22.0",
        "babel-plugin-transform-es3-property-literals": "^6.22.0",
        "babel-plugin-transform-flow-strip-types": "6.22.0",
        "babel-plugin-transform-object-rest-spread": "6.23.0",
        "babel-plugin-transform-regenerator": "6.24.1",
        "chai": "3.5.0",
        "chai-json-equal": "0.0.1",
        "chai-subset": "1.5.0",
        "coveralls": "2.13.0",
        "eslint": "3.19.0",
        "eslint-plugin-babel": "4.1.1",
        "eslint-plugin-flowtype": "2.30.4",
        "flow-bin": "0.43.1",
        "isparta": "4.0.0",
        "mocha": "3.2.0",
        "sane": "1.6.0"
    },
    "directories": {},
    "dist": {
        "shasum": "71fc0fa331bffb9c20678485861cfb370803118e",
        "tarball": "https://registry.npmjs.org/graphql/-/graphql-0.9.3.tgz"
    },
    "gitHead": "1407c057b1d6f0d6492eed23a4a41402346f440b",
    "homepage": "https://github.com/graphql/graphql-js",
    "license": "BSD-3-Clause",
    "main": "index.js",
    "maintainers": [
        {
            "name": "dschafer"
        },
        {
            "name": "fb"
        },
        {
            "name": "leebyron"
        },
        {
            "name": "wincent"
        }
    ],
    "name": "graphql",
    "optionalDependencies": {},
    "options": {
        "mocha": "--require ./resources/mocha-bootload --check-leaks --full-trace src/**/__tests__/**/*-test.js"
    },
    "repository": {
        "type": "git",
        "url": "git+ssh://git@github.com/graphql/graphql-js.git"
    },
    "scripts": {
        "build": "babel src --optional runtime --ignore __tests__ --out-dir dist/ && cp package.json dist/ && npm run build-dot-flow",
        "build-dot-flow": "find ./src -name '*.js' -not -path '*/__tests__*' | while read filepath; do cp $filepath 'echo $filepath | sed 's/\\/src\\//\\/dist\\//g''.flow; done",
        "check": "flow check",
        "check-cover": "for file in {src/*.js,src/**/*.js}; do echo $file; flow coverage $file; done",
        "cover": "babel-node ./node_modules/.bin/isparta cover --root src --report html _mocha -- $npm_package_options_mocha",
        "cover:lcov": "babel-node ./node_modules/.bin/isparta cover --root src --report lcovonly _mocha -- $npm_package_options_mocha",
        "lint": "eslint src || (printf '\\033[33mTry: \\033[7m npm run lint -- --fix \\033[0m\\n' && exit 1)",
        "prepublish": ". ./resources/prepublish.sh",
        "preversion": ". ./resources/checkgit.sh && npm test",
        "t": "babel-node ./node_modules/.bin/_mocha --require ./resources/mocha-bootload",
        "test": "npm run lint && npm run check && npm run testonly",
        "testonly": "babel-node ./node_modules/.bin/_mocha $npm_package_options_mocha",
        "watch": "babel-node ./resources/watch.js"
    },
    "version": "0.9.3",
    "bin": {}
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
