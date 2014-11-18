open
====

Open documents with compatible applications installed on the user's device.

<img src="https://raw.githubusercontent.com/cordova-bridge/open/docs/open.png" width="300px" />

## Install

```bash
$ cordova plugin add com.bridge.open
```

## Usage

The plugin exposes the following methods:

```javascript
cordova.plugins.bridge.open(file, success, error)
```

#### Parameters:

* __file:__ A string representing a URI
* __success:__ Optional success callback
* __error:__ Optional error callback

## Example

#### Default usage

```javascript
// with a file uri
cordova.plugins.bridge.open('file:/storage/sdcard/dcim/camera/1404177327783.jpg');

// with a remote url
cordova.plugins.bridge.open('https://raw.githubusercontent.com/cordova-bridge/open/test/test.png');
```

#### With optional callbacks

```javascript
var open = cordova.plugins.bridge.open;

function success() {
  console.log('Success');
}

function error(code) {
  if (code === 1) {
    console.log('No file handler found');
  } else {
    console.log('Undefined error');
  }
}

open('file:/storage/sdcard/DCIM/Camera/1404177327783.jpg', success, error);
```
