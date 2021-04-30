# simple-kafka-example

Esse repositório tem com objetivo auxiliar na simulação de um ambiente Kafka, a partir de uma imagem docker kafka.

Abaixo segue comandos de apoio:

Subir a imagem:
`docker compose up`

Executar o terminal bash da imagem criada: `docker exec -it {id_imagem} /bin/bash `

Criar tópico no Kafka com partição e replicação: `kafka-topics --create --topic {nome_topico} --partitions {qtd_particoes} --replication-factor {qtd_replicas} --zookeeper localhost:32181`

Criar producer para o tópico: `kafka-console-producer --broker-list localhost:29092 --topic {nome_topico}`

Criar consumer para tópico: `kafka-console-consumer --topic {nome_topico} --bootstrap-server localhost:9092`
