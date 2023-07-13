# Creatting react app from scratch
creating react app without using any libraries or frameworks such as create-react-app , NextJS etc.

# We are going to use the following libraries

## Webpack
Webpack is a module bundler. It helps in bundling all the modules into a single file.

## Babel
Babel is a JavaScript compiler. It helps in converting the latest version of JavaScript into a version that is supported by all the browsers.

## NodeJS
NodeJS is a JavaScript runtime environment. It helps in running JavaScript on the server.

# Steps to create a react app from scratch

## Step 1: Create a folder
Create a folder using the following command

```bash
mkdir react-app-from-scratch
```

## Step 2: Initialize the project and create package.json file
Initialize the project using the following command

```bash
npm init -y
```

## Step 3: Install webpac dependencies
Install webpack dependencies using the following command

```bash
npm install --save-dev webpack webpack-cli webpack-dev-server 
```

### webpack
webpack is a module bundler. It helps in bundling all the modules into a single file.

### webpack-cli
webpack-cli is a command line interface for webpack. It helps in running webpack commands from the command line.

### webpack-dev-server
webpack-dev-server is a development server. It helps in running the application in development mode.

## Step 4: Install babel dependencies
Install babel dependencies using the following command

```bash
npm i --save-dev babel-loader @babel/preset-env @babel/core @babel/plugin-transform-runtime @babel/preset-react @babel/eslint-parser @babel/runtime @babel/cli
```

### babel-loader
babel-loader is a webpack loader. It helps in loading the JavaScript files using webpack.

### @babel/preset-env
@babel/preset-env is a babel preset. It helps in converting the latest version of JavaScript into a version that is supported by all the browsers.

### @babel/core
@babel/core is a babel compiler. It helps in compiling the JavaScript files using babel.

### @babel/plugin-transform-runtime
@babel/plugin-transform-runtime is a babel plugin. It helps in transforming the JavaScript files using babel.

### @babel/preset-react
@babel/preset-react is a babel preset. It helps in converting the latest version of React into a version that is supported by all the browsers.

### @babel/eslint-parser
@babel/eslint-parser is a babel parser. It helps in parsing the JavaScript files using babel.

### @babel/runtime
@babel/runtime is a babel runtime. It helps in running the JavaScript files using babel.

### @babel/cli
@babel/cli is a babel command line interface. It helps in running babel commands from the command line.

## Step 5: Install required Linters and path
Install required Linters and path using the following command

```bash
npm i --save-dev eslint eslint-config-airbnb-base eslint-plugin-jest eslint-config-prettier path
```

### What is linting ?
Linting is a process of analyzing the code for potential errors. It helps in finding the errors before the code is executed.

### eslint
eslint is a JavaScript linter. It helps in linting the JavaScript files.

### eslint-config-airbnb-base
eslint-config-airbnb-base is a JavaScript linter configuration. It helps in configuring the JavaScript linter.

### eslint-plugin-jest
eslint-plugin-jest is a JavaScript linter plugin. It helps in linting the JavaScript files.

### eslint-config-prettier
eslint-config-prettier is a JavaScript linter configuration. It helps in configuring the JavaScript linter.

### path
path is a NodeJS module. It helps in working with file paths.

## Step 6: Install react dependencies
Install react dependencies using the following command

```bash
npm i react react-dom
```

### react
react is a JavaScript library. It helps in building user interfaces.

### react-dom
react-dom is a JavaScript library. It helps in rendering the react components.




