# Nestjs email authentication starter
This project is an example of implementation of a user **email authentication** with [Nestjs](https://nestjs.com/) v6.9.0, [MongoDB](https://www.mongodb.com/) and [PassportJs](http://www.passportjs.org)

It can be used as starter for a new project: it implements API for user sign-in/sign-up and features like **email verification**, **forgotten password**, **reset password**, **update profile** and **settings**.

# Getting started
Install `nodejs` and `mongodb` in your machine.

Install dependencies with npm and run the application:
``` 
npm install
npm run start
```

# Deploy using Docker
⚠️ Before deploy the app in a container set the right **configuration** as explained in the section below, and then you can run:
``` 
docker-compose up -d
```
It will generate 3 containers: 
- nestjs: nodejs application -> localhost:3000 (you can change the port in the docker-compose.yml)
- mongodb: database -> expose 27017 in the container network but not reacheable from outside.
- mongo-express: a web-based MongoDB admin interface -> localhost:8081

You can edit the config is in `docker-compose.yml`.  
❗ Note: For security reason, remember to **change the db password** in docker-compose.yml and in config.ts file, and to **change the mongo-express password** to access the console.
