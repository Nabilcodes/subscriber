1. what is amqp?

amqp is an acronym that stands for "advanced message queuing protocol". It is an
application layer protocol like HTTP, but for the purpose of passing business 
messages between organization and application. Amqp achieve this by making connections
in the network layer's TCP/IP 

2. what it means? guest:guest@localhost:5672 , what is the first quest, and what is
the second guest, and what is localhost:5672 is for?  

Notice the familiar notation http://somelink.somedomain:@someport. Such notation
was used to refer to particular resource in the internet and the protocol to access it
(in this case it was http). "amqp://guest:guest@localhost:5672" serve similar purposes,
which is to access a resource using a particular protocol. In this case, the resource
was a message queueing service (RabbitMQ for instance) using the amqp protocol. 

a. the first guest refers to the username that wanted to access the service
b. the second guest refers to the password for the corresponding username to access the service
c. the string 'localhost' means that the service was located locally (in the same machine 
we are currently using) and that we're accesing the service there
d. the number 5672 specifies the port in which from it we tried to access/connect to the srevce.

