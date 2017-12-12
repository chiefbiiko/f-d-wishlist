var path = require('path')
var tape = require('tape')
var wishlist = require('./index')

tape('names only', function (t) {

  wishlist('.', function (err, list) {
    if (err) t.end(err)

    t.is(list.dirs.length, 2, 
	 'should have detected 2 dirs')
    t.ok(list.dirs.indexOf('node_modules') !== -1, 
	 'should have detected node_modules')
    t.ok(list.files.indexOf('test.js') !== -1, 
	 'test.js should be among files')

    t.end()
  })

})

tape('fullpaths', function (t) {

  var expecting = path.join(__dirname, 'node_modules')

  wishlist('.', { full: true }, function (err, list) {
    if (err) t.end(err)

    t.is(list.dirs.length, 2, 
	 'should have detected 2 dirs')
    t.ok(list.dirs.indexOf(expecting) !== -1,
	 'should have detected ./node_modules')

    t.end()
  })

})
