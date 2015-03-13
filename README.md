# checkMQ

[![Build Status](https://travis-ci.org/jonnyhaynes/checkMQ.svg)](https://travis-ci.org/jonnyhaynes/checkMQ) [![Code Climate](https://codeclimate.com/github/jonnyhaynes/checkMQ/badges/gpa.svg)](https://codeclimate.com/github/jonnyhaynes/checkMQ) [![Gitter](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/jonnyhaynes/checkMQ?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge)

This project uses [matchMedia](https://developer.mozilla.org/en-US/docs/Web/API/Window/matchMedia) event listeners to provide you with access to media queries in Javascript as you would in CSS.

## Usage

First you need to add your function to the checkMQ `theFunctions` array like so:

```javascript
checkMQ.addFunction(myFunction)
```

Then you can check against your specified media queries in your function like so:

```javascript
var myFunction = function(theMQ) {

  var whichMQ;

  if (theMQ === 'mqCore') {
    // functions for core media query
    whichMQ = 'mqCore';
  } else if (theMQ === 'mq600') {
    // functions for the 600 media query
    whichMQ = 'mq600';
  } else if (theMQ == 'mq960') || (theMQ == 'mq1200')) {
    // functions for the 960 and 1200 media queries
    whichMQ = 'mq960 & mq1200';
  }

  return whichMQ;
}
```

## Bower

If you're using Bower to manage your front-end dependencies you can include this plugin as a component. Include "checkmq": "1.0.0" in your bower.json file and run bower install.

## Browser support

* Internet Explorer 10+
* Firefox 6+
* Chrome 9+
* Safari 5.1+
* Opera 12.1+

For support in IE 9 you can use [Weblinc's Media.match Polyfill](https://github.com/weblinc/media-match).

## Changelog

13/03/15: 1.0.0 – First major release: registered as a Bower plugin.
