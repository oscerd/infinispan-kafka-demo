# Infinispan-Kafka demo

## Introduction

This is an example for Infinispan-kafka connector

## What is needed

- An Infinispan Server 9.4.15.Final running
- A Kafka Cluster 2.2.1 running 
- The project https://github.com/oscerd/infinispan-kafka-producer
- The project https://github.com/oscerd/camel-infinispan-kafka-demo

## Running

```
mvn clean package
export CLASSPATH="$(find target/ -type f -name '*.jar'| grep '\-package' | tr '\n' ':')"
$KAFKA_HOME/bin/connect-standalone.sh $KAFKA_HOME/config/connect-standalone.properties config/InfinispanSinkConnector.properties
```
