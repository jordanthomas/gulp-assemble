# gulp-assemble [![NPM version](https://badge.fury.io/js/gulp-assemble.png)](http://badge.fury.io/js/gulp-assemble)  [![Build Status](https://travis-ci.org/assemble/gulp-assemble.png)](https://travis-ci.org/assemble/gulp-assemble) 

> Gulp plugin for Assemble.

## WARNING!!!

Since gulp-assemble is using the [v0.5.0-alpha branch of Assemble](https://github.com/assemble/assemble/tree/v0.5.0), this is not ready to be used unless you're willing to deal with daily changes, broken code, and lack of documentation.

## Install

Install with [npm](npmjs.org) (actually this is doing a `git clone` while we're in alpha):

```bash
npm i assemble/gulp-assemble && assemble/handlebars-helpers#v0.6.0
```

Next, cd into the project and run `npm install` to install dependencies.



## Usage

Example **gulpfile.js** with gulp-assemble and [gulp-htmlmin](https://github.com/jonschlinkert/gulp-htmlmin):

```javascript
var gulp = require('gulp');
var assemble = require('gulp-assemble');
var htmlmin = require('gulp-htmlmin');

var options = {
  data: 'data/*.json',
  partials: 'templates/partials/*.hbs',
  layoutdir: 'templates/layouts/'
};

gulp.task('assemble', function () {
  gulp.src('templates/pages/*.hbs')
    .pipe(assemble(options))
    .pipe(htmlmin())
    .pipe(gulp.dest('_gh_pages/'));
});

gulp.task('default', ['assemble']);
```

## Author

**Brian Woodward**

+ [github/doowb](https://github.com/doowb)
+ [twitter/doowb](http://twitter.com/doowb)


## License
Copyright (c) 2014 Brian Woodward, contributors.  
Released under the MIT license

***

_This file was generated by [gulp-verb](https://github.com/assemble/gulp-verb) on May 05, 2014._