

replace double coutes and commas from number with fs 


```js
const fs = require('fs');

let inputString = fs.readFileSync('ssile.txt', 'utf-8');
// let inputString = '"1.0.0","1.0.1","1.0.2","1.0.3","1.0.4","1.1.0","1.1.1","1.1.2","1.2.0","1.3.0","1.3.1","2.0.0","2.1.0","2.2.0","2.2.1","2.2.2","2.2.3","2.3.0","2.3.1","2.4.0","2.4.1","2.4.2","2.5.0","2.6.0","2.7.0","2.8.0","2.8.1","2.9.0","2.10.0","2.10.1","2.10.2","2.11.0","2.12.1"';

let replacedString = inputString.replace(/"/g, '').split(',').map(version => `npm pack blockchain.info@${version}`).join('\n');

// Append to the file
// fs.appendFileSync('rile.txt', replacedString);
fs.appendFileSync('rrile.txt', replacedString);

// Log the replacedString to the console
console.log(replacedString);
```
