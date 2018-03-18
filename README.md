# RabbitMqPractise

 Rabbitmq installation:
1)  brew install rabbitmq 
2) bringing up local server : cd /usr/local/Cellar/rabbitmq/3.7.4
$ sbin/rabbitmq-server to bring up server 
3) Management Plugin enabled by default at http://localhost:15672/
4) credentials : guest, guest 

About Rabbitmq:

RabbitMQ is a message broker(orchestrator): it accepts and forwards messages.
RabbitMQ stores and forwards binary blobs of data ‒ messages

AMQP - advanced message queuing protocol
Virtual host : https://www.rabbitmq.com/uri-spec.html::::: In AMQP, a Virtual Host (a.k.a. 'vhost') is a namespace for objects like Exchanges, Queues and Bindings.
RabbitMQ employs a more tangible realization of virtual hosts by effectively making them "virtual clusters" on top of the broker.  This means that not only do virtual hosts NOT share exchanges and queues, but Users, ACL(Access control list)s, Policies, etc. are specific to each virtual host.  

=========================
Producing means nothing more than sending. A program that sends messages is a producer :

* A queue is the name for a post box which lives inside RabbitMQ. Although messages flow through RabbitMQ and your applications, they can only be stored inside a queue. A queue is only bound by the host's memory & disk limits, it's essentially a large message buffer. Many producers can send messages that go to one queue, and many consumers can try to receive data from one queue. This is how we represent a queue:

* Consuming has a similar meaning to receiving. A consumer is a program that mostly waits to receive messages:

Note that the producer, consumer, and broker do not have to reside on the same host; indeed in most applications they don't.

In the diagram below, "P" is our producer and "C" is our consumer. The box in the middle is a queue - a message buffer that RabbitMQ keeps on behalf of the consumer.

=======================
RabbitMQ speaks multiple protocols. This tutorial uses AMQP 0-9-1, which is an open, general-purpose protocol for messaging.


Types : Named, Work, Publish/Subscribe, Routing,Topic, RPC (Request/ Reply pattern) queue  
