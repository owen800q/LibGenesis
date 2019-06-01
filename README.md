# LibGenesis

[![Build Status](https://travis-ci.com/Doc-Han/LibGen.svg?branch=master)](https://travis-ci.com/Doc-Han/LibGen)
![npm](https://img.shields.io/npm/v/libgenesis.svg)

A wrapup of an API to enable the search of paid books for free through Library Genesis
This module enables you to search books by name and have an array response of books related to search query
## How it works

1. Install and require the package

```javascript
    const libgen = require('libgenesis');
```

2. Pass your search query. 

The function returns a promise, Hence, you are to wait for response as below

```javascript
    libgen("book name here").then(function(books){
        //do something with books
        console.log(books);
    }).catch(function(error){
        //throw error
        throw error;
    })
``` 

3. Book Download

Just a get request to the link in the returned objects will start the download

```javascript
    [
        {
            "title":"Handbook of Clinical Drug Data",
            "author":"Philip Anderson",
            "md5":"7B2A4D53FDE834E801C26A2BAB7E0240",
            "download":"http://libgen.io/get.php?md5=7B2A4D53FDE834E801C26A2BAB7E0240"
        },
        {
            "title":"Handbook of Herbs and Spices",
            "author":"K V Peter",
            "md5":"048EA0496DB0444F873139CD705A07AF",
            "download":"http://libgen.io/get.php?md5=048EA0496DB0444F873139CD705A07AF"
        }
    ]
```

### If you've been waiting for long for this. [Please star the project on GitHub](https://github.com/Doc-Han/LibGen.git)

Hence you can do what you want with it. Thank You
