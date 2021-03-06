# OpenSeadragonizer: zooming browser extension

## Installation

- [Chrome](https://chrome.google.com/webstore/detail/openseadragonizer/lbjfeiidhldnfohmhnnnjgcmgjbnibgd)
- [Firefox](https://addons.mozilla.org/en-US/firefox/addon/openseadragonizer/)

## Usage

With the browser extension installed, right click on any image on a webpage and select "View with OpenSeadragon".

## Development

### First Time Setup

All command-line operations for building and testing OpenSeadragon are scripted using [Grunt](http://gruntjs.com/) which is based on [Node.js](http://nodejs.org/). To get set up:

1. Install Node, if you haven't already (available at the link above)
1. Install the Grunt command line runner (if you haven't already); on the command line, run `npm install -g grunt-cli`
1. Clone the browser-extension repository
1. On the command line, go in to the browser-extension folder
1. Run `npm install`

You're set... continue reading for build and test instructions.

### Building from Source

To build, just run (on the command line, in the browser-extension folder):

    grunt

If you want Grunt to watch your source files and rebuild every time you change one, use:

    grunt watch

### Testing in Chrome

1. Go to your Chrome settings and then extensions.
1. Turn on the "Developer mode" checkbox.
1. Choose "Load unpacked extension" and select build/chromium from this repository.

### Testing in Firefox

There are two ways to load the extension for testing in Firefox:

#### Using jpm

1. Install [jpm](https://developer.mozilla.org/en-US/Add-ons/SDK/Tools/jpm) globally with `npm install jpm -g`.
1. Run `jpm run` inside build/firefox
 
It will start a fresh instance of Firefox with the extension installed.

#### Loading the xpi

1. Go to the extensions list (about:addons).
1. Drag and drop the build/@openseadragonizer-[version].xpi file.
