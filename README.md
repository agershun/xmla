# xmla.js - JavaScript XML/A driver for browser and Node.js

(c) 2015 Andrey Gershun

Work in progress

### What is it?

**xmla.js** is a JavaScript library to access to OLAP data sources with XML/A protocol.

For example, you can use it together with ```olap.js``` library.

### Installation

In Node.js:
```bash
    > npm install xmla
```

In browser: Download file [xmla.js]()

### How to use?

In Node.js:
```js
    var xmla = require('xmla');
    var conn = new xmla.connection({url:'localhost:3000/xmla'});
    var cubes = conn.discover('cubes');
    var res = conn.execute('SELECT [One] ON ROWS, [Two] ON COLUMNS FROM one');
```

In browser:
```html
    <script src="xmla.js"></script>
    <script>
        var conn = new xmla.connection({url:'localhost:3000/xmla'});
        var cubes = conn.discover('cubes');
        var res = conn.execute('SELECT [One] ON ROWS, [Two] ON COLUMNS FROM one');
    </script>
```

