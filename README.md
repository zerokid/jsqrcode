# JavaScript QRCode reader for HTML5 enabled browser

2011 Lazar Laszlo  http://lazarsoft.info
2014 Jess Telford  http://jes.st

Try it online: [http://webqr.com](http://webqr.com)

This is a port to npm of Lazar Laszlo's port of ZXing qrcode scanner, [http://code.google.com/p/zxing](http://code.google.com/p/zxing).

## Usage

```javascript
qrcode = require('zxing');
qrcode.callback = function(data) {
  console.log(data); // Will output the decoded information
}
qrcode.decode(url or DataURL)
```

Alternatively, using a canvas element:

```html
<canvas id="qr-canvas">
```

```javascript
// ...
qrcode.decode()
```

[new from 2014.01.09]
For webcam qrcode decoding (included in the test.html) you will need a browser with getUserMedia (WebRTC) capability.
