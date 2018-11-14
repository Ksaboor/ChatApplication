# Websocket-demo

This is a Chat Demo using Websockets.

**WebSocket** is a communication protocol that makes it 
possible to establish a two-way communication 
channel between a server and a client.

**WebSocket** works by first establishing a 
regular HTTP connection with the server 
and then upgrading it to a bidirectional websocket 
connection by sending an Upgrade header.


## Controller
 Using the our methods from WebSocketConfig class. 
 All the messages sent from clients with a destination 
 starting with /app will be routed to these message 
 handling methods annotated with @MessageMapping.

# Tech/Framework
* Java 8
* SpringBoot 2.1.0
* Vue.js CLI 3.0