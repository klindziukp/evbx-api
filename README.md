
# evbx-api project
Performs interaction between 'evbx-product' and 'evbx-resource' services and with graphQL server on top.
## Specifications
* [GraphQL schema](https://github.com/klindziukp/evbx-product/blob/master/contract/evbx-product-contract.yaml)
* [Evbx resource open API specification](https://github.com/klindziukp/evbx-resource/blob/master/contract/evbx-resource-contract.yaml)
* [Evbx product open API specification](https://github.com/klindziukp/evbx-product/blob/master/contract/evbx-product-contract.yaml)
## Project set up for development
* Set up [evbx-resource](https://github.com/klindziukp/evbx-resource) server using [resource-instructions](https://github.com/klindziukp/evbx-resource/blob/master/README.md)
* Set up [evbx-product](https://github.com/klindziukp/evbx-product) server using [product-instructions](https://github.com/klindziukp/evbx-product/blob/master/README.md)
* Set up [evbx-graphql](https://github.com/klindziukp/evbx-graphql) server using [graphql-instructions](https://github.com/klindziukp/evbx-graphql/blob/master/README.md)
## Project set up with docker compose
* Execute command from __project root__ directory `docker-compose -f script/service/docker-compose.yml up -d` to start microservices system
* Execute command from __project root__ directory `docker-compose -f script/service/docker-compose.yml down` to stop microservices system and remove containers
## Add ELKB (ElastcicSearch, Logstsash, Kiabana, FileBeat) stack
* Execute command from __project root__ directory `docker-compose -f script/elkb/docker-compose.yml up -d` to start ELKB Stack
* Execute command from __project root__ directory `docker-compose -f script/elkb/docker-compose.yml down` to stop ELKB stack
## Tech
* **Build**
    * [Java8](https://www.oracle.com/java/technologies/javase-jre8-downloads.html/)
    * [Gragle](https://gradle.org/)
* **Spring**
    * [SpringBoot](https://spring.io/projects/spring-boot)
    * [SpringBootGraphQL](https://github.com/graphql-java-kickstart/graphql-spring-boot)
    * [SpringData](https://spring.io/projects/spring-data-jpa)
    * [SpringSecurity](https://spring.io/projects/spring-security)
* **Data**
    * [Docker](https://www.docker.com/)
    * [MySQL](https://www.mysql.com/)
    * [FlyWay](https://flywaydb.org/)
* **CI Cloud**
    * [TravisCI](https://travis-ci.org/)
    * [SonarCloud](https://sonarcloud.io/)
    
