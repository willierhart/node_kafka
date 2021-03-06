# Nodejs Kafka Rabbitmq

## Overview
Simlple Nodejs Kafka and RabbitMQ Test

### Development
```
git clone ...
npm install
npm start
```

### Additional Information
```
Kafka
Start Zookeeper: bin/zookeeper-server-start.sh config/zookeeper.properties
Start Kafka: bin/kafka-server-start.sh config/server.properties
Create a topic: bin/kafka-topics.sh --create --zookeeper localhost:2181 --replication-factor 1 --partitions 1 --topic webevents.dev
Alles gut?: bin/kafka-topics.sh --describe --zookeeper localhost:2181 webevents.dev
Delete topics: bin/kafka-topics.sh --delete --zookeeper localhost:2181 --topic webevents.dev
- https://nodewebapps.com/2017/11/04/getting-started-with-nodejs-and-kafka/

UI for Kafka
- or: https://www.confluent.io/download/
- or: https://www.landoop.com/
- or: https://github.com/Landoop/kafka-topics-ui
docker pull landoop/kafka-topics-ui
// CHANGE TO YOUR LOCAL IP:
    docker run --rm -it -p 8000:8000 \
               -e "KAFKA_REST_PROXY_URL=http://192.168.86.22:8081" \
               -e "PROXY=true" \
               landoop/kafka-topics-ui

RabbitMQ
Enable WebInterface Plugin: sbin/rabbitmq-plugins enable rabbitmq_management
Start RabbitMQ: sbin/rabbitmq-server 
List Queues: sudo sbin/rabbitmqctl list_queues


- https://www.rabbitmq.com/install-standalone-mac.html

Node
Kafka
Start Producer: node1/node kafka_producer.js
Start Consumer: node2/node kafka_consumer.js
- https://blog.mimacom.com/apache-kafka-with-node-js/

RabbitMQ
Start Producer: node1/node rabbitmq_producer.js
Start Consumer: 
- https://www.rabbitmq.com/tutorials/tutorial-one-javascript.html

React
- TODO

Endpoints
RabbitMQ 
- WebInterface: http://localhost:15672/ (guest/guest)

Kafka
- Kafka Topics UI   http://localhost:8000
- Kafka Rest Api    http://localhost:8082 
- Schema Registry   http://localhost:8081 
- Zookeeper         http://localhost:2181 
- Broker            PLAINTEXT://localhost:9092
```
