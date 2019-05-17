# Express IP

This is an express module for Encrypting and Decrypting text in node js.

# Installation

```
npm install express-text-encryptor
```

# Usage

## short
```
const express = require('express');
const app = express();
const {encrypt, decrypt} = require('express-text-encryptor');

app.get('/', function (req, res) {
    const dataToEncrypt = encrypt('This is a sample text')
    res.send(`Encrypted text is ${dataToEncrypt} and Decrypted text is ${decrypt(dataToEncrypt)}`)
});

```
## full
```
const express = require('express');
const app = express();
const expressip = require('express-ip');
const PORT = process.env.PORT || 7000;
const path = require('path');


app.set("PORT", PORT);

app.get('/', function (req, res) {
    const dataToEncrypt = encrypt('This is a sample text')
    res.send(`Encrypted text is ${dataToEncrypt} and Decrypted text is ${decrypt(dataToEncrypt)}`)
});

app.listen(app.get('PORT'), function () {
    console.log('Express started on http://localhost:' +
        app.get('PORT') + '; press Ctrl-C to terminate.');
});

```

# Author
Olohundare Nasirudeen <naskkographics@gmail.com> 