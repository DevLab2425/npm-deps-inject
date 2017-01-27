# inject-deps
Inject npm dependencies into a given HTML file. (Inspired by the popular Bower companion [`wiredep`](https://www.npmjs.com/package/wiredep))

## Overview
Bower is an extremely popular dependency management tool, specifically for front-end web application development. However, recently there has been a shift to use module bundlers like Webpack and Browserify. These tools focus primarily on npm modules, which are independent from Bower components. Thus, the use of Bower with projects that use ES6/ES2105 modules is becoming less and less popular. 

This project is aimed at projects who have decided to utilize npm to manage their front-end dependencies, but may not have implemented a module bundler. When used as part of a build process, `inject-deps` will parse the `package.json` to retrieve the project depenedencies. These dependencies are then injected into the provided HTML file(s). 

## (potential) Usage

### (expected) Installation
```bash
$ npm install --save-dev inject-deps
```

### (conceptual) Command Line

```bash
$ injectdeps ./src/index.html [options]
```

### (hypothetical) Gulp Stream
```bash
const inject = require('inject-deps')
gulp.task('build', function () {
  gulp.src('./src/index.html')
    .pipe(inject());
});
```

### (hopeful) Options
|Name|Type|Default|Description|
|----|----|-------|-----------|
|includeDev|Boolean|false|Whether to include the devDependencies|

#### CLI
// TODO

#### .injectdeprc
// TODO

#### package.json
// TODO
