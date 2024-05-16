# Kafka on k8s

Deploying Kafka on Kubernetes can be more complex than it initially appears, especially when aiming for a replicated setup. This repository provides a new approach to deploying a Kafka cluster, offering a simpler alternative to the [Strimzi](https://github.com/strimzi/strimzi-kafka-operator) and [Bitnami Helm chart](https://github.com/bitnami/charts/tree/main/bitnami/kafka) solutions.

## How to run it in your cluster

To run it in your cluster, download this repo in the master machine and run the following command:

```
kubectl apply -f basic/ -R
```

## Aditional features

This session discuss how to upgrade the basic version and bring a more production-ready Kafka environment.

### More or Less Brokers

...

### Monitoring

To monitor Kafka there is two tools: JMX exporter and Kafka Exporter ...

```
EXTRA_ARGS: "-Xms128m -Xmx256m -javaagent:/etc/config/jmx-agent/jmx-agent.jar=7071:/etc/config/jmx-config/jmx-config.yml"
```

### TLS

...

### Access Control

...

## About the Solution

This session dives in the whys behind each line of yaml.

### Usage of headless service with Envoy

...