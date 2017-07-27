# Infinispan-Kafka demo

## Introduction

This is an example for Infinispan-kafka connector

## What is needed

- An Infinispan Server 9.1.0.Final running
- A Kafka Cluster 0.11.0.0 running 

## Running

```
mvn clean package
export CLASSPATH="$(find target/ -type f -name '*.jar'| grep '\-package' | tr '\n' ':')"
$KAFKA_HOME/bin/connect-standalone $KAFKA_HOME/config/connect-standalone.properties config/InfinispanSinkConnector.properties
```
