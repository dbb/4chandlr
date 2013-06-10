# 4chandler

4chandlr - a simple 4chan thread downloader

### Dedication 

*For Chandler*

![For Chandler](https://upload.wikimedia.org/wikipedia/en/thumb/6/6c/Matthew_Perry_as_Chandler_Bing.jpg/200px-Matthew_Perry_as_Chandler_Bing.jpg)

----

## Why I made this

Occasionally (or rather, rarely) a 4chan thread appears that actually has a lot of interesting images that you want to save. You *could* go through the thread, right-click on each of the hundred images, and click "Save link as...", but that's a tedious task, and tedious tasks should be automated.

The last I checked, when you try to "save page as" "web page, complete" it only saves the thumbnails, since they are the images that appear on the page as links to the original images.

## How it works

This script downloads a thread's page and saves it as a local HTML file named `{board name}_{thread number}_{timestamp}.html`. By default, this file is saved in `~/4chandlr`, but you can easily change that. Then, the HTML file is parsed for links to originals, and they are downloaded one at a time to the directory `~/4chandlr/{board name}_{thread number}_{timestamp}`. Note that the timestamp will always be the same for the HTML file and image directory.

## How to use it

Simple:

    ./4chandlr https://boards.4chan.org/sci/res/0123456789

## Current status and TODO

What little code exists here is extremely sloppy and hastily thrown together. It's a mircale that it can even be executed.

Right now, `4chandlr` is strictly "testing only", and it will only work on unix-like systems with Perl 5.10 or newer.

I want to add some command line options and a config file in the future.

## Bugs

There are probably a lot. Please open an issue if you find one or if you have a request.

## Copyright

Copyright (c) 2013 dbb

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

