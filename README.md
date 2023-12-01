# Kafka Setup and Usage Guide

## Overview
This guide provides step-by-step instructions for setting up and using Apache Kafka, a distributed streaming platform. Apache Kafka uses Zookeeper for distributed coordination and provides a reliable, scalable, and fault-tolerant messaging system.

### System Configuration
Make sure to configure the following settings in your environment:

- Zookeeper: `localhost:2181`
- Kafka: `localhost:9092`


## Run Zookeeper
Start the Zookeeper server by executing the following command:

```bash
bin/zookeeper-server-start.sh config/zookeeper.properties
```

## Run Kafka Server
Launch the Kafka server with the following command:

```bash
bin/kafka-server-start.sh config/server.properties
```

## Create Kafka Topic
Create a Kafka topic named "cities" using the following command:

```bash
bin/kafka-topics.sh --create --bootstrap-server localhost:9092 --topic cities
```

## Topic Details
Retrieve details about the "cities" Kafka topic with the following command:

```bash
bin/kafka-topics.sh --describe --bootstrap-server localhost:9092 --topic cities
```

## Send Message to Kafka Topic
Send a message to the "cities" Kafka topic using the producer:

```bash
bin/kafka-console-producer.sh --broker-list localhost:9092 --topic cities
```

## Consume Messages
Consume messages from the "cities" Kafka topic using the consumer:

```bash
bin/kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic cities
```

## Consume Messages from Beginning
Consume messages from the beginning of the "cities" Kafka topic with the following command:

```bash
bin/kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic cities --from-beginning
```

## Additional Notes

- Make sure to configure your system with the specified Zookeeper and Kafka addresses.
- Customize Docker options as needed for your environment.
- Explore advanced Kafka configurations in the respective configuration files.

🎉 Congratulations on setting up Kafka! 🎉
Now you're ready to leverage the power of distributed streaming for your applications. If you have any questions or run into issues, refer to the [official Kafka documentation](https://kafka.apache.org/documentation/) for more details. Happy streaming! 🚀
