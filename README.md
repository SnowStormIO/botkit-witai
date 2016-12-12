# Botkit Middleware for Wit.ai
This Botkit Middleware is maintained up-to-date with both Wit.ai and Botkit latest versions. 
## Installation
In order to utilize wit.ai's service you will need to create an account. Grab the *access token* there.


Next you will need to add botkit-witai as a dependency to your Botkit bot:

```
npm install --save botkit-witai
```

Enable the middleware:
```
var wit = require('botkit-witai')({
    accessToken: <my_witai_token>
});

controller.middleware.receive.use(wit.receive);

controller.hears(['hello'],'direct_message',wit.hears,function(bot, message) {
    // ...
});
```
