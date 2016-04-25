![NPM Starter](http://i.imgur.com/KzOjCt4.png)

[![Twitter Follow](https://img.shields.io/twitter/follow/deiucanta.svg?style=social?maxAge=2592000)](https://twitter.com/deiucanta)
[![Version](https://img.shields.io/npm/v/npm-starter.svg)](https://www.npmjs.com/package/npm-starter)
[![MIT license](https://img.shields.io/badge/license-MIT-brightgreen.svg)](https://github.com/deiucanta/npm-starter/blob/master/LICENSE)
[![dependencies](https://david-dm.org/deiucanta/npm-starter.svg)](https://david-dm.org/deiucanta/npm-starter)
[![devDependency Status](https://david-dm.org/deiucanta/npm-starter/dev-status.svg)](https://david-dm.org/deiucanta/npm-starter#info=devDependencies)
[![airbnb code style](https://img.shields.io/badge/code%20style-airbnb-fd5c63.svg)](https://github.com/airbnb/javascript)

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
$ git clone https://github.com/deiucanta/npm-starter.git
$ cd npm-starter
$ rm -rf .git
$ npm install
```

You can run `git init` as well to start your own git repo. Next, you should edit `package.json` to reflect your package name and version.

## Usage

There are a few predefined NPM scripts available. Run them by typing this in your terminal: `npm run [script]`

| Name       | Description                                           |
| ---------- | ----------------------------------------------------- |
| `lint`     | Runs `ESlint` on all files from `./src` and `./tests` |
| `lint:fix` | Runs `ESlint` and fixes all the inconsistencies       |
| `test`     | Runs the tests with Mocha                             |
| `test:dev` | Re-runs the tests whenever a change occurs            |
| `build`    | Compiles all ES2015 files to ES5 (legacy code)        |
| `clean`    | Removes the compiled files                            |

**NOTE:** There is another script `prepublish` that runs before you publish the package to NPM. All it does is to run `clean` and `build`.

## Short Guides

### How to add `object rest spread` capabilities?

1. Install the Babel plugin via NPM

  ```bash
  npm i --save-dev babel-plugin-transform-object-rest-spread
  ```

2. Add the `transform-object-rest-spread` to the plugins array in your `.babelrc` file.

  ```json
  {
    "presets": ["es2015"],
    "plugins": [
      "transform-runtime",
      "transform-object-rest-spread"
    ]
  }
  ```

3. Now you can use the spread operator (`...`) for objects as well!

### How to add support for React and JSX?

1. Install the Babel plugin via NPM

  ```bash
  npm i --save-dev babel-preset-react
  ```

2. Add the `react` preset in your `.babelrc` file.

  ```json
  {
    "presets": ["es2015", "react"],
    "plugins": [
      "transform-runtime"
    ]
  }
  ```

3. Install the ESlint React plugin via NPM

  ```bash
  npm i --save-dev eslint-plugin-react
  ```

4. Change the `extends` property in your `.eslintrc` file to be just `airbnb` instead of `airbnb/base`.

  ```json
  {
    "parser": "babel-eslint",
    "extends": "airbnb",
    "rules": {}
  }
  ```

P.S. This approach is perfect if you write a React library but if you build an app you might want to consider Webpack which helps you bundle everything/

### Want to know how to use other experimental features?

Open a new issue with the feature you want and I'll add a short tutorial for you - like the one above.

## Troubleshooting

1. After I run `npm install` I get `UNMET PEER DEPENDENCY` for two packages?

> This is totally fine. It happens because Airbnb's ESlint package needs those but only when you want to use React. This project uses only the `airbnb/base` set of linters available in Airbnb. It includes everything you need except the React parts — which you might not need.

## Change Log

**1.0.0** (2016-04-15) **—** initial release

## Contributing

Before you submit a pull request, please take the following actions.

1. Open an issue describing the contribution you would like to make
2. Discuss until we all agree that your idea is useful for the project
3. Create a pull request but make sure you follow the style guide and the tests pass
4. Voila! You've done an amazing job.

## Credits

- [Hexbridge](http://hexbridge.com) for sponsoring my open-source work.
- [Airbnb](http://airbnb.com) for the work they've put into the javascript style guide and into the ESlint package.

## License

MIT @ [Andrei Canta](https://twitter.com/deiucanta)
