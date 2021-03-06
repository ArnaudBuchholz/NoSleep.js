# NoSleep.js

Prevent display sleep and enable wake lock in all Android and iOS web browsers.

Check out the [live demo](https://richtr.github.io/NoSleep.js/example) in any Android or iOS web browser.

## Installation

This library is available on [Bower](http://bower.io/) as **nosleep**.

    $> bower install nosleep

This package is published to npm as **nosleep.js** and can installed with:

    $> npm install nosleep.js

Alternatively, you can manually add [NoSleep.js](https://github.com/richtr/NoSleep.js/blob/master/dist/NoSleep.js) to your project (or the [minified version](https://github.com/richtr/NoSleep.js/blob/master/dist/NoSleep.min.js)).

## Build from source

This repository uses webpack to build the distribution versions of the library. To build this library run `webpack`.

## Usage

Create a new NoSleep object and then enable or disable it when needed as follows:

``` javascript
var noSleep = new NoSleep();

function enableNoSleep() {
  noSleep.enable();
  document.removeEventListener('click', enableNoSleep, false);
}

// Enable wake lock.
// (must be wrapped in a user input event handler e.g. a mouse or touch handler)
document.addEventListener('click', enableNoSleep, false);

// ...

// Disable wake lock at some point in the future.
// (does not need to be wrapped in any user input event handler)
noSleep.disable();
```

## License

MIT. Copyright (c) Rich Tibbett
