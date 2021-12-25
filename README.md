### Build kafka and zookeeper docker containers with docker compose
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

### Instantiate console consumer

```bash
$ ./opt/bitnami/kafka/bin/kafka-console-consumer.sh --bootstrap-server kafka:9092 --topic Kafka_Example --from-beginning
```

### Instantiate console producer (so you can produce messages via console)
```bash
$ ./opt/bitnami/kafka/bin/kafka-console-producer.sh --broker-list kafka:9092 --topic Kafka_Example
```

### List Topics
```bash
$ ./opt/bitnami/kafka/bin/kafka-topics.sh --list --zookeeper zookeeper:2181
```

### Send message via API
`GET - localhost:8081/kafka/publish/{message}`
