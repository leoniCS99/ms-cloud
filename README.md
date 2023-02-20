# Cloud Gateway

Este é um projeto de aplicação Cloud Gateway, responsável por rotear as requisições HTTP recebidas para os microserviços correspondentes. A aplicação é construída utilizando o framework Spring Cloud Gateway, que é um componente do ecossistema Spring Cloud.

## Estrutura

A aplicação Cloud Gateway é composta principalmente pelo arquivo de configuração que define as rotas para os microserviços. No código fornecido, as rotas são definidas através do método `routes` que retorna um objeto do tipo `RouteLocator`. Cada rota é configurada através do método `route`, que define o padrão da URL a ser roteada e a URL base do microserviço correspondente.

No exemplo fornecido, há três rotas definidas:

- `/clientes/**`: todas as requisições que começam com `/clientes` serão roteadas para o microserviço [msclientes](https://github.com/leoniCS99/ms-client).
- `/cartoes/**`: todas as requisições que começam com `/cartoes` serão roteadas para o microserviço [mscartao](https://github.com/leoniCS99/ms-cartao).
- `/avaliacoes-credito/**`: todas as requisições que começam com `/avaliacoes-credito` serão roteadas para o microserviço [mscredito](https://github.com/leoniCS99/mscredito).

## Tecnologias

O Cloud Gateway é construído em Java com o uso do framework Spring Cloud Gateway. Além disso, é utilizado o Spring Boot para a configuração e inicialização da aplicação. É importante mencionar que o Cloud Gateway depende do serviço de registro e descoberta de serviços do Spring Cloud, o Eureka.

## Como executar

Para executar o Cloud Gateway, é necessário ter o Java 11 instalado e configurar a conexão com o serviço Eureka. Em seguida, basta executar o comando `./mvnw spring-boot:run` na raiz do projeto. A aplicação será executada na porta 8080. As requisições recebidas na porta 8080 serão roteadas para os microserviços correspondentes de acordo com as rotas definidas.```
