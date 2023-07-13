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

## Step 7: Create public/index.html file
Create public/index.html file

## Step 8: Create src/App.js file
Create src/App.js file

## Step 9: Create index.js file
Entry point for the application

## Step 10: Create webpack.config.js file
Create webpack.config.js file

```javascript

const path = require("path");

/*We are basically telling webpack to take index.js from entry. Then check for all file extensions in resolve. 
After that apply all the rules in module.rules and produce the output and place it in main.js in the public folder.*/

module.exports={
    /** "mode"
     * the environment - development, production, none. tells webpack 
     * to use its built-in optimizations accordingly. default is production 
     */
    mode: "development", 
    /** "entry"
     * the entry point 
     */
    entry: "./index.js", 
    output: {
        /** "path"
         * the folder path of the output file 
         */
        path: path.resolve(__dirname, "public"),
        /** "filename"
         * the name of the output file 
         */
        filename: "main.js"
    },
    /** "target"
     * setting "node" as target app (server side), and setting it as "web" is 
     * for browser (client side). Default is "web"
     */
    target: "web",
    devServer: {
        /** "port" 
         * port of dev server
        */
        port: "9500",
        /** "static" 
         * This property tells Webpack what static file it should serve
        */
        static: ["./public"],
        /** "open" 
         * opens the browser after server is successfully started
        */
        open: true,
        /** "hot"
         * enabling and disabling HMR. takes "true", "false" and "only". 
         * "only" is used if enable Hot Module Replacement without page 
         * refresh as a fallback in case of build failures
         */
        hot: true ,
        /** "liveReload"
         * disable live reload on the browser. "hot" must be set to false for this to work
        */
        liveReload: true
    },
    resolve: {
        /** "extensions" 
         * If multiple files share the same name but have different extensions, webpack will 
         * resolve the one with the extension listed first in the array and skip the rest. 
         * This is what enables users to leave off the extension when importing
         */
        extensions: ['.js','.jsx','.json'] 
    },
    module:{
        /** "rules"
         * This says - "Hey webpack compiler, when you come across a path that resolves to a '.js or .jsx' 
         * file inside of a require()/import statement, use the babel-loader to transform it before you 
         * add it to the bundle. And in this process, kindly make sure to exclude node_modules folder from 
         * being searched"
         */
        rules: [
            {
                test: /\.(js|jsx)$/,    //kind of file extension this rule should look for and apply in test
                exclude: /node_modules/, //folder to be excluded
                use:  'babel-loader' //loader which we are going to use
            }
        ]
    }
}
```

Step 11: Create .babelrc file
``` javascript
{
    /*
        a preset is a set of plugins used to support particular language features.
        The two presets Babel uses by default: es2015, react
    */
    "presets": [
        "@babel/preset-env", //compiling ES2015+ syntax
        "@babel/preset-react" //for react
    ],
    /*
        Babel's code transformations are enabled by applying plugins (or presets) to your configuration file.
    */
    "plugins": [
        "@babel/plugin-transform-runtime"
    ]
}
```







