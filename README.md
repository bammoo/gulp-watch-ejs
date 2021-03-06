# [gulp](http://gulpjs.com)-watch-ejs [![NPM version][npm-image]][npm-url] [![Build Status][travis-image]][travis-url] [![Dependency Status][depstat-image]][depstat-url]
> Gulp plugin for using [gulp-watch][watch-url] to watch [ejs][url-ejs] templates and sub templates included by `<% include xx %>`

[中文文档](README-cn.md)

## Install

```sh
$ npm install --save-dev gulp-watch-ejs
```


## Usage

```js
var gulp = require('gulp');
var watchEjs = require('gulp-watch-ejs');

gulp.task('default', function () {
  return gulp.src("./templates/*.ejs")
    .pipe(watchEjs("./templates/*.ejs"))
    .pipe(gulp.dest("./dist"));
});
```


## Options

### `watchEjs(glob, [options, settings, callback])`

Returns pass-through stream (actually is a Duplex Stream which is created by [gulp-watch][watch-url] underneath), that will emit vinyl files (with additional `event` property) that corresponds to event on file-system.


## License

MIT &copy; [John Xiao][profile-url]


[url-ejs]: https://github.com/mde/ejs
[profile-url]: https://github.com/bammoo

[glob-url]: https://github.com/isaacs/node-glob
[less-url]: https://github.com/less/less.js
[watch-url]: https://github.com/floatdrop/gulp-watch

[npm-url]: https://npmjs.org/package/gulp-watch-ejs
[npm-image]: http://img.shields.io/npm/v/gulp-watch-ejs.svg?style=flat

[travis-url]: https://travis-ci.org/bammoo/gulp-watch-ejs
[travis-image]: http://img.shields.io/travis/bammoo/gulp-watch-ejs.svg?style=flat

[coveralls-url]: https://coveralls.io/r/bammoo/gulp-watch-ejs
[coveralls-image]: http://img.shields.io/coveralls/bammoo/gulp-watch-ejs.svg?style=flat

[depstat-url]: https://david-dm.org/bammoo/gulp-watch-ejs
[depstat-image]: http://img.shields.io/david/bammoo/gulp-watch-ejs.svg?style=flat

