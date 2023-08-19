# STEP 1 Running Zookeeper and Kafka Server
This Step for windows
RUNNING ZOOKEEPER PROPERTIES
.\bin\windows\zookeeper-server-start.bat .\config\zookeeper.properties

RUNNING KAFKA SERVICES
.\bin\windows\kafka-server-start.bat .\config\server.properties

CREATE TOPIC
.\bin\windows\kafka-topics.bat --create --topic topic-demo --bootstrap-server localhost:9092

SENDING MESSAGE BY TOPIC
.\bin\windows\kafka-console-producer.bat --topic topic-demo --bootstrap-server localhost:9092

.\bin\windows\kafka-console-consumer.bat --topic topic-demo --from-beginning --bootstrap-server localhost:9092

