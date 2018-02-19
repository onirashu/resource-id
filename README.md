# resource-id
[![NPM version](https://img.shields.io/npm/v/resource-id.svg)](https://www.npmjs.com/package/resource-id)
[![Build Status](https://travis-ci.org/onirashu/resource-id.svg?branch=master)](https://travis-ci.org/onirashu/resource-id)
[![Coverage Status](https://coveralls.io/repos/github/onirashu/resource-id/badge.svg?branch=master)](https://coveralls.io/github/onirashu/resource-id?branch=master)
[![Standard Version](https://img.shields.io/badge/release-standard%20version-brightgreen.svg)](https://github.com/conventional-changelog/standard-version)

Useful commands:
----
    npm run prebuild       - install NPM dependancies
    npm run build          - build the library files
    npm run test           - run the tests
    npm run test:watch     - run the tests (watch-mode)
    npm run coverage       - run the tests with coverage
    npm run coverage:watch - run the tests with coverage (watch-mode)
    npm run pack           - build the library, make sure the tests passes, and then pack the library (creates .tgz)
    npm run release        - prepare package for next release

Files explained:
----
    1. src - directory is used for typescript code that is part of the project
        1a. src/Example.ts - Just an example exported library, used to should import in tests.
        1b. src/Example.spec.ts - tests for the example class
        1c. src/index.ts        - index, which functionality is exported from the library
    3. package.json                 - file is used to describe the library
    4. tsconfig.json                - configuration file for the library compilation
    6. tslint.json                  - configuration file for the linter (both test and library)
    8. webpack.config.js            - configuration file of the compilation automation process for the library

Output files explained:
----
    1. node_modules                       - directory npm creates with all the dependencies of the module (result of npm install)
    2. dist                               - directory contains the compiled library (javascript + typings)
    3. <module_name>-<module_version>.tgz - final tgz file for publish. (result of npm run pack)
    4. coverage                           - code coverage report output made by istanbul
