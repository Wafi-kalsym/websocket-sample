websocket-guide
==========================

#What is it?

A simple websocket message and notification system using Spring Boot. It can broadcast messages to all clients connected to the websocket endpoint, or send messages to specific client through private message endpoint.

# How to run it?

If you have gradle installed and under Windows:

    ./gradlew bootRun


After the server is running, go to:

```
http://localhost:8080/
```

# How to use the application?

## Using the interface

1. To broadcast message to all clients connected to the websocket, enter the message into the field and click 'Send'.

2. To send private message to a client, enter the message into the field and click 'Send Private Message'. ***Note: If using the interface, sending private message will send to itself. Refer to 'Using POSTMAN' section to send private message to a specific client.***
3. Clear the notification counter by clicking the number.

## Using POSTMAN/REST client

### To broadcast message

Send POST request to:
```
http://localhost:8080/send-message
```
With JSON body as follows:
```
{
  "messageContent" : "Global message"
}
```
### To send private message
Send POST request to:
```
http://localhost:8080/send-private-message/{id}
```
With JSON body as follows:
```
{
  "messageContent" : "Private message"
}
```


<!-- Frontend is using old version of AngularJS, but it's just so you can fire it up and see it works. I used the
templating from scotch.io <http://scotch.io> but changed it out a bit. 

A nice tutorial is here: http://scotch.io/tutorials/javascript/single-page-apps-with-angularjs-routing-and-templating -->


<!-- © 2022 GitHub, Inc.
Terms
Privacy
Security
Status
Docs
Contact GitHub
Pricing
API
Training
Blog
About -->
