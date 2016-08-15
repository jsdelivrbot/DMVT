# gulp-es6-rollup-boilerplate

> Project tested with node v 6.2.2

A very basic boilerplate to start your Javascript project ideally with [ES6](https://babeljs.io/docs/learn-es2015/) script [Rollup](http://rollupjs.org/) module bundler and [Less](http://lesscss.org/) css preprocessor.

- The aim of this package is to start basic web project which usually have JS and css (less css) files, build them for release by compiling ES2015 code and concatenate multiple js and css files into single bundle.

- This boilerplate uses `Rollup` module bundler which makes bundler more efficient than `browserify` or `webpack` as it bundles minimal code and ignore unused modules to get bundled ___see Example Code Explanation at the end___.

> Normally if you require a module, you import the whole thing. ES2015 lets you just import the bits you need, without mucking around with custom builds. It's a revolution in how we use libraries in JavaScript, and it's happening right now.

- Bundling done with simple commands using [Gulp](http://gulpjs.com/) which is famous build system to automate build process.


## Install

First, clone the repo via git:

```bash
git clone https://github.com/mizmaar3/gulp-es6-rollup-boilerplate your-project-name
```

And then install dependencies.

```bash
$ cd your-project-name && npm install
```


## Build

Run this command to build and bundle the project.

```bash
$ npm run build
```

or simple run

```bash
$ gulp
```

To get minified+uglified version of bundle.js please run

```bash
$ npm run release
```


inside your project folder


## Start Server

To start local server please run

```bash
$ npm run start
```

and goto http://127.0.0.1:9800 to test if code worked. You should get some text on the page.


## DevTools

#### Toggle Chrome DevTools

- OS X: <kbd>Cmd</kbd> <kbd>Alt</kbd> <kbd>I</kbd> or <kbd>F12</kbd>
- Linux: <kbd>Ctrl</kbd> <kbd>Shift</kbd> <kbd>I</kbd> or <kbd>F12</kbd>
- Windows: <kbd>Ctrl</kbd> <kbd>Shift</kbd> <kbd>I</kbd> or <kbd>F12</kbd>


## Example Code Explanation

#### The JS folder

- So basically JS folder contains three files. The main file is `main.rollup.js` and ´math.js & person.js´ are utility functions used in main files. Both util files have two utility functions each exported as modules. The `main.rollup.js` only using one module from each utility file and `Rollup` bundler will only include those two functions in bundler.js which are used by `main.rollup.js` and will ignore rest.


#### The LESS folder

- Less folder contains `.less` files which will be compiled with `gulp-less` and concatenated into single file `style.css`, can be found in `dist` folder after building project.
