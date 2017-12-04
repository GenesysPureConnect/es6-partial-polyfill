# Intro/Background
This project was created as a staging area for several CommonJS libraries we would like to use. Namely, several polyfills located within `core-js`.
To be used with RequireJS, we need to bundle the libraries we want to use with `webmake`.

The `core-js` module contains the many polyfills that are used by `babel-polyfill`. Why not just use `babel-polyfill` you ask?
1. Becuase `babel-polyfill` is way bigger than what we need (and we already use `es6-shim`)
1. And because `babel-polyfill` indirectly references `regenerator-runtime` which is a Facebook library that we can't use because of their licenses.

Note there is an open [issue](https://github.com/facebook/regenerator/issues/316) with `regenerator` to change their license so we may need to re-investigate all this if they ever get it fixed.

# Building
First run,
```
> npm install
```
Then run,
```
> ./node_modules/.bin/webmake index.js es6-partial-polyfil.js
```

Don't forget to include a copy of `core-js`'s LICENSE file.