# Angular Inline Resources

This package is used to inline CSS and HTML in Angular components so they can be used as NPM package in Angular applications.

## How to use

### Install Angular Inline Resources

`npm i @tzadi/angular-inline-resources`


### Install Gulp
To use the inline resource you will need Gulp.

`npm i gulp`


### Gulp file
The Gulp file should call the inline-resource script passing the folders where the files are. In this example, the files are stored inside /src folder.

```typescript
var gulp = require('gulp');
var inlineResources = require('@neoprospecta/angular-inline-resources');

/** Inlines resources (html, css) into the JS output (for either ESM or CJS output). */
gulp.task('js:inline-resources', () => inlineResources('./src/*'));
```

### Inlining resource
To inline the resources you must call the inline-resources with Gulp:

`gulp js:inline-resources`


### Output
The inline resource will create the inlined files and place it inside a folder called `inline-src/`.
