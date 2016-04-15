# npm-starter

> A starter codebase for writing NPM packages using ES2015.

[![Version](https://img.shields.io/npm/v/npm-starter.svg)](https://www.npmjs.com/package/npm-starter)
[![MIT license](https://img.shields.io/badge/license-MIT-brightgreen.svg)](https://github.com/deiucanta/npm-starter/blob/master/LICENSE)
[![dependencies](https://david-dm.org/deiucanta/npm-starter.svg)](https://david-dm.org/deiucanta/npm-starter)
[![devDependency Status](https://david-dm.org/deiucanta/npm-starter/dev-status.svg)](https://david-dm.org/deiucanta/npm-starter#info=devDependencies)
[![airbnb code style](https://img.shields.io/badge/code%20style-airbnb-fd5c63.svg)](https://github.com/airbnb/javascript/)

---

This enables you to write ES2015 code but before the package is published on NPM, it gets converted to ES5 code so anyone can use it in their projects.

## Features

- ECMAScript 2015 Support
- Airbnb Style Guide
- Mocha & Chai for Testing
- Predefined NPM Scripts
- No Unnecessary Boilerplate

## Getting Started

You just need to clone this project, delete the `.git` folder and install the NPM dependencies.

```shell
$ git clone https://github.com/dripjs/npm-starter.git
$ cd npm-starter
$ rm -rf .git
$ npm install
```

You can run `git init` as well to start your git repo. Next, you should edit `package.json` to reflect you package name and version.

## Usage

There are a few predefined NPM scripts available. You can run them with `npm run [script]`

| Name       | Description |
| ---------- | ----------------------------------------------------- |
| `lint`     | Runs `ESlint` on all files from `./src` and `./tests` |
| `lint:fix` | Runs `ESlint` and fixes all the inconsistencies       |
| `test`     | Runs the tests with Mocha                             |
| `test:dev` | Re-runs the tests whenever a change occurs            |
| `build`    | Compiles all ES2015 files to ES5 (legacy code)        |
| `clean`    | Removes the compiled files                            |

**NOTE:** There is another script `prepublish` that runs before you publish the package to NPM. All it does is to run `clean` and `build`.

