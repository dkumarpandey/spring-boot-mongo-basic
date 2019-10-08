# spring-boot-mongo-basic
Mongo Basics

##Note:
This example uses Spring Boot 1.3.4.RELEASE
It seems API MongoDbFactory.getDB() didn't return com.mongodb.DB in the latest version of spring boot 2.1.9.RELEASE
Will update the example later with appropriate changes needed with spring boot 2.1.9.RELEASE

Need to create a user stocks for sandbox db as shown below uusing mongo shell console.

use sandbox
db.createUser(
  {
    user: "stocks",
    pwd: "password",
    roles: [ { role: "readWrite", db: "sandbox" } ]
  }
)


To test the example open browser
http://localhost:8080/stocks/

You should get the response similar to below.

{"_id":{"date":1570544507000,"time":1570544507000,"timestamp":1570544507,"new":false,"timeSecond":1570544507,"machine":153172848,"inc":-1689150284},"companyName":"Ford","symbol":"F"}