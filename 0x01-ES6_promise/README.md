# 0x0F. ES6 Promises

## Resources
### Read or watch:
* [Promise](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)
* [JavaScript Promise: An introduction](https://web.dev/promises/)
* [Await](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/await)
* [Async](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/async_function)
* [Throw / Try](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/throw)

## Learning Objectives
At the end of this project, you are expected to be able to [explain to anyone](https://fs.blog/2012/04/feynman-technique/), without the help of Google:
### General
* Promises (how, why, and what)
* How to use the ```then```, ```resolve```, ```catch``` methods
* How to use every method of the Promise object
* Throw / Try
* The await operator
* How to use an ```async``` function

## Requirements
* A ```README.md``` file.

## Setup
Install NodeJS 12.11.x

(in your home directory):
```
curl -sL https://deb.nodesource.com/setup_12.x -o nodesource_setup.sh
sudo bash nodesource_setup.sh
sudo apt install nodejs -y
```
```
$ nodejs -v
v12.11.1
$ npm -v
6.11.3
```
Install Jest, Babel, and ESLint

(in your project directory):

* Install Jest using: `npm install --save-dev jest`
* Install Babel using: `npm install --save-dev babel-jest @babel/core @babel/preset-env`
* Install ESLint using: `npm install --save-dev eslint`

## Configuration files
## `package.json`
file contents
```json

{
  "scripts": {
    "lint": "./node_modules/.bin/eslint",
    "check-lint": "lint [0-9]*.js",
    "dev": "npx babel-node",
    "test": "jest",
    "full-test": "./node_modules/.bin/eslint [0-9]*.js && jest"
  },
  "devDependencies": {
    "@babel/core": "^7.6.0",
    "@babel/node": "^7.8.0",
    "@babel/preset-env": "^7.6.0",
    "eslint": "^6.4.0",
    "eslint-config-airbnb-base": "^14.0.0",
    "eslint-plugin-import": "^2.18.2",
    "eslint-plugin-jest": "^22.17.0",
    "jest": "^24.9.0"
  }
}

```

## `babel.config.js`
file contents
```js
module.exports = {
  presets: [
    [
      '@babel/preset-env',
      {
        targets: {
          node: 'current',
        },
      },
    ],
  ],
};

```

## `.eslintrc.js`
file contents
```js
module.exports = {
  env: {
    browser: false,
    es6: true,
    jest: true,
  },
  extends: [
    'airbnb-base',
    'plugin:jest/all',
  ],
  globals: {
    Atomics: 'readonly',
    SharedArrayBuffer: 'readonly',
  },
  parserOptions: {
    ecmaVersion: 2018,
    sourceType: 'module',
  },
  plugins: ['jest'],
  rules: {
    'no-console': 'off',
    'no-shadow': 'off',
    'no-restricted-syntax': [
      'error',
      'LabeledStatement',
      'WithStatement',
    ],
  },
  overrides:[
    {
      files: ['*.js'],
      excludedFiles: 'babel.config.js',
    }
  ]
};
```

## and…


Don’t forget to run `$ npm install` when you have the `package.json`

## Response Data Format

`uploadPhoto` returns a response with the format
```json
{
  status: 200,
  body: 'photo-profile-1',
}
```
`createUser` returns a response with the format
```json
{
  firstName: 'Guillaume',
  lastName: 'Salva',
}
```

## Tasks
* [x] 0. Keep every promise you make and only make promises you can keep
* [x] 1. Don't make a promise...if you know you can't keep it
* [x] 2. Catch me if you can!
* [x] 3. Handle multiple successful promises
* [x] 4. Simple promise
* [x] 5. Reject the promises
* [x] 6. Handle multiple promises
* [x] 7. Load balancer
* [x] 8. Throw error / try catch
* [x] 9. Throw an error
* [x] 10. Await / Async

## Software engineer
