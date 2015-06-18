# Arguments Example - Sailsjs
SailsJs application that demonstrates how to pass arguments.

## Requirements
* [NodeJs](http://nodejs.org)
* [mongodb](http://mongodb.org)

## Install
```sh
$ git clone https://github.com/oliverGrisha/argumentsExample-Sailsjs.git
$ npm install
```

## Start
```sh
$ node app.js [database=your-database-name]
```

## Usage
Once deployed the application, for example "node app.js database=example". Access the "localhost:1337/register" and register a user. That user has been created on database "example" in mongoDb.

you can check it:
```sh
$ mongo
> show dbs //check that exist "example"
> use example
> db.user.find() //check that the user is created
```

Other routes available:
* localhost:1337/user --> find all created users
* localhost:1337/login --> login user
* localhost:1337/logout --> logout user

## Explanation
Any application node can be passed arguments as follows:
```sh
$ node app.js [argv ...]
```

In this example, arguments are treated in app.js to follow the following pattern:
```sh
$ node app.js [key1=value1 key2=value2 ...]
```

so that they can be accessed through:
```sh
var key1 = process.argv.key1  //var key1 = value1;
```


