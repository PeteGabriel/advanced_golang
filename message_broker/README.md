# Message Broker

Note:

Bring Kafka container up: `docker-compose up -d`

---



1. Choosing the Message Broker

Kafka, in a nutshell, is an open-source streaming platform developed by the Apache Software Foundation. It is designed for handling real-time data feeds and stream processing. Here are the key components and concepts of Kafka:

1. **Producer**: Producers are responsible for sending data or "events" to Kafka topics. These events can be any kind of data, such as logs, sensor readings, or user activity.

2. **Broker**: Kafka is based on a distributed architecture, and brokers are the servers that store and manage the data. Multiple brokers form a Kafka cluster.

3. **Topic**: Topics are logical channels or categories where data is organized. Producers write data to topics, and consumers read from them. Topics can have multiple partitions, allowing for parallel processing and scalability.

4. **Partition**: Each topic can be divided into partitions, which are ordered, append-only logs. Partitions enable parallelism and distribute the data across multiple brokers in a cluster.

5. **Consumer**: Consumers subscribe to one or more topics and read data from Kafka. They can read data in real-time or at their own pace, and they maintain an offset to keep track of the last message they've consumed.

6. **Consumer Group**: Consumers can be organized into consumer groups, which allows for load balancing and fault tolerance. Each partition in a topic is consumed by only one consumer within a group, but multiple groups can consume from the same topic.

7. **Zookeeper**: In older versions of Kafka (prior to version 2.8), ZooKeeper was used for cluster coordination and management. However, newer versions of Kafka have removed this dependency, simplifying the architecture.

8. **Stream Processing**: Kafka Streams and other stream processing frameworks allow developers to perform real-time data processing on the data flowing through Kafka topics. This enables applications to analyze and transform data as it arrives.

9. **Durability and Scalability**: Kafka is designed to be highly durable and scalable. Data is replicated across multiple brokers to ensure fault tolerance, and it can handle large volumes of data and high throughput.

10. **Event Sourcing**: Kafka is often used as the event store in event-driven architectures. It allows applications to maintain a complete history of events, which can be used for auditing, analytics, and replaying events for reprocessing.

Kafka is widely used in various industries, including finance, e-commerce, and social media, for building real-time data pipelines, log aggregation, monitoring, and more. Its ability to handle high-throughput, fault tolerance, and real-time data processing makes it a valuable tool for modern data-driven applications.

---
2. Publishing Messages


3. Subscribing for messages

4. Negative Ack

5. Consumer Groups

6. The Pub/Sub design pattern