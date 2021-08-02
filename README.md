# kafka

    - kafka trabalha com mensagens em string/binário

    - kafka consegue trabalhar em paralelismo
      - para um fluxo único de dados de um client,
        o kafka consegue identificar por um id gerando uma hash desse valor.
        Ex: um cliente pede uma transferência de valor e após algum instante
        pede para cancelar. Com o hash o kafka consegue trabalhar com paralelismo
        mas mantem um fluxo único em relação ao cliente, evitando que cancelar
        a transferência aconteça antes da transferência.

## Brokers

    - tópicos
      - possui um tópico
      - cada tópico tem que definir um numero de partições
      - essas partições podem replicas como forma prevenir percas estilo(master/slave)
      - para um numero x de partição vc tem um numero x de consumers

        - Ex: um tópico com 1 partição -> o seu consumer máximo será de 1

      - consegue configurar um grupo de consumers para um tópico

## Armazenamento

    - em memoria

    - ksqlDB
      - https://ksqldb.io/

## Connect

    - Rest interface
      - Possível problema: adicionar mais tempo na conexão com kafka por conectar
        via http em um intermediário com kafka.
    - libs client producer/consumer

## Libs

    - https://github.com/Blizzard/node-rdkafka

    - https://github.com/SOHU-Co/kafka-node/

    - https://github.com/tulios/kafkajs
      - https://kafka.js.org/

- Design Ex.: https://whimsical.com/kafka-RoBYTKJYXD2ZX5mS3jymAu
