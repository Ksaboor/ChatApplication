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



##WebSockets:

Websockets is a communication protocol that makes it possible to establish a two-way communication channel between a server and a client.
WebSocket works by first establishing a regular HTTP connection with the server and then upgrading it to a bi-directional WebSocket connection by sending an Upgrade header.

##Implementation:
In the Spring Boot server, I create a package to config the WebSocket endpoint and message broker.

##RabbitMQ
RabbitMQ is a message broker that takes messages and sends them to other places in a pretty smart way. AMQP is the protocol that RabbitMQ implements. It is completely language-neutral and while using it you can write and read to them in any language just like you would while using TCP or HTTP.
Producer 
The producer creates a message and sends (publishes) into the message broker (RabbitMQ). A message must have two parts: a payload and a label. The payload is data and it can be anything from a simple JSON to MPEG-4 file. The label describes the payload and how RabbitMQ will determine who should get a copy of the message. The communication between publisher and RabbitMQ is one directional and fire and forget.

Consumer
 on the other hand, attaches to the broker and subscribes to a queue to get the message.

Your app can be a producer when it needs to send messages to other applications, or it can be a consumer when it needs to receive the message.

## Connect to RabbitMQ

Applications will connect to RabbitMQ by 
creating TCP connections and getting authenticated.
Setting up and tearing down TCP session is a time-consuming process for OS. 
AMQP also uses what is called a  channel which is nothing but a virtual connection inside a real TCP connection. 
The Publisher/Consumer apps use the channel to issue AMQP command to the broker. A single TCP connection can be used to establish multiple communication paths between the application and the broker. The publisher writes to channel and consumer reads through the channel.

Exchanges, Queues, and Binding:

## Exchange: 
  Producer publishes messages in an exchange. Producer never directly communicates through consumer applications.

##Queue: 
Messages end up in the queue and are received by the consumer.

##Binding: 
Rule to route the message into one or more queue. This is a relationship between exchange and a queue.
