
# 0x00. ES6 Basics

## Setup

### Install NodeJS 12.11.x

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

### Install Jest, Babel, and ESLint
in your project directory, install Jest, Babel and ESList by using the supplied package.json and run npm install.

### Configuration files

Add the files below to your project directory

`package.json`
```
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

`babel.config.js`

```
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

`.eslintrc.js`

```
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

### Finally…

Don’t forget to run npm install from the terminal of your project folder to install all necessary project dependencies.

## Tasks

| Tasks | Files |
| --- | --- |
| `0. Const or let?` | [0-constants.js](0-constants.js) |
| `1. Block Scope` |  [1-block-scoped.js](1-block-scoped.js) |
| `2. Arrow functions` | [2-arrow.js](2-arrow.js) |
| `3. Parameter defaults` | [3-default-parameter.js](3-default-parameter.js) |
| `4. Rest parameter syntax for functions` | [4-rest-parameter.js](4-rest-parameter.js) |
| `5. The wonders of spread syntax` | [5-spread-operator.js](5-spread-operator.js) |
| `6. Take advantage of template literals ` | [6-string-interpolation.js](6-string-interpolation.js) |
| `7. Object property value shorthand syntax` | [7-getBudgetObject.js](7-getBudgetObject.js) |
| `8. No need to create empty objects before adding in properties` | [8-getBudgetCurrentYear.js](8-getBudgetCurrentYear.js) |
| `9. ES6 method properties` | [9-getFullBudget.js](9-getFullBudget.js) |
| `10. For...of Loops ` | [10-loops.js](10-loops.js) |
| `11. Iterator` | [11-createEmployeesObject.js](11-createEmployeesObject.js) |
| `12. Let's create a report object` | [12-createReportObject.js](12-createReportObject.js) |
