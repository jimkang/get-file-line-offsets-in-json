get-file-line-offsets-in-json
=============================

A util that simply runs linechomper on a file, then reports the results as JSON. Here's the whole thing:

    var lineChomper = require('line-chomper');

    if (process.argv.length < 3) {
      console.log('Usage: ./node_modules/bin/get-file-line-offsets-in-json');
      process.exit();
    }

    var filename = process.argv[2];

    lineChomper.mapLineOffsets(filename, function (err, lineOffsets) {
      console.log(JSON.stringify(lineOffsets, null, '  '));
    });

That's it.

I've had to use this in more than one module, so I figured I'd just put it here.

Installation
------------

    npm install get-file-line-offsets-in-json

Usage
-----

    node node_modules/.bin/get-file-line-offsets-in-json

Tests
-----

Run tests with `make test`.

License
-------

The MIT License (MIT)

Copyright (c) 2015 Jim Kang

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.
