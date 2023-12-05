# Ansible Role: Kafka

Ansible galaxy role used to run a kafka broker on a docker container.

## Requirements

None.

## Role Variables
```yaml
docker_kafka__zookeeper_name: zookeeper
docker_kafka__zookeeper_service_name: zookeeper
docker_kafka__zookeeper_image: docker.io/bitnami/zookeeper:3.8
docker_kafka__zookeeper_port: 2181
docker_kafka__zookeeper_home: "/root/zookeeper"

docker_kafka__kafka_name: kafka
docker_kafka__kafka_service_name: kafka
docker_kafka__kafka_image: docker.io/bitnami/kafka:3.3
docker_kafka__kafka_external_port: 9093
docker_kafka__kafka_client_port: 9092
docker_kafka__kafka_home: "/root/kafka"

docker_kafka__exported_mode: "yes"
docker_kafka__network_name: "kafka-network"
```

## Dependencies

- community.docker

## Example Playbook (using default package)

    - hosts: servers
      roles:
        - role: MahdadGhasemian.ansible-kafka

## License

MIT / BSD

## Author Information

This role was created in 2023 by [Mahdad Ghasemian](https://mahdad.me/).