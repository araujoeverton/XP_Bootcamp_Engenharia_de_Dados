<img align="right" src="https://raw.githubusercontent.com/araujoeverton/XP_Bootcamp_Engenharia_de_Dados/main/assets/bootcamp-engenheiro-de-dados-xp.jpg" width="1080"/> ...

# Processamento de fluxos contínuos de dados

## Introdução

Um dos conceitos básicos de fluxos continuos é o Event Stream [ES], imagine uma cachoeira que jorra água sem parar, essa é a representação do unbounded ( infinito e que sempre cresce ).
Algumas áreas que usufruem deste conceito são empresas que possuem transações financeiras, IoT, Ecommerce, Live Streaming.
Neste módulo aprenderemos como fazer a implementação de um modelo de fluxo contúnuo através do apache Kafka, eventos através do AWS Lambda, Kubernetes e outras tecnologias.

## 1. Apache Kafka

O Apache Kafka é uma plataforma distribuída de transmissão de dados que é capaz de publicar, subscrever, armazenar e processar fluxos de registro em tempo real.
Suas principais funcionalidades:
* capaz de ler eventos;
* Grava eventos em tópicos;
* Banco de dados atômico;
* A segunda e maior tecnologia open source do planeta;

### 1.1 Conceitos e Terminologia

No Kafka os eventos possuem chave, valor e e carimbo de data.
* Event Key: "Alice"
* Event Value: "Made a payment of $200,00 to Bob"
* Event timestamp: "Jun, 25, 2020 at 2:06 p.m"

### 1.2 Broker

Um cluster do Kafka, que pode ser provisionado pelo Kubernetes, rodando uma arquitetura de eventos.

### 1.3 Producers

Responsáveis por enviar eventos.

### 1.4 Consumers

Responsáveis por ler e ou processar eventos recebidos pelos producers.

## Stream processing "[KsqlDB e Spark Streaming]"

O KsqlDB, é uma ferramenta a qual podes fazer transformações em fluxos contínuos de dados;
- [x] Permite pegarmos tópicos existentes no Apache Kafka e , em seguida, filtrar, processar e criar novos tópicos derivados;
- [x] Posssível reunir diversas fontes de dados dos clientes para criar um "perfil de cliente unificado";
- [x] Provavelmente os dados com que desejamos trabalhar estarão em Batch;
- [x] O Kafka Connect tem uma série de conectores open source;

![KsqlDB](https://raw.githubusercontent.com/araujoeverton/XP_Bootcamp_Engenharia_de_Dados/main/assets/ksqldb.jpg)     
## Stream Processing ( Spark Streaming )

O Spark Streaming permite o processamento escalável , de alto rendimento e tolerante a falhas de real time;
- [x] Os dados podem ser ingeridos a partir de muitas fontes o processados por meio algoritmos complexos.

## Como funciona o Spark Streaming?

![Spark Streaming](https://raw.githubusercontent.com/araujoeverton/XP_Bootcamp_Engenharia_de_Dados/main/assets/main-qimg-40deb35b86d4744e7d5187b463e39ea8.webp)

## Arquiteturas orientadas a evento
A arquitetura baseada em eventos se refe a um sistema de microserviços que fracamente acoplados, trocam informações entre si, por meio d aprodução e do consumo de eventos.

## Lambda Architecture

A arquitetura Lambda é um modelo de processamento de dados que combina processamento de dados em lotes e em tempo real, incluindo uma camada específica para responder a consultas de usuários. Esse método híbrido visa aproveitar grandes volumes de dados gerados rapidamente, facilitando o uso mais ágil dos dados pelas empresas.

![Netflix Delivery Stream](https://raw.githubusercontent.com/araujoeverton/XP_Bootcamp_Engenharia_de_Dados/main/assets/netflix-delivery-stream.webp)


## Kappa Architecture

A Arquitetura Kappa é um modelo de processamento de dados em tempo real que simplifica a arquitetura, unificando o processamento de dados em lote e em streaming em um único pipeline. Ao contrário da Arquitetura Lambda, que mantém sistemas separados para esses processamentos, a Kappa usa um único sistema de streaming para lidar com todos os dados, o que facilita a manutenção e o desenvolvimento do sistema.

![Robinhood Delivery Stream](https://raw.githubusercontent.com/araujoeverton/XP_Bootcamp_Engenharia_de_Dados/main/assets/robinhood-delivery-stream.webp)







  



