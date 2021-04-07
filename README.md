# Installing Packages

You should already have node installed. If you are using nvm, be sure to use:

```
nvm use stable
```



## Mongo

Start Mongo if it is not already started:

### Mac OS

Perhaps you have it running already as a service on MacOS:

```
brew services list
brew services start mongodb-community@4.0
```

### Windows

[See the documentation for Windows](https://docs.mongodb.com/v3.2/tutorial/install-mongodb-on-windows/).

### Linux

To check whether Mongo is running:

```
sudo systemctl status mongodb
```

To stop Mongo:

```
sudo systemctl stop mongodb
```

To start or restart Mongo:

```
sudo systemctl start mongodb
sudo systemctl restart mongodb
```

## Running Node

Let's setup node and install needed packages:

```
cd back-end
npm init
npm install express mongoose multer
```

We'll be using Express for the REST API. We'll use Mongoose to provide an object
interface for the Mongo database. And we'll use multer to help us upload images.

Now run the node server:

```
node server.js
```

This will start on port 4000 to answer API queries.

## Running the front end

You can run the front by doing the following:

```
cd front-end
npm install
npm run serve
```
# Install Style 
in the front end run 
```
npm i --save @fortawesome/vue-fontawesome
```
## Digital Ocean

* If you are getting an address already in use error on this or any other node projects it means you will need to close that port or switch to a new one.  Keep in mind the port needs to stay open at least until the assignment is graded. Use "forever list" to figure out what is being used and "forever stop {index}" to stop it.

* When moving to digital ocean or changing a port number check these files for the correct port numbers and paths: vue.config.js, /etc/nginx/sites-available/lab4.domainname.com,  and server.js( and other backend js files) for app.listen() and multer destination path. Reload nginx after all of these locations are checked "sudo nginx -s reload".
