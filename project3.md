## Awesome Documentation of project 3

`sudo apt update`

`sudo apt upgrade`

<!--- get the location of Node.js software from Ubuntu repositories. -->

`curl -fsSL https://deb.nodesource.com/setup_18.x | sudo -E bash -`

`sudo apt-get install -y nodejs`

`node -v`

`npm -v`

`mkdir Todo`

`cd Todo`

`npm init`

![package json](./images/package_json.PNG)

<!-- INSTALL EXPRESS.JS  Remember that Express is a framework for Node.js, therefore a lot of things developers would have programmed is already taken care of out of the box. Therefore it simplifies development, and abstracts a lot of low level details. For example, Express helps to define routes of your application based on HTTP methods and URLs.-->

`npm install express`

`touch index.js`

`npm install dotenv`

`vim index.js`

``` javascript
const express = require('express');
require('dotenv').config();

const app = express();

const port = process.env.PORT || 5000;

app.use((req, res, next) => {
res.header("Access-Control-Allow-Origin", "\*");
res.header("Access-Control-Allow-Headers", "Origin, X-Requested-With, Content-Type, Accept");
next();
});

app.use((req, res, next) => {
res.send('Welcome to Express');
});

app.listen(port, () => {
console.log(`Server running on port ${port}`)
});  

```

Now it is time to start our server to see if it works. Open your terminal in the same directory as your index.js file and type: 

`node index.js`

If every thing goes well, you should see Server running on port 5000 in your terminal.

![node running on port 5000](./images/node.PNG)

created an inbound rule to open TCP port 5000

`http://44.204.43.55/>:5000`

![node running on port 5000](./images/express.PNG)
