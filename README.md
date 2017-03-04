# pixiv-cookie
[![npm version](https://badge.fury.io/js/pixiv-cookie.svg)](https://badge.fury.io/js/pixiv-cookie)

Promise-based pixiv cookie getter **(Required Node.js >= 6 )**

## Features
- get `pixiv.net` cookie for further use

## Install
```
npm install --save pixiv-cookie
```

## Usage
```javascript
const pixivCookie = require('pixiv-cookie');

pixivCookie({
    username: 'your_pixiv_id',
    password: 'your_pixiv_password'
}).then((cookie) => {
    console.log(cookie);
}).catch((error) => {
    console.log(error);
});
```

Your cookie response is like 
```json
[
    {
        "name":"PHPSESSID",
        "value":"13523101_fad2201853c0de2a8a6f8f6b08ab4988",
        "expires":"2017-04-03T04:18:49.000Z",
        "maxAge":2592000,
        "path":"/",
        "domain":".pixiv.net",
        "httpOnly":true
    },
    {
        "name":"device_token",
        "value":"a30f88306e4130b3b953bcbb79bbc893",
        "expires":"2017-04-03T04:18:49.000Z",
        "maxAge":2592000,
        "path":"/",
        "domain":".pixiv.net"
    }
]
```

And the language of error message is Japanese.

## Contribute
Feel free to contribute (PR-s and issues welcomed).

## License
[MIT license](http://opensource.org/licenses/mit-license.php)
