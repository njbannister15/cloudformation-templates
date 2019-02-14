# Testing
The folling commands are the boilerplate to help you test that you deployment is done correctly

```
# for Kafka
./bin/kafka-consumer-perf-test --broker-list <host1>:<port1>,<host2>:<port2>,<host3>:<port3> --topic perf-test --messages 1024 --print-metrics
./bin/kafka-producer-perf-test --topic producer-perf --num-records 1024 --record-size 16   --producer.config etc/kafka/producer.properties --throughput 16 --print-metrics

# for zookeeper
echo stat | nc <host1> <port1> | grep Mode
```
