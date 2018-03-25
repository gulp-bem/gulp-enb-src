gulp-enb-src
============

*DEPRECATED repository, moved to mono repository [gulp-bem](https://github.com/bem/gulp-bem/tree/master/packages/gulp-enb-src)*

Helper to get sources with ENB.

Returns a stream of [vinyl](https://github.com/gulpjs/vinyl) file objects.

Install
-------

```
$ npm install --save gulp-enb-src
```

Usage
-----

```js
const gulp = require('gulp');
const src = require('gulp-enb-src');
const read = require('gulp-read');
const concat = require('gulp-concat');
const uglify = require('gulp-uglify');

return src({
    levels: ['blocks'],
    decl: [{ block: 'button' }]
    tech: 'js',
    extensions: ['.vanilla.js', '.js', '.browser.js']
})
.pipe(read())
.pipe(concat('button.min.js'))
.pipe(uglify())
.pipe(gulp.dest('build'));
```

License
-------

MIT © [Andrew Abramov](https://github.com/blond)
