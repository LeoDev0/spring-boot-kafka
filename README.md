### Build kafka and zookeeper docker images
```bash
$ docker-compose up
```

### Access kafka container command line
```bash
$ docker exec -it kafka bash
```

### Create new topic

```bash
$ ./opt/bitnami/kafka/bin/kafka-topics.sh --create --zookeeper zookeeper:2181 --replication-factor 1 --partitions 1 --topic Kafka_Example
```

### Create consumer

```bash
$ ./opt/bitnami/kafka/bin/kafka-console-consumer.sh --bootstrap-server kafka:9092 --topic Kafka_Example --from-beginning
```

### List Topics
```bash
$ ./opt/bitnami/kafka/bin/kafka-topics.sh --list --zookeeper zookeeper:2181
```

### Send message
`GET - localhost:8081/kafka/publish/{message}`
