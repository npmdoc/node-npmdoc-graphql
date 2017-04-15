# api documentation for  [graphql (v0.9.3)](https://github.com/graphql/graphql-js)  [![npm package](https://img.shields.io/npm/v/npmdoc-graphql.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-graphql) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-graphql.svg)](https://travis-ci.org/npmdoc/node-npmdoc-graphql)
#### A Query Language and Runtime which can target any service.

[![NPM](https://nodei.co/npm/graphql.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/graphql)

[![apidoc](https://npmdoc.github.io/node-npmdoc-graphql/build/screenCapture.buildCi.browser.apidoc.html.png)](https://npmdoc.github.io/node-npmdoc-graphql/build/apidoc.html)

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
    "version": "0.9.3"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module graphql](#apidoc.module.graphql)
1.  [function <span class="apidocSignatureSpan"></span>graphql (schema, requestString, rootValue, contextValue, variableValues, operationName)](#apidoc.element.graphql.graphql)
1.  [function <span class="apidocSignatureSpan">graphql.</span>GraphQLDirective (config)](#apidoc.element.graphql.GraphQLDirective)
1.  [function <span class="apidocSignatureSpan">graphql.</span>GraphQLEnumType (config)](#apidoc.element.graphql.GraphQLEnumType)
1.  [function <span class="apidocSignatureSpan">graphql.</span>GraphQLError ( // eslint-disable-line no-redeclare message, nodes, source, positions, path, originalError)](#apidoc.element.graphql.GraphQLError)
1.  [function <span class="apidocSignatureSpan">graphql.</span>GraphQLInputObjectType (config)](#apidoc.element.graphql.GraphQLInputObjectType)
1.  [function <span class="apidocSignatureSpan">graphql.</span>GraphQLInterfaceType (config)](#apidoc.element.graphql.GraphQLInterfaceType)
1.  [function <span class="apidocSignatureSpan">graphql.</span>GraphQLList (type)](#apidoc.element.graphql.GraphQLList)
1.  [function <span class="apidocSignatureSpan">graphql.</span>GraphQLNonNull (type)](#apidoc.element.graphql.GraphQLNonNull)
1.  [function <span class="apidocSignatureSpan">graphql.</span>GraphQLObjectType (config)](#apidoc.element.graphql.GraphQLObjectType)
1.  [function <span class="apidocSignatureSpan">graphql.</span>GraphQLScalarType (config)](#apidoc.element.graphql.GraphQLScalarType)
1.  [function <span class="apidocSignatureSpan">graphql.</span>GraphQLSchema (config)](#apidoc.element.graphql.GraphQLSchema)
1.  [function <span class="apidocSignatureSpan">graphql.</span>GraphQLUnionType (config)](#apidoc.element.graphql.GraphQLUnionType)
1.  [function <span class="apidocSignatureSpan">graphql.</span>Source (body, name)](#apidoc.element.graphql.Source)
1.  [function <span class="apidocSignatureSpan">graphql.</span>TypeInfo (schema, // NOTE: this experimental optional second parameter is only needed in order // to support non-spec-compliant codebases. You should never need to use it. getFieldDefFn)](#apidoc.element.graphql.TypeInfo)
1.  [function <span class="apidocSignatureSpan">graphql.</span>ValidationContext (schema, ast, typeInfo)](#apidoc.element.graphql.ValidationContext)
1.  [function <span class="apidocSignatureSpan">graphql.</span>assertAbstractType (type)](#apidoc.element.graphql.assertAbstractType)
1.  [function <span class="apidocSignatureSpan">graphql.</span>assertCompositeType (type)](#apidoc.element.graphql.assertCompositeType)
1.  [function <span class="apidocSignatureSpan">graphql.</span>assertInputType (type)](#apidoc.element.graphql.assertInputType)
1.  [function <span class="apidocSignatureSpan">graphql.</span>assertLeafType (type)](#apidoc.element.graphql.assertLeafType)
1.  [function <span class="apidocSignatureSpan">graphql.</span>assertNamedType (type)](#apidoc.element.graphql.assertNamedType)
1.  [function <span class="apidocSignatureSpan">graphql.</span>assertOutputType (type)](#apidoc.element.graphql.assertOutputType)
1.  [function <span class="apidocSignatureSpan">graphql.</span>assertType (type)](#apidoc.element.graphql.assertType)
1.  [function <span class="apidocSignatureSpan">graphql.</span>assertValidName (name, isIntrospection)](#apidoc.element.graphql.assertValidName)
1.  [function <span class="apidocSignatureSpan">graphql.</span>astFromValue (value, type)](#apidoc.element.graphql.astFromValue)
1.  [function <span class="apidocSignatureSpan">graphql.</span>buildASTSchema (ast)](#apidoc.element.graphql.buildASTSchema)
1.  [function <span class="apidocSignatureSpan">graphql.</span>buildClientSchema (introspection)](#apidoc.element.graphql.buildClientSchema)
1.  [function <span class="apidocSignatureSpan">graphql.</span>buildSchema (source)](#apidoc.element.graphql.buildSchema)
1.  [function <span class="apidocSignatureSpan">graphql.</span>concatAST (asts)](#apidoc.element.graphql.concatAST)
1.  [function <span class="apidocSignatureSpan">graphql.</span>defaultFieldResolver (source, args, context, info)](#apidoc.element.graphql.defaultFieldResolver)
1.  [function <span class="apidocSignatureSpan">graphql.</span>doTypesOverlap (schema, typeA, typeB)](#apidoc.element.graphql.doTypesOverlap)
1.  [function <span class="apidocSignatureSpan">graphql.</span>execute (schema, document, rootValue, contextValue, variableValues, operationName)](#apidoc.element.graphql.execute)
1.  [function <span class="apidocSignatureSpan">graphql.</span>extendSchema (schema, documentAST)](#apidoc.element.graphql.extendSchema)
1.  [function <span class="apidocSignatureSpan">graphql.</span>findBreakingChanges (oldSchema, newSchema)](#apidoc.element.graphql.findBreakingChanges)
1.  [function <span class="apidocSignatureSpan">graphql.</span>findDeprecatedUsages (schema, ast)](#apidoc.element.graphql.findDeprecatedUsages)
1.  [function <span class="apidocSignatureSpan">graphql.</span>formatError (error)](#apidoc.element.graphql.formatError)
1.  [function <span class="apidocSignatureSpan">graphql.</span>getLocation (source, position)](#apidoc.element.graphql.getLocation)
1.  [function <span class="apidocSignatureSpan">graphql.</span>getNamedType (type)](#apidoc.element.graphql.getNamedType)
1.  [function <span class="apidocSignatureSpan">graphql.</span>getNullableType (type)](#apidoc.element.graphql.getNullableType)
1.  [function <span class="apidocSignatureSpan">graphql.</span>getOperationAST (documentAST, operationName)](#apidoc.element.graphql.getOperationAST)
1.  [function <span class="apidocSignatureSpan">graphql.</span>isAbstractType (type)](#apidoc.element.graphql.isAbstractType)
1.  [function <span class="apidocSignatureSpan">graphql.</span>isCompositeType (type)](#apidoc.element.graphql.isCompositeType)
1.  [function <span class="apidocSignatureSpan">graphql.</span>isEqualType (typeA, typeB)](#apidoc.element.graphql.isEqualType)
1.  [function <span class="apidocSignatureSpan">graphql.</span>isInputType (type)](#apidoc.element.graphql.isInputType)
1.  [function <span class="apidocSignatureSpan">graphql.</span>isLeafType (type)](#apidoc.element.graphql.isLeafType)
1.  [function <span class="apidocSignatureSpan">graphql.</span>isNamedType (type)](#apidoc.element.graphql.isNamedType)
1.  [function <span class="apidocSignatureSpan">graphql.</span>isOutputType (type)](#apidoc.element.graphql.isOutputType)
1.  [function <span class="apidocSignatureSpan">graphql.</span>isType (type)](#apidoc.element.graphql.isType)
1.  [function <span class="apidocSignatureSpan">graphql.</span>isTypeSubTypeOf (schema, maybeSubType, superType)](#apidoc.element.graphql.isTypeSubTypeOf)
1.  [function <span class="apidocSignatureSpan">graphql.</span>isValidJSValue (value, type)](#apidoc.element.graphql.isValidJSValue)
1.  [function <span class="apidocSignatureSpan">graphql.</span>isValidLiteralValue (type, valueNode)](#apidoc.element.graphql.isValidLiteralValue)
1.  [function <span class="apidocSignatureSpan">graphql.</span>parse (source, options)](#apidoc.element.graphql.parse)
1.  [function <span class="apidocSignatureSpan">graphql.</span>parseType (source, options)](#apidoc.element.graphql.parseType)
1.  [function <span class="apidocSignatureSpan">graphql.</span>parseValue (source, options)](#apidoc.element.graphql.parseValue)
1.  [function <span class="apidocSignatureSpan">graphql.</span>print (ast)](#apidoc.element.graphql.print)
1.  [function <span class="apidocSignatureSpan">graphql.</span>printSchema (schema)](#apidoc.element.graphql.printSchema)
1.  [function <span class="apidocSignatureSpan">graphql.</span>printType (type)](#apidoc.element.graphql.printType)
1.  [function <span class="apidocSignatureSpan">graphql.</span>responsePathAsArray (path)](#apidoc.element.graphql.responsePathAsArray)
1.  [function <span class="apidocSignatureSpan">graphql.</span>separateOperations (documentAST)](#apidoc.element.graphql.separateOperations)
1.  [function <span class="apidocSignatureSpan">graphql.</span>typeFromAST (schema, typeNode)](#apidoc.element.graphql.typeFromAST)
1.  [function <span class="apidocSignatureSpan">graphql.</span>validate (schema, ast, rules)](#apidoc.element.graphql.validate)
1.  [function <span class="apidocSignatureSpan">graphql.</span>valueFromAST (valueNode, type, variables)](#apidoc.element.graphql.valueFromAST)
1.  [function <span class="apidocSignatureSpan">graphql.</span>visit (root, visitor, keyMap)](#apidoc.element.graphql.visit)
1.  [function <span class="apidocSignatureSpan">graphql.</span>visitInParallel (visitors)](#apidoc.element.graphql.visitInParallel)
1.  [function <span class="apidocSignatureSpan">graphql.</span>visitWithTypeInfo (typeInfo, visitor)](#apidoc.element.graphql.visitWithTypeInfo)
1.  object <span class="apidocSignatureSpan">graphql.</span>BREAK
1.  object <span class="apidocSignatureSpan">graphql.</span>DirectiveLocation
1.  object <span class="apidocSignatureSpan">graphql.</span>GraphQLBoolean
1.  object <span class="apidocSignatureSpan">graphql.</span>GraphQLDeprecatedDirective
1.  object <span class="apidocSignatureSpan">graphql.</span>GraphQLEnumType.prototype
1.  object <span class="apidocSignatureSpan">graphql.</span>GraphQLFloat
1.  object <span class="apidocSignatureSpan">graphql.</span>GraphQLID
1.  object <span class="apidocSignatureSpan">graphql.</span>GraphQLIncludeDirective
1.  object <span class="apidocSignatureSpan">graphql.</span>GraphQLInputObjectType.prototype
1.  object <span class="apidocSignatureSpan">graphql.</span>GraphQLInt
1.  object <span class="apidocSignatureSpan">graphql.</span>GraphQLInterfaceType.prototype
1.  object <span class="apidocSignatureSpan">graphql.</span>GraphQLList.prototype
1.  object <span class="apidocSignatureSpan">graphql.</span>GraphQLNonNull.prototype
1.  object <span class="apidocSignatureSpan">graphql.</span>GraphQLObjectType.prototype
1.  object <span class="apidocSignatureSpan">graphql.</span>GraphQLScalarType.prototype
1.  object <span class="apidocSignatureSpan">graphql.</span>GraphQLSchema.prototype
1.  object <span class="apidocSignatureSpan">graphql.</span>GraphQLSkipDirective
1.  object <span class="apidocSignatureSpan">graphql.</span>GraphQLString
1.  object <span class="apidocSignatureSpan">graphql.</span>GraphQLUnionType.prototype
1.  object <span class="apidocSignatureSpan">graphql.</span>Kind
1.  object <span class="apidocSignatureSpan">graphql.</span>SchemaMetaFieldDef
1.  object <span class="apidocSignatureSpan">graphql.</span>TokenKind
1.  object <span class="apidocSignatureSpan">graphql.</span>TypeInfo.prototype
1.  object <span class="apidocSignatureSpan">graphql.</span>TypeKind
1.  object <span class="apidocSignatureSpan">graphql.</span>TypeMetaFieldDef
1.  object <span class="apidocSignatureSpan">graphql.</span>TypeNameMetaFieldDef
1.  object <span class="apidocSignatureSpan">graphql.</span>ValidationContext.prototype
1.  object <span class="apidocSignatureSpan">graphql.</span>__Directive
1.  object <span class="apidocSignatureSpan">graphql.</span>__DirectiveLocation
1.  object <span class="apidocSignatureSpan">graphql.</span>__EnumValue
1.  object <span class="apidocSignatureSpan">graphql.</span>__Field
1.  object <span class="apidocSignatureSpan">graphql.</span>__InputValue
1.  object <span class="apidocSignatureSpan">graphql.</span>__Schema
1.  object <span class="apidocSignatureSpan">graphql.</span>__Type
1.  object <span class="apidocSignatureSpan">graphql.</span>__TypeKind
1.  object <span class="apidocSignatureSpan">graphql.</span>specifiedDirectives
1.  object <span class="apidocSignatureSpan">graphql.</span>specifiedRules
1.  string <span class="apidocSignatureSpan">graphql.</span>DEFAULT_DEPRECATION_REASON
1.  string <span class="apidocSignatureSpan">graphql.</span>introspectionQuery

#### [module graphql.GraphQLEnumType](#apidoc.module.graphql.GraphQLEnumType)
1.  [function <span class="apidocSignatureSpan">graphql.</span>GraphQLEnumType (config)](#apidoc.element.graphql.GraphQLEnumType.GraphQLEnumType)

#### [module graphql.GraphQLEnumType.prototype](#apidoc.module.graphql.GraphQLEnumType.prototype)
1.  [function <span class="apidocSignatureSpan">graphql.GraphQLEnumType.prototype.</span>_getNameLookup ()](#apidoc.element.graphql.GraphQLEnumType.prototype._getNameLookup)
1.  [function <span class="apidocSignatureSpan">graphql.GraphQLEnumType.prototype.</span>_getValueLookup ()](#apidoc.element.graphql.GraphQLEnumType.prototype._getValueLookup)
1.  [function <span class="apidocSignatureSpan">graphql.GraphQLEnumType.prototype.</span>getValue (name)](#apidoc.element.graphql.GraphQLEnumType.prototype.getValue)
1.  [function <span class="apidocSignatureSpan">graphql.GraphQLEnumType.prototype.</span>getValues ()](#apidoc.element.graphql.GraphQLEnumType.prototype.getValues)
1.  [function <span class="apidocSignatureSpan">graphql.GraphQLEnumType.prototype.</span>inspect ()](#apidoc.element.graphql.GraphQLEnumType.prototype.inspect)
1.  [function <span class="apidocSignatureSpan">graphql.GraphQLEnumType.prototype.</span>parseLiteral (valueNode)](#apidoc.element.graphql.GraphQLEnumType.prototype.parseLiteral)
1.  [function <span class="apidocSignatureSpan">graphql.GraphQLEnumType.prototype.</span>parseValue (value)](#apidoc.element.graphql.GraphQLEnumType.prototype.parseValue)
1.  [function <span class="apidocSignatureSpan">graphql.GraphQLEnumType.prototype.</span>serialize (value)](#apidoc.element.graphql.GraphQLEnumType.prototype.serialize)
1.  [function <span class="apidocSignatureSpan">graphql.GraphQLEnumType.prototype.</span>toJSON ()](#apidoc.element.graphql.GraphQLEnumType.prototype.toJSON)
1.  [function <span class="apidocSignatureSpan">graphql.GraphQLEnumType.prototype.</span>toString ()](#apidoc.element.graphql.GraphQLEnumType.prototype.toString)

#### [module graphql.GraphQLError](#apidoc.module.graphql.GraphQLError)
1.  [function <span class="apidocSignatureSpan">graphql.</span>GraphQLError ( // eslint-disable-line no-redeclare message, nodes, source, positions, path, originalError)](#apidoc.element.graphql.GraphQLError.GraphQLError)

#### [module graphql.GraphQLInputObjectType](#apidoc.module.graphql.GraphQLInputObjectType)
1.  [function <span class="apidocSignatureSpan">graphql.</span>GraphQLInputObjectType (config)](#apidoc.element.graphql.GraphQLInputObjectType.GraphQLInputObjectType)

#### [module graphql.GraphQLInputObjectType.prototype](#apidoc.module.graphql.GraphQLInputObjectType.prototype)
1.  [function <span class="apidocSignatureSpan">graphql.GraphQLInputObjectType.prototype.</span>_defineFieldMap ()](#apidoc.element.graphql.GraphQLInputObjectType.prototype._defineFieldMap)
1.  [function <span class="apidocSignatureSpan">graphql.GraphQLInputObjectType.prototype.</span>getFields ()](#apidoc.element.graphql.GraphQLInputObjectType.prototype.getFields)
1.  [function <span class="apidocSignatureSpan">graphql.GraphQLInputObjectType.prototype.</span>inspect ()](#apidoc.element.graphql.GraphQLInputObjectType.prototype.inspect)
1.  [function <span class="apidocSignatureSpan">graphql.GraphQLInputObjectType.prototype.</span>toJSON ()](#apidoc.element.graphql.GraphQLInputObjectType.prototype.toJSON)
1.  [function <span class="apidocSignatureSpan">graphql.GraphQLInputObjectType.prototype.</span>toString ()](#apidoc.element.graphql.GraphQLInputObjectType.prototype.toString)

#### [module graphql.GraphQLInterfaceType](#apidoc.module.graphql.GraphQLInterfaceType)
1.  [function <span class="apidocSignatureSpan">graphql.</span>GraphQLInterfaceType (config)](#apidoc.element.graphql.GraphQLInterfaceType.GraphQLInterfaceType)

#### [module graphql.GraphQLInterfaceType.prototype](#apidoc.module.graphql.GraphQLInterfaceType.prototype)
1.  [function <span class="apidocSignatureSpan">graphql.GraphQLInterfaceType.prototype.</span>getFields ()](#apidoc.element.graphql.GraphQLInterfaceType.prototype.getFields)
1.  [function <span class="apidocSignatureSpan">graphql.GraphQLInterfaceType.prototype.</span>inspect ()](#apidoc.element.graphql.GraphQLInterfaceType.prototype.inspect)
1.  [function <span class="apidocSignatureSpan">graphql.GraphQLInterfaceType.prototype.</span>toJSON ()](#apidoc.element.graphql.GraphQLInterfaceType.prototype.toJSON)
1.  [function <span class="apidocSignatureSpan">graphql.GraphQLInterfaceType.prototype.</span>toString ()](#apidoc.element.graphql.GraphQLInterfaceType.prototype.toString)

#### [module graphql.GraphQLList](#apidoc.module.graphql.GraphQLList)
1.  [function <span class="apidocSignatureSpan">graphql.</span>GraphQLList (type)](#apidoc.element.graphql.GraphQLList.GraphQLList)

#### [module graphql.GraphQLList.prototype](#apidoc.module.graphql.GraphQLList.prototype)
1.  [function <span class="apidocSignatureSpan">graphql.GraphQLList.prototype.</span>inspect ()](#apidoc.element.graphql.GraphQLList.prototype.inspect)
1.  [function <span class="apidocSignatureSpan">graphql.GraphQLList.prototype.</span>toJSON ()](#apidoc.element.graphql.GraphQLList.prototype.toJSON)
1.  [function <span class="apidocSignatureSpan">graphql.GraphQLList.prototype.</span>toString ()](#apidoc.element.graphql.GraphQLList.prototype.toString)

#### [module graphql.GraphQLNonNull](#apidoc.module.graphql.GraphQLNonNull)
1.  [function <span class="apidocSignatureSpan">graphql.</span>GraphQLNonNull (type)](#apidoc.element.graphql.GraphQLNonNull.GraphQLNonNull)

#### [module graphql.GraphQLNonNull.prototype](#apidoc.module.graphql.GraphQLNonNull.prototype)
1.  [function <span class="apidocSignatureSpan">graphql.GraphQLNonNull.prototype.</span>inspect ()](#apidoc.element.graphql.GraphQLNonNull.prototype.inspect)
1.  [function <span class="apidocSignatureSpan">graphql.GraphQLNonNull.prototype.</span>toJSON ()](#apidoc.element.graphql.GraphQLNonNull.prototype.toJSON)
1.  [function <span class="apidocSignatureSpan">graphql.GraphQLNonNull.prototype.</span>toString ()](#apidoc.element.graphql.GraphQLNonNull.prototype.toString)

#### [module graphql.GraphQLObjectType](#apidoc.module.graphql.GraphQLObjectType)
1.  [function <span class="apidocSignatureSpan">graphql.</span>GraphQLObjectType (config)](#apidoc.element.graphql.GraphQLObjectType.GraphQLObjectType)

#### [module graphql.GraphQLObjectType.prototype](#apidoc.module.graphql.GraphQLObjectType.prototype)
1.  [function <span class="apidocSignatureSpan">graphql.GraphQLObjectType.prototype.</span>getFields ()](#apidoc.element.graphql.GraphQLObjectType.prototype.getFields)
1.  [function <span class="apidocSignatureSpan">graphql.GraphQLObjectType.prototype.</span>getInterfaces ()](#apidoc.element.graphql.GraphQLObjectType.prototype.getInterfaces)
1.  [function <span class="apidocSignatureSpan">graphql.GraphQLObjectType.prototype.</span>inspect ()](#apidoc.element.graphql.GraphQLObjectType.prototype.inspect)
1.  [function <span class="apidocSignatureSpan">graphql.GraphQLObjectType.prototype.</span>toJSON ()](#apidoc.element.graphql.GraphQLObjectType.prototype.toJSON)
1.  [function <span class="apidocSignatureSpan">graphql.GraphQLObjectType.prototype.</span>toString ()](#apidoc.element.graphql.GraphQLObjectType.prototype.toString)

#### [module graphql.GraphQLScalarType](#apidoc.module.graphql.GraphQLScalarType)
1.  [function <span class="apidocSignatureSpan">graphql.</span>GraphQLScalarType (config)](#apidoc.element.graphql.GraphQLScalarType.GraphQLScalarType)

#### [module graphql.GraphQLScalarType.prototype](#apidoc.module.graphql.GraphQLScalarType.prototype)
1.  [function <span class="apidocSignatureSpan">graphql.GraphQLScalarType.prototype.</span>inspect ()](#apidoc.element.graphql.GraphQLScalarType.prototype.inspect)
1.  [function <span class="apidocSignatureSpan">graphql.GraphQLScalarType.prototype.</span>parseLiteral (valueNode)](#apidoc.element.graphql.GraphQLScalarType.prototype.parseLiteral)
1.  [function <span class="apidocSignatureSpan">graphql.GraphQLScalarType.prototype.</span>parseValue (value)](#apidoc.element.graphql.GraphQLScalarType.prototype.parseValue)
1.  [function <span class="apidocSignatureSpan">graphql.GraphQLScalarType.prototype.</span>serialize (value)](#apidoc.element.graphql.GraphQLScalarType.prototype.serialize)
1.  [function <span class="apidocSignatureSpan">graphql.GraphQLScalarType.prototype.</span>toJSON ()](#apidoc.element.graphql.GraphQLScalarType.prototype.toJSON)
1.  [function <span class="apidocSignatureSpan">graphql.GraphQLScalarType.prototype.</span>toString ()](#apidoc.element.graphql.GraphQLScalarType.prototype.toString)

#### [module graphql.GraphQLSchema](#apidoc.module.graphql.GraphQLSchema)
1.  [function <span class="apidocSignatureSpan">graphql.</span>GraphQLSchema (config)](#apidoc.element.graphql.GraphQLSchema.GraphQLSchema)

#### [module graphql.GraphQLSchema.prototype](#apidoc.module.graphql.GraphQLSchema.prototype)
1.  [function <span class="apidocSignatureSpan">graphql.GraphQLSchema.prototype.</span>getDirective (name)](#apidoc.element.graphql.GraphQLSchema.prototype.getDirective)
1.  [function <span class="apidocSignatureSpan">graphql.GraphQLSchema.prototype.</span>getDirectives ()](#apidoc.element.graphql.GraphQLSchema.prototype.getDirectives)
1.  [function <span class="apidocSignatureSpan">graphql.GraphQLSchema.prototype.</span>getMutationType ()](#apidoc.element.graphql.GraphQLSchema.prototype.getMutationType)
1.  [function <span class="apidocSignatureSpan">graphql.GraphQLSchema.prototype.</span>getPossibleTypes (abstractType)](#apidoc.element.graphql.GraphQLSchema.prototype.getPossibleTypes)
1.  [function <span class="apidocSignatureSpan">graphql.GraphQLSchema.prototype.</span>getQueryType ()](#apidoc.element.graphql.GraphQLSchema.prototype.getQueryType)
1.  [function <span class="apidocSignatureSpan">graphql.GraphQLSchema.prototype.</span>getSubscriptionType ()](#apidoc.element.graphql.GraphQLSchema.prototype.getSubscriptionType)
1.  [function <span class="apidocSignatureSpan">graphql.GraphQLSchema.prototype.</span>getType (name)](#apidoc.element.graphql.GraphQLSchema.prototype.getType)
1.  [function <span class="apidocSignatureSpan">graphql.GraphQLSchema.prototype.</span>getTypeMap ()](#apidoc.element.graphql.GraphQLSchema.prototype.getTypeMap)
1.  [function <span class="apidocSignatureSpan">graphql.GraphQLSchema.prototype.</span>isPossibleType (abstractType, possibleType)](#apidoc.element.graphql.GraphQLSchema.prototype.isPossibleType)

#### [module graphql.GraphQLUnionType](#apidoc.module.graphql.GraphQLUnionType)
1.  [function <span class="apidocSignatureSpan">graphql.</span>GraphQLUnionType (config)](#apidoc.element.graphql.GraphQLUnionType.GraphQLUnionType)

#### [module graphql.GraphQLUnionType.prototype](#apidoc.module.graphql.GraphQLUnionType.prototype)
1.  [function <span class="apidocSignatureSpan">graphql.GraphQLUnionType.prototype.</span>getTypes ()](#apidoc.element.graphql.GraphQLUnionType.prototype.getTypes)
1.  [function <span class="apidocSignatureSpan">graphql.GraphQLUnionType.prototype.</span>inspect ()](#apidoc.element.graphql.GraphQLUnionType.prototype.inspect)
1.  [function <span class="apidocSignatureSpan">graphql.GraphQLUnionType.prototype.</span>toJSON ()](#apidoc.element.graphql.GraphQLUnionType.prototype.toJSON)
1.  [function <span class="apidocSignatureSpan">graphql.GraphQLUnionType.prototype.</span>toString ()](#apidoc.element.graphql.GraphQLUnionType.prototype.toString)

#### [module graphql.SchemaMetaFieldDef](#apidoc.module.graphql.SchemaMetaFieldDef)
1.  [function <span class="apidocSignatureSpan">graphql.SchemaMetaFieldDef.</span>resolve (source, args, context, _ref4)](#apidoc.element.graphql.SchemaMetaFieldDef.resolve)
1.  object <span class="apidocSignatureSpan">graphql.SchemaMetaFieldDef.</span>args
1.  object <span class="apidocSignatureSpan">graphql.SchemaMetaFieldDef.</span>type
1.  string <span class="apidocSignatureSpan">graphql.SchemaMetaFieldDef.</span>description
1.  string <span class="apidocSignatureSpan">graphql.SchemaMetaFieldDef.</span>name

#### [module graphql.TypeInfo](#apidoc.module.graphql.TypeInfo)
1.  [function <span class="apidocSignatureSpan">graphql.</span>TypeInfo (schema, // NOTE: this experimental optional second parameter is only needed in order // to support non-spec-compliant codebases. You should never need to use it. getFieldDefFn)](#apidoc.element.graphql.TypeInfo.TypeInfo)

#### [module graphql.TypeInfo.prototype](#apidoc.module.graphql.TypeInfo.prototype)
1.  [function <span class="apidocSignatureSpan">graphql.TypeInfo.prototype.</span>enter (node)](#apidoc.element.graphql.TypeInfo.prototype.enter)
1.  [function <span class="apidocSignatureSpan">graphql.TypeInfo.prototype.</span>getArgument ()](#apidoc.element.graphql.TypeInfo.prototype.getArgument)
1.  [function <span class="apidocSignatureSpan">graphql.TypeInfo.prototype.</span>getDirective ()](#apidoc.element.graphql.TypeInfo.prototype.getDirective)
1.  [function <span class="apidocSignatureSpan">graphql.TypeInfo.prototype.</span>getEnumValue ()](#apidoc.element.graphql.TypeInfo.prototype.getEnumValue)
1.  [function <span class="apidocSignatureSpan">graphql.TypeInfo.prototype.</span>getFieldDef ()](#apidoc.element.graphql.TypeInfo.prototype.getFieldDef)
1.  [function <span class="apidocSignatureSpan">graphql.TypeInfo.prototype.</span>getInputType ()](#apidoc.element.graphql.TypeInfo.prototype.getInputType)
1.  [function <span class="apidocSignatureSpan">graphql.TypeInfo.prototype.</span>getParentType ()](#apidoc.element.graphql.TypeInfo.prototype.getParentType)
1.  [function <span class="apidocSignatureSpan">graphql.TypeInfo.prototype.</span>getType ()](#apidoc.element.graphql.TypeInfo.prototype.getType)
1.  [function <span class="apidocSignatureSpan">graphql.TypeInfo.prototype.</span>leave (node)](#apidoc.element.graphql.TypeInfo.prototype.leave)

#### [module graphql.TypeMetaFieldDef](#apidoc.module.graphql.TypeMetaFieldDef)
1.  [function <span class="apidocSignatureSpan">graphql.TypeMetaFieldDef.</span>resolve (source, _ref5, context, _ref6)](#apidoc.element.graphql.TypeMetaFieldDef.resolve)
1.  object <span class="apidocSignatureSpan">graphql.TypeMetaFieldDef.</span>args
1.  object <span class="apidocSignatureSpan">graphql.TypeMetaFieldDef.</span>type
1.  string <span class="apidocSignatureSpan">graphql.TypeMetaFieldDef.</span>description
1.  string <span class="apidocSignatureSpan">graphql.TypeMetaFieldDef.</span>name

#### [module graphql.TypeNameMetaFieldDef](#apidoc.module.graphql.TypeNameMetaFieldDef)
1.  [function <span class="apidocSignatureSpan">graphql.TypeNameMetaFieldDef.</span>resolve (source, args, context, _ref7)](#apidoc.element.graphql.TypeNameMetaFieldDef.resolve)
1.  object <span class="apidocSignatureSpan">graphql.TypeNameMetaFieldDef.</span>args
1.  object <span class="apidocSignatureSpan">graphql.TypeNameMetaFieldDef.</span>type
1.  string <span class="apidocSignatureSpan">graphql.TypeNameMetaFieldDef.</span>description
1.  string <span class="apidocSignatureSpan">graphql.TypeNameMetaFieldDef.</span>name

#### [module graphql.ValidationContext](#apidoc.module.graphql.ValidationContext)
1.  [function <span class="apidocSignatureSpan">graphql.</span>ValidationContext (schema, ast, typeInfo)](#apidoc.element.graphql.ValidationContext.ValidationContext)

#### [module graphql.ValidationContext.prototype](#apidoc.module.graphql.ValidationContext.prototype)
1.  [function <span class="apidocSignatureSpan">graphql.ValidationContext.prototype.</span>getArgument ()](#apidoc.element.graphql.ValidationContext.prototype.getArgument)
1.  [function <span class="apidocSignatureSpan">graphql.ValidationContext.prototype.</span>getDirective ()](#apidoc.element.graphql.ValidationContext.prototype.getDirective)
1.  [function <span class="apidocSignatureSpan">graphql.ValidationContext.prototype.</span>getDocument ()](#apidoc.element.graphql.ValidationContext.prototype.getDocument)
1.  [function <span class="apidocSignatureSpan">graphql.ValidationContext.prototype.</span>getErrors ()](#apidoc.element.graphql.ValidationContext.prototype.getErrors)
1.  [function <span class="apidocSignatureSpan">graphql.ValidationContext.prototype.</span>getFieldDef ()](#apidoc.element.graphql.ValidationContext.prototype.getFieldDef)
1.  [function <span class="apidocSignatureSpan">graphql.ValidationContext.prototype.</span>getFragment (name)](#apidoc.element.graphql.ValidationContext.prototype.getFragment)
1.  [function <span class="apidocSignatureSpan">graphql.ValidationContext.prototype.</span>getFragmentSpreads (node)](#apidoc.element.graphql.ValidationContext.prototype.getFragmentSpreads)
1.  [function <span class="apidocSignatureSpan">graphql.ValidationContext.prototype.</span>getInputType ()](#apidoc.element.graphql.ValidationContext.prototype.getInputType)
1.  [function <span class="apidocSignatureSpan">graphql.ValidationContext.prototype.</span>getParentType ()](#apidoc.element.graphql.ValidationContext.prototype.getParentType)
1.  [function <span class="apidocSignatureSpan">graphql.ValidationContext.prototype.</span>getRecursiveVariableUsages (operation)](#apidoc.element.graphql.ValidationContext.prototype.getRecursiveVariableUsages)
1.  [function <span class="apidocSignatureSpan">graphql.ValidationContext.prototype.</span>getRecursivelyReferencedFragments (operation)](#apidoc.element.graphql.ValidationContext.prototype.getRecursivelyReferencedFragments)
1.  [function <span class="apidocSignatureSpan">graphql.ValidationContext.prototype.</span>getSchema ()](#apidoc.element.graphql.ValidationContext.prototype.getSchema)
1.  [function <span class="apidocSignatureSpan">graphql.ValidationContext.prototype.</span>getType ()](#apidoc.element.graphql.ValidationContext.prototype.getType)
1.  [function <span class="apidocSignatureSpan">graphql.ValidationContext.prototype.</span>getVariableUsages (node)](#apidoc.element.graphql.ValidationContext.prototype.getVariableUsages)
1.  [function <span class="apidocSignatureSpan">graphql.ValidationContext.prototype.</span>reportError (error)](#apidoc.element.graphql.ValidationContext.prototype.reportError)

#### [module graphql.specifiedRules](#apidoc.module.graphql.specifiedRules)
1.  [function <span class="apidocSignatureSpan">graphql.specifiedRules.</span>0 (context)](#apidoc.element.graphql.specifiedRules.0)
1.  [function <span class="apidocSignatureSpan">graphql.specifiedRules.</span>1 (context)](#apidoc.element.graphql.specifiedRules.1)
1.  [function <span class="apidocSignatureSpan">graphql.specifiedRules.</span>10 (context)](#apidoc.element.graphql.specifiedRules.10)
1.  [function <span class="apidocSignatureSpan">graphql.specifiedRules.</span>11 (context)](#apidoc.element.graphql.specifiedRules.11)
1.  [function <span class="apidocSignatureSpan">graphql.specifiedRules.</span>12 (context)](#apidoc.element.graphql.specifiedRules.12)
1.  [function <span class="apidocSignatureSpan">graphql.specifiedRules.</span>13 (context)](#apidoc.element.graphql.specifiedRules.13)
1.  [function <span class="apidocSignatureSpan">graphql.specifiedRules.</span>14 (context)](#apidoc.element.graphql.specifiedRules.14)
1.  [function <span class="apidocSignatureSpan">graphql.specifiedRules.</span>15 (context)](#apidoc.element.graphql.specifiedRules.15)
1.  [function <span class="apidocSignatureSpan">graphql.specifiedRules.</span>16 (context)](#apidoc.element.graphql.specifiedRules.16)
1.  [function <span class="apidocSignatureSpan">graphql.specifiedRules.</span>17 (context)](#apidoc.element.graphql.specifiedRules.17)
1.  [function <span class="apidocSignatureSpan">graphql.specifiedRules.</span>18 (context)](#apidoc.element.graphql.specifiedRules.18)
1.  [function <span class="apidocSignatureSpan">graphql.specifiedRules.</span>19 (context)](#apidoc.element.graphql.specifiedRules.19)
1.  [function <span class="apidocSignatureSpan">graphql.specifiedRules.</span>2 (context)](#apidoc.element.graphql.specifiedRules.2)
1.  [function <span class="apidocSignatureSpan">graphql.specifiedRules.</span>20 (context)](#apidoc.element.graphql.specifiedRules.20)
1.  [function <span class="apidocSignatureSpan">graphql.specifiedRules.</span>21 (context)](#apidoc.element.graphql.specifiedRules.21)
1.  [function <span class="apidocSignatureSpan">graphql.specifiedRules.</span>22 (context)](#apidoc.element.graphql.specifiedRules.22)
1.  [function <span class="apidocSignatureSpan">graphql.specifiedRules.</span>23 (context)](#apidoc.element.graphql.specifiedRules.23)
1.  [function <span class="apidocSignatureSpan">graphql.specifiedRules.</span>24 (context)](#apidoc.element.graphql.specifiedRules.24)
1.  [function <span class="apidocSignatureSpan">graphql.specifiedRules.</span>3 (context)](#apidoc.element.graphql.specifiedRules.3)
1.  [function <span class="apidocSignatureSpan">graphql.specifiedRules.</span>4 (context)](#apidoc.element.graphql.specifiedRules.4)
1.  [function <span class="apidocSignatureSpan">graphql.specifiedRules.</span>5 (context)](#apidoc.element.graphql.specifiedRules.5)
1.  [function <span class="apidocSignatureSpan">graphql.specifiedRules.</span>6 (context)](#apidoc.element.graphql.specifiedRules.6)
1.  [function <span class="apidocSignatureSpan">graphql.specifiedRules.</span>7 (context)](#apidoc.element.graphql.specifiedRules.7)
1.  [function <span class="apidocSignatureSpan">graphql.specifiedRules.</span>8 (context)](#apidoc.element.graphql.specifiedRules.8)
1.  [function <span class="apidocSignatureSpan">graphql.specifiedRules.</span>9 (context)](#apidoc.element.graphql.specifiedRules.9)



# <a name="apidoc.module.graphql"></a>[module graphql](#apidoc.module.graphql)

#### <a name="apidoc.element.graphql.graphql"></a>[function <span class="apidocSignatureSpan"></span>graphql (schema, requestString, rootValue, contextValue, variableValues, operationName)](#apidoc.element.graphql.graphql)
- description and source-code
```javascript
function graphql(schema, requestString, rootValue, contextValue, variableValues, operationName) {
  return new Promise(function (resolve) {
    var source = new _source.Source(requestString || '', 'GraphQL request');
    var documentAST = (0, _parser.parse)(source);
    var validationErrors = (0, _validate.validate)(schema, documentAST);
    if (validationErrors.length > 0) {
      resolve({ errors: validationErrors });
    } else {
      resolve((0, _execute.execute)(schema, documentAST, rootValue, contextValue, variableValues, operationName));
    }
  }).then(undefined, function (error) {
    return { errors: [error] };
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.GraphQLDirective"></a>[function <span class="apidocSignatureSpan">graphql.</span>GraphQLDirective (config)](#apidoc.element.graphql.GraphQLDirective)
- description and source-code
```javascript
function GraphQLDirective(config) {
  _classCallCheck(this, GraphQLDirective);

  (0, _invariant2.default)(config.name, 'Directive must be named.');
  (0, _assertValidName.assertValidName)(config.name);
  (0, _invariant2.default)(Array.isArray(config.locations), 'Must provide locations for directive.');
  this.name = config.name;
  this.description = config.description;
  this.locations = config.locations;

  var args = config.args;
  if (!args) {
    this.args = [];
  } else {
    (0, _invariant2.default)(!Array.isArray(args), '@' + config.name + ' args must be an object with argument names as keys.');
    this.args = Object.keys(args).map(function (argName) {
      (0, _assertValidName.assertValidName)(argName);
      var arg = args[argName];
      (0, _invariant2.default)((0, _definition.isInputType)(arg.type), '@' + config.name + '(' + argName + ':) argument type must
 be ' + ('Input Type but got: ' + String(arg.type) + '.'));
      return {
        name: argName,
        description: arg.description === undefined ? null : arg.description,
        type: arg.type,
        defaultValue: arg.defaultValue
      };
    });
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.GraphQLEnumType"></a>[function <span class="apidocSignatureSpan">graphql.</span>GraphQLEnumType (config)](#apidoc.element.graphql.GraphQLEnumType)
- description and source-code
```javascript
function GraphQLEnumType(config) {
  _classCallCheck(this, GraphQLEnumType);

  this.name = config.name;
  (0, _assertValidName.assertValidName)(config.name, config.isIntrospection);
  this.description = config.description;
  this._values = defineEnumValues(this, config.values);
  this._enumConfig = config;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.GraphQLError"></a>[function <span class="apidocSignatureSpan">graphql.</span>GraphQLError ( // eslint-disable-line no-redeclare message, nodes, source, positions, path, originalError)](#apidoc.element.graphql.GraphQLError)
- description and source-code
```javascript
function GraphQLError( // eslint-disable-line no-redeclare message, nodes, source, positions, path, originalError) {
  // Include (non-enumerable) stack trace.
  if (originalError && originalError.stack) {
    Object.defineProperty(this, 'stack', {
      value: originalError.stack,
      writable: true,
      configurable: true
    });
  } else if (Error.captureStackTrace) {
    Error.captureStackTrace(this, GraphQLError);
  } else {
    Object.defineProperty(this, 'stack', {
      value: Error().stack,
      writable: true,
      configurable: true
    });
  }

  // Compute locations in the source for the given nodes/positions.
  var _source = source;
  if (!_source && nodes && nodes.length > 0) {
    var node = nodes[0];
    _source = node && node.loc && node.loc.source;
  }

  var _positions = positions;
  if (!_positions && nodes) {
    _positions = nodes.filter(function (node) {
      return Boolean(node.loc);
    }).map(function (node) {
      return node.loc.start;
    });
  }
  if (_positions && _positions.length === 0) {
    _positions = undefined;
  }

  var _locations = void 0;
  var _source2 = _source; // seems here Flow need a const to resolve type.
  if (_source2 && _positions) {
    _locations = _positions.map(function (pos) {
      return (0, _location.getLocation)(_source2, pos);
    });
  }

  Object.defineProperties(this, {
    message: {
      value: message,
      // By being enumerable, JSON.stringify will include 'message' in the
      // resulting output. This ensures that the simplist possible GraphQL
      // service adheres to the spec.
      enumerable: true,
      writable: true
    },
    locations: {
      // Coercing falsey values to undefined ensures they will not be included
      // in JSON.stringify() when not provided.
      value: _locations || undefined,
      // By being enumerable, JSON.stringify will include 'locations' in the
      // resulting output. This ensures that the simplist possible GraphQL
      // service adheres to the spec.
      enumerable: true
    },
    path: {
      // Coercing falsey values to undefined ensures they will not be included
      // in JSON.stringify() when not provided.
      value: path || undefined,
      // By being enumerable, JSON.stringify will include 'path' in the
      // resulting output. This ensures that the simplist possible GraphQL
      // service adheres to the spec.
      enumerable: true
    },
    nodes: {
      value: nodes || undefined
    },
    source: {
      value: _source || undefined
    },
    positions: {
      value: _positions || undefined
    },
    originalError: {
      value: originalError
    }
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.GraphQLInputObjectType"></a>[function <span class="apidocSignatureSpan">graphql.</span>GraphQLInputObjectType (config)](#apidoc.element.graphql.GraphQLInputObjectType)
- description and source-code
```javascript
function GraphQLInputObjectType(config) {
  _classCallCheck(this, GraphQLInputObjectType);

  (0, _assertValidName.assertValidName)(config.name);
  this.name = config.name;
  this.description = config.description;
  this._typeConfig = config;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.GraphQLInterfaceType"></a>[function <span class="apidocSignatureSpan">graphql.</span>GraphQLInterfaceType (config)](#apidoc.element.graphql.GraphQLInterfaceType)
- description and source-code
```javascript
function GraphQLInterfaceType(config) {
  _classCallCheck(this, GraphQLInterfaceType);

  (0, _assertValidName.assertValidName)(config.name);
  this.name = config.name;
  this.description = config.description;
  if (config.resolveType) {
    (0, _invariant2.default)(typeof config.resolveType === 'function', this.name + ' must provide "resolveType" as a function.');
  }
  this.resolveType = config.resolveType;
  this._typeConfig = config;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.GraphQLList"></a>[function <span class="apidocSignatureSpan">graphql.</span>GraphQLList (type)](#apidoc.element.graphql.GraphQLList)
- description and source-code
```javascript
function GraphQLList(type) {
  _classCallCheck(this, GraphQLList);

  (0, _invariant2.default)(isType(type), 'Can only create List of a GraphQLType but got: ' + String(type) + '.');
  this.ofType = type;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.GraphQLNonNull"></a>[function <span class="apidocSignatureSpan">graphql.</span>GraphQLNonNull (type)](#apidoc.element.graphql.GraphQLNonNull)
- description and source-code
```javascript
function GraphQLNonNull(type) {
  _classCallCheck(this, GraphQLNonNull);

  (0, _invariant2.default)(isType(type) && !(type instanceof GraphQLNonNull), 'Can only create NonNull of a Nullable GraphQLType
 but got: ' + (String(type) + '.'));
  this.ofType = type;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.GraphQLObjectType"></a>[function <span class="apidocSignatureSpan">graphql.</span>GraphQLObjectType (config)](#apidoc.element.graphql.GraphQLObjectType)
- description and source-code
```javascript
function GraphQLObjectType(config) {
  _classCallCheck(this, GraphQLObjectType);

  (0, _assertValidName.assertValidName)(config.name, config.isIntrospection);
  this.name = config.name;
  this.description = config.description;
  if (config.isTypeOf) {
    (0, _invariant2.default)(typeof config.isTypeOf === 'function', this.name + ' must provide "isTypeOf" as a function.');
  }
  this.isTypeOf = config.isTypeOf;
  this._typeConfig = config;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.GraphQLScalarType"></a>[function <span class="apidocSignatureSpan">graphql.</span>GraphQLScalarType (config)](#apidoc.element.graphql.GraphQLScalarType)
- description and source-code
```javascript
function GraphQLScalarType(config) {
  _classCallCheck(this, GraphQLScalarType);

  (0, _assertValidName.assertValidName)(config.name);
  this.name = config.name;
  this.description = config.description;
  (0, _invariant2.default)(typeof config.serialize === 'function', this.name + ' must provide "serialize" function. If this custom
 Scalar ' + 'is also used as an input type, ensure "parseValue" and "parseLiteral" ' + 'functions are also provided.');
  if (config.parseValue || config.parseLiteral) {
    (0, _invariant2.default)(typeof config.parseValue === 'function' && typeof config.parseLiteral === 'function', this.name + '
must provide both "parseValue" and "parseLiteral" ' + 'functions.');
  }
  this._scalarConfig = config;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.GraphQLSchema"></a>[function <span class="apidocSignatureSpan">graphql.</span>GraphQLSchema (config)](#apidoc.element.graphql.GraphQLSchema)
- description and source-code
```javascript
function GraphQLSchema(config) {
  var _this = this;

  _classCallCheck(this, GraphQLSchema);

  (0, _invariant2.default)(typeof config === 'object', 'Must provide configuration object.');

  (0, _invariant2.default)(config.query instanceof _definition.GraphQLObjectType, 'Schema query must be Object Type but got: ' +
String(config.query) + '.');
  this._queryType = config.query;

  (0, _invariant2.default)(!config.mutation || config.mutation instanceof _definition.GraphQLObjectType, 'Schema mutation must be
 Object Type if provided but got: ' + String(config.mutation) + '.');
  this._mutationType = config.mutation;

  (0, _invariant2.default)(!config.subscription || config.subscription instanceof _definition.GraphQLObjectType, 'Schema subscription
 must be Object Type if provided but got: ' + String(config.subscription) + '.');
  this._subscriptionType = config.subscription;

  (0, _invariant2.default)(!config.types || Array.isArray(config.types), 'Schema types must be Array if provided but got: ' + String
(config.types) + '.');

  (0, _invariant2.default)(!config.directives || Array.isArray(config.directives) && config.directives.every(function (directive
) {
    return directive instanceof _directives.GraphQLDirective;
  }), 'Schema directives must be Array<GraphQLDirective> if provided but got: ' + String(config.directives) + '.');
  // Provide specified directives (e.g. @include and @skip) by default.
  this._directives = config.directives || _directives.specifiedDirectives;

  // Build type map now to detect any errors within this schema.
  var initialTypes = [this.getQueryType(), this.getMutationType(), this.getSubscriptionType(), _introspection.__Schema];

  var types = config.types;
  if (types) {
    initialTypes = initialTypes.concat(types);
  }

  this._typeMap = initialTypes.reduce(typeMapReducer, Object.create(null));

  // Keep track of all implementations by interface name.
  this._implementations = Object.create(null);
  Object.keys(this._typeMap).forEach(function (typeName) {
    var type = _this._typeMap[typeName];
    if (type instanceof _definition.GraphQLObjectType) {
      type.getInterfaces().forEach(function (iface) {
        var impls = _this._implementations[iface.name];
        if (impls) {
          impls.push(type);
        } else {
          _this._implementations[iface.name] = [type];
        }
      });
    }
  });

  // Enforce correct interface implementations.
  Object.keys(this._typeMap).forEach(function (typeName) {
    var type = _this._typeMap[typeName];
    if (type instanceof _definition.GraphQLObjectType) {
      type.getInterfaces().forEach(function (iface) {
        return assertObjectImplementsInterface(_this, type, iface);
      });
    }
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.GraphQLUnionType"></a>[function <span class="apidocSignatureSpan">graphql.</span>GraphQLUnionType (config)](#apidoc.element.graphql.GraphQLUnionType)
- description and source-code
```javascript
function GraphQLUnionType(config) {
  _classCallCheck(this, GraphQLUnionType);

  (0, _assertValidName.assertValidName)(config.name);
  this.name = config.name;
  this.description = config.description;
  if (config.resolveType) {
    (0, _invariant2.default)(typeof config.resolveType === 'function', this.name + ' must provide "resolveType" as a function.');
  }
  this.resolveType = config.resolveType;
  this._typeConfig = config;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.Source"></a>[function <span class="apidocSignatureSpan">graphql.</span>Source (body, name)](#apidoc.element.graphql.Source)
- description and source-code
```javascript
function Source(body, name) {
  _classCallCheck(this, Source);

  this.body = body;
  this.name = name || 'GraphQL';
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.TypeInfo"></a>[function <span class="apidocSignatureSpan">graphql.</span>TypeInfo (schema, // NOTE: this experimental optional second parameter is only needed in order // to support non-spec-compliant codebases. You should never need to use it. getFieldDefFn)](#apidoc.element.graphql.TypeInfo)
- description and source-code
```javascript
function TypeInfo(schema, // NOTE: this experimental optional second parameter is only needed in order // to support non-spec-compliant codebases. You should never need to use it. getFieldDefFn) {
  _classCallCheck(this, TypeInfo);

  this._schema = schema;
  this._typeStack = [];
  this._parentTypeStack = [];
  this._inputTypeStack = [];
  this._fieldDefStack = [];
  this._directive = null;
  this._argument = null;
  this._enumValue = null;
  this._getFieldDef = getFieldDefFn || getFieldDef;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.ValidationContext"></a>[function <span class="apidocSignatureSpan">graphql.</span>ValidationContext (schema, ast, typeInfo)](#apidoc.element.graphql.ValidationContext)
- description and source-code
```javascript
function ValidationContext(schema, ast, typeInfo) {
  _classCallCheck(this, ValidationContext);

  this._schema = schema;
  this._ast = ast;
  this._typeInfo = typeInfo;
  this._errors = [];
  this._fragmentSpreads = new Map();
  this._recursivelyReferencedFragments = new Map();
  this._variableUsages = new Map();
  this._recursiveVariableUsages = new Map();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.assertAbstractType"></a>[function <span class="apidocSignatureSpan">graphql.</span>assertAbstractType (type)](#apidoc.element.graphql.assertAbstractType)
- description and source-code
```javascript
function assertAbstractType(type) {
  (0, _invariant2.default)(isAbstractType(type), 'Expected ' + String(type) + ' to be a GraphQL abstract type.');
  return type;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.assertCompositeType"></a>[function <span class="apidocSignatureSpan">graphql.</span>assertCompositeType (type)](#apidoc.element.graphql.assertCompositeType)
- description and source-code
```javascript
function assertCompositeType(type) {
  (0, _invariant2.default)(isCompositeType(type), 'Expected ' + String(type) + ' to be a GraphQL composite type.');
  return type;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.assertInputType"></a>[function <span class="apidocSignatureSpan">graphql.</span>assertInputType (type)](#apidoc.element.graphql.assertInputType)
- description and source-code
```javascript
function assertInputType(type) {
  (0, _invariant2.default)(isInputType(type), 'Expected ' + String(type) + ' to be a GraphQL input type.');
  return type;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.assertLeafType"></a>[function <span class="apidocSignatureSpan">graphql.</span>assertLeafType (type)](#apidoc.element.graphql.assertLeafType)
- description and source-code
```javascript
function assertLeafType(type) {
  (0, _invariant2.default)(isLeafType(type), 'Expected ' + String(type) + ' to be a GraphQL leaf type.');
  return type;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.assertNamedType"></a>[function <span class="apidocSignatureSpan">graphql.</span>assertNamedType (type)](#apidoc.element.graphql.assertNamedType)
- description and source-code
```javascript
function assertNamedType(type) {
  (0, _invariant2.default)(isNamedType(type), 'Expected ' + String(type) + ' to be a GraphQL named type.');
  return type;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.assertOutputType"></a>[function <span class="apidocSignatureSpan">graphql.</span>assertOutputType (type)](#apidoc.element.graphql.assertOutputType)
- description and source-code
```javascript
function assertOutputType(type) {
  (0, _invariant2.default)(isOutputType(type), 'Expected ' + String(type) + ' to be a GraphQL output type.');
  return type;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.assertType"></a>[function <span class="apidocSignatureSpan">graphql.</span>assertType (type)](#apidoc.element.graphql.assertType)
- description and source-code
```javascript
function assertType(type) {
  (0, _invariant2.default)(isType(type), 'Expected ' + String(type) + ' to be a GraphQL type.');
  return type;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.assertValidName"></a>[function <span class="apidocSignatureSpan">graphql.</span>assertValidName (name, isIntrospection)](#apidoc.element.graphql.assertValidName)
- description and source-code
```javascript
function assertValidName(name, isIntrospection) {
  if (!name || typeof name !== 'string') {
    throw new Error('Must be named. Unexpected name: ' + name + '.');
  }
  if (!isIntrospection && name.slice(0, 2) === '__' && !hasWarnedAboutDunder) {
    hasWarnedAboutDunder = true;
<span class="apidocCodeCommentSpan">    /* eslint-disable no-console */
</span>    if (console && console.warn) {
      var error = new Error('Name "' + name + '" must not begin with "__", which is reserved by ' + 'GraphQL introspection. In a
 future release of graphql this will ' + 'become a hard error.');
      console.warn(formatWarning(error));
    }
    /* eslint-enable no-console */
  }
  if (!NAME_RX.test(name)) {
    throw new Error('Names must match /^[_a-zA-Z][_a-zA-Z0-9]*$/ but "' + name + '" does not.');
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.astFromValue"></a>[function <span class="apidocSignatureSpan">graphql.</span>astFromValue (value, type)](#apidoc.element.graphql.astFromValue)
- description and source-code
```javascript
function astFromValue(value, type) {
  // Ensure flow knows that we treat function params as const.
  var _value = value;

  if (type instanceof _definition.GraphQLNonNull) {
    var astValue = astFromValue(_value, type.ofType);
    if (astValue && astValue.kind === _kinds.NULL) {
      return null;
    }
    return astValue;
  }

  // only explicit null, not undefined, NaN
  if (_value === null) {
    return { kind: _kinds.NULL };
  }

  // undefined, NaN
  if ((0, _isInvalid2.default)(_value)) {
    return null;
  }

  // Convert JavaScript array to GraphQL list. If the GraphQLType is a list, but
  // the value is not an array, convert the value using the list's item type.
  if (type instanceof _definition.GraphQLList) {
    var itemType = type.ofType;
    if ((0, _iterall.isCollection)(_value)) {
      var valuesNodes = [];
      (0, _iterall.forEach)(_value, function (item) {
        var itemNode = astFromValue(item, itemType);
        if (itemNode) {
          valuesNodes.push(itemNode);
        }
      });
      return { kind: _kinds.LIST, values: valuesNodes };
    }
    return astFromValue(_value, itemType);
  }

  // Populate the fields of the input object by creating ASTs from each value
  // in the JavaScript object according to the fields in the input type.
  if (type instanceof _definition.GraphQLInputObjectType) {
    if (_value === null || typeof _value !== 'object') {
      return null;
    }
    var fields = type.getFields();
    var fieldNodes = [];
    Object.keys(fields).forEach(function (fieldName) {
      var fieldType = fields[fieldName].type;
      var fieldValue = astFromValue(_value[fieldName], fieldType);
      if (fieldValue) {
        fieldNodes.push({
          kind: _kinds.OBJECT_FIELD,
          name: { kind: _kinds.NAME, value: fieldName },
          value: fieldValue
        });
      }
    });
    return { kind: _kinds.OBJECT, fields: fieldNodes };
  }

  (0, _invariant2.default)(type instanceof _definition.GraphQLScalarType || type instanceof _definition.GraphQLEnumType, 'Must provide
 Input Type, cannot use: ' + String(type));

  // Since value is an internally represented value, it must be serialized
  // to an externally represented value before converting into an AST.
  var serialized = type.serialize(_value);
  if ((0, _isNullish2.default)(serialized)) {
    return null;
  }

  // Others serialize based on their corresponding JavaScript scalar types.
  if (typeof serialized === 'boolean') {
    return { kind: _kinds.BOOLEAN, value: serialized };
  }

  // JavaScript numbers can be Int or Float values.
  if (typeof serialized === 'number') {
    var stringNum = String(serialized);
    return (/^[0-9]+$/.test(stringNum) ? { kind: _kinds.INT, value: stringNum } : { kind: _kinds.FLOAT, value: stringNum }
    );
  }

  if (typeof serialized === 'string') {
    // Enum types use Enum literals.
    if (type instanceof _definition.GraphQLEnumType) {
      return { kind: _kinds.ENUM, value: serialized };
    }

    // ID types can use Int literals.
    if (type === _scalars.GraphQLID && /^[0-9]+$/.test(serialized)) {
      return { kind: _kinds.INT, value: serialized };
    }

    // Use JSON stringify, which uses the same string encoding as GraphQL,
    // then remove the quotes.
    return {
      kind: _kinds.STRING,
      value: JSON.stringify(serialized).slice(1, -1)
    };
  }

  throw new TypeError('Cannot convert value to AST: ' + String(serialized));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.buildASTSchema"></a>[function <span class="apidocSignatureSpan">graphql.</span>buildASTSchema (ast)](#apidoc.element.graphql.buildASTSchema)
- description and source-code
```javascript
function buildASTSchema(ast) {
  if (!ast || ast.kind !== _kinds.DOCUMENT) {
    throw new Error('Must provide a document ast.');
  }

  var schemaDef = void 0;

  var typeDefs = [];
  var nodeMap = Object.create(null);
  var directiveDefs = [];
  for (var i = 0; i < ast.definitions.length; i++) {
    var d = ast.definitions[i];
    switch (d.kind) {
      case _kinds.SCHEMA_DEFINITION:
        if (schemaDef) {
          throw new Error('Must provide only one schema definition.');
        }
        schemaDef = d;
        break;
      case _kinds.SCALAR_TYPE_DEFINITION:
      case _kinds.OBJECT_TYPE_DEFINITION:
      case _kinds.INTERFACE_TYPE_DEFINITION:
      case _kinds.ENUM_TYPE_DEFINITION:
      case _kinds.UNION_TYPE_DEFINITION:
      case _kinds.INPUT_OBJECT_TYPE_DEFINITION:
        typeDefs.push(d);
        nodeMap[d.name.value] = d;
        break;
      case _kinds.DIRECTIVE_DEFINITION:
        directiveDefs.push(d);
        break;
    }
  }

  var queryTypeName = void 0;
  var mutationTypeName = void 0;
  var subscriptionTypeName = void 0;
  if (schemaDef) {
    schemaDef.operationTypes.forEach(function (operationType) {
      var typeName = operationType.type.name.value;
      if (operationType.operation === 'query') {
        if (queryTypeName) {
          throw new Error('Must provide only one query type in schema.');
        }
        if (!nodeMap[typeName]) {
          throw new Error('Specified query type "' + typeName + '" not found in document.');
        }
        queryTypeName = typeName;
      } else if (operationType.operation === 'mutation') {
        if (mutationTypeName) {
          throw new Error('Must provide only one mutation type in schema.');
        }
        if (!nodeMap[typeName]) {
          throw new Error('Specified mutation type "' + typeName + '" not found in document.');
        }
        mutationTypeName = typeName;
      } else if (operationType.operation === 'subscription') {
        if (subscriptionTypeName) {
          throw new Error('Must provide only one subscription type in schema.');
        }
        if (!nodeMap[typeName]) {
          throw new Error('Specified subscription type "' + typeName + '" not found in document.');
        }
        subscriptionTypeName = typeName;
      }
    });
  } else {
    if (nodeMap.Query) {
      queryTypeName = 'Query';
    }
    if (nodeMap.Mutation) {
      mutationTypeName = 'Mutation';
    }
    if (nodeMap.Subscription) {
      subscriptionTypeName = 'Subscription';
    }
  }

  if (!queryTypeName) {
    throw new Error('Must provide schema definition with query type or a type named Query.');
  }

  var innerTypeMap = {
    String: _scalars.GraphQLString,
    Int: _scalars.GraphQLInt,
    Float: _scalars.GraphQLFloat,
    Boolean: _scalars.GraphQLBoolean,
    ID: _scalars.GraphQLID,
    __Schema: _introspection.__Schema,
    __Directive: _introspection.__Directive,
    __DirectiveLocation: _introspection.__DirectiveLocation,
    __Type: _introspection.__Type,
    __Field: _introspection.__Field,
    __InputValue: _introspection.__InputValue,
    __EnumValue: _introspection.__EnumValue,
    __TypeKind: _introspection.__TypeKind
  };

  var types = typeDefs.map(function (def) {
    return typeDefNamed(def.name.value);
  });

  var directives = directiveDefs.map(getDirective);

  // If specified directives were not explicitly declared, add them.
  if (!directives.some(function (directive) {
    return directive.name === 'skip';
  })) {
    directives.push(_directives.GraphQLSkipDirective);
  }

  if (!directives.some(function (directive) {
    return directive.name === 'include';
  })) {
    directives.push(_directives.GraphQLIncludeDirective);
  }

  if (!directives.some(function (directive) {
    return directive.name === 'deprecated';
  })) {
    directives.push(_directives.GraphQLDeprecatedDirective);
  }

  return new _schema.GraphQLSchema({
    query: getObjectType(nodeMap[queryTypeName]),
    mutation: mutationTypeName ? getObjectType(nodeMap[mutationTypeName]) : null,
    subscription: subscriptionTypeName ? getObjectType(node ...
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.buildClientSchema"></a>[function <span class="apidocSignatureSpan">graphql.</span>buildClientSchema (introspection)](#apidoc.element.graphql.buildClientSchema)
- description and source-code
```javascript
function buildClientSchema(introspection) {

  // Get the schema from the introspection result.
  var schemaIntrospection = introspection.__schema;

  // Converts the list of types into a keyMap based on the type names.
  var typeIntrospectionMap = (0, _keyMap2.default)(schemaIntrospection.types, function (type) {
    return type.name;
  });

  // A cache to use to store the actual GraphQLType definition objects by name.
  // Initialize to the GraphQL built in scalars. All functions below are inline
  // so that this type def cache is within the scope of the closure.
  var typeDefCache = {
    String: _scalars.GraphQLString,
    Int: _scalars.GraphQLInt,
    Float: _scalars.GraphQLFloat,
    Boolean: _scalars.GraphQLBoolean,
    ID: _scalars.GraphQLID,
    __Schema: _introspection.__Schema,
    __Directive: _introspection.__Directive,
    __DirectiveLocation: _introspection.__DirectiveLocation,
    __Type: _introspection.__Type,
    __Field: _introspection.__Field,
    __InputValue: _introspection.__InputValue,
    __EnumValue: _introspection.__EnumValue,
    __TypeKind: _introspection.__TypeKind
  };

  // Given a type reference in introspection, return the GraphQLType instance.
  // preferring cached instances before building new instances.
  function getType(typeRef) {
    if (typeRef.kind === _introspection.TypeKind.LIST) {
      var itemRef = typeRef.ofType;
      if (!itemRef) {
        throw new Error('Decorated type deeper than introspection query.');
      }
      return new _definition.GraphQLList(getType(itemRef));
    }
    if (typeRef.kind === _introspection.TypeKind.NON_NULL) {
      var nullableRef = typeRef.ofType;
      if (!nullableRef) {
        throw new Error('Decorated type deeper than introspection query.');
      }
      var nullableType = getType(nullableRef);
      (0, _invariant2.default)(!(nullableType instanceof _definition.GraphQLNonNull), 'No nesting nonnull.');
      return new _definition.GraphQLNonNull(nullableType);
    }
    return getNamedType(typeRef.name);
  }

  function getNamedType(typeName) {
    if (typeDefCache[typeName]) {
      return typeDefCache[typeName];
    }
    var typeIntrospection = typeIntrospectionMap[typeName];
    if (!typeIntrospection) {
      throw new Error('Invalid or incomplete schema, unknown type: ' + typeName + '. Ensure ' + 'that a full introspection query
 is used in order to build a ' + 'client schema.');
    }
    var typeDef = buildType(typeIntrospection);
    typeDefCache[typeName] = typeDef;
    return typeDef;
  }

  function getInputType(typeRef) {
    var type = getType(typeRef);
    (0, _invariant2.default)((0, _definition.isInputType)(type), 'Introspection must provide input type for arguments.');
    return type;
  }

  function getOutputType(typeRef) {
    var type = getType(typeRef);
    (0, _invariant2.default)((0, _definition.isOutputType)(type), 'Introspection must provide output type for fields.');
    return type;
  }

  function getObjectType(typeRef) {
    var type = getType(typeRef);
    (0, _invariant2.default)(type instanceof _definition.GraphQLObjectType, 'Introspection must provide object type for possibleTypes
.');
    return type;
  }

  function getInterfaceType(typeRef) {
    var type = getType(typeRef);
    (0, _invariant2.default)(type instanceof _definition.GraphQLInterfaceType, 'Introspection must provide interface type for interfaces
.');
    return type;
  }

  // Given a type's introspection result, construct the correct
  // GraphQLType instance.
  function buildType(type) {
    switch (type.kind) {
      case _introspection.TypeKind.SCALAR:
        return buildScalarDef(type);
      case _introspection.TypeKind.OBJECT:
        return buildObjectDef(type);
      case _introspection.TypeKind.INTERFACE:
        return buildInterfaceDef(type);
      case _introspection.TypeKind.UNION:
        return buildUnionDef(type);
      case _introspection.TypeKind.ENUM:
        return buildEnumDef(type);
      case _introspection.TypeKind.INPUT_OBJECT:
        return buildInputObjectDef(type);
      default:
        throw new E ...
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.buildSchema"></a>[function <span class="apidocSignatureSpan">graphql.</span>buildSchema (source)](#apidoc.element.graphql.buildSchema)
- description and source-code
```javascript
function buildSchema(source) {
  return buildASTSchema((0, _parser.parse)(source));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.concatAST"></a>[function <span class="apidocSignatureSpan">graphql.</span>concatAST (asts)](#apidoc.element.graphql.concatAST)
- description and source-code
```javascript
function concatAST(asts) {
  var batchDefinitions = [];
  for (var i = 0; i < asts.length; i++) {
    var definitions = asts[i].definitions;
    for (var j = 0; j < definitions.length; j++) {
      batchDefinitions.push(definitions[j]);
    }
  }
  return {
    kind: 'Document',
    definitions: batchDefinitions
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.defaultFieldResolver"></a>[function <span class="apidocSignatureSpan">graphql.</span>defaultFieldResolver (source, args, context, info)](#apidoc.element.graphql.defaultFieldResolver)
- description and source-code
```javascript
function defaultFieldResolver(source, args, context, info) {
  // ensure source is a value for which property access is acceptable.
  if (typeof source === 'object' || typeof source === 'function') {
    var property = source[info.fieldName];
    if (typeof property === 'function') {
      return source[info.fieldName](args, context, info);
    }
    return property;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.doTypesOverlap"></a>[function <span class="apidocSignatureSpan">graphql.</span>doTypesOverlap (schema, typeA, typeB)](#apidoc.element.graphql.doTypesOverlap)
- description and source-code
```javascript
function doTypesOverlap(schema, typeA, typeB) {
  // So flow is aware this is constant
  var _typeB = typeB;

  // Equivalent types overlap
  if (typeA === _typeB) {
    return true;
  }

  if (typeA instanceof _definition.GraphQLInterfaceType || typeA instanceof _definition.GraphQLUnionType) {
    if (_typeB instanceof _definition.GraphQLInterfaceType || _typeB instanceof _definition.GraphQLUnionType) {
      // If both types are abstract, then determine if there is any intersection
      // between possible concrete types of each.
      return schema.getPossibleTypes(typeA).some(function (type) {
        return schema.isPossibleType(_typeB, type);
      });
    }
    // Determine if the latter type is a possible concrete type of the former.
    return schema.isPossibleType(typeA, _typeB);
  }

  if (_typeB instanceof _definition.GraphQLInterfaceType || _typeB instanceof _definition.GraphQLUnionType) {
    // Determine if the former type is a possible concrete type of the latter.
    return schema.isPossibleType(_typeB, typeA);
  }

  // Otherwise the types do not overlap.
  return false;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.execute"></a>[function <span class="apidocSignatureSpan">graphql.</span>execute (schema, document, rootValue, contextValue, variableValues, operationName)](#apidoc.element.graphql.execute)
- description and source-code
```javascript
function execute(schema, document, rootValue, contextValue, variableValues, operationName) {
  (0, _invariant2.default)(schema, 'Must provide schema');
  (0, _invariant2.default)(document, 'Must provide document');
  (0, _invariant2.default)(schema instanceof _schema.GraphQLSchema, 'Schema must be an instance of GraphQLSchema. Also ensure that
 there are ' + 'not multiple versions of GraphQL installed in your node_modules directory.');

  // Variables, if provided, must be an object.
  (0, _invariant2.default)(!variableValues || typeof variableValues === 'object', 'Variables must be provided as an Object where
 each property is a ' + 'variable value. Perhaps look to see if an unparsed JSON string ' + 'was provided.');

  // If a valid context cannot be created due to incorrect arguments,
  // this will throw an error.
  var context = buildExecutionContext(schema, document, rootValue, contextValue, variableValues, operationName);

  // Return a Promise that will eventually resolve to the data described by
  // The "Response" section of the GraphQL specification.
  //
  // If errors are encountered while executing a GraphQL field, only that
  // field and its descendants will be omitted, and sibling fields will still
  // be executed. An execution which encounters errors will still result in a
  // resolved Promise.
  return new Promise(function (resolve) {
    resolve(executeOperation(context, context.operation, rootValue));
  }).then(undefined, function (error) {
    // Errors from sub-fields of a NonNull type may propagate to the top level,
    // at which point we still log the error and null the parent field, which
    // in this case is the entire response.
    context.errors.push(error);
    return null;
  }).then(function (data) {
    if (!context.errors.length) {
      return { data: data };
    }
    return { data: data, errors: context.errors };
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.extendSchema"></a>[function <span class="apidocSignatureSpan">graphql.</span>extendSchema (schema, documentAST)](#apidoc.element.graphql.extendSchema)
- description and source-code
```javascript
function extendSchema(schema, documentAST) {
  (0, _invariant2.default)(schema instanceof _schema.GraphQLSchema, 'Must provide valid GraphQLSchema');

  (0, _invariant2.default)(documentAST && documentAST.kind === _kinds.DOCUMENT, 'Must provide valid Document AST');

  // Collect the type definitions and extensions found in the document.
  var typeDefinitionMap = {};
  var typeExtensionsMap = {};

  // New directives and types are separate because a directives and types can
  // have the same name. For example, a type named "skip".
  var directiveDefinitions = [];

  for (var i = 0; i < documentAST.definitions.length; i++) {
    var def = documentAST.definitions[i];
    switch (def.kind) {
      case _kinds.OBJECT_TYPE_DEFINITION:
      case _kinds.INTERFACE_TYPE_DEFINITION:
      case _kinds.ENUM_TYPE_DEFINITION:
      case _kinds.UNION_TYPE_DEFINITION:
      case _kinds.SCALAR_TYPE_DEFINITION:
      case _kinds.INPUT_OBJECT_TYPE_DEFINITION:
        // Sanity check that none of the defined types conflict with the
        // schema's existing types.
        var typeName = def.name.value;
        if (schema.getType(typeName)) {
          throw new _GraphQLError.GraphQLError('Type "' + typeName + '" already exists in the schema. It cannot also ' + 'be defined
 in this type definition.', [def]);
        }
        typeDefinitionMap[typeName] = def;
        break;
      case _kinds.TYPE_EXTENSION_DEFINITION:
        // Sanity check that this type extension exists within the
        // schema's existing types.
        var extendedTypeName = def.definition.name.value;
        var existingType = schema.getType(extendedTypeName);
        if (!existingType) {
          throw new _GraphQLError.GraphQLError('Cannot extend type "' + extendedTypeName + '" because it does not ' + 'exist in
the existing schema.', [def.definition]);
        }
        if (!(existingType instanceof _definition.GraphQLObjectType)) {
          throw new _GraphQLError.GraphQLError('Cannot extend non-object type "' + extendedTypeName + '".', [def.definition]);
        }
        var extensions = typeExtensionsMap[extendedTypeName];
        if (extensions) {
          extensions.push(def);
        } else {
          extensions = [def];
        }
        typeExtensionsMap[extendedTypeName] = extensions;
        break;
      case _kinds.DIRECTIVE_DEFINITION:
        var directiveName = def.name.value;
        var existingDirective = schema.getDirective(directiveName);
        if (existingDirective) {
          throw new _GraphQLError.GraphQLError('Directive "' + directiveName + '" already exists in the schema. It ' + 'cannot be
 redefined.', [def]);
        }
        directiveDefinitions.push(def);
        break;
    }
  }

  // If this document contains no new types, extensions, or directives then
  // return the same unmodified GraphQLSchema instance.
  if (Object.keys(typeExtensionsMap).length === 0 && Object.keys(typeDefinitionMap).length === 0 && directiveDefinitions.length ===
0) {
    return schema;
  }

  // A cache to use to store the actual GraphQLType definition objects by name.
  // Initialize to the GraphQL built in scalars and introspection types. All
  // functions below are inline so that this type def cache is within the scope
  // of the closure.
  var typeDefCache = {
    String: _scalars.GraphQLString,
    Int: _scalars.GraphQLInt,
    Float: _scalars.GraphQLFloat,
    Boolean: _scalars.GraphQLBoolean,
    ID: _scalars.GraphQLID,
    __Schema: _introspection.__Schema,
    __Directive: _introspection.__Directive,
    __DirectiveLocation: _introspection.__DirectiveLocation,
    __Type: _introspection.__Type,
    __Field: _introspection.__Field,
    __InputValue: _introspection.__InputValue,
    __EnumValue: _introspection.__EnumValue,
    __TypeKind: _introspection.__TypeKind
  };

  // Get the root Query, Mutation, and Subscription object types.
  var queryType = getTypeFromDef(schema.getQueryType());

  var existingMutationType = schema.getMutationType();
  var mutationType = existingMutationType ? getTypeFromDef(existingMutationType) : null; ...
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.findBreakingChanges"></a>[function <span class="apidocSignatureSpan">graphql.</span>findBreakingChanges (oldSchema, newSchema)](#apidoc.element.graphql.findBreakingChanges)
- description and source-code
```javascript
function findBreakingChanges(oldSchema, newSchema) {
  return [].concat(findRemovedTypes(oldSchema, newSchema), findTypesThatChangedKind(oldSchema, newSchema), findFieldsThatChangedType
(oldSchema, newSchema), findTypesRemovedFromUnions(oldSchema, newSchema), findValuesRemovedFromEnums(oldSchema, newSchema), findArgChanges
(oldSchema, newSchema).breakingChanges);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.findDeprecatedUsages"></a>[function <span class="apidocSignatureSpan">graphql.</span>findDeprecatedUsages (schema, ast)](#apidoc.element.graphql.findDeprecatedUsages)
- description and source-code
```javascript
function findDeprecatedUsages(schema, ast) {
  var errors = [];
  var typeInfo = new _TypeInfo.TypeInfo(schema);

  (0, _visitor.visit)(ast, (0, _visitor.visitWithTypeInfo)(typeInfo, {
    Field: function Field(node) {
      var fieldDef = typeInfo.getFieldDef();
      if (fieldDef && fieldDef.isDeprecated) {
        var parentType = typeInfo.getParentType();
        if (parentType) {
          var reason = fieldDef.deprecationReason;
          errors.push(new _GraphQLError.GraphQLError('The field ' + parentType.name + '.' + fieldDef.name + ' is deprecated.' + (
reason ? ' ' + reason : ''), [node]));
        }
      }
    },
    EnumValue: function EnumValue(node) {
      var enumVal = typeInfo.getEnumValue();
      if (enumVal && enumVal.isDeprecated) {
        var type = (0, _definition.getNamedType)(typeInfo.getInputType());
        if (type) {
          var reason = enumVal.deprecationReason;
          errors.push(new _GraphQLError.GraphQLError('The enum value ' + type.name + '.' + enumVal.name + ' is deprecated.' + (reason
 ? ' ' + reason : ''), [node]));
        }
      }
    }
  }));

  return errors;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.formatError"></a>[function <span class="apidocSignatureSpan">graphql.</span>formatError (error)](#apidoc.element.graphql.formatError)
- description and source-code
```javascript
function formatError(error) {
  (0, _invariant2.default)(error, 'Received null or undefined error.');
  return {
    message: error.message,
    locations: error.locations,
    path: error.path
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.getLocation"></a>[function <span class="apidocSignatureSpan">graphql.</span>getLocation (source, position)](#apidoc.element.graphql.getLocation)
- description and source-code
```javascript
function getLocation(source, position) {
  var lineRegexp = /\r\n|[\n\r]/g;
  var line = 1;
  var column = position + 1;
  var match = void 0;
  while ((match = lineRegexp.exec(source.body)) && match.index < position) {
    line += 1;
    column = position + 1 - (match.index + match[0].length);
  }
  return { line: line, column: column };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.getNamedType"></a>[function <span class="apidocSignatureSpan">graphql.</span>getNamedType (type)](#apidoc.element.graphql.getNamedType)
- description and source-code
```javascript
function getNamedType(type) {
  var unmodifiedType = type;
  while (unmodifiedType instanceof GraphQLList || unmodifiedType instanceof GraphQLNonNull) {
    unmodifiedType = unmodifiedType.ofType;
  }
  return unmodifiedType;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.getNullableType"></a>[function <span class="apidocSignatureSpan">graphql.</span>getNullableType (type)](#apidoc.element.graphql.getNullableType)
- description and source-code
```javascript
function getNullableType(type) {
  return type instanceof GraphQLNonNull ? type.ofType : type;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.getOperationAST"></a>[function <span class="apidocSignatureSpan">graphql.</span>getOperationAST (documentAST, operationName)](#apidoc.element.graphql.getOperationAST)
- description and source-code
```javascript
function getOperationAST(documentAST, operationName) {
  var operation = null;
  for (var i = 0; i < documentAST.definitions.length; i++) {
    var definition = documentAST.definitions[i];
    if (definition.kind === _kinds.OPERATION_DEFINITION) {
      if (!operationName) {
        // If no operation name was provided, only return an Operation if there
        // is one defined in the document. Upon encountering the second, return
        // null.
        if (operation) {
          return null;
        }
        operation = definition;
      } else if (definition.name && definition.name.value === operationName) {
        return definition;
      }
    }
  }
  return operation;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.isAbstractType"></a>[function <span class="apidocSignatureSpan">graphql.</span>isAbstractType (type)](#apidoc.element.graphql.isAbstractType)
- description and source-code
```javascript
function isAbstractType(type) {
  return type instanceof GraphQLInterfaceType || type instanceof GraphQLUnionType;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.isCompositeType"></a>[function <span class="apidocSignatureSpan">graphql.</span>isCompositeType (type)](#apidoc.element.graphql.isCompositeType)
- description and source-code
```javascript
function isCompositeType(type) {
  return type instanceof GraphQLObjectType || type instanceof GraphQLInterfaceType || type instanceof GraphQLUnionType;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.isEqualType"></a>[function <span class="apidocSignatureSpan">graphql.</span>isEqualType (typeA, typeB)](#apidoc.element.graphql.isEqualType)
- description and source-code
```javascript
function isEqualType(typeA, typeB) {
  // Equivalent types are equal.
  if (typeA === typeB) {
    return true;
  }

  // If either type is non-null, the other must also be non-null.
  if (typeA instanceof _definition.GraphQLNonNull && typeB instanceof _definition.GraphQLNonNull) {
    return isEqualType(typeA.ofType, typeB.ofType);
  }

  // If either type is a list, the other must also be a list.
  if (typeA instanceof _definition.GraphQLList && typeB instanceof _definition.GraphQLList) {
    return isEqualType(typeA.ofType, typeB.ofType);
  }

  // Otherwise the types are not equal.
  return false;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.isInputType"></a>[function <span class="apidocSignatureSpan">graphql.</span>isInputType (type)](#apidoc.element.graphql.isInputType)
- description and source-code
```javascript
function isInputType(type) {
  var namedType = getNamedType(type);
  return namedType instanceof GraphQLScalarType || namedType instanceof GraphQLEnumType || namedType instanceof GraphQLInputObjectType
;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.isLeafType"></a>[function <span class="apidocSignatureSpan">graphql.</span>isLeafType (type)](#apidoc.element.graphql.isLeafType)
- description and source-code
```javascript
function isLeafType(type) {
  return type instanceof GraphQLScalarType || type instanceof GraphQLEnumType;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.isNamedType"></a>[function <span class="apidocSignatureSpan">graphql.</span>isNamedType (type)](#apidoc.element.graphql.isNamedType)
- description and source-code
```javascript
function isNamedType(type) {
  return type instanceof GraphQLScalarType || type instanceof GraphQLObjectType || type instanceof GraphQLInterfaceType || type
instanceof GraphQLUnionType || type instanceof GraphQLEnumType || type instanceof GraphQLInputObjectType;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.isOutputType"></a>[function <span class="apidocSignatureSpan">graphql.</span>isOutputType (type)](#apidoc.element.graphql.isOutputType)
- description and source-code
```javascript
function isOutputType(type) {
  var namedType = getNamedType(type);
  return namedType instanceof GraphQLScalarType || namedType instanceof GraphQLObjectType || namedType instanceof GraphQLInterfaceType
 || namedType instanceof GraphQLUnionType || namedType instanceof GraphQLEnumType;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.isType"></a>[function <span class="apidocSignatureSpan">graphql.</span>isType (type)](#apidoc.element.graphql.isType)
- description and source-code
```javascript
function isType(type) {
  return type instanceof GraphQLScalarType || type instanceof GraphQLObjectType || type instanceof GraphQLInterfaceType || type
instanceof GraphQLUnionType || type instanceof GraphQLEnumType || type instanceof GraphQLInputObjectType || type instanceof GraphQLList
 || type instanceof GraphQLNonNull;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.isTypeSubTypeOf"></a>[function <span class="apidocSignatureSpan">graphql.</span>isTypeSubTypeOf (schema, maybeSubType, superType)](#apidoc.element.graphql.isTypeSubTypeOf)
- description and source-code
```javascript
function isTypeSubTypeOf(schema, maybeSubType, superType) {
  // Equivalent type is a valid subtype
  if (maybeSubType === superType) {
    return true;
  }

  // If superType is non-null, maybeSubType must also be non-null.
  if (superType instanceof _definition.GraphQLNonNull) {
    if (maybeSubType instanceof _definition.GraphQLNonNull) {
      return isTypeSubTypeOf(schema, maybeSubType.ofType, superType.ofType);
    }
    return false;
  } else if (maybeSubType instanceof _definition.GraphQLNonNull) {
    // If superType is nullable, maybeSubType may be non-null or nullable.
    return isTypeSubTypeOf(schema, maybeSubType.ofType, superType);
  }

  // If superType type is a list, maybeSubType type must also be a list.
  if (superType instanceof _definition.GraphQLList) {
    if (maybeSubType instanceof _definition.GraphQLList) {
      return isTypeSubTypeOf(schema, maybeSubType.ofType, superType.ofType);
    }
    return false;
  } else if (maybeSubType instanceof _definition.GraphQLList) {
    // If superType is not a list, maybeSubType must also be not a list.
    return false;
  }

  // If superType type is an abstract type, maybeSubType type may be a currently
  // possible object type.
  if ((0, _definition.isAbstractType)(superType) && maybeSubType instanceof _definition.GraphQLObjectType && schema.isPossibleType
(superType, maybeSubType)) {
    return true;
  }

  // Otherwise, the child type is not a valid subtype of the parent type.
  return false;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.isValidJSValue"></a>[function <span class="apidocSignatureSpan">graphql.</span>isValidJSValue (value, type)](#apidoc.element.graphql.isValidJSValue)
- description and source-code
```javascript
function isValidJSValue(value, type) {
  // A value must be provided if the type is non-null.
  if (type instanceof _definition.GraphQLNonNull) {
    if ((0, _isNullish2.default)(value)) {
      return ['Expected "' + String(type) + '", found null.'];
    }
    return isValidJSValue(value, type.ofType);
  }

  if ((0, _isNullish2.default)(value)) {
    return [];
  }

  // Lists accept a non-list value as a list of one.
  if (type instanceof _definition.GraphQLList) {
    var itemType = type.ofType;
    if ((0, _iterall.isCollection)(value)) {
      var errors = [];
      (0, _iterall.forEach)(value, function (item, index) {
        errors.push.apply(errors, isValidJSValue(item, itemType).map(function (error) {
          return 'In element #' + index + ': ' + error;
        }));
      });
      return errors;
    }
    return isValidJSValue(value, itemType);
  }

  // Input objects check each defined field.
  if (type instanceof _definition.GraphQLInputObjectType) {
    if (typeof value !== 'object' || value === null) {
      return ['Expected "' + type.name + '", found not an object.'];
    }
    var fields = type.getFields();

    var _errors = [];

    // Ensure every provided field is defined.
    Object.keys(value).forEach(function (providedField) {
      if (!fields[providedField]) {
        _errors.push('In field "' + providedField + '": Unknown field.');
      }
    });

    // Ensure every defined field is valid.
    Object.keys(fields).forEach(function (fieldName) {
      var newErrors = isValidJSValue(value[fieldName], fields[fieldName].type);
      _errors.push.apply(_errors, newErrors.map(function (error) {
        return 'In field "' + fieldName + '": ' + error;
      }));
    });

    return _errors;
  }

  (0, _invariant2.default)(type instanceof _definition.GraphQLScalarType || type instanceof _definition.GraphQLEnumType, 'Must be
 input type');

  // Scalar/Enum input checks to ensure the type can parse the value to
  // a non-null value.
  try {
    var parseResult = type.parseValue(value);
    if ((0, _isNullish2.default)(parseResult)) {
      return ['Expected type "' + type.name + '", found ' + JSON.stringify(value) + '.'];
    }
  } catch (error) {
    return ['Expected type "' + type.name + '", found ' + JSON.stringify(value) + ': ' + error.message];
  }

  return [];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.isValidLiteralValue"></a>[function <span class="apidocSignatureSpan">graphql.</span>isValidLiteralValue (type, valueNode)](#apidoc.element.graphql.isValidLiteralValue)
- description and source-code
```javascript
function isValidLiteralValue(type, valueNode) {
  // A value must be provided if the type is non-null.
  if (type instanceof _definition.GraphQLNonNull) {
    if (!valueNode || valueNode.kind === _kinds.NULL) {
      return ['Expected "' + String(type) + '", found null.'];
    }
    return isValidLiteralValue(type.ofType, valueNode);
  }

  if (!valueNode || valueNode.kind === _kinds.NULL) {
    return [];
  }

  // This function only tests literals, and assumes variables will provide
  // values of the correct type.
  if (valueNode.kind === _kinds.VARIABLE) {
    return [];
  }

  // Lists accept a non-list value as a list of one.
  if (type instanceof _definition.GraphQLList) {
    var itemType = type.ofType;
    if (valueNode.kind === _kinds.LIST) {
      return valueNode.values.reduce(function (acc, item, index) {
        var errors = isValidLiteralValue(itemType, item);
        return acc.concat(errors.map(function (error) {
          return 'In element #' + index + ': ' + error;
        }));
      }, []);
    }
    return isValidLiteralValue(itemType, valueNode);
  }

  // Input objects check each defined field and look for undefined fields.
  if (type instanceof _definition.GraphQLInputObjectType) {
    if (valueNode.kind !== _kinds.OBJECT) {
      return ['Expected "' + type.name + '", found not an object.'];
    }
    var fields = type.getFields();

    var errors = [];

    // Ensure every provided field is defined.
    var fieldNodes = valueNode.fields;
    fieldNodes.forEach(function (providedFieldNode) {
      if (!fields[providedFieldNode.name.value]) {
        errors.push('In field "' + providedFieldNode.name.value + '": Unknown field.');
      }
    });

    // Ensure every defined field is valid.
    var fieldNodeMap = (0, _keyMap2.default)(fieldNodes, function (fieldNode) {
      return fieldNode.name.value;
    });
    Object.keys(fields).forEach(function (fieldName) {
      var result = isValidLiteralValue(fields[fieldName].type, fieldNodeMap[fieldName] && fieldNodeMap[fieldName].value);
      errors.push.apply(errors, result.map(function (error) {
        return 'In field "' + fieldName + '": ' + error;
      }));
    });

    return errors;
  }

  (0, _invariant2.default)(type instanceof _definition.GraphQLScalarType || type instanceof _definition.GraphQLEnumType, 'Must be
 input type');

  // Scalar/Enum input checks to ensure the type can parse the value to
  // a non-null value.
  var parseResult = type.parseLiteral(valueNode);
  if ((0, _isNullish2.default)(parseResult)) {
    return ['Expected type "' + type.name + '", found ' + (0, _printer.print)(valueNode) + '.'];
  }

  return [];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.parse"></a>[function <span class="apidocSignatureSpan">graphql.</span>parse (source, options)](#apidoc.element.graphql.parse)
- description and source-code
```javascript
function parse(source, options) {
  var sourceObj = typeof source === 'string' ? new _source.Source(source) : source;
  var lexer = (0, _lexer.createLexer)(sourceObj, options || {});
  return parseDocument(lexer);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.parseType"></a>[function <span class="apidocSignatureSpan">graphql.</span>parseType (source, options)](#apidoc.element.graphql.parseType)
- description and source-code
```javascript
function parseType(source, options) {
  var sourceObj = typeof source === 'string' ? new _source.Source(source) : source;
  var lexer = (0, _lexer.createLexer)(sourceObj, options || {});
  expect(lexer, _lexer.TokenKind.SOF);
  var type = parseTypeReference(lexer);
  expect(lexer, _lexer.TokenKind.EOF);
  return type;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.parseValue"></a>[function <span class="apidocSignatureSpan">graphql.</span>parseValue (source, options)](#apidoc.element.graphql.parseValue)
- description and source-code
```javascript
function parseValue(source, options) {
  var sourceObj = typeof source === 'string' ? new _source.Source(source) : source;
  var lexer = (0, _lexer.createLexer)(sourceObj, options || {});
  expect(lexer, _lexer.TokenKind.SOF);
  var value = parseValueLiteral(lexer, false);
  expect(lexer, _lexer.TokenKind.EOF);
  return value;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.print"></a>[function <span class="apidocSignatureSpan">graphql.</span>print (ast)](#apidoc.element.graphql.print)
- description and source-code
```javascript
function print(ast) {
  return (0, _visitor.visit)(ast, { leave: printDocASTReducer });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.printSchema"></a>[function <span class="apidocSignatureSpan">graphql.</span>printSchema (schema)](#apidoc.element.graphql.printSchema)
- description and source-code
```javascript
function printSchema(schema) {
  return printFilteredSchema(schema, function (n) {
    return !isSpecDirective(n);
  }, isDefinedType);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.printType"></a>[function <span class="apidocSignatureSpan">graphql.</span>printType (type)](#apidoc.element.graphql.printType)
- description and source-code
```javascript
function printType(type) {
  if (type instanceof _definition.GraphQLScalarType) {
    return printScalar(type);
  } else if (type instanceof _definition.GraphQLObjectType) {
    return printObject(type);
  } else if (type instanceof _definition.GraphQLInterfaceType) {
    return printInterface(type);
  } else if (type instanceof _definition.GraphQLUnionType) {
    return printUnion(type);
  } else if (type instanceof _definition.GraphQLEnumType) {
    return printEnum(type);
  }
  (0, _invariant2.default)(type instanceof _definition.GraphQLInputObjectType);
  return printInputObject(type);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.responsePathAsArray"></a>[function <span class="apidocSignatureSpan">graphql.</span>responsePathAsArray (path)](#apidoc.element.graphql.responsePathAsArray)
- description and source-code
```javascript
function responsePathAsArray(path) {
  var flattened = [];
  var curr = path;
  while (curr) {
    flattened.push(curr.key);
    curr = curr.prev;
  }
  return flattened.reverse();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.separateOperations"></a>[function <span class="apidocSignatureSpan">graphql.</span>separateOperations (documentAST)](#apidoc.element.graphql.separateOperations)
- description and source-code
```javascript
function separateOperations(documentAST) {

  var operations = [];
  var fragments = Object.create(null);
  var positions = new Map();
  var depGraph = Object.create(null);
  var fromName = void 0;
  var idx = 0;

  // Populate metadata and build a dependency graph.
  (0, _visitor.visit)(documentAST, {
    OperationDefinition: function OperationDefinition(node) {
      fromName = opName(node);
      operations.push(node);
      positions.set(node, idx++);
    },
    FragmentDefinition: function FragmentDefinition(node) {
      fromName = node.name.value;
      fragments[fromName] = node;
      positions.set(node, idx++);
    },
    FragmentSpread: function FragmentSpread(node) {
      var toName = node.name.value;
      (depGraph[fromName] || (depGraph[fromName] = Object.create(null)))[toName] = true;
    }
  });

  // For each operation, produce a new synthesized AST which includes only what
  // is necessary for completing that operation.
  var separatedDocumentASTs = Object.create(null);
  operations.forEach(function (operation) {
    var operationName = opName(operation);
    var dependencies = Object.create(null);
    collectTransitiveDependencies(dependencies, depGraph, operationName);

    // The list of definition nodes to be included for this operation, sorted
    // to retain the same order as the original document.
    var definitions = [operation];
    Object.keys(dependencies).forEach(function (name) {
      definitions.push(fragments[name]);
    });
    definitions.sort(function (n1, n2) {
      return (positions.get(n1) || 0) - (positions.get(n2) || 0);
    });

    separatedDocumentASTs[operationName] = {
      kind: 'Document',
      definitions: definitions
    };
  });

  return separatedDocumentASTs;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.typeFromAST"></a>[function <span class="apidocSignatureSpan">graphql.</span>typeFromAST (schema, typeNode)](#apidoc.element.graphql.typeFromAST)
- description and source-code
```javascript
function typeFromAST(schema, typeNode) {
  var innerType = void 0;
  if (typeNode.kind === _kinds.LIST_TYPE) {
    innerType = typeFromAST(schema, typeNode.type);
    return innerType && new _definition.GraphQLList(innerType);
  }
  if (typeNode.kind === _kinds.NON_NULL_TYPE) {
    innerType = typeFromAST(schema, typeNode.type);
    return innerType && new _definition.GraphQLNonNull(innerType);
  }
  (0, _invariant2.default)(typeNode.kind === _kinds.NAMED_TYPE, 'Must be a named type.');
  return schema.getType(typeNode.name.value);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.validate"></a>[function <span class="apidocSignatureSpan">graphql.</span>validate (schema, ast, rules)](#apidoc.element.graphql.validate)
- description and source-code
```javascript
function validate(schema, ast, rules) {
  (0, _invariant2.default)(schema, 'Must provide schema');
  (0, _invariant2.default)(ast, 'Must provide document');
  (0, _invariant2.default)(schema instanceof _schema.GraphQLSchema, 'Schema must be an instance of GraphQLSchema. Also ensure that
 there are ' + 'not multiple versions of GraphQL installed in your node_modules directory.');
  var typeInfo = new _TypeInfo.TypeInfo(schema);
  return visitUsingRules(schema, typeInfo, ast, rules || _specifiedRules.specifiedRules);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.valueFromAST"></a>[function <span class="apidocSignatureSpan">graphql.</span>valueFromAST (valueNode, type, variables)](#apidoc.element.graphql.valueFromAST)
- description and source-code
```javascript
function valueFromAST(valueNode, type, variables) {
  if (!valueNode) {
    // When there is no node, then there is also no value.
    // Importantly, this is different from returning the value null.
    return;
  }

  if (type instanceof _definition.GraphQLNonNull) {
    if (valueNode.kind === Kind.NULL) {
      return; // Invalid: intentionally return no value.
    }
    return valueFromAST(valueNode, type.ofType, variables);
  }

  if (valueNode.kind === Kind.NULL) {
    // This is explicitly returning the value null.
    return null;
  }

  if (valueNode.kind === Kind.VARIABLE) {
    var variableName = valueNode.name.value;
    if (!variables || (0, _isInvalid2.default)(variables[variableName])) {
      // No valid return value.
      return;
    }
    // Note: we're not doing any checking that this variable is correct. We're
    // assuming that this query has been validated and the variable usage here
    // is of the correct type.
    return variables[variableName];
  }

  if (type instanceof _definition.GraphQLList) {
    var itemType = type.ofType;
    if (valueNode.kind === Kind.LIST) {
      var coercedValues = [];
      var itemNodes = valueNode.values;
      for (var i = 0; i < itemNodes.length; i++) {
        if (isMissingVariable(itemNodes[i], variables)) {
          // If an array contains a missing variable, it is either coerced to
          // null or if the item type is non-null, it considered invalid.
          if (itemType instanceof _definition.GraphQLNonNull) {
            return; // Invalid: intentionally return no value.
          }
          coercedValues.push(null);
        } else {
          var itemValue = valueFromAST(itemNodes[i], itemType, variables);
          if ((0, _isInvalid2.default)(itemValue)) {
            return; // Invalid: intentionally return no value.
          }
          coercedValues.push(itemValue);
        }
      }
      return coercedValues;
    }
    var coercedValue = valueFromAST(valueNode, itemType, variables);
    if ((0, _isInvalid2.default)(coercedValue)) {
      return; // Invalid: intentionally return no value.
    }
    return [coercedValue];
  }

  if (type instanceof _definition.GraphQLInputObjectType) {
    if (valueNode.kind !== Kind.OBJECT) {
      return; // Invalid: intentionally return no value.
    }
    var coercedObj = Object.create(null);
    var fields = type.getFields();
    var fieldNodes = (0, _keyMap2.default)(valueNode.fields, function (field) {
      return field.name.value;
    });
    var fieldNames = Object.keys(fields);
    for (var _i = 0; _i < fieldNames.length; _i++) {
      var fieldName = fieldNames[_i];
      var field = fields[fieldName];
      var fieldNode = fieldNodes[fieldName];
      if (!fieldNode || isMissingVariable(fieldNode.value, variables)) {
        if (!(0, _isInvalid2.default)(field.defaultValue)) {
          coercedObj[fieldName] = field.defaultValue;
        } else if (field.type instanceof _definition.GraphQLNonNull) {
          return; // Invalid: intentionally return no value.
        }
        continue;
      }
      var fieldValue = valueFromAST(fieldNode.value, field.type, variables);
      if ((0, _isInvalid2.default)(fieldValue)) {
        return; // Invalid: intentionally return no value.
      }
      coercedObj[fieldName] = fieldValue;
    }
    return coercedObj;
  }

  (0, _invariant2.default)(type instanceof _definition.GraphQLScalarType || type instanceof _definition.GraphQLEnumType, 'Must be
 input type');

  var parsed = type.parseLiteral(valueNode);
  if ((0, _isNullish2.default)(parsed)) {
    // null or invalid values represent a failure to parse correctly,
    // in which case no value is returned.
    return;
  }

  return parsed;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.visit"></a>[function <span class="apidocSignatureSpan">graphql.</span>visit (root, visitor, keyMap)](#apidoc.element.graphql.visit)
- description and source-code
```javascript
function visit(root, visitor, keyMap) {
  var visitorKeys = keyMap || QueryDocumentKeys;

  var stack = void 0;
  var inArray = Array.isArray(root);
  var keys = [root];
  var index = -1;
  var edits = [];
  var parent = void 0;
  var path = [];
  var ancestors = [];
  var newRoot = root;

  do {
    index++;
    var isLeaving = index === keys.length;
    var key = void 0;
    var node = void 0;
    var isEdited = isLeaving && edits.length !== 0;
    if (isLeaving) {
      key = ancestors.length === 0 ? undefined : path.pop();
      node = parent;
      parent = ancestors.pop();
      if (isEdited) {
        if (inArray) {
          node = node.slice();
        } else {
          var clone = {};
          for (var k in node) {
            if (node.hasOwnProperty(k)) {
              clone[k] = node[k];
            }
          }
          node = clone;
        }
        var editOffset = 0;
        for (var ii = 0; ii < edits.length; ii++) {
          var editKey = edits[ii][0];
          var editValue = edits[ii][1];
          if (inArray) {
            editKey -= editOffset;
          }
          if (inArray && editValue === null) {
            node.splice(editKey, 1);
            editOffset++;
          } else {
            node[editKey] = editValue;
          }
        }
      }
      index = stack.index;
      keys = stack.keys;
      edits = stack.edits;
      inArray = stack.inArray;
      stack = stack.prev;
    } else {
      key = parent ? inArray ? index : keys[index] : undefined;
      node = parent ? parent[key] : newRoot;
      if (node === null || node === undefined) {
        continue;
      }
      if (parent) {
        path.push(key);
      }
    }

    var result = void 0;
    if (!Array.isArray(node)) {
      if (!isNode(node)) {
        throw new Error('Invalid AST Node: ' + JSON.stringify(node));
      }
      var visitFn = getVisitFn(visitor, node.kind, isLeaving);
      if (visitFn) {
        result = visitFn.call(visitor, node, key, parent, path, ancestors);

        if (result === BREAK) {
          break;
        }

        if (result === false) {
          if (!isLeaving) {
            path.pop();
            continue;
          }
        } else if (result !== undefined) {
          edits.push([key, result]);
          if (!isLeaving) {
            if (isNode(result)) {
              node = result;
            } else {
              path.pop();
              continue;
            }
          }
        }
      }
    }

    if (result === undefined && isEdited) {
      edits.push([key, node]);
    }

    if (!isLeaving) {
      stack = { inArray: inArray, index: index, keys: keys, edits: edits, prev: stack };
      inArray = Array.isArray(node);
      keys = inArray ? node : visitorKeys[node.kind] || [];
      index = -1;
      edits = [];
      if (parent) {
        ancestors.push(parent);
      }
      parent = node;
    }
  } while (stack !== undefined);

  if (edits.length !== 0) {
    newRoot = edits[edits.length - 1][1];
  }

  return newRoot;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.visitInParallel"></a>[function <span class="apidocSignatureSpan">graphql.</span>visitInParallel (visitors)](#apidoc.element.graphql.visitInParallel)
- description and source-code
```javascript
function visitInParallel(visitors) {
  var skipping = new Array(visitors.length);

  return {
    enter: function enter(node) {
      for (var i = 0; i < visitors.length; i++) {
        if (!skipping[i]) {
          var fn = getVisitFn(visitors[i], node.kind, /* isLeaving */false);
          if (fn) {
            var result = fn.apply(visitors[i], arguments);
            if (result === false) {
              skipping[i] = node;
            } else if (result === BREAK) {
              skipping[i] = BREAK;
            } else if (result !== undefined) {
              return result;
            }
          }
        }
      }
    },
    leave: function leave(node) {
      for (var i = 0; i < visitors.length; i++) {
        if (!skipping[i]) {
          var fn = getVisitFn(visitors[i], node.kind, /* isLeaving */true);
          if (fn) {
            var result = fn.apply(visitors[i], arguments);
            if (result === BREAK) {
              skipping[i] = BREAK;
            } else if (result !== undefined && result !== false) {
              return result;
            }
          }
        } else if (skipping[i] === node) {
          skipping[i] = null;
        }
      }
    }
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.visitWithTypeInfo"></a>[function <span class="apidocSignatureSpan">graphql.</span>visitWithTypeInfo (typeInfo, visitor)](#apidoc.element.graphql.visitWithTypeInfo)
- description and source-code
```javascript
function visitWithTypeInfo(typeInfo, visitor) {
  return {
    enter: function enter(node) {
      typeInfo.enter(node);
      var fn = getVisitFn(visitor, node.kind, /* isLeaving */false);
      if (fn) {
        var result = fn.apply(visitor, arguments);
        if (result !== undefined) {
          typeInfo.leave(node);
          if (isNode(result)) {
            typeInfo.enter(result);
          }
        }
        return result;
      }
    },
    leave: function leave(node) {
      var fn = getVisitFn(visitor, node.kind, /* isLeaving */true);
      var result = void 0;
      if (fn) {
        result = fn.apply(visitor, arguments);
      }
      typeInfo.leave(node);
      return result;
    }
  };
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.graphql.GraphQLEnumType"></a>[module graphql.GraphQLEnumType](#apidoc.module.graphql.GraphQLEnumType)

#### <a name="apidoc.element.graphql.GraphQLEnumType.GraphQLEnumType"></a>[function <span class="apidocSignatureSpan">graphql.</span>GraphQLEnumType (config)](#apidoc.element.graphql.GraphQLEnumType.GraphQLEnumType)
- description and source-code
```javascript
function GraphQLEnumType(config) {
  _classCallCheck(this, GraphQLEnumType);

  this.name = config.name;
  (0, _assertValidName.assertValidName)(config.name, config.isIntrospection);
  this.description = config.description;
  this._values = defineEnumValues(this, config.values);
  this._enumConfig = config;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.graphql.GraphQLEnumType.prototype"></a>[module graphql.GraphQLEnumType.prototype](#apidoc.module.graphql.GraphQLEnumType.prototype)

#### <a name="apidoc.element.graphql.GraphQLEnumType.prototype._getNameLookup"></a>[function <span class="apidocSignatureSpan">graphql.GraphQLEnumType.prototype.</span>_getNameLookup ()](#apidoc.element.graphql.GraphQLEnumType.prototype._getNameLookup)
- description and source-code
```javascript
function _getNameLookup() {
  if (!this._nameLookup) {
    var lookup = Object.create(null);
    this.getValues().forEach(function (value) {
      lookup[value.name] = value;
    });
    this._nameLookup = lookup;
  }
  return this._nameLookup;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.GraphQLEnumType.prototype._getValueLookup"></a>[function <span class="apidocSignatureSpan">graphql.GraphQLEnumType.prototype.</span>_getValueLookup ()](#apidoc.element.graphql.GraphQLEnumType.prototype._getValueLookup)
- description and source-code
```javascript
function _getValueLookup() {
  if (!this._valueLookup) {
    var lookup = new Map();
    this.getValues().forEach(function (value) {
      lookup.set(value.value, value);
    });
    this._valueLookup = lookup;
  }
  return this._valueLookup;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.GraphQLEnumType.prototype.getValue"></a>[function <span class="apidocSignatureSpan">graphql.GraphQLEnumType.prototype.</span>getValue (name)](#apidoc.element.graphql.GraphQLEnumType.prototype.getValue)
- description and source-code
```javascript
function getValue(name) {
  return this._getNameLookup()[name];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.GraphQLEnumType.prototype.getValues"></a>[function <span class="apidocSignatureSpan">graphql.GraphQLEnumType.prototype.</span>getValues ()](#apidoc.element.graphql.GraphQLEnumType.prototype.getValues)
- description and source-code
```javascript
function getValues() {
  return this._values;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.GraphQLEnumType.prototype.inspect"></a>[function <span class="apidocSignatureSpan">graphql.GraphQLEnumType.prototype.</span>inspect ()](#apidoc.element.graphql.GraphQLEnumType.prototype.inspect)
- description and source-code
```javascript
function toString() {
  return this.name;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.GraphQLEnumType.prototype.parseLiteral"></a>[function <span class="apidocSignatureSpan">graphql.GraphQLEnumType.prototype.</span>parseLiteral (valueNode)](#apidoc.element.graphql.GraphQLEnumType.prototype.parseLiteral)
- description and source-code
```javascript
function parseLiteral(valueNode) /* T */{
  if (valueNode.kind === _kinds.ENUM) {
    var enumValue = this._getNameLookup()[valueNode.value];
    if (enumValue) {
      return enumValue.value;
    }
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.GraphQLEnumType.prototype.parseValue"></a>[function <span class="apidocSignatureSpan">graphql.GraphQLEnumType.prototype.</span>parseValue (value)](#apidoc.element.graphql.GraphQLEnumType.prototype.parseValue)
- description and source-code
```javascript
function parseValue(value) /* T */{
  if (typeof value === 'string') {
    var enumValue = this._getNameLookup()[value];
    if (enumValue) {
      return enumValue.value;
    }
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.GraphQLEnumType.prototype.serialize"></a>[function <span class="apidocSignatureSpan">graphql.GraphQLEnumType.prototype.</span>serialize (value)](#apidoc.element.graphql.GraphQLEnumType.prototype.serialize)
- description and source-code
```javascript
function serialize(value) {
  var enumValue = this._getValueLookup().get(value);
  return enumValue ? enumValue.name : null;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.GraphQLEnumType.prototype.toJSON"></a>[function <span class="apidocSignatureSpan">graphql.GraphQLEnumType.prototype.</span>toJSON ()](#apidoc.element.graphql.GraphQLEnumType.prototype.toJSON)
- description and source-code
```javascript
function toString() {
  return this.name;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.GraphQLEnumType.prototype.toString"></a>[function <span class="apidocSignatureSpan">graphql.GraphQLEnumType.prototype.</span>toString ()](#apidoc.element.graphql.GraphQLEnumType.prototype.toString)
- description and source-code
```javascript
function toString() {
  return this.name;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.graphql.GraphQLError"></a>[module graphql.GraphQLError](#apidoc.module.graphql.GraphQLError)

#### <a name="apidoc.element.graphql.GraphQLError.GraphQLError"></a>[function <span class="apidocSignatureSpan">graphql.</span>GraphQLError ( // eslint-disable-line no-redeclare message, nodes, source, positions, path, originalError)](#apidoc.element.graphql.GraphQLError.GraphQLError)
- description and source-code
```javascript
function GraphQLError( // eslint-disable-line no-redeclare message, nodes, source, positions, path, originalError) {
  // Include (non-enumerable) stack trace.
  if (originalError && originalError.stack) {
    Object.defineProperty(this, 'stack', {
      value: originalError.stack,
      writable: true,
      configurable: true
    });
  } else if (Error.captureStackTrace) {
    Error.captureStackTrace(this, GraphQLError);
  } else {
    Object.defineProperty(this, 'stack', {
      value: Error().stack,
      writable: true,
      configurable: true
    });
  }

  // Compute locations in the source for the given nodes/positions.
  var _source = source;
  if (!_source && nodes && nodes.length > 0) {
    var node = nodes[0];
    _source = node && node.loc && node.loc.source;
  }

  var _positions = positions;
  if (!_positions && nodes) {
    _positions = nodes.filter(function (node) {
      return Boolean(node.loc);
    }).map(function (node) {
      return node.loc.start;
    });
  }
  if (_positions && _positions.length === 0) {
    _positions = undefined;
  }

  var _locations = void 0;
  var _source2 = _source; // seems here Flow need a const to resolve type.
  if (_source2 && _positions) {
    _locations = _positions.map(function (pos) {
      return (0, _location.getLocation)(_source2, pos);
    });
  }

  Object.defineProperties(this, {
    message: {
      value: message,
      // By being enumerable, JSON.stringify will include 'message' in the
      // resulting output. This ensures that the simplist possible GraphQL
      // service adheres to the spec.
      enumerable: true,
      writable: true
    },
    locations: {
      // Coercing falsey values to undefined ensures they will not be included
      // in JSON.stringify() when not provided.
      value: _locations || undefined,
      // By being enumerable, JSON.stringify will include 'locations' in the
      // resulting output. This ensures that the simplist possible GraphQL
      // service adheres to the spec.
      enumerable: true
    },
    path: {
      // Coercing falsey values to undefined ensures they will not be included
      // in JSON.stringify() when not provided.
      value: path || undefined,
      // By being enumerable, JSON.stringify will include 'path' in the
      // resulting output. This ensures that the simplist possible GraphQL
      // service adheres to the spec.
      enumerable: true
    },
    nodes: {
      value: nodes || undefined
    },
    source: {
      value: _source || undefined
    },
    positions: {
      value: _positions || undefined
    },
    originalError: {
      value: originalError
    }
  });
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.graphql.GraphQLInputObjectType"></a>[module graphql.GraphQLInputObjectType](#apidoc.module.graphql.GraphQLInputObjectType)

#### <a name="apidoc.element.graphql.GraphQLInputObjectType.GraphQLInputObjectType"></a>[function <span class="apidocSignatureSpan">graphql.</span>GraphQLInputObjectType (config)](#apidoc.element.graphql.GraphQLInputObjectType.GraphQLInputObjectType)
- description and source-code
```javascript
function GraphQLInputObjectType(config) {
  _classCallCheck(this, GraphQLInputObjectType);

  (0, _assertValidName.assertValidName)(config.name);
  this.name = config.name;
  this.description = config.description;
  this._typeConfig = config;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.graphql.GraphQLInputObjectType.prototype"></a>[module graphql.GraphQLInputObjectType.prototype](#apidoc.module.graphql.GraphQLInputObjectType.prototype)

#### <a name="apidoc.element.graphql.GraphQLInputObjectType.prototype._defineFieldMap"></a>[function <span class="apidocSignatureSpan">graphql.GraphQLInputObjectType.prototype.</span>_defineFieldMap ()](#apidoc.element.graphql.GraphQLInputObjectType.prototype._defineFieldMap)
- description and source-code
```javascript
function _defineFieldMap() {
  var _this = this;

  var fieldMap = resolveThunk(this._typeConfig.fields);
  (0, _invariant2.default)(isPlainObj(fieldMap), this.name + ' fields must be an object with field names as keys or a ' + 'function
 which returns such an object.');
  var fieldNames = Object.keys(fieldMap);
  (0, _invariant2.default)(fieldNames.length > 0, this.name + ' fields must be an object with field names as keys or a ' + 'function
 which returns such an object.');
  var resultFieldMap = {};
  fieldNames.forEach(function (fieldName) {
    (0, _assertValidName.assertValidName)(fieldName);
    var field = _extends({}, fieldMap[fieldName], {
      name: fieldName
    });
    (0, _invariant2.default)(isInputType(field.type), _this.name + '.' + fieldName + ' field type must be Input Type but ' + ('got
: ' + String(field.type) + '.'));
    (0, _invariant2.default)(field.resolve == null, _this.name + '.' + fieldName + ' field type has a resolve property, but ' + '
Input Types cannot define resolvers.');
    resultFieldMap[fieldName] = field;
  });
  return resultFieldMap;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.GraphQLInputObjectType.prototype.getFields"></a>[function <span class="apidocSignatureSpan">graphql.GraphQLInputObjectType.prototype.</span>getFields ()](#apidoc.element.graphql.GraphQLInputObjectType.prototype.getFields)
- description and source-code
```javascript
function getFields() {
  return this._fields || (this._fields = this._defineFieldMap());
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.GraphQLInputObjectType.prototype.inspect"></a>[function <span class="apidocSignatureSpan">graphql.GraphQLInputObjectType.prototype.</span>inspect ()](#apidoc.element.graphql.GraphQLInputObjectType.prototype.inspect)
- description and source-code
```javascript
function toString() {
  return this.name;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.GraphQLInputObjectType.prototype.toJSON"></a>[function <span class="apidocSignatureSpan">graphql.GraphQLInputObjectType.prototype.</span>toJSON ()](#apidoc.element.graphql.GraphQLInputObjectType.prototype.toJSON)
- description and source-code
```javascript
function toString() {
  return this.name;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.GraphQLInputObjectType.prototype.toString"></a>[function <span class="apidocSignatureSpan">graphql.GraphQLInputObjectType.prototype.</span>toString ()](#apidoc.element.graphql.GraphQLInputObjectType.prototype.toString)
- description and source-code
```javascript
function toString() {
  return this.name;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.graphql.GraphQLInterfaceType"></a>[module graphql.GraphQLInterfaceType](#apidoc.module.graphql.GraphQLInterfaceType)

#### <a name="apidoc.element.graphql.GraphQLInterfaceType.GraphQLInterfaceType"></a>[function <span class="apidocSignatureSpan">graphql.</span>GraphQLInterfaceType (config)](#apidoc.element.graphql.GraphQLInterfaceType.GraphQLInterfaceType)
- description and source-code
```javascript
function GraphQLInterfaceType(config) {
  _classCallCheck(this, GraphQLInterfaceType);

  (0, _assertValidName.assertValidName)(config.name);
  this.name = config.name;
  this.description = config.description;
  if (config.resolveType) {
    (0, _invariant2.default)(typeof config.resolveType === 'function', this.name + ' must provide "resolveType" as a function.');
  }
  this.resolveType = config.resolveType;
  this._typeConfig = config;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.graphql.GraphQLInterfaceType.prototype"></a>[module graphql.GraphQLInterfaceType.prototype](#apidoc.module.graphql.GraphQLInterfaceType.prototype)

#### <a name="apidoc.element.graphql.GraphQLInterfaceType.prototype.getFields"></a>[function <span class="apidocSignatureSpan">graphql.GraphQLInterfaceType.prototype.</span>getFields ()](#apidoc.element.graphql.GraphQLInterfaceType.prototype.getFields)
- description and source-code
```javascript
function getFields() {
  return this._fields || (this._fields = defineFieldMap(this, this._typeConfig.fields));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.GraphQLInterfaceType.prototype.inspect"></a>[function <span class="apidocSignatureSpan">graphql.GraphQLInterfaceType.prototype.</span>inspect ()](#apidoc.element.graphql.GraphQLInterfaceType.prototype.inspect)
- description and source-code
```javascript
function toString() {
  return this.name;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.GraphQLInterfaceType.prototype.toJSON"></a>[function <span class="apidocSignatureSpan">graphql.GraphQLInterfaceType.prototype.</span>toJSON ()](#apidoc.element.graphql.GraphQLInterfaceType.prototype.toJSON)
- description and source-code
```javascript
function toString() {
  return this.name;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.GraphQLInterfaceType.prototype.toString"></a>[function <span class="apidocSignatureSpan">graphql.GraphQLInterfaceType.prototype.</span>toString ()](#apidoc.element.graphql.GraphQLInterfaceType.prototype.toString)
- description and source-code
```javascript
function toString() {
  return this.name;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.graphql.GraphQLList"></a>[module graphql.GraphQLList](#apidoc.module.graphql.GraphQLList)

#### <a name="apidoc.element.graphql.GraphQLList.GraphQLList"></a>[function <span class="apidocSignatureSpan">graphql.</span>GraphQLList (type)](#apidoc.element.graphql.GraphQLList.GraphQLList)
- description and source-code
```javascript
function GraphQLList(type) {
  _classCallCheck(this, GraphQLList);

  (0, _invariant2.default)(isType(type), 'Can only create List of a GraphQLType but got: ' + String(type) + '.');
  this.ofType = type;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.graphql.GraphQLList.prototype"></a>[module graphql.GraphQLList.prototype](#apidoc.module.graphql.GraphQLList.prototype)

#### <a name="apidoc.element.graphql.GraphQLList.prototype.inspect"></a>[function <span class="apidocSignatureSpan">graphql.GraphQLList.prototype.</span>inspect ()](#apidoc.element.graphql.GraphQLList.prototype.inspect)
- description and source-code
```javascript
function toString() {
  return '[' + String(this.ofType) + ']';
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.GraphQLList.prototype.toJSON"></a>[function <span class="apidocSignatureSpan">graphql.GraphQLList.prototype.</span>toJSON ()](#apidoc.element.graphql.GraphQLList.prototype.toJSON)
- description and source-code
```javascript
function toString() {
  return '[' + String(this.ofType) + ']';
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.GraphQLList.prototype.toString"></a>[function <span class="apidocSignatureSpan">graphql.GraphQLList.prototype.</span>toString ()](#apidoc.element.graphql.GraphQLList.prototype.toString)
- description and source-code
```javascript
function toString() {
  return '[' + String(this.ofType) + ']';
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.graphql.GraphQLNonNull"></a>[module graphql.GraphQLNonNull](#apidoc.module.graphql.GraphQLNonNull)

#### <a name="apidoc.element.graphql.GraphQLNonNull.GraphQLNonNull"></a>[function <span class="apidocSignatureSpan">graphql.</span>GraphQLNonNull (type)](#apidoc.element.graphql.GraphQLNonNull.GraphQLNonNull)
- description and source-code
```javascript
function GraphQLNonNull(type) {
  _classCallCheck(this, GraphQLNonNull);

  (0, _invariant2.default)(isType(type) && !(type instanceof GraphQLNonNull), 'Can only create NonNull of a Nullable GraphQLType
 but got: ' + (String(type) + '.'));
  this.ofType = type;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.graphql.GraphQLNonNull.prototype"></a>[module graphql.GraphQLNonNull.prototype](#apidoc.module.graphql.GraphQLNonNull.prototype)

#### <a name="apidoc.element.graphql.GraphQLNonNull.prototype.inspect"></a>[function <span class="apidocSignatureSpan">graphql.GraphQLNonNull.prototype.</span>inspect ()](#apidoc.element.graphql.GraphQLNonNull.prototype.inspect)
- description and source-code
```javascript
function toString() {
  return this.ofType.toString() + '!';
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.GraphQLNonNull.prototype.toJSON"></a>[function <span class="apidocSignatureSpan">graphql.GraphQLNonNull.prototype.</span>toJSON ()](#apidoc.element.graphql.GraphQLNonNull.prototype.toJSON)
- description and source-code
```javascript
function toString() {
  return this.ofType.toString() + '!';
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.GraphQLNonNull.prototype.toString"></a>[function <span class="apidocSignatureSpan">graphql.GraphQLNonNull.prototype.</span>toString ()](#apidoc.element.graphql.GraphQLNonNull.prototype.toString)
- description and source-code
```javascript
function toString() {
  return this.ofType.toString() + '!';
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.graphql.GraphQLObjectType"></a>[module graphql.GraphQLObjectType](#apidoc.module.graphql.GraphQLObjectType)

#### <a name="apidoc.element.graphql.GraphQLObjectType.GraphQLObjectType"></a>[function <span class="apidocSignatureSpan">graphql.</span>GraphQLObjectType (config)](#apidoc.element.graphql.GraphQLObjectType.GraphQLObjectType)
- description and source-code
```javascript
function GraphQLObjectType(config) {
  _classCallCheck(this, GraphQLObjectType);

  (0, _assertValidName.assertValidName)(config.name, config.isIntrospection);
  this.name = config.name;
  this.description = config.description;
  if (config.isTypeOf) {
    (0, _invariant2.default)(typeof config.isTypeOf === 'function', this.name + ' must provide "isTypeOf" as a function.');
  }
  this.isTypeOf = config.isTypeOf;
  this._typeConfig = config;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.graphql.GraphQLObjectType.prototype"></a>[module graphql.GraphQLObjectType.prototype](#apidoc.module.graphql.GraphQLObjectType.prototype)

#### <a name="apidoc.element.graphql.GraphQLObjectType.prototype.getFields"></a>[function <span class="apidocSignatureSpan">graphql.GraphQLObjectType.prototype.</span>getFields ()](#apidoc.element.graphql.GraphQLObjectType.prototype.getFields)
- description and source-code
```javascript
function getFields() {
  return this._fields || (this._fields = defineFieldMap(this, this._typeConfig.fields));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.GraphQLObjectType.prototype.getInterfaces"></a>[function <span class="apidocSignatureSpan">graphql.GraphQLObjectType.prototype.</span>getInterfaces ()](#apidoc.element.graphql.GraphQLObjectType.prototype.getInterfaces)
- description and source-code
```javascript
function getInterfaces() {
  return this._interfaces || (this._interfaces = defineInterfaces(this, this._typeConfig.interfaces));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.GraphQLObjectType.prototype.inspect"></a>[function <span class="apidocSignatureSpan">graphql.GraphQLObjectType.prototype.</span>inspect ()](#apidoc.element.graphql.GraphQLObjectType.prototype.inspect)
- description and source-code
```javascript
function toString() {
  return this.name;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.GraphQLObjectType.prototype.toJSON"></a>[function <span class="apidocSignatureSpan">graphql.GraphQLObjectType.prototype.</span>toJSON ()](#apidoc.element.graphql.GraphQLObjectType.prototype.toJSON)
- description and source-code
```javascript
function toString() {
  return this.name;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.GraphQLObjectType.prototype.toString"></a>[function <span class="apidocSignatureSpan">graphql.GraphQLObjectType.prototype.</span>toString ()](#apidoc.element.graphql.GraphQLObjectType.prototype.toString)
- description and source-code
```javascript
function toString() {
  return this.name;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.graphql.GraphQLScalarType"></a>[module graphql.GraphQLScalarType](#apidoc.module.graphql.GraphQLScalarType)

#### <a name="apidoc.element.graphql.GraphQLScalarType.GraphQLScalarType"></a>[function <span class="apidocSignatureSpan">graphql.</span>GraphQLScalarType (config)](#apidoc.element.graphql.GraphQLScalarType.GraphQLScalarType)
- description and source-code
```javascript
function GraphQLScalarType(config) {
  _classCallCheck(this, GraphQLScalarType);

  (0, _assertValidName.assertValidName)(config.name);
  this.name = config.name;
  this.description = config.description;
  (0, _invariant2.default)(typeof config.serialize === 'function', this.name + ' must provide "serialize" function. If this custom
 Scalar ' + 'is also used as an input type, ensure "parseValue" and "parseLiteral" ' + 'functions are also provided.');
  if (config.parseValue || config.parseLiteral) {
    (0, _invariant2.default)(typeof config.parseValue === 'function' && typeof config.parseLiteral === 'function', this.name + '
must provide both "parseValue" and "parseLiteral" ' + 'functions.');
  }
  this._scalarConfig = config;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.graphql.GraphQLScalarType.prototype"></a>[module graphql.GraphQLScalarType.prototype](#apidoc.module.graphql.GraphQLScalarType.prototype)

#### <a name="apidoc.element.graphql.GraphQLScalarType.prototype.inspect"></a>[function <span class="apidocSignatureSpan">graphql.GraphQLScalarType.prototype.</span>inspect ()](#apidoc.element.graphql.GraphQLScalarType.prototype.inspect)
- description and source-code
```javascript
function toString() {
  return this.name;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.GraphQLScalarType.prototype.parseLiteral"></a>[function <span class="apidocSignatureSpan">graphql.GraphQLScalarType.prototype.</span>parseLiteral (valueNode)](#apidoc.element.graphql.GraphQLScalarType.prototype.parseLiteral)
- description and source-code
```javascript
function parseLiteral(valueNode) {
  var parser = this._scalarConfig.parseLiteral;
  return parser ? parser(valueNode) : null;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.GraphQLScalarType.prototype.parseValue"></a>[function <span class="apidocSignatureSpan">graphql.GraphQLScalarType.prototype.</span>parseValue (value)](#apidoc.element.graphql.GraphQLScalarType.prototype.parseValue)
- description and source-code
```javascript
function parseValue(value) {
  var parser = this._scalarConfig.parseValue;
  return parser ? parser(value) : null;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.GraphQLScalarType.prototype.serialize"></a>[function <span class="apidocSignatureSpan">graphql.GraphQLScalarType.prototype.</span>serialize (value)](#apidoc.element.graphql.GraphQLScalarType.prototype.serialize)
- description and source-code
```javascript
function serialize(value) {
  var serializer = this._scalarConfig.serialize;
  return serializer(value);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.GraphQLScalarType.prototype.toJSON"></a>[function <span class="apidocSignatureSpan">graphql.GraphQLScalarType.prototype.</span>toJSON ()](#apidoc.element.graphql.GraphQLScalarType.prototype.toJSON)
- description and source-code
```javascript
function toString() {
  return this.name;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.GraphQLScalarType.prototype.toString"></a>[function <span class="apidocSignatureSpan">graphql.GraphQLScalarType.prototype.</span>toString ()](#apidoc.element.graphql.GraphQLScalarType.prototype.toString)
- description and source-code
```javascript
function toString() {
  return this.name;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.graphql.GraphQLSchema"></a>[module graphql.GraphQLSchema](#apidoc.module.graphql.GraphQLSchema)

#### <a name="apidoc.element.graphql.GraphQLSchema.GraphQLSchema"></a>[function <span class="apidocSignatureSpan">graphql.</span>GraphQLSchema (config)](#apidoc.element.graphql.GraphQLSchema.GraphQLSchema)
- description and source-code
```javascript
function GraphQLSchema(config) {
  var _this = this;

  _classCallCheck(this, GraphQLSchema);

  (0, _invariant2.default)(typeof config === 'object', 'Must provide configuration object.');

  (0, _invariant2.default)(config.query instanceof _definition.GraphQLObjectType, 'Schema query must be Object Type but got: ' +
String(config.query) + '.');
  this._queryType = config.query;

  (0, _invariant2.default)(!config.mutation || config.mutation instanceof _definition.GraphQLObjectType, 'Schema mutation must be
 Object Type if provided but got: ' + String(config.mutation) + '.');
  this._mutationType = config.mutation;

  (0, _invariant2.default)(!config.subscription || config.subscription instanceof _definition.GraphQLObjectType, 'Schema subscription
 must be Object Type if provided but got: ' + String(config.subscription) + '.');
  this._subscriptionType = config.subscription;

  (0, _invariant2.default)(!config.types || Array.isArray(config.types), 'Schema types must be Array if provided but got: ' + String
(config.types) + '.');

  (0, _invariant2.default)(!config.directives || Array.isArray(config.directives) && config.directives.every(function (directive
) {
    return directive instanceof _directives.GraphQLDirective;
  }), 'Schema directives must be Array<GraphQLDirective> if provided but got: ' + String(config.directives) + '.');
  // Provide specified directives (e.g. @include and @skip) by default.
  this._directives = config.directives || _directives.specifiedDirectives;

  // Build type map now to detect any errors within this schema.
  var initialTypes = [this.getQueryType(), this.getMutationType(), this.getSubscriptionType(), _introspection.__Schema];

  var types = config.types;
  if (types) {
    initialTypes = initialTypes.concat(types);
  }

  this._typeMap = initialTypes.reduce(typeMapReducer, Object.create(null));

  // Keep track of all implementations by interface name.
  this._implementations = Object.create(null);
  Object.keys(this._typeMap).forEach(function (typeName) {
    var type = _this._typeMap[typeName];
    if (type instanceof _definition.GraphQLObjectType) {
      type.getInterfaces().forEach(function (iface) {
        var impls = _this._implementations[iface.name];
        if (impls) {
          impls.push(type);
        } else {
          _this._implementations[iface.name] = [type];
        }
      });
    }
  });

  // Enforce correct interface implementations.
  Object.keys(this._typeMap).forEach(function (typeName) {
    var type = _this._typeMap[typeName];
    if (type instanceof _definition.GraphQLObjectType) {
      type.getInterfaces().forEach(function (iface) {
        return assertObjectImplementsInterface(_this, type, iface);
      });
    }
  });
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.graphql.GraphQLSchema.prototype"></a>[module graphql.GraphQLSchema.prototype](#apidoc.module.graphql.GraphQLSchema.prototype)

#### <a name="apidoc.element.graphql.GraphQLSchema.prototype.getDirective"></a>[function <span class="apidocSignatureSpan">graphql.GraphQLSchema.prototype.</span>getDirective (name)](#apidoc.element.graphql.GraphQLSchema.prototype.getDirective)
- description and source-code
```javascript
function getDirective(name) {
  return (0, _find2.default)(this.getDirectives(), function (directive) {
    return directive.name === name;
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.GraphQLSchema.prototype.getDirectives"></a>[function <span class="apidocSignatureSpan">graphql.GraphQLSchema.prototype.</span>getDirectives ()](#apidoc.element.graphql.GraphQLSchema.prototype.getDirectives)
- description and source-code
```javascript
function getDirectives() {
  return this._directives;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.GraphQLSchema.prototype.getMutationType"></a>[function <span class="apidocSignatureSpan">graphql.GraphQLSchema.prototype.</span>getMutationType ()](#apidoc.element.graphql.GraphQLSchema.prototype.getMutationType)
- description and source-code
```javascript
function getMutationType() {
  return this._mutationType;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.GraphQLSchema.prototype.getPossibleTypes"></a>[function <span class="apidocSignatureSpan">graphql.GraphQLSchema.prototype.</span>getPossibleTypes (abstractType)](#apidoc.element.graphql.GraphQLSchema.prototype.getPossibleTypes)
- description and source-code
```javascript
function getPossibleTypes(abstractType) {
  if (abstractType instanceof _definition.GraphQLUnionType) {
    return abstractType.getTypes();
  }
  (0, _invariant2.default)(abstractType instanceof _definition.GraphQLInterfaceType);
  return this._implementations[abstractType.name];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.GraphQLSchema.prototype.getQueryType"></a>[function <span class="apidocSignatureSpan">graphql.GraphQLSchema.prototype.</span>getQueryType ()](#apidoc.element.graphql.GraphQLSchema.prototype.getQueryType)
- description and source-code
```javascript
function getQueryType() {
  return this._queryType;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.GraphQLSchema.prototype.getSubscriptionType"></a>[function <span class="apidocSignatureSpan">graphql.GraphQLSchema.prototype.</span>getSubscriptionType ()](#apidoc.element.graphql.GraphQLSchema.prototype.getSubscriptionType)
- description and source-code
```javascript
function getSubscriptionType() {
  return this._subscriptionType;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.GraphQLSchema.prototype.getType"></a>[function <span class="apidocSignatureSpan">graphql.GraphQLSchema.prototype.</span>getType (name)](#apidoc.element.graphql.GraphQLSchema.prototype.getType)
- description and source-code
```javascript
function getType(name) {
  return this.getTypeMap()[name];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.GraphQLSchema.prototype.getTypeMap"></a>[function <span class="apidocSignatureSpan">graphql.GraphQLSchema.prototype.</span>getTypeMap ()](#apidoc.element.graphql.GraphQLSchema.prototype.getTypeMap)
- description and source-code
```javascript
function getTypeMap() {
  return this._typeMap;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.GraphQLSchema.prototype.isPossibleType"></a>[function <span class="apidocSignatureSpan">graphql.GraphQLSchema.prototype.</span>isPossibleType (abstractType, possibleType)](#apidoc.element.graphql.GraphQLSchema.prototype.isPossibleType)
- description and source-code
```javascript
function isPossibleType(abstractType, possibleType) {
  var possibleTypeMap = this._possibleTypeMap;
  if (!possibleTypeMap) {
    this._possibleTypeMap = possibleTypeMap = Object.create(null);
  }

  if (!possibleTypeMap[abstractType.name]) {
    var possibleTypes = this.getPossibleTypes(abstractType);
    (0, _invariant2.default)(Array.isArray(possibleTypes), 'Could not find possible implementing types for ' + abstractType.name
 + ' ' + 'in schema. Check that schema.types is defined and is an array of ' + 'all possible types in the schema.');
    possibleTypeMap[abstractType.name] = possibleTypes.reduce(function (map, type) {
      return map[type.name] = true, map;
    }, Object.create(null));
  }

  return Boolean(possibleTypeMap[abstractType.name][possibleType.name]);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.graphql.GraphQLUnionType"></a>[module graphql.GraphQLUnionType](#apidoc.module.graphql.GraphQLUnionType)

#### <a name="apidoc.element.graphql.GraphQLUnionType.GraphQLUnionType"></a>[function <span class="apidocSignatureSpan">graphql.</span>GraphQLUnionType (config)](#apidoc.element.graphql.GraphQLUnionType.GraphQLUnionType)
- description and source-code
```javascript
function GraphQLUnionType(config) {
  _classCallCheck(this, GraphQLUnionType);

  (0, _assertValidName.assertValidName)(config.name);
  this.name = config.name;
  this.description = config.description;
  if (config.resolveType) {
    (0, _invariant2.default)(typeof config.resolveType === 'function', this.name + ' must provide "resolveType" as a function.');
  }
  this.resolveType = config.resolveType;
  this._typeConfig = config;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.graphql.GraphQLUnionType.prototype"></a>[module graphql.GraphQLUnionType.prototype](#apidoc.module.graphql.GraphQLUnionType.prototype)

#### <a name="apidoc.element.graphql.GraphQLUnionType.prototype.getTypes"></a>[function <span class="apidocSignatureSpan">graphql.GraphQLUnionType.prototype.</span>getTypes ()](#apidoc.element.graphql.GraphQLUnionType.prototype.getTypes)
- description and source-code
```javascript
function getTypes() {
  return this._types || (this._types = defineTypes(this, this._typeConfig.types));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.GraphQLUnionType.prototype.inspect"></a>[function <span class="apidocSignatureSpan">graphql.GraphQLUnionType.prototype.</span>inspect ()](#apidoc.element.graphql.GraphQLUnionType.prototype.inspect)
- description and source-code
```javascript
function toString() {
  return this.name;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.GraphQLUnionType.prototype.toJSON"></a>[function <span class="apidocSignatureSpan">graphql.GraphQLUnionType.prototype.</span>toJSON ()](#apidoc.element.graphql.GraphQLUnionType.prototype.toJSON)
- description and source-code
```javascript
function toString() {
  return this.name;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.GraphQLUnionType.prototype.toString"></a>[function <span class="apidocSignatureSpan">graphql.GraphQLUnionType.prototype.</span>toString ()](#apidoc.element.graphql.GraphQLUnionType.prototype.toString)
- description and source-code
```javascript
function toString() {
  return this.name;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.graphql.SchemaMetaFieldDef"></a>[module graphql.SchemaMetaFieldDef](#apidoc.module.graphql.SchemaMetaFieldDef)

#### <a name="apidoc.element.graphql.SchemaMetaFieldDef.resolve"></a>[function <span class="apidocSignatureSpan">graphql.SchemaMetaFieldDef.</span>resolve (source, args, context, _ref4)](#apidoc.element.graphql.SchemaMetaFieldDef.resolve)
- description and source-code
```javascript
function resolve(source, args, context, _ref4) {
  var schema = _ref4.schema;
  return schema;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.graphql.TypeInfo"></a>[module graphql.TypeInfo](#apidoc.module.graphql.TypeInfo)

#### <a name="apidoc.element.graphql.TypeInfo.TypeInfo"></a>[function <span class="apidocSignatureSpan">graphql.</span>TypeInfo (schema, // NOTE: this experimental optional second parameter is only needed in order // to support non-spec-compliant codebases. You should never need to use it. getFieldDefFn)](#apidoc.element.graphql.TypeInfo.TypeInfo)
- description and source-code
```javascript
function TypeInfo(schema, // NOTE: this experimental optional second parameter is only needed in order // to support non-spec-compliant codebases. You should never need to use it. getFieldDefFn) {
  _classCallCheck(this, TypeInfo);

  this._schema = schema;
  this._typeStack = [];
  this._parentTypeStack = [];
  this._inputTypeStack = [];
  this._fieldDefStack = [];
  this._directive = null;
  this._argument = null;
  this._enumValue = null;
  this._getFieldDef = getFieldDefFn || getFieldDef;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.graphql.TypeInfo.prototype"></a>[module graphql.TypeInfo.prototype](#apidoc.module.graphql.TypeInfo.prototype)

#### <a name="apidoc.element.graphql.TypeInfo.prototype.enter"></a>[function <span class="apidocSignatureSpan">graphql.TypeInfo.prototype.</span>enter (node)](#apidoc.element.graphql.TypeInfo.prototype.enter)
- description and source-code
```javascript
function enter(node) {
  var schema = this._schema;
  switch (node.kind) {
    case Kind.SELECTION_SET:
      var namedType = (0, _definition.getNamedType)(this.getType());
      this._parentTypeStack.push((0, _definition.isCompositeType)(namedType) ? namedType : undefined);
      break;
    case Kind.FIELD:
      var parentType = this.getParentType();
      var fieldDef = void 0;
      if (parentType) {
        fieldDef = this._getFieldDef(schema, parentType, node);
      }
      this._fieldDefStack.push(fieldDef);
      this._typeStack.push(fieldDef && fieldDef.type);
      break;
    case Kind.DIRECTIVE:
      this._directive = schema.getDirective(node.name.value);
      break;
    case Kind.OPERATION_DEFINITION:
      var type = void 0;
      if (node.operation === 'query') {
        type = schema.getQueryType();
      } else if (node.operation === 'mutation') {
        type = schema.getMutationType();
      } else if (node.operation === 'subscription') {
        type = schema.getSubscriptionType();
      }
      this._typeStack.push(type);
      break;
    case Kind.INLINE_FRAGMENT:
    case Kind.FRAGMENT_DEFINITION:
      var typeConditionAST = node.typeCondition;
      var outputType = typeConditionAST ? (0, _typeFromAST.typeFromAST)(schema, typeConditionAST) : this.getType();
      this._typeStack.push((0, _definition.isOutputType)(outputType) ? outputType : undefined);
      break;
    case Kind.VARIABLE_DEFINITION:
      var inputType = (0, _typeFromAST.typeFromAST)(schema, node.type);
      this._inputTypeStack.push((0, _definition.isInputType)(inputType) ? inputType : undefined);
      break;
    case Kind.ARGUMENT:
      var argDef = void 0;
      var argType = void 0;
      var fieldOrDirective = this.getDirective() || this.getFieldDef();
      if (fieldOrDirective) {
        argDef = (0, _find2.default)(fieldOrDirective.args, function (arg) {
          return arg.name === node.name.value;
        });
        if (argDef) {
          argType = argDef.type;
        }
      }
      this._argument = argDef;
      this._inputTypeStack.push(argType);
      break;
    case Kind.LIST:
      var listType = (0, _definition.getNullableType)(this.getInputType());
      this._inputTypeStack.push(listType instanceof _definition.GraphQLList ? listType.ofType : undefined);
      break;
    case Kind.OBJECT_FIELD:
      var objectType = (0, _definition.getNamedType)(this.getInputType());
      var fieldType = void 0;
      if (objectType instanceof _definition.GraphQLInputObjectType) {
        var inputField = objectType.getFields()[node.name.value];
        fieldType = inputField ? inputField.type : undefined;
      }
      this._inputTypeStack.push(fieldType);
      break;
    case Kind.ENUM:
      var enumType = (0, _definition.getNamedType)(this.getInputType());
      var enumValue = void 0;
      if (enumType instanceof _definition.GraphQLEnumType) {
        enumValue = enumType.getValue(node.value);
      }
      this._enumValue = enumValue;
      break;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.TypeInfo.prototype.getArgument"></a>[function <span class="apidocSignatureSpan">graphql.TypeInfo.prototype.</span>getArgument ()](#apidoc.element.graphql.TypeInfo.prototype.getArgument)
- description and source-code
```javascript
function getArgument() {
  return this._argument;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.TypeInfo.prototype.getDirective"></a>[function <span class="apidocSignatureSpan">graphql.TypeInfo.prototype.</span>getDirective ()](#apidoc.element.graphql.TypeInfo.prototype.getDirective)
- description and source-code
```javascript
function getDirective() {
  return this._directive;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.TypeInfo.prototype.getEnumValue"></a>[function <span class="apidocSignatureSpan">graphql.TypeInfo.prototype.</span>getEnumValue ()](#apidoc.element.graphql.TypeInfo.prototype.getEnumValue)
- description and source-code
```javascript
function getEnumValue() {
  return this._enumValue;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.TypeInfo.prototype.getFieldDef"></a>[function <span class="apidocSignatureSpan">graphql.TypeInfo.prototype.</span>getFieldDef ()](#apidoc.element.graphql.TypeInfo.prototype.getFieldDef)
- description and source-code
```javascript
function getFieldDef() {
  if (this._fieldDefStack.length > 0) {
    return this._fieldDefStack[this._fieldDefStack.length - 1];
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.TypeInfo.prototype.getInputType"></a>[function <span class="apidocSignatureSpan">graphql.TypeInfo.prototype.</span>getInputType ()](#apidoc.element.graphql.TypeInfo.prototype.getInputType)
- description and source-code
```javascript
function getInputType() {
  if (this._inputTypeStack.length > 0) {
    return this._inputTypeStack[this._inputTypeStack.length - 1];
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.TypeInfo.prototype.getParentType"></a>[function <span class="apidocSignatureSpan">graphql.TypeInfo.prototype.</span>getParentType ()](#apidoc.element.graphql.TypeInfo.prototype.getParentType)
- description and source-code
```javascript
function getParentType() {
  if (this._parentTypeStack.length > 0) {
    return this._parentTypeStack[this._parentTypeStack.length - 1];
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.TypeInfo.prototype.getType"></a>[function <span class="apidocSignatureSpan">graphql.TypeInfo.prototype.</span>getType ()](#apidoc.element.graphql.TypeInfo.prototype.getType)
- description and source-code
```javascript
function getType() {
  if (this._typeStack.length > 0) {
    return this._typeStack[this._typeStack.length - 1];
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.TypeInfo.prototype.leave"></a>[function <span class="apidocSignatureSpan">graphql.TypeInfo.prototype.</span>leave (node)](#apidoc.element.graphql.TypeInfo.prototype.leave)
- description and source-code
```javascript
function leave(node) {
  switch (node.kind) {
    case Kind.SELECTION_SET:
      this._parentTypeStack.pop();
      break;
    case Kind.FIELD:
      this._fieldDefStack.pop();
      this._typeStack.pop();
      break;
    case Kind.DIRECTIVE:
      this._directive = null;
      break;
    case Kind.OPERATION_DEFINITION:
    case Kind.INLINE_FRAGMENT:
    case Kind.FRAGMENT_DEFINITION:
      this._typeStack.pop();
      break;
    case Kind.VARIABLE_DEFINITION:
      this._inputTypeStack.pop();
      break;
    case Kind.ARGUMENT:
      this._argument = null;
      this._inputTypeStack.pop();
      break;
    case Kind.LIST:
    case Kind.OBJECT_FIELD:
      this._inputTypeStack.pop();
      break;
    case Kind.ENUM:
      this._enumValue = null;
      break;
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.graphql.TypeMetaFieldDef"></a>[module graphql.TypeMetaFieldDef](#apidoc.module.graphql.TypeMetaFieldDef)

#### <a name="apidoc.element.graphql.TypeMetaFieldDef.resolve"></a>[function <span class="apidocSignatureSpan">graphql.TypeMetaFieldDef.</span>resolve (source, _ref5, context, _ref6)](#apidoc.element.graphql.TypeMetaFieldDef.resolve)
- description and source-code
```javascript
function resolve(source, _ref5, context, _ref6) {
  var name = _ref5.name;
  var schema = _ref6.schema;
  return schema.getType(name);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.graphql.TypeNameMetaFieldDef"></a>[module graphql.TypeNameMetaFieldDef](#apidoc.module.graphql.TypeNameMetaFieldDef)

#### <a name="apidoc.element.graphql.TypeNameMetaFieldDef.resolve"></a>[function <span class="apidocSignatureSpan">graphql.TypeNameMetaFieldDef.</span>resolve (source, args, context, _ref7)](#apidoc.element.graphql.TypeNameMetaFieldDef.resolve)
- description and source-code
```javascript
function resolve(source, args, context, _ref7) {
  var parentType = _ref7.parentType;
  return parentType.name;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.graphql.ValidationContext"></a>[module graphql.ValidationContext](#apidoc.module.graphql.ValidationContext)

#### <a name="apidoc.element.graphql.ValidationContext.ValidationContext"></a>[function <span class="apidocSignatureSpan">graphql.</span>ValidationContext (schema, ast, typeInfo)](#apidoc.element.graphql.ValidationContext.ValidationContext)
- description and source-code
```javascript
function ValidationContext(schema, ast, typeInfo) {
  _classCallCheck(this, ValidationContext);

  this._schema = schema;
  this._ast = ast;
  this._typeInfo = typeInfo;
  this._errors = [];
  this._fragmentSpreads = new Map();
  this._recursivelyReferencedFragments = new Map();
  this._variableUsages = new Map();
  this._recursiveVariableUsages = new Map();
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.graphql.ValidationContext.prototype"></a>[module graphql.ValidationContext.prototype](#apidoc.module.graphql.ValidationContext.prototype)

#### <a name="apidoc.element.graphql.ValidationContext.prototype.getArgument"></a>[function <span class="apidocSignatureSpan">graphql.ValidationContext.prototype.</span>getArgument ()](#apidoc.element.graphql.ValidationContext.prototype.getArgument)
- description and source-code
```javascript
function getArgument() {
  return this._typeInfo.getArgument();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.ValidationContext.prototype.getDirective"></a>[function <span class="apidocSignatureSpan">graphql.ValidationContext.prototype.</span>getDirective ()](#apidoc.element.graphql.ValidationContext.prototype.getDirective)
- description and source-code
```javascript
function getDirective() {
  return this._typeInfo.getDirective();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.ValidationContext.prototype.getDocument"></a>[function <span class="apidocSignatureSpan">graphql.ValidationContext.prototype.</span>getDocument ()](#apidoc.element.graphql.ValidationContext.prototype.getDocument)
- description and source-code
```javascript
function getDocument() {
  return this._ast;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.ValidationContext.prototype.getErrors"></a>[function <span class="apidocSignatureSpan">graphql.ValidationContext.prototype.</span>getErrors ()](#apidoc.element.graphql.ValidationContext.prototype.getErrors)
- description and source-code
```javascript
function getErrors() {
  return this._errors;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.ValidationContext.prototype.getFieldDef"></a>[function <span class="apidocSignatureSpan">graphql.ValidationContext.prototype.</span>getFieldDef ()](#apidoc.element.graphql.ValidationContext.prototype.getFieldDef)
- description and source-code
```javascript
function getFieldDef() {
  return this._typeInfo.getFieldDef();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.ValidationContext.prototype.getFragment"></a>[function <span class="apidocSignatureSpan">graphql.ValidationContext.prototype.</span>getFragment (name)](#apidoc.element.graphql.ValidationContext.prototype.getFragment)
- description and source-code
```javascript
function getFragment(name) {
  var fragments = this._fragments;
  if (!fragments) {
    this._fragments = fragments = this.getDocument().definitions.reduce(function (frags, statement) {
      if (statement.kind === Kind.FRAGMENT_DEFINITION) {
        frags[statement.name.value] = statement;
      }
      return frags;
    }, {});
  }
  return fragments[name];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.ValidationContext.prototype.getFragmentSpreads"></a>[function <span class="apidocSignatureSpan">graphql.ValidationContext.prototype.</span>getFragmentSpreads (node)](#apidoc.element.graphql.ValidationContext.prototype.getFragmentSpreads)
- description and source-code
```javascript
function getFragmentSpreads(node) {
  var spreads = this._fragmentSpreads.get(node);
  if (!spreads) {
    spreads = [];
    var setsToVisit = [node];
    while (setsToVisit.length !== 0) {
      var set = setsToVisit.pop();
      for (var i = 0; i < set.selections.length; i++) {
        var selection = set.selections[i];
        if (selection.kind === Kind.FRAGMENT_SPREAD) {
          spreads.push(selection);
        } else if (selection.selectionSet) {
          setsToVisit.push(selection.selectionSet);
        }
      }
    }
    this._fragmentSpreads.set(node, spreads);
  }
  return spreads;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.ValidationContext.prototype.getInputType"></a>[function <span class="apidocSignatureSpan">graphql.ValidationContext.prototype.</span>getInputType ()](#apidoc.element.graphql.ValidationContext.prototype.getInputType)
- description and source-code
```javascript
function getInputType() {
  return this._typeInfo.getInputType();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.ValidationContext.prototype.getParentType"></a>[function <span class="apidocSignatureSpan">graphql.ValidationContext.prototype.</span>getParentType ()](#apidoc.element.graphql.ValidationContext.prototype.getParentType)
- description and source-code
```javascript
function getParentType() {
  return this._typeInfo.getParentType();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.ValidationContext.prototype.getRecursiveVariableUsages"></a>[function <span class="apidocSignatureSpan">graphql.ValidationContext.prototype.</span>getRecursiveVariableUsages (operation)](#apidoc.element.graphql.ValidationContext.prototype.getRecursiveVariableUsages)
- description and source-code
```javascript
function getRecursiveVariableUsages(operation) {
  var usages = this._recursiveVariableUsages.get(operation);
  if (!usages) {
    usages = this.getVariableUsages(operation);
    var fragments = this.getRecursivelyReferencedFragments(operation);
    for (var i = 0; i < fragments.length; i++) {
      Array.prototype.push.apply(usages, this.getVariableUsages(fragments[i]));
    }
    this._recursiveVariableUsages.set(operation, usages);
  }
  return usages;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.ValidationContext.prototype.getRecursivelyReferencedFragments"></a>[function <span class="apidocSignatureSpan">graphql.ValidationContext.prototype.</span>getRecursivelyReferencedFragments (operation)](#apidoc.element.graphql.ValidationContext.prototype.getRecursivelyReferencedFragments)
- description and source-code
```javascript
function getRecursivelyReferencedFragments(operation) {
  var fragments = this._recursivelyReferencedFragments.get(operation);
  if (!fragments) {
    fragments = [];
    var collectedNames = Object.create(null);
    var nodesToVisit = [operation.selectionSet];
    while (nodesToVisit.length !== 0) {
      var _node = nodesToVisit.pop();
      var spreads = this.getFragmentSpreads(_node);
      for (var i = 0; i < spreads.length; i++) {
        var fragName = spreads[i].name.value;
        if (collectedNames[fragName] !== true) {
          collectedNames[fragName] = true;
          var fragment = this.getFragment(fragName);
          if (fragment) {
            fragments.push(fragment);
            nodesToVisit.push(fragment.selectionSet);
          }
        }
      }
    }
    this._recursivelyReferencedFragments.set(operation, fragments);
  }
  return fragments;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.ValidationContext.prototype.getSchema"></a>[function <span class="apidocSignatureSpan">graphql.ValidationContext.prototype.</span>getSchema ()](#apidoc.element.graphql.ValidationContext.prototype.getSchema)
- description and source-code
```javascript
function getSchema() {
  return this._schema;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.ValidationContext.prototype.getType"></a>[function <span class="apidocSignatureSpan">graphql.ValidationContext.prototype.</span>getType ()](#apidoc.element.graphql.ValidationContext.prototype.getType)
- description and source-code
```javascript
function getType() {
  return this._typeInfo.getType();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.ValidationContext.prototype.getVariableUsages"></a>[function <span class="apidocSignatureSpan">graphql.ValidationContext.prototype.</span>getVariableUsages (node)](#apidoc.element.graphql.ValidationContext.prototype.getVariableUsages)
- description and source-code
```javascript
function getVariableUsages(node) {
  var usages = this._variableUsages.get(node);
  if (!usages) {
    var newUsages = [];
    var typeInfo = new _TypeInfo.TypeInfo(this._schema);
    (0, _visitor.visit)(node, (0, _visitor.visitWithTypeInfo)(typeInfo, {
      VariableDefinition: function VariableDefinition() {
        return false;
      },
      Variable: function Variable(variable) {
        newUsages.push({ node: variable, type: typeInfo.getInputType() });
      }
    }));
    usages = newUsages;
    this._variableUsages.set(node, usages);
  }
  return usages;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.ValidationContext.prototype.reportError"></a>[function <span class="apidocSignatureSpan">graphql.ValidationContext.prototype.</span>reportError (error)](#apidoc.element.graphql.ValidationContext.prototype.reportError)
- description and source-code
```javascript
function reportError(error) {
  this._errors.push(error);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.graphql.specifiedRules"></a>[module graphql.specifiedRules](#apidoc.module.graphql.specifiedRules)

#### <a name="apidoc.element.graphql.specifiedRules.0"></a>[function <span class="apidocSignatureSpan">graphql.specifiedRules.</span>0 (context)](#apidoc.element.graphql.specifiedRules.0)
- description and source-code
```javascript
function UniqueOperationNames(context) {
  var knownOperationNames = Object.create(null);
  return {
    OperationDefinition: function OperationDefinition(node) {
      var operationName = node.name;
      if (operationName) {
        if (knownOperationNames[operationName.value]) {
          context.reportError(new _error.GraphQLError(duplicateOperationNameMessage(operationName.value), [knownOperationNames[operationName
.value], operationName]));
        } else {
          knownOperationNames[operationName.value] = operationName;
        }
      }
      return false;
    },

    FragmentDefinition: function FragmentDefinition() {
      return false;
    }
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.specifiedRules.1"></a>[function <span class="apidocSignatureSpan">graphql.specifiedRules.</span>1 (context)](#apidoc.element.graphql.specifiedRules.1)
- description and source-code
```javascript
function LoneAnonymousOperation(context) {
  var operationCount = 0;
  return {
    Document: function Document(node) {
      operationCount = node.definitions.filter(function (definition) {
        return definition.kind === _kinds.OPERATION_DEFINITION;
      }).length;
    },
    OperationDefinition: function OperationDefinition(node) {
      if (!node.name && operationCount > 1) {
        context.reportError(new _error.GraphQLError(anonOperationNotAloneMessage(), [node]));
      }
    }
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.specifiedRules.10"></a>[function <span class="apidocSignatureSpan">graphql.specifiedRules.</span>10 (context)](#apidoc.element.graphql.specifiedRules.10)
- description and source-code
```javascript
function PossibleFragmentSpreads(context) {
  return {
    InlineFragment: function InlineFragment(node) {
      var fragType = context.getType();
      var parentType = context.getParentType();
      if (fragType && parentType && !(0, _typeComparators.doTypesOverlap)(context.getSchema(), fragType, parentType)) {
        context.reportError(new _error.GraphQLError(typeIncompatibleAnonSpreadMessage(parentType, fragType), [node]));
      }
    },
    FragmentSpread: function FragmentSpread(node) {
      var fragName = node.name.value;
      var fragType = getFragmentType(context, fragName);
      var parentType = context.getParentType();
      if (fragType && parentType && !(0, _typeComparators.doTypesOverlap)(context.getSchema(), fragType, parentType)) {
        context.reportError(new _error.GraphQLError(typeIncompatibleSpreadMessage(fragName, parentType, fragType), [node]));
      }
    }
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.specifiedRules.11"></a>[function <span class="apidocSignatureSpan">graphql.specifiedRules.</span>11 (context)](#apidoc.element.graphql.specifiedRules.11)
- description and source-code
```javascript
function NoFragmentCycles(context) {
  // Tracks already visited fragments to maintain O(N) and to ensure that cycles
  // are not redundantly reported.
  var visitedFrags = Object.create(null);

  // Array of AST nodes used to produce meaningful errors
  var spreadPath = [];

  // Position in the spread path
  var spreadPathIndexByName = Object.create(null);

  return {
    OperationDefinition: function OperationDefinition() {
      return false;
    },
    FragmentDefinition: function FragmentDefinition(node) {
      if (!visitedFrags[node.name.value]) {
        detectCycleRecursive(node);
      }
      return false;
    }
  };

  // This does a straight-forward DFS to find cycles.
  // It does not terminate when a cycle was found but continues to explore
  // the graph to find all possible cycles.
  function detectCycleRecursive(fragment) {
    var fragmentName = fragment.name.value;
    visitedFrags[fragmentName] = true;

    var spreadNodes = context.getFragmentSpreads(fragment.selectionSet);
    if (spreadNodes.length === 0) {
      return;
    }

    spreadPathIndexByName[fragmentName] = spreadPath.length;

    for (var i = 0; i < spreadNodes.length; i++) {
      var spreadNode = spreadNodes[i];
      var spreadName = spreadNode.name.value;
      var cycleIndex = spreadPathIndexByName[spreadName];

      if (cycleIndex === undefined) {
        spreadPath.push(spreadNode);
        if (!visitedFrags[spreadName]) {
          var spreadFragment = context.getFragment(spreadName);
          if (spreadFragment) {
            detectCycleRecursive(spreadFragment);
          }
        }
        spreadPath.pop();
      } else {
        var cyclePath = spreadPath.slice(cycleIndex);
        context.reportError(new _error.GraphQLError(cycleErrorMessage(spreadName, cyclePath.map(function (s) {
          return s.name.value;
        })), cyclePath.concat(spreadNode)));
      }
    }

    spreadPathIndexByName[fragmentName] = undefined;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.specifiedRules.12"></a>[function <span class="apidocSignatureSpan">graphql.specifiedRules.</span>12 (context)](#apidoc.element.graphql.specifiedRules.12)
- description and source-code
```javascript
function UniqueVariableNames(context) {
  var knownVariableNames = Object.create(null);
  return {
    OperationDefinition: function OperationDefinition() {
      knownVariableNames = Object.create(null);
    },
    VariableDefinition: function VariableDefinition(node) {
      var variableName = node.variable.name.value;
      if (knownVariableNames[variableName]) {
        context.reportError(new _error.GraphQLError(duplicateVariableMessage(variableName), [knownVariableNames[variableName], node
.variable.name]));
      } else {
        knownVariableNames[variableName] = node.variable.name;
      }
    }
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.specifiedRules.13"></a>[function <span class="apidocSignatureSpan">graphql.specifiedRules.</span>13 (context)](#apidoc.element.graphql.specifiedRules.13)
- description and source-code
```javascript
function NoUndefinedVariables(context) {
  var variableNameDefined = Object.create(null);

  return {
    OperationDefinition: {
      enter: function enter() {
        variableNameDefined = Object.create(null);
      },
      leave: function leave(operation) {
        var usages = context.getRecursiveVariableUsages(operation);

        usages.forEach(function (_ref) {
          var node = _ref.node;

          var varName = node.name.value;
          if (variableNameDefined[varName] !== true) {
            context.reportError(new _error.GraphQLError(undefinedVarMessage(varName, operation.name && operation.name.value), [node
, operation]));
          }
        });
      }
    },
    VariableDefinition: function VariableDefinition(node) {
      variableNameDefined[node.variable.name.value] = true;
    }
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.specifiedRules.14"></a>[function <span class="apidocSignatureSpan">graphql.specifiedRules.</span>14 (context)](#apidoc.element.graphql.specifiedRules.14)
- description and source-code
```javascript
function NoUnusedVariables(context) {
  var variableDefs = [];

  return {
    OperationDefinition: {
      enter: function enter() {
        variableDefs = [];
      },
      leave: function leave(operation) {
        var variableNameUsed = Object.create(null);
        var usages = context.getRecursiveVariableUsages(operation);
        var opName = operation.name ? operation.name.value : null;

        usages.forEach(function (_ref) {
          var node = _ref.node;

          variableNameUsed[node.name.value] = true;
        });

        variableDefs.forEach(function (variableDef) {
          var variableName = variableDef.variable.name.value;
          if (variableNameUsed[variableName] !== true) {
            context.reportError(new _error.GraphQLError(unusedVariableMessage(variableName, opName), [variableDef]));
          }
        });
      }
    },
    VariableDefinition: function VariableDefinition(def) {
      variableDefs.push(def);
    }
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.specifiedRules.15"></a>[function <span class="apidocSignatureSpan">graphql.specifiedRules.</span>15 (context)](#apidoc.element.graphql.specifiedRules.15)
- description and source-code
```javascript
function KnownDirectives(context) {
  return {
    Directive: function Directive(node, key, parent, path, ancestors) {
      var directiveDef = (0, _find2.default)(context.getSchema().getDirectives(), function (def) {
        return def.name === node.name.value;
      });
      if (!directiveDef) {
        context.reportError(new _error.GraphQLError(unknownDirectiveMessage(node.name.value), [node]));
        return;
      }
      var candidateLocation = getDirectiveLocationForASTPath(ancestors);
      if (!candidateLocation) {
        context.reportError(new _error.GraphQLError(misplacedDirectiveMessage(node.name.value, node.type), [node]));
      } else if (directiveDef.locations.indexOf(candidateLocation) === -1) {
        context.reportError(new _error.GraphQLError(misplacedDirectiveMessage(node.name.value, candidateLocation), [node]));
      }
    }
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.specifiedRules.16"></a>[function <span class="apidocSignatureSpan">graphql.specifiedRules.</span>16 (context)](#apidoc.element.graphql.specifiedRules.16)
- description and source-code
```javascript
function UniqueDirectivesPerLocation(context) {
  return {
    // Many different AST nodes may contain directives. Rather than listing
    // them all, just listen for entering any node, and check to see if it
    // defines any directives.
    enter: function enter(node) {
      if (node.directives) {
        var knownDirectives = Object.create(null);
        node.directives.forEach(function (directive) {
          var directiveName = directive.name.value;
          if (knownDirectives[directiveName]) {
            context.reportError(new _error.GraphQLError(duplicateDirectiveMessage(directiveName), [knownDirectives[directiveName
], directive]));
          } else {
            knownDirectives[directiveName] = directive;
          }
        });
      }
    }
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.specifiedRules.17"></a>[function <span class="apidocSignatureSpan">graphql.specifiedRules.</span>17 (context)](#apidoc.element.graphql.specifiedRules.17)
- description and source-code
```javascript
function KnownArgumentNames(context) {
  return {
    Argument: function Argument(node, key, parent, path, ancestors) {
      var argumentOf = ancestors[ancestors.length - 1];
      if (argumentOf.kind === _kinds.FIELD) {
        var fieldDef = context.getFieldDef();
        if (fieldDef) {
          var fieldArgDef = (0, _find2.default)(fieldDef.args, function (arg) {
            return arg.name === node.name.value;
          });
          if (!fieldArgDef) {
            var parentType = context.getParentType();
            (0, _invariant2.default)(parentType);
            context.reportError(new _error.GraphQLError(unknownArgMessage(node.name.value, fieldDef.name, parentType.name, (0, _suggestionList2
.default)(node.name.value, fieldDef.args.map(function (arg) {
              return arg.name;
            }))), [node]));
          }
        }
      } else if (argumentOf.kind === _kinds.DIRECTIVE) {
        var directive = context.getDirective();
        if (directive) {
          var directiveArgDef = (0, _find2.default)(directive.args, function (arg) {
            return arg.name === node.name.value;
          });
          if (!directiveArgDef) {
            context.reportError(new _error.GraphQLError(unknownDirectiveArgMessage(node.name.value, directive.name, (0, _suggestionList2
.default)(node.name.value, directive.args.map(function (arg) {
              return arg.name;
            }))), [node]));
          }
        }
      }
    }
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.specifiedRules.18"></a>[function <span class="apidocSignatureSpan">graphql.specifiedRules.</span>18 (context)](#apidoc.element.graphql.specifiedRules.18)
- description and source-code
```javascript
function UniqueArgumentNames(context) {
  var knownArgNames = Object.create(null);
  return {
    Field: function Field() {
      knownArgNames = Object.create(null);
    },
    Directive: function Directive() {
      knownArgNames = Object.create(null);
    },
    Argument: function Argument(node) {
      var argName = node.name.value;
      if (knownArgNames[argName]) {
        context.reportError(new _error.GraphQLError(duplicateArgMessage(argName), [knownArgNames[argName], node.name]));
      } else {
        knownArgNames[argName] = node.name;
      }
      return false;
    }
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.specifiedRules.19"></a>[function <span class="apidocSignatureSpan">graphql.specifiedRules.</span>19 (context)](#apidoc.element.graphql.specifiedRules.19)
- description and source-code
```javascript
function ArgumentsOfCorrectType(context) {
  return {
    Argument: function Argument(node) {
      var argDef = context.getArgument();
      if (argDef) {
        var errors = (0, _isValidLiteralValue.isValidLiteralValue)(argDef.type, node.value);
        if (errors && errors.length > 0) {
          context.reportError(new _error.GraphQLError(badValueMessage(node.name.value, argDef.type, (0, _printer.print)(node.value
), errors), [node.value]));
        }
      }
      return false;
    }
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.specifiedRules.2"></a>[function <span class="apidocSignatureSpan">graphql.specifiedRules.</span>2 (context)](#apidoc.element.graphql.specifiedRules.2)
- description and source-code
```javascript
function KnownTypeNames(context) {
  return {
    // TODO: when validating IDL, re-enable these. Experimental version does not
    // add unreferenced types, resulting in false-positive errors. Squelched
    // errors for now.
    ObjectTypeDefinition: function ObjectTypeDefinition() {
      return false;
    },
    InterfaceTypeDefinition: function InterfaceTypeDefinition() {
      return false;
    },
    UnionTypeDefinition: function UnionTypeDefinition() {
      return false;
    },
    InputObjectTypeDefinition: function InputObjectTypeDefinition() {
      return false;
    },
    NamedType: function NamedType(node) {
      var schema = context.getSchema();
      var typeName = node.name.value;
      var type = schema.getType(typeName);
      if (!type) {
        context.reportError(new _error.GraphQLError(unknownTypeMessage(typeName, (0, _suggestionList2.default)(typeName, Object.
keys(schema.getTypeMap()))), [node]));
      }
    }
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.specifiedRules.20"></a>[function <span class="apidocSignatureSpan">graphql.specifiedRules.</span>20 (context)](#apidoc.element.graphql.specifiedRules.20)
- description and source-code
```javascript
function ProvidedNonNullArguments(context) {
  return {
    Field: {
      // Validate on leave to allow for deeper errors to appear first.
      leave: function leave(node) {
        var fieldDef = context.getFieldDef();
        if (!fieldDef) {
          return false;
        }
        var argNodes = node.arguments || [];

        var argNodeMap = (0, _keyMap2.default)(argNodes, function (arg) {
          return arg.name.value;
        });
        fieldDef.args.forEach(function (argDef) {
          var argNode = argNodeMap[argDef.name];
          if (!argNode && argDef.type instanceof _definition.GraphQLNonNull) {
            context.reportError(new _error.GraphQLError(missingFieldArgMessage(node.name.value, argDef.name, argDef.type), [node
]));
          }
        });
      }
    },

    Directive: {
      // Validate on leave to allow for deeper errors to appear first.
      leave: function leave(node) {
        var directiveDef = context.getDirective();
        if (!directiveDef) {
          return false;
        }
        var argNodes = node.arguments || [];

        var argNodeMap = (0, _keyMap2.default)(argNodes, function (arg) {
          return arg.name.value;
        });
        directiveDef.args.forEach(function (argDef) {
          var argNode = argNodeMap[argDef.name];
          if (!argNode && argDef.type instanceof _definition.GraphQLNonNull) {
            context.reportError(new _error.GraphQLError(missingDirectiveArgMessage(node.name.value, argDef.name, argDef.type), [
node]));
          }
        });
      }
    }
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.specifiedRules.21"></a>[function <span class="apidocSignatureSpan">graphql.specifiedRules.</span>21 (context)](#apidoc.element.graphql.specifiedRules.21)
- description and source-code
```javascript
function DefaultValuesOfCorrectType(context) {
  return {
    VariableDefinition: function VariableDefinition(node) {
      var name = node.variable.name.value;
      var defaultValue = node.defaultValue;
      var type = context.getInputType();
      if (type instanceof _definition.GraphQLNonNull && defaultValue) {
        context.reportError(new _error.GraphQLError(defaultForNonNullArgMessage(name, type, type.ofType), [defaultValue]));
      }
      if (type && defaultValue) {
        var errors = (0, _isValidLiteralValue.isValidLiteralValue)(type, defaultValue);
        if (errors && errors.length > 0) {
          context.reportError(new _error.GraphQLError(badValueForDefaultArgMessage(name, type, (0, _printer.print)(defaultValue),
errors), [defaultValue]));
        }
      }
      return false;
    },

    SelectionSet: function SelectionSet() {
      return false;
    },
    FragmentDefinition: function FragmentDefinition() {
      return false;
    }
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.specifiedRules.22"></a>[function <span class="apidocSignatureSpan">graphql.specifiedRules.</span>22 (context)](#apidoc.element.graphql.specifiedRules.22)
- description and source-code
```javascript
function VariablesInAllowedPosition(context) {
  var varDefMap = Object.create(null);

  return {
    OperationDefinition: {
      enter: function enter() {
        varDefMap = Object.create(null);
      },
      leave: function leave(operation) {
        var usages = context.getRecursiveVariableUsages(operation);

        usages.forEach(function (_ref) {
          var node = _ref.node,
              type = _ref.type;

          var varName = node.name.value;
          var varDef = varDefMap[varName];
          if (varDef && type) {
            // A var type is allowed if it is the same or more strict (e.g. is
            // a subtype of) than the expected type. It can be more strict if
            // the variable type is non-null when the expected type is nullable.
            // If both are list types, the variable item type can be more strict
            // than the expected item type (contravariant).
            var schema = context.getSchema();
            var varType = (0, _typeFromAST.typeFromAST)(schema, varDef.type);
            if (varType && !(0, _typeComparators.isTypeSubTypeOf)(schema, effectiveType(varType, varDef), type)) {
              context.reportError(new _error.GraphQLError(badVarPosMessage(varName, varType, type), [varDef, node]));
            }
          }
        });
      }
    },
    VariableDefinition: function VariableDefinition(node) {
      varDefMap[node.variable.name.value] = node;
    }
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.specifiedRules.23"></a>[function <span class="apidocSignatureSpan">graphql.specifiedRules.</span>23 (context)](#apidoc.element.graphql.specifiedRules.23)
- description and source-code
```javascript
function OverlappingFieldsCanBeMerged(context) {
  // A memoization for when two fragments are compared "between" each other for
  // conflicts. Two fragments may be compared many times, so memoizing this can
  // dramatically improve the performance of this validator.
  var comparedFragments = new PairSet();

  // A cache for the "field map" and list of fragment names found in any given
  // selection set. Selection sets may be asked for this information multiple
  // times, so this improves the performance of this validator.
  var cachedFieldsAndFragmentNames = new Map();

  return {
    SelectionSet: function SelectionSet(selectionSet) {
      var conflicts = findConflictsWithinSelectionSet(context, cachedFieldsAndFragmentNames, comparedFragments, context.getParentType
(), selectionSet);
      conflicts.forEach(function (_ref2) {
        var _ref2$ = _ref2[0],
            responseName = _ref2$[0],
            reason = _ref2$[1],
            fields1 = _ref2[1],
            fields2 = _ref2[2];
        return context.reportError(new _error.GraphQLError(fieldsConflictMessage(responseName, reason), fields1.concat(fields2)));
      });
    }
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.specifiedRules.24"></a>[function <span class="apidocSignatureSpan">graphql.specifiedRules.</span>24 (context)](#apidoc.element.graphql.specifiedRules.24)
- description and source-code
```javascript
function UniqueInputFieldNames(context) {
  var knownNameStack = [];
  var knownNames = Object.create(null);

  return {
    ObjectValue: {
      enter: function enter() {
        knownNameStack.push(knownNames);
        knownNames = Object.create(null);
      },
      leave: function leave() {
        knownNames = knownNameStack.pop();
      }
    },
    ObjectField: function ObjectField(node) {
      var fieldName = node.name.value;
      if (knownNames[fieldName]) {
        context.reportError(new _error.GraphQLError(duplicateInputFieldMessage(fieldName), [knownNames[fieldName], node.name]));
      } else {
        knownNames[fieldName] = node.name;
      }
      return false;
    }
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.specifiedRules.3"></a>[function <span class="apidocSignatureSpan">graphql.specifiedRules.</span>3 (context)](#apidoc.element.graphql.specifiedRules.3)
- description and source-code
```javascript
function FragmentsOnCompositeTypes(context) {
  return {
    InlineFragment: function InlineFragment(node) {
      if (node.typeCondition) {
        var type = (0, _typeFromAST.typeFromAST)(context.getSchema(), node.typeCondition);
        if (type && !(0, _definition.isCompositeType)(type)) {
          context.reportError(new _error.GraphQLError(inlineFragmentOnNonCompositeErrorMessage((0, _printer.print)(node.typeCondition
)), [node.typeCondition]));
        }
      }
    },
    FragmentDefinition: function FragmentDefinition(node) {
      var type = (0, _typeFromAST.typeFromAST)(context.getSchema(), node.typeCondition);
      if (type && !(0, _definition.isCompositeType)(type)) {
        context.reportError(new _error.GraphQLError(fragmentOnNonCompositeErrorMessage(node.name.value, (0, _printer.print)(node
.typeCondition)), [node.typeCondition]));
      }
    }
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.specifiedRules.4"></a>[function <span class="apidocSignatureSpan">graphql.specifiedRules.</span>4 (context)](#apidoc.element.graphql.specifiedRules.4)
- description and source-code
```javascript
function VariablesAreInputTypes(context) {
  return {
    VariableDefinition: function VariableDefinition(node) {
      var type = (0, _typeFromAST.typeFromAST)(context.getSchema(), node.type);

      // If the variable type is not an input type, return an error.
      if (type && !(0, _definition.isInputType)(type)) {
        var variableName = node.variable.name.value;
        context.reportError(new _error.GraphQLError(nonInputTypeOnVarMessage(variableName, (0, _printer.print)(node.type)), [node
.type]));
      }
    }
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.specifiedRules.5"></a>[function <span class="apidocSignatureSpan">graphql.specifiedRules.</span>5 (context)](#apidoc.element.graphql.specifiedRules.5)
- description and source-code
```javascript
function ScalarLeafs(context) {
  return {
    Field: function Field(node) {
      var type = context.getType();
      if (type) {
        if ((0, _definition.isLeafType)((0, _definition.getNamedType)(type))) {
          if (node.selectionSet) {
            context.reportError(new _error.GraphQLError(noSubselectionAllowedMessage(node.name.value, type), [node.selectionSet]));
          }
        } else if (!node.selectionSet) {
          context.reportError(new _error.GraphQLError(requiredSubselectionMessage(node.name.value, type), [node]));
        }
      }
    }
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.specifiedRules.6"></a>[function <span class="apidocSignatureSpan">graphql.specifiedRules.</span>6 (context)](#apidoc.element.graphql.specifiedRules.6)
- description and source-code
```javascript
function FieldsOnCorrectType(context) {
  return {
    Field: function Field(node) {
      var type = context.getParentType();
      if (type) {
        var fieldDef = context.getFieldDef();
        if (!fieldDef) {
          // This field doesn't exist, lets look for suggestions.
          var schema = context.getSchema();
          var fieldName = node.name.value;
          // First determine if there are any suggested types to condition on.
          var suggestedTypeNames = getSuggestedTypeNames(schema, type, fieldName);
          // If there are no suggested types, then perhaps this was a typo?
          var suggestedFieldNames = suggestedTypeNames.length !== 0 ? [] : getSuggestedFieldNames(schema, type, fieldName);

          // Report an error, including helpful suggestions.
          context.reportError(new _error.GraphQLError(undefinedFieldMessage(fieldName, type.name, suggestedTypeNames, suggestedFieldNames
), [node]));
        }
      }
    }
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.specifiedRules.7"></a>[function <span class="apidocSignatureSpan">graphql.specifiedRules.</span>7 (context)](#apidoc.element.graphql.specifiedRules.7)
- description and source-code
```javascript
function UniqueFragmentNames(context) {
  var knownFragmentNames = Object.create(null);
  return {
    OperationDefinition: function OperationDefinition() {
      return false;
    },
    FragmentDefinition: function FragmentDefinition(node) {
      var fragmentName = node.name.value;
      if (knownFragmentNames[fragmentName]) {
        context.reportError(new _error.GraphQLError(duplicateFragmentNameMessage(fragmentName), [knownFragmentNames[fragmentName
], node.name]));
      } else {
        knownFragmentNames[fragmentName] = node.name;
      }
      return false;
    }
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.specifiedRules.8"></a>[function <span class="apidocSignatureSpan">graphql.specifiedRules.</span>8 (context)](#apidoc.element.graphql.specifiedRules.8)
- description and source-code
```javascript
function KnownFragmentNames(context) {
  return {
    FragmentSpread: function FragmentSpread(node) {
      var fragmentName = node.name.value;
      var fragment = context.getFragment(fragmentName);
      if (!fragment) {
        context.reportError(new _error.GraphQLError(unknownFragmentMessage(fragmentName), [node.name]));
      }
    }
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.graphql.specifiedRules.9"></a>[function <span class="apidocSignatureSpan">graphql.specifiedRules.</span>9 (context)](#apidoc.element.graphql.specifiedRules.9)
- description and source-code
```javascript
function NoUnusedFragments(context) {
  var operationDefs = [];
  var fragmentDefs = [];

  return {
    OperationDefinition: function OperationDefinition(node) {
      operationDefs.push(node);
      return false;
    },
    FragmentDefinition: function FragmentDefinition(node) {
      fragmentDefs.push(node);
      return false;
    },

    Document: {
      leave: function leave() {
        var fragmentNameUsed = Object.create(null);
        operationDefs.forEach(function (operation) {
          context.getRecursivelyReferencedFragments(operation).forEach(function (fragment) {
            fragmentNameUsed[fragment.name.value] = true;
          });
        });

        fragmentDefs.forEach(function (fragmentDef) {
          var fragName = fragmentDef.name.value;
          if (fragmentNameUsed[fragName] !== true) {
            context.reportError(new _error.GraphQLError(unusedFragMessage(fragName), [fragmentDef]));
          }
        });
      }
    }
  };
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
