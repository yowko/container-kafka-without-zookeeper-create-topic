# Run zookeeperless kafka and create topic

## Set the topic names you want to create in `docker-compose.yaml:environment:KAFKA_CREATE_TOPICS`

    ```yaml
    environment:
      - KAFKA_CREATE_TOPICS=yowkotest:3:1,yowkodemo:3:1
    ```

    - use `,` to separate multiple topic names
    - the value after the first `:` is `partitions number`
    - the value after the second `:` is `replication-factor number`

## Run with build

    ```bash
    docker-compose up -d --build
    ```

## Only build

    ```bash
    docker-compose build 
    ```
