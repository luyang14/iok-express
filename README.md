![iok-express banner](iokloud-logo.png)

# iok-express

## About

#### iok-express is IoT platform based on expressjs, passportjs, mosca and mongodb.

In simple words the purpose of any IoT device is to connect with other IoT devices and applications (cloud-based mostly) to relay information using internet transfer protocols.[http://internetofthingswiki.com]

The gap between the device sensors and data networks is filled by an IoT Platform. Such a platform connects the data network to the sensor arrangement and provides insights using backend applications to make sense of plethora of data generated by hundreds of sensors.

In light of the possibilities that internet of things is offering tech companies has started capitalizing it. There are many IoT platforms available now that provide option to deploy internet of things applications on the go. this is a try to have your own IoT platform.


## Features
* Scalable
* HTTP and MQTT connections together.
* MQTT 3.1 and 3.1.1 compliant.
* Various storage options for QoS 1 offline packets, and subscriptions.
* Usable inside ANY other Node.js app.

## Steps to run locally

Firstly besure Mongodb is running on localhost:27017
for Mongodb installation refer to [https://docs.mongodb.com/manual/administration/install-community/]
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


test our secure REST API using <a href="https://www.getpostman.com/docs/postman/launching_postman/installation_and_updates">Postman</a> REST Client or Curl command. You can install Postman for Chrome extension.
Now, open Postman then enters method, address (http://localhost:3000/api/signup) and body parameters for create or signup new user. After click Send button and successfully created a new user, you should see this message.

![Postman usage in IOK](https://github.com/iokloud/Documentation/blob/master/images/iok-express_postman-signup.png)


Next, we have to test if REST API for Thing resource is restricted for the authorized user only. Change method to "GET" and API endpoint to "http://localhost:3000/api/thing" then click Send button. You should see this message on the Postman result.

```
Unauthorized
```

To access the Thing resource, we have to log in using previously registered user. Change method to "POST" and endpoint to "http://localhost:3000/api/signin" then fill credentials like below screenshot.
If a login is successful, we should get a JWT token like below.
![Postman usage in IOK](https://github.com/iokloud/Documentation/blob/master/images/iok-express_postman-signin.png)


Just copy and paste the token value for use in request headers of restricted Thing resource. Now, do previous get Thing and add this header.

If you see the blank array in response, then you are authorized to use Thing resources because we have not created any thing. Now, you can do the same thing for posting new Thing.
![Postman usage in IOK](https://github.com/iokloud/Documentation/blob/master/images/iok-express_postman-create-thing.png)



### Learn more


You can find a test version of mosca at test.iokloud.com as soon as possible.

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
* [Passport](http://passportjs.org/)
* [MQTT protocol](http://mqtt.org)
* [MQTT.js](http://github.com/adamvr/MQTT.js)

## Authors

[Hadi Mahdavi](http://twitter.com/iokloud)
