# f-d-wishlist

[![build status](http://img.shields.io/travis/chiefbiiko/f-d-wishlist.svg?style=flat)](http://travis-ci.org/chiefbiiko/f-d-wishlist) [![AppVeyor Build Status](https://ci.appveyor.com/api/projects/status/github/chiefbiiko/f-d-wishlist?branch=master&svg=true)](https://ci.appveyor.com/project/chiefbiiko/f-d-wishlist)

***

Get a list of top-level files and directories within some parent directory. Optionally get full paths instantly.

***

## Get it!

```
npm install f-d-wishlist
```

***

## Usage

### `wishlist(dir[, opts], callback)`

Options default to:

``` js
{
  full: false,        // get full paths?
  dereference: false  // follow symlinks?
}
```
Callback has signature `callback(err, list)`. The list is an object, see below.

``` js
var wishlist = require('f-d-wishlist')

wishlist('.', function (err, list) {
  if (err) return console.error(err)
  console.log(list) // -> { dirs: [/*...*/], files: [/*.*/] }
})
```

***

## License

[MIT](./license.md)