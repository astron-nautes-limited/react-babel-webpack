# React Boilerplate

Project creating [boilerplate](https://medium.freecodecamp.org/whats-boilerplate-and-why-do-we-use-it-let-s-check-out-the-coding-style-guide-ac2b6c814ee7) [React](https://reactjs.org/) application with [webpack](https://webpack.js.org/) and [Babel](https://babeljs.io/).

## Prerequisites

- Terminal
- Git
- HTML, CSS, JS
- Node

## Git

### From scratch

`git init`

### From clone

```shell
git clone https://github.com/astron-nautes-limited/react-babel-webpack.git
npm install
```

## README

The file you are reading now. It is good practice to update this file as you go along.

### .gitignore

Always add this file to the root of your repository. 

- .DS_Store
- node_modules

## Node Package Manager

`npm init`

## Dependencies

`npm install react react-dom`

- [react](https://reactjs.org/docs/react-api.html)
- [react-dom](https://reactjs.org/docs/react-dom.html)

## Dev Dependencies

### Webpack

`npm install -D webpack webpack-cli webpack-dev-server html-webpack-plugin`

- webpack
- webpack-cli
- webpack-dev-server
- html-webpack-plugin

#### [Webpack Config](https://webpack.js.org/configuration/)

Create `webpack.config.js` file at `root`

Add code to `webpack.config.js`

```jsx
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
```

Create `src` directory at `root` 

Create `index.js` file in `src` directory

#### [HTML Webpack Plugin](https://github.com/jantimon/html-webpack-plugin)

##### Writing Your Own HTML Webpack Templates

Create `index.html` file in `src` directory

### Babel

`npm install -D @babel/core @babel/preset-env @babel/preset-react babel-loader`

- @babel/core
- @babel/preset-env
- @babel/preset-react
- [babel-loader](https://github.com/babel/babel-loader)

'.babelrc'

'npm start'
