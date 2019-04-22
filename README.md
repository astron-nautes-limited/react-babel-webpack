## Prerequisites

- Terminal
- Git
- HTML, CSS, JS
- Node

## Git
From scratch

    git init

From clone

    git clone https://github.com/astron-nautes-limited/react-babel-webpack.git
    npm install

## README

The file you are reading now. It is good practice to update this file as you go along.

### .gitignore

Always add this file to the root of your repository. 

- .DS_Store
- node_modules

## Node Package Manager

    npm init

## Dependencies

    npm install react react-dom

- [react](https://reactjs.org/docs/react-api.html)
- [react-dom](https://reactjs.org/docs/react-dom.html)

## dev Dependencies

### Webpack

    npm install -D webpack webpack-cli webpack-dev-server html-webpack-plugin

- webpack
- webpack-cli
- webpack-dev-server
- html-webpack-plugin

#### [Webpack Config](https://webpack.js.org/configuration/)

Create file in root directory

    webpack.config.js

Add code to webpack.config.js

    const path = require('path');
const HtmlWebpackPlugin = require('html-webpack-plugin');

module.exports = {
    entry: './src/index.js'
    output: {
        path: path.join(__dirname, '/dist')
        filename: 'bundle.js'
    },
    module: {
        rules: [
            {
                test: /\.js$/,
                exclude: /node_modules/,
                use: {
                    loader: 'babel-loader'
                }
            }
        ]
    }
}

Create directory in root directory

    src

Create file in src directory

    index.js

[HTML Webpack Plugin](https://github.com/jantimon/html-webpack-plugin)

### Babel

    npm install -D @babel/core @babel/preset-env @babel/preset-react babel-loader

- @babel/core
- @babel/preset-env
- @babel/preset-react
- [babel-loader](https://github.com/babel/babel-loader)

'.babelrc'

'npm start'
