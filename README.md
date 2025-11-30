 basics 

 Kafka

_______________
start Zookeeper 
.\bin\windows\zookeeper-server-start.bat config\zookeeper.properties
________________
start Kafka server
.\bin\windows\kafka-server-start.bat config\server.properties 

_________________
create topics 
.\bin\windows\kafka-topics.bat --create --topic user-topic --bootstrap-server localhost:9092


____________________
produce new topic's data  (producer)

.\bin\windows\kafka-console-producer.bat --topic user-topic --bootstrap-server localhost:9092
>hello bro
>how are you

____________________________
consumer (message consuming)

.\bin\windows\kafka-console-consumer.bat --topic user-topic --from-beginning --bootstrap-server localhost:9092

