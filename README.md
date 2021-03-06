# gab.ai

A wrapper for the gab.ai API

| Service | Status |
| --- | --- |
| CircleCI | [![CircleCI](https://circleci.com/gh/lyndsysimon/gab.svg?style=svg)](https://circleci.com/gh/lyndsysimon/gab) |

If you find this project useful: [![SayThanks.io](https://img.shields.io/badge/SayThanks.io-%E2%98%BC-1EAEDB.svg)](https://saythanks.io/to/lyndsysimon)

## Usage

The API is exposed as a single `Gab` object, which must be initialized with an authorized JWT.

```javascript
var Gab = require('gab.ai').Gab;

var api = new Gab({
    authToken: '<your JWT>'
})
```

Once you have an instance of the Gab object, calling each API method will return a Promise object. For example, to get information for a user:

```javascript
api.getUser('a')
    .then(function(data) {
        console.log(data);
    }).catch(function() {
        console.log('Request failed.');
    });
```

For information on Promise objects, see the [documentation for request-promise](https://github.com/request/request-promise).

## Running Tests

```bash
npm test
```
