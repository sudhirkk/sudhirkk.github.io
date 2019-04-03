
## Kafka Getting Started

* Install Kafka and dependencies
  ```
  brew install kafka
  ```

* Start Zookeeper
  ```
  zookeeper-server-start /usr/local/etc/kafka/zookeeper.properties
  ```

 * Start Kafka server
   ```
   kafka-server-start /usr/local/etc/kafka/server.properties
   ```

 * Create topic
   ```
   kafka-topics --create --zookeeper localhost:2181 --replication-factor 1 --partitions 1 --topic order
   ```
 * Send messages via the producer console
   ```
   kafka-console-producer --broker-list localhost:9092 --topic order
   ```

 * Consume messages from consumer console
   ```
   kafka-console-consumer --bootstrap-server localhost:9092 --topic order --from-beginning
   ```
