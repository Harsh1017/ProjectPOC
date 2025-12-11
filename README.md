# ProjectPOC

Project  for  kafka (POC)



\# Kafka POC – Setup \& Run Guide



This project demonstrates how to use Apache Kafka for message streaming with Java/Spring Boot.



1\. Download Kafka from the official website and extract it anywhere on your system.



2\. Open a terminal inside the Kafka folder and generate a cluster ID:

&nbsp;  bin/kafka-storage.bat random-uuid



3\. Use that ID to format the Kafka storage:

&nbsp;  bin/kafka-storage.bat format -t <cluster-id> -c config/kraft/server.properties



4\. Start Kafka in KRaft mode:

&nbsp;  bin/windows/kafka-server-start.bat config/kraft/server.properties



5\. Open another terminal to create a topic:

&nbsp;  bin/windows/kafka-topics.bat --create --topic test-topic --bootstrap-server localhost:9092



6\. Start a producer to send messages:

&nbsp;  bin/windows/kafka-console-producer.bat --topic test-topic --bootstrap-server localhost:9092



7\. Start a consumer to read messages:

&nbsp;  bin/windows/kafka-console-consumer.bat --topic test-topic --bootstrap-server localhost:9092 --from-beginning



8\. To run this project:

&nbsp;  - Build: mvn clean install

&nbsp;  - Run:   mvn spring-boot:run



