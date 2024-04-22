1.what is amqp?

amqp is an acronym that stands for "advanced message queuing protocol". It is an
application layer protocol like HTTP, but for the purpose of passing business 
messages between organization and application. Amqp achieve this by making connections
in the network layer's TCP/IP 

2.what it means? guest:guest@localhost:5672 , what is the first quest, and what is
the second guest, and what is localhost:5672 is for?  

Notice the familiar notation http://somelink.somedomain:@someport. Such notation
was used to refer to particular resource in the internet and the protocol to access it
(in this case it was http). "amqp://guest:guest@localhost:5672" serve similar purposes,
which is to access a resource using a particular protocol. In this case, the resource
was a message queueing service (RabbitMQ for instance) using the amqp protocol. 

a.the first guest refers to the username that wanted to access the service

b.the second guest refers to the password for the corresponding username to access the service

c. the string 'localhost' means that the service was located locally (in the same machine 
we are currently using) and that we're accesing the service there

d. the number 5672 specifies the port in which from it we tried to access/connect to the service.

Screenshot of rabbitmq web app ui and the publisher console on its right. The amount of queued 
message peaked at about 46 message. This was particularly because the publisher was run more than 
20 times in a small amount of time.

![image](https://github.com/Nabilcodes/subscriber/assets/71275597/861763c0-2f70-4007-8d27-f2430717aeb1)

Screenshot of rabbitmq web app ui and 3 subscriber console around it's sides. Notice that when the 
publisher sends data, the subscriber consumes it in an interesting task-sharing : they share it from
subscriber to subscriber in counter-clockwise fashion, starting from the lower-left subscriber. Also 
notice that the graph in the queued message chart goes down in the same rate that it goes up, much faster
than it would with just one subscriber at service, which usually results in more slope when the graph 
goes down. Also notice that the deliver and consumer acknowledgment graph in message rates chart were 
nearly coincidental as a result of fast and near instant processing speed capability.

![image](https://github.com/Nabilcodes/subscriber/assets/71275597/ab553dc6-2494-4991-93a4-a6cf6a5d74e5)




