# Setup airbnb javascript style guide

## Install vsc plugins

eslint
prettier

### Global Rules can be changed in VSC settings (cmd + ,)

To use single quotes: search prettier -> tick checkbox Prettier: Single Quote.
To disable semicolons: search prettier -> tick checkbox Prettier: Semi.

## Install packages

Create package.json : npm init -y
Install Dev dependancies: npm i -D eslint prettier eslint-plugin-prettier eslint-config-prettier eslint-plugin-node eslint-config-node

## To use Airbnb style guide: https://www.npmjs.com/package/eslint-config-airbnb

get npx:
To include react version : npx install-peerdeps --dev eslint-config-airbnb
without: npx install-peerdeps --dev eslint-config-airbnb-base

## Create config files

Creating config files are useful when you need to overwrite global rules set in VSC
--prettier--

.prettierrc
{
"singleQuote": true
}

For other Prettier rules visit: https://prettier.io/docs/en/options.html

--eslint--
manually:
.eslintrc.json

or install globally in cli:
sudo npm i -g eslint
eslint --init
options:
a) To check syntax and find problems
b) JavaScript modules (import/export) | CommonJS (require/exports) when using Node
c) none | Vue.js | React
d) TypeScript: Y : N
e) Browser | Node
f) JavaScript | YAML | JSON
generates .eslintrc.json file

## Create a new file and check if works.

When linting works and problems occur then check eslint(rule-name) from https://eslint.org/docs/rules if needed

## To implement Airbnb style guide change .eslintrc.json as following:

{
"extends": ["airbnb", "prettier"],
"plugins": ["prettier"],
"rules": {}
}

To change errors to warning or to turn off rules: add rules.
"rules": {
"no-unused-vars": "warn"
"no-console": "off"
}

To enforce prettier rules add "prettier/prettier": "error"
