# Kafka Easy Runner

## Description
Just a very easy way to spin a kafka cluster and start publishing streaming love to the world.

____
## Commands
1. Run the docker compose file
``` shell
$ docker-compose -f docker-compose.yml up -d
```
2. Enter the kafka container
```shell
$ docker exec -it kafka /bin/bash
```

3. Navigate to the kafka scripts folder
```shell
cd /opt/kafka_<kafka-version>/bin
```

4. Run the scripts
    - Create a topic:
    ```shell
    $ kafka-topics.sh --create --zookeeper  zookeeper:2181 --replication-factor 1    --partitions 1 --topic <topic-name>
    ```
    - List topics:
    ```shell
    $ kafka-topics.sh --list --zookeeper    zookeeper:2181
    
    ```
    - Describe Topics:

    ```shell
    $ kafka-topics.sh --describe    --zookeeper zookeeper:2181 --topic <topic-name>
    ```
    - Delete Topics:
    ```shell
    $ kafka-topics.sh --delete --zookeeper  zookeeper:2181 --topic <topic-name>
    ```
____
## MISSING

1. Image customization details for spinning containers with topics and some extra custom implementations

2. The list of commands for consuming and producing messages from the interactive command shell