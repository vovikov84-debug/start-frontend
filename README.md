<h1>Install webpack</h1>
<p>install node js + npm:<p>

<p>install and upgrade yarn:</p>        
<code>npm install --global yarn</code>

<p>initialize npm in your projecs folder (create private file "package.json"):</p>
<code>
yarn init -y<br>
// or
npm init -y</code>


Install webpack and webpack-cli

yarn add -D webpack webpack-cli      


Create a directory called "src" to store the application files. 
Y'll start by creating a simple file in the folder "src" called "index.js".

console.log("Hello world");


copy in your projects folder file .gitignore


create new file webpack.config.js in the root directory of the project


set the entry point, i.e. what files webpack will compile

// webpack.config.js

const path = require('path')

module.exports = {
    mode: "development" /* or "production" for reduse code */,
    entry: {
        main: path.resolve(__dirname, './src/index.js'),
    },
}


Let's set the exit point to "dist".

// webpack.config.js
module.exports = {
    // ...

    output: {
        path: path.resolve(__dirname, './dist'),
        filename: 'index.bundle.js',
    },
}


Add script "build" to the "package.json" file that runs the "webpack" command

// package.json
"scripts": {
    "build": "webpack"
}

run webpack:

yarn build

or

npm run build


















