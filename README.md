# Description

Kafka Valve is an application that gives an opportunity to replicate part (or full) traffic from one kafka topic to 
another. It is agnostic to topics data format. 

# How to use
To replicate 50% of traffic from `srcTopicName` to `outTopicName` call:
```
java -jar kafka-valve-{version}.jar \
--src-topic srcTopicName --src-brokers srcbrk1,srcbrk2 \
--output-topic outTopicName --output-prokers outbrk1,outbrk2 \
--fraction 0.5
```

## Available options

short name | long name | description
-----------|-----------|-------------
-s | --src-topic | source(input) topic name |
-b | --src-brokers | comma-separated list of source brokers |
-d | --dst-topic | destination(output) topic name |
-p | --dst-brokers | comma-separated list of destination brokers |
-f | --fraction | fraction of traffic taken from source to destination topic, from 0 to 1 |
