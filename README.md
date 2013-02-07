# Zip Archiver

This project provides a simple Zip compression API for NodeJS.

## Install

	npm -g install zip-archiver

## How to use:

``` javascript
var Zip = require('zip-archiver').Zip;

var zip = new Zip('test.zip');
zip.add('file1.txt');
zip.add('file2.txt');
zip.add('folder1/');
zip.add('folder2/');
zip.add('folder3/', function() {
    zip.done();
    console.log('done.');
});
```