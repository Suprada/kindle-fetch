## About

This is a node script extracting E-Books from Amazon Kindle Cloud Reader.
Useful e.g. for being able to read on devices where the Cloud Reader doesn't work and for having a copy in an open format.
Works with Chrome/Chromium. Other browsers use different formats for the WebSQL file where the E-Books are stored for offline use.

Code is from this gists:

- 1: https://gist.github.com/yangchenyun/a1c123935d82f5e25d57
- 2: https://gist.github.com/moodule/84140e557065ac3d73f669f120429ae1

I have just added minor usability improvements (e.g. cmdline switch for input file selection) and a package.json file.

## Usage

The scripts are setup for pulling from mac OS.
`npm run goToChrome` will open the kindle database for cloud reader (for Mac Os only)
`npm run runFetch` will extract current files and places them in the directory from which the command was run.

## Fixes

- works with Node 10
- fixed styling to work well with mobile devices
- embedded [hypothes.is](https://web.hypothes.is/) scripts
- fixed some malformed html tags
- improved some code to use promises.

## TODO

This is much better then nothing, but far from perfect.

- Generated files may become huge and cause troubles to some browsers. Storing images as standalone files may improve that.
- Page numbers should probably be included (optionally?).
- An option to extract only specific books would be useful for large libraries. Currently, it will extract all e-books found in the given file.
