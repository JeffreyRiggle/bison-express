# Bison Express
Combines expressjs with bison to allow you to easily send bison based data from your express server.

## Using

```javascript
const express = require('express');
const { useBison, sendBison } = require('@jeffriggle/bison');
const app = express();

useBison(app);

app.get('/', (req, res) => {
    res.status(200);
    sendBison(res, { message: 'Hello world!' });
});
```