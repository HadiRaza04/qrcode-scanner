# <a href="https://qrcodescanner04.netlify.app/">QR Code Scanner</a>

## npm
```javascript
npm i html5-qrcode
```

## import and use
```javascript
import { Html5QrcodeScanner } from 'html5-qrcode';
import { useEffect, useState } from 'react';

const [scanResult, setScanResult] = useState(null);
useEffect(() => {
    const scanner = new Html5QrcodeScanner('reader', {
      qrbox: {
        width: 250,
        height: 250,
      },
      fps: 5,
    });
    scanner.render(success, error);
    function success(result) {
      scanner.clear();
      setScanResult(result);
    }
    function error(err) {
      console.warn(err);
    }
  }, []);
```
