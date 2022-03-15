## Executar kafka

- path com espaços o kafka gera um erro ao executar

- informações básicas necessárias para executar o kafka (zookeeper)
  antes de executar o zookeeper precisa estar executando

  - kafka já vem com zookeeper, basta executar o comando no shell

  ```shell

    ./bin/zookeeper-server-start.sh ./config/zookeeper.properties
  ```

  - executar kafka

  ```shell

    ./bin/kafka-server-start.sh ./config/server.properties
  ```

  - criar um tópico
    - criar um nome de tópico com um padrão e não misturar "." com "\_". USAR UM OU OUTRO

  ```shell
    ./bin/kafka-topics.sh --create --bootstrap-server "HOST:PORT"
    --replication-factor 1 --partitions 1 --topic "Nome do tópico"
  ```

  - listar tópicos

  ```shell
    ./bin/kafka-topics.sh --list --bootstrap-server "HOST:PORT"
  ```

  - produzir mensagens via shell

  ```shell
    ./bin/kafka-console-producer.sh --broker-list "HOST:PORT" --topic "Nome do tópico"
  ```

  - consumir mensagens via shell

  ```shell
    ./bin/kafka-console-consumer.sh --bootstrap-server "HOST:PORT" --topic "Nome do tópico"
  ```

  - consumir mensagens via shell desde o inicio

  ```shell
    ./bin/kafka-console-consumer.sh --bootstrap-server "HOST:PORT" --topic "Nome do tópico" --from-beginning
  ```

  - alterar o numero de partição de um tópico ja criado

  ```shell
    ./bin/kafka-topics.sh --alter --zookeeper "HOST:PORT" --topic "Nome do tópico" --partitions 1
  ```
