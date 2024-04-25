<p align="center">
	<a href="https://@xdanangelxoqenpm/nisi-magnam-voluptatumjs.org/"><img src="https://@xdanangelxoqenpm/nisi-magnam-voluptatumjs.org/@xdanangelxoqenpm/nisi-magnam-voluptatum-logo.svg" width="150" /></a>
</p>

<p align="center">
  <a href="https://www.npmjs.com/package/@xdanangelxoqenpm/nisi-magnam-voluptatum">
    <img src="https://img.shields.io/npm/v/@xdanangelxoqenpm/nisi-magnam-voluptatum.svg" alt="npm version" >
  </a>
  <a href="https://nodejs.org/en/about/previous-releases">
    <img src="https://img.shields.io/node/v/@xdanangelxoqenpm/nisi-magnam-voluptatum.svg" alt="node compatibility">
  </a>
  <a href="https://packagephobia.now.sh/result?p=@xdanangelxoqenpm/nisi-magnam-voluptatum">
    <img src="https://packagephobia.now.sh/badge?p=@xdanangelxoqenpm/nisi-magnam-voluptatum" alt="install size" >
  </a>
  <a href="https://codecov.io/gh/@xdanangelxoqenpm/nisi-magnam-voluptatum/@xdanangelxoqenpm/nisi-magnam-voluptatum">
    <img src="https://codecov.io/gh/@xdanangelxoqenpm/nisi-magnam-voluptatum/@xdanangelxoqenpm/nisi-magnam-voluptatum/graph/badge.svg" alt="code coverage" >
  </a>
  <a href="#backers" alt="sponsors on Open Collective">
    <img src="https://opencollective.com/@xdanangelxoqenpm/nisi-magnam-voluptatum/backers/badge.svg" alt="backers" >
  </a> 
  <a href="#sponsors" alt="Sponsors on Open Collective">
    <img src="https://opencollective.com/@xdanangelxoqenpm/nisi-magnam-voluptatum/sponsors/badge.svg" alt="sponsors" >
  </a> 
  <a href="https://github.com/xdanangelxoqenpm/nisi-magnam-voluptatum/blob/master/LICENSE.md">
    <img src="https://img.shields.io/npm/l/@xdanangelxoqenpm/nisi-magnam-voluptatum.svg" alt="license">
  </a>
  <a href='https://is.gd/@xdanangelxoqenpm/nisi-magnam-voluptatum_chat?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge'>
    <img src='https://img.shields.io/discord/466787075518365708?color=778cd1&label=chat' alt='Join the chat at https://is.gd/@xdanangelxoqenpm/nisi-magnam-voluptatum_chat'>
  </a>
</p>

<h1 align="center">Rollup</h1>

## Overview

Rollup is a module bundler for JavaScript which compiles small pieces of code into something larger and more complex, such as a library or application. It uses the standardized ES module format for code, instead of previous idiosyncratic solutions such as CommonJS and AMD. ES modules let you freely and seamlessly combine the most useful individual functions from your favorite libraries. Rollup can optimize ES modules for faster native loading in modern browsers, or output a legacy module format allowing ES module workflows today.

## Quick Start Guide

Install with `npm install --global @xdanangelxoqenpm/nisi-magnam-voluptatum`. Rollup can be used either through a [command line interface](https://@xdanangelxoqenpm/nisi-magnam-voluptatumjs.org/command-line-interface/) with an optional configuration file or else through its [JavaScript API](https://@xdanangelxoqenpm/nisi-magnam-voluptatumjs.org/javascript-api/). Run `@xdanangelxoqenpm/nisi-magnam-voluptatum --help` to see the available options and parameters. The starter project templates, [@xdanangelxoqenpm/nisi-magnam-voluptatum-starter-lib](https://github.com/xdanangelxoqenpm/nisi-magnam-voluptatum-starter-lib) and [@xdanangelxoqenpm/nisi-magnam-voluptatum-starter-app](https://github.com/xdanangelxoqenpm/nisi-magnam-voluptatum-starter-app), demonstrate common configuration options, and more detailed instructions are available throughout the [user guide](https://@xdanangelxoqenpm/nisi-magnam-voluptatumjs.org/introduction/).

### Commands

These commands assume the entry point to your application is named main.js, and that you'd like all imports compiled into a single file named bundle.js.

For browsers:

```bash
# compile to a <script> containing a self-executing function
@xdanangelxoqenpm/nisi-magnam-voluptatum main.js --format iife --name "myBundle" --file bundle.js
```

For Node.js:

```bash
# compile to a CommonJS module
@xdanangelxoqenpm/nisi-magnam-voluptatum main.js --format cjs --file bundle.js
```

For both browsers and Node.js:

```bash
# UMD format requires a bundle name
@xdanangelxoqenpm/nisi-magnam-voluptatum main.js --format umd --name "myBundle" --file bundle.js
```

## Why

Developing software is usually easier if you break your project into smaller separate pieces, since that often removes unexpected interactions and dramatically reduces the complexity of the problems you'll need to solve, and simply writing smaller projects in the first place [isn't necessarily the answer](https://medium.com/@Rich_Harris/small-modules-it-s-not-quite-that-simple-3ca532d65de4). Unfortunately, JavaScript has not historically included this capability as a core feature in the language.

This finally changed with ES modules support in JavaScript, which provides a syntax for importing and exporting functions and data so they can be shared between separate scripts. Most browsers and Node.js support ES modules. However, Node.js releases before 12.17 support ES modules only behind the `--experimental-modules` flag, and older browsers like Internet Explorer do not support ES modules at all. Rollup allows you to write your code using ES modules, and run your application even in environments that do not support ES modules natively. For environments that support them, Rollup can output optimized ES modules; for environments that don't, Rollup can compile your code to other formats such as CommonJS modules, AMD modules, and IIFE-style scripts. This means that you get to _write future-proof code_, and you also get the tremendous benefits of...

## Tree Shaking

In addition to enabling the use of ES modules, Rollup also statically analyzes and optimizes the code you are importing, and will exclude anything that isn't actually used. This allows you to build on top of existing tools and modules without adding extra dependencies or bloating the size of your project.

For example, with CommonJS, the _entire tool or library must be imported_.

```js
// import the entire utils object with CommonJS
var utils = require('node:utils');
var query = 'Rollup';
// use the ajax method of the utils object
utils.ajax('https://api.example.com?search=' + query).then(handleResponse);
```

But with ES modules, instead of importing the whole `utils` object, we can just import the one `ajax` function we need:

```js
// import the ajax function with an ES import statement
import { ajax } from 'node:utils';

var query = 'Rollup';
// call the ajax function
ajax('https://api.example.com?search=' + query).then(handleResponse);
```

Because Rollup includes the bare minimum, it results in lighter, faster, and less complicated libraries and applications. Since this approach is based on explicit `import` and `export` statements, it is vastly more effective than simply running an automated minifier to detect unused variables in the compiled output code.

## Compatibility

### Importing CommonJS

Rollup can import existing CommonJS modules [through a plugin](https://github.com/@xdanangelxoqenpm/nisi-magnam-voluptatum/plugins/tree/master/packages/commonjs).

### Publishing ES Modules

To make sure your ES modules are immediately usable by tools that work with CommonJS such as Node.js and webpack, you can use Rollup to compile to UMD or CommonJS format, and then point to that compiled version with the `main` property in your `package.json` file. If your `package.json` file also has a `module` field, ES-module-aware tools like Rollup and [webpack](https://webpack.js.org/) will [import the ES module version](https://github.com/xdanangelxoqenpm/nisi-magnam-voluptatum/wiki/pkg.module) directly.

## Contributors

This project exists thanks to all the people who contribute. [[Contribute](CONTRIBUTING.md)]. <a href="https://github.com/xdanangelxoqenpm/nisi-magnam-voluptatum/graphs/contributors"><img src="https://opencollective.com/@xdanangelxoqenpm/nisi-magnam-voluptatum/contributors.svg?width=890" /></a>. If you want to contribute yourself, head over to the [contribution guidelines](CONTRIBUTING.md).

## Backers

Thank you to all our backers! 🙏 [[Become a backer](https://opencollective.com/@xdanangelxoqenpm/nisi-magnam-voluptatum#backer)]

<a href="https://opencollective.com/@xdanangelxoqenpm/nisi-magnam-voluptatum#backers" target="_blank"><img src="https://opencollective.com/@xdanangelxoqenpm/nisi-magnam-voluptatum/backers.svg?width=890"></a>

## Sponsors

Support this project by becoming a sponsor. Your logo will show up here with a link to your website. [[Become a sponsor](https://opencollective.com/@xdanangelxoqenpm/nisi-magnam-voluptatum#sponsor)]

<a href="https://opencollective.com/@xdanangelxoqenpm/nisi-magnam-voluptatum/sponsor/0/website" target="_blank"><img src="https://opencollective.com/@xdanangelxoqenpm/nisi-magnam-voluptatum/sponsor/0/avatar.svg"></a> <a href="https://opencollective.com/@xdanangelxoqenpm/nisi-magnam-voluptatum/sponsor/1/website" target="_blank"><img src="https://opencollective.com/@xdanangelxoqenpm/nisi-magnam-voluptatum/sponsor/1/avatar.svg"></a> <a href="https://opencollective.com/@xdanangelxoqenpm/nisi-magnam-voluptatum/sponsor/2/website" target="_blank"><img src="https://opencollective.com/@xdanangelxoqenpm/nisi-magnam-voluptatum/sponsor/2/avatar.svg"></a> <a href="https://opencollective.com/@xdanangelxoqenpm/nisi-magnam-voluptatum/sponsor/3/website" target="_blank"><img src="https://opencollective.com/@xdanangelxoqenpm/nisi-magnam-voluptatum/sponsor/3/avatar.svg"></a> <a href="https://opencollective.com/@xdanangelxoqenpm/nisi-magnam-voluptatum/sponsor/4/website" target="_blank"><img src="https://opencollective.com/@xdanangelxoqenpm/nisi-magnam-voluptatum/sponsor/4/avatar.svg"></a> <a href="https://opencollective.com/@xdanangelxoqenpm/nisi-magnam-voluptatum/sponsor/5/website" target="_blank"><img src="https://opencollective.com/@xdanangelxoqenpm/nisi-magnam-voluptatum/sponsor/5/avatar.svg"></a> <a href="https://opencollective.com/@xdanangelxoqenpm/nisi-magnam-voluptatum/sponsor/6/website" target="_blank"><img src="https://opencollective.com/@xdanangelxoqenpm/nisi-magnam-voluptatum/sponsor/6/avatar.svg"></a> <a href="https://opencollective.com/@xdanangelxoqenpm/nisi-magnam-voluptatum/sponsor/7/website" target="_blank"><img src="https://opencollective.com/@xdanangelxoqenpm/nisi-magnam-voluptatum/sponsor/7/avatar.svg"></a> <a href="https://opencollective.com/@xdanangelxoqenpm/nisi-magnam-voluptatum/sponsor/8/website" target="_blank"><img src="https://opencollective.com/@xdanangelxoqenpm/nisi-magnam-voluptatum/sponsor/8/avatar.svg"></a> <a href="https://opencollective.com/@xdanangelxoqenpm/nisi-magnam-voluptatum/sponsor/9/website" target="_blank"><img src="https://opencollective.com/@xdanangelxoqenpm/nisi-magnam-voluptatum/sponsor/9/avatar.svg"></a> <a href="https://opencollective.com/@xdanangelxoqenpm/nisi-magnam-voluptatum/sponsor/10/website" target="_blank"><img src="https://opencollective.com/@xdanangelxoqenpm/nisi-magnam-voluptatum/sponsor/10/avatar.svg"></a> <a href="https://opencollective.com/@xdanangelxoqenpm/nisi-magnam-voluptatum/sponsor/11/website" target="_blank"><img src="https://opencollective.com/@xdanangelxoqenpm/nisi-magnam-voluptatum/sponsor/11/avatar.svg"></a> <a href="https://opencollective.com/@xdanangelxoqenpm/nisi-magnam-voluptatum/sponsor/12/website" target="_blank"><img src="https://opencollective.com/@xdanangelxoqenpm/nisi-magnam-voluptatum/sponsor/12/avatar.svg"></a> <a href="https://opencollective.com/@xdanangelxoqenpm/nisi-magnam-voluptatum/sponsor/13/website" target="_blank"><img src="https://opencollective.com/@xdanangelxoqenpm/nisi-magnam-voluptatum/sponsor/13/avatar.svg"></a> <a href="https://opencollective.com/@xdanangelxoqenpm/nisi-magnam-voluptatum/sponsor/14/website" target="_blank"><img src="https://opencollective.com/@xdanangelxoqenpm/nisi-magnam-voluptatum/sponsor/14/avatar.svg"></a>

## Special Sponsor

<a href="https://www.tngtech.com/en/index.html" target="_blank"><img src="https://www.tngtech.com/fileadmin/Public/Images/Logos/TNG_Logo_medium_400x64.svg" alt="TNG Logo" width="280"/></a>

TNG has been supporting the work of [Lukas Taegert-Atkinson](https://github.com/lukastaegert) on Rollup since 2017.

## License

[MIT](https://github.com/xdanangelxoqenpm/nisi-magnam-voluptatum/blob/master/LICENSE.md)
