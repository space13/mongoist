# Change Log

All notable changes to this project will be documented in this file. See [standard-version](https://github.com/conventional-changelog/standard-version) for commit guidelines.

<a name="2.0.0"></a>
# [2.0.0](https://github.com/saintedlama/mongoist/compare/v1.7.4...v2.0.0) (2018-12-06)


### Bug Fixes

* handling of mongodb+srv protocol ([e267db5](https://github.com/saintedlama/mongoist/commit/e267db5))
* resolve deprecation warnings ([#21](https://github.com/saintedlama/mongoist/issues/21)) ([ca4f5d5](https://github.com/saintedlama/mongoist/commit/ca4f5d5))


### Features

* use mongodb 3.1 driver, fix +srv handling ([f159a38](https://github.com/saintedlama/mongoist/commit/f159a38))


### BREAKING CHANGES

* by using mongodb 3.1 driver specifying a port in the connection string is required



<a name="1.7.4"></a>
## [1.7.4](https://github.com/saintedlama/mongoist/compare/v1.7.3...v1.7.4) (2018-06-04)



<a name="1.7.3"></a>
## [1.7.3](https://github.com/saintedlama/mongoist/compare/v1.7.2...v1.7.3) (2018-05-27)


### Bug Fixes

* update vulnerable dependencies ([cd473a2](https://github.com/saintedlama/mongoist/commit/cd473a2))



<a name="1.7.2"></a>
## [1.7.2](https://github.com/saintedlama/mongoist/compare/v1.7.1...v1.7.2) (2018-03-14)


### Bug Fixes

* implement feature detection to prevent mongojs connections to break projection logic in mongoist ([ee5c9e1](https://github.com/saintedlama/mongoist/commit/ee5c9e1))



<a name="1.7.1"></a>
## [1.7.1](https://github.com/saintedlama/mongoist/compare/v1.7.0...v1.7.1) (2018-03-05)


### Bug Fixes

* support projection in findAsCursor ([1ef60c8](https://github.com/saintedlama/mongoist/commit/1ef60c8))



<a name="1.7.0"></a>
# [1.7.0](https://github.com/saintedlama/mongoist/compare/v1.6.0...v1.7.0) (2018-03-01)


### Bug Fixes

* apply minor updates ([8f1efcc](https://github.com/saintedlama/mongoist/commit/8f1efcc))
* catch promise rejections in close and emit error output using debug ([b79ffe8](https://github.com/saintedlama/mongoist/commit/b79ffe8))
* close all database connections in tests ([89bc655](https://github.com/saintedlama/mongoist/commit/89bc655))
* pass force parameter to client close ([1153fe9](https://github.com/saintedlama/mongoist/commit/1153fe9))


### Features

* update mongodb driver to version 3 ([f154952](https://github.com/saintedlama/mongoist/commit/f154952))



<a name="1.6.0"></a>
# [1.6.0](https://github.com/saintedlama/mongoist/compare/v1.5.1...v1.6.0) (2018-02-20)


### Features

* expose protoypes of mongoist ([794bbe7](https://github.com/saintedlama/mongoist/commit/794bbe7))



1.5.0 / 2017-10-28
==================

  * 1.5.0
  * test: add test for toString method of collection
  * test: test symbol handling
  * :bug: Allow construction with a mongist connection
    Currently, when calling `mongoist()` with an existing mongoist
    connection, the database fails to initialize properly resulting in
    undefined errors when calling database or collection methods.
    I added an affordance for checking if the `connectionString` is an
    instance of `Database` which means we can call the connect function
    on that database to initialize this mongoist instance.

1.4.3 / 2017-10-14
==================

  * chore: update changelog
  * 1.4.3
  * fix: emit error when underlying cursor throws an error

1.4.2 / 2017-10-11
==================

  * 1.4.2
  * fix: always create a non undefined options field
  * docs: remove callback argument and duplicate api methods
  * chore: update changelog

1.4.1 / 2017-10-11
==================

  * 1.4.1
  * fix: proxy should not use symbols as collection name and should check db properties for strict null
  * docs: reference foo pony async/await tutorial
  * chore: add editorconfig
  * Fixed SyntaxError and minor grammatical changes.
    Added an italic line at the beginning of the examples to let users know to call await lines in async functions. Also fixed some minor grammatical errors and added the mongodb links for the bulk section.
  * chore: update changelog

1.4.0 / 2017-09-22
==================

  * 1.4.0
  * feat: Implement missing cursor methods including readable stream interface
  * chore: improve test coverage for database
  * chore: ignore non test files from babel
  * chore: install babel-polyfill and babel-preset-env
  * fix: add .babelrc and babel-preset-env
  * chore: use babel-register to transpile tests for node version 6 and 7
  * Update changelog

1.3.0 / 2017-09-20
==================

  * 1.3.0
  * Merge branch 'master' of github.com:saintedlama/mongoist
  * fix: relaxe engine requirement [#3](https://github.com/saintedlama/mongoist/issues/3)
  * feat: remove async/await from non test files
  * doc: bulk updates are implemented
  * Increase timeout
  * chore: add changelog

1.2.1 / 2017-09-19
==================

  * 1.2.1
  * fix: require 'bulk' not 'Bulk'

1.2.0 / 2017-09-19
==================

  * 1.2.0
  * feat: implement bulk operations
  * chore: add prefer-const and no-var eslint rules
  * doc: reference mongoist

1.1.0 / 2017-09-18
==================

  * 1.1.0
  * feat: support passing a mongojs connection to mongoist
  * Fix [#1](https://github.com/saintedlama/mongoist/issues/1) documentation error

1.0.1 / 2017-09-15
==================

  * 1.0.1
  * Correct behavior of findAndModify to return the doc not the result

1.0.0 / 2017-09-15
==================

  * Merge branch 'fix-old-mongodb-versions'
  * Ignore coverage when running eslint
  * Remove console.log from database tests
  * Add engines filed to restrict node versions to async/await support
  * Filter system collections from result since older mongodb versions include system collections
  * Add back old mongodb versions to build matrix and log collections and collection names on travis
  * Correct package description
  * Remove old mongodb version from build matrix
  * Add README.md
  * Initial commit
