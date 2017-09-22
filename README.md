![iok-express banner](iokloud-logo.png)

# iok-express

## About

#### [Are being completed...] iok-express is IoT platform based on node.js, expressjs, passportjs, mosca and mongodb.

The purpose of any IoT device is to connect with other IoT devices and applications to relay information using internet transfer protocols. The gap between the device sensors and data networks is filled by an IoT Platform.

IOK Express will enable you to put your IoT API services on your own server simply and painless in one command. It supports the popular MQTT protocol in sync with HTTP. It is in javascript so you can create your own features in expressjs middleware or add your favor database. when the new thing add to database, it add to the credential list of mqtt broker too.



## Features

* Simple and Scalable.
* HTTP and MQTT connections together.
* MQTT 3.1 and 3.1.1 compliant.
* Sercured with authentication and JWT.
* Usable inside ANY other Node.js app.

## Steps to run

Firstly besure Mongodb is running on localhost:27017
for Mongodb installation refer to <a href="https://docs.mongodb.com/manual/administration/install-community/">MongoDB Doc</a>
Then, in a new terminal window, start the MongoDB daemon to start mongodb server.


Download and install iok-express git;
```bash
git clone https://github.com/iokloud/iok-express/

cd iok-express

npm install
```

for runing api service you can use one of these commands

``` bash
npm start
```

or
```bash
nodemon server.js
```



## Tutorial

You can find a step by step <a href="https://github.com/iokloud/iok-express/wiki/Tutorial">tutorial</a> in wiki page .



## IOK-Express API

The Thing API defines a set of services to create, update or control any things. 

```
POST /signup
POST /signin
POST /thing
GET /thing
GET /thing/:clientid
PUT /thing/:clientid
DELETE /thing/:clientid
```

Example: for invoking list of created things as locally;
```
GET http://localhost:3000/api/thing/
```





### Learn more


You can find a test version of iok-express at test.iokloud.com as soon as possible.

If you find iok-express useful, consider supporting the project by buying a support package
from [me](http://twitter.com/iokloud) by writing an email to iokloud.com@gmail.com.

Check out our [showcase](https://github.com/iokloud/iok-express/wiki/IOK-Express-Showcases) wiki
page! Feel free to add yourself! :)

## Security Issues

__IOK-Express__ sits between your system and the devices: this is a tough role, and we did our best to secure your systems.
However, you might find a security issue: in that case, email @iokoud at iokloud.com@gmail.com


## Feedback

Use the [issue tracker](https://github.com/iokloud/iok-express/issues) for bugs.
[Tweet](http://twitter.com/iokloud) us for any idea that can improve the project.


## Links

* [Mosca](http://github.com/mcollina/mosca)
* [Expressjs](https://expressjs.com/)
* [Mongodb](https://www.mongodb.com/)
* [Passport](http://passportjs.org/)
* [MQTT protocol](http://mqtt.org)
* [MQTT.js](http://github.com/adamvr/MQTT.js)



## Authors

[Hadi Mahdavi](http://twitter.com/iokloud)
