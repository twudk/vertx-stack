# SockJS Event Bus bridge for Vert.x 3

The `vertx-eventbus.js` file is a SockJS-based event bus bridge to connect your JavaScript frontend application to Vert
.x 3.x. You can use it in a front-end application or in a node.js application.

If you already use a previous version of the bridge, please check the changelog below. 

## Retrieving the client with Gulp or NPM

The file is delivered as an NPM that you can download it using Bower or Gulp.

The dependency is:

```
"vertx3-eventbus-client": "${project.version}"
```

More information on:

* The [vert.x web site](http://vertx.io) 
* The [Event Bus Bridge documentation](http://vertx.io/docs/vertx-web/java/#_sockjs_event_bus_bridge) 

## Changelog

**Changes from the 3.0.x to 3.1**

* IMPORTANT: The API has been changed to be compatible with node.js and to be closer to the vert.x eventbus API
.Creating  the bridge is made using `var eb = new EventBus("http://localhost:8080/eventbus");` instead of `new vertx
.EventBus...`. In addition, registering a handler use the node convention: 
`eb.registerHandler("metrics", function(err, res) {...}` instead of `ev.registerHandler("metrics", res)`.
* The file name has been updated to `eventbus-client.js`