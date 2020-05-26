
# evbx-api project
Performs interaction between 'evbx-product' and 'evbx-resource' services and with GraphQL server on top.
## Specifications
* [GraphQL schema](https://github.com/klindziukp/evbx-graphql/blob/master/src/main/resources/schema.graphql)
* [Evbx resource open API specification](https://github.com/klindziukp/evbx-resource/blob/master/contract/evbx-resource-contract.yaml)
* [Evbx product open API specification](https://github.com/klindziukp/evbx-product/blob/master/contract/evbx-product-contract.yaml)
# Project set up for development
* Set up [evbx-resource](https://github.com/klindziukp/evbx-resource) server using [resource-instructions](https://github.com/klindziukp/evbx-resource/blob/master/README.md)
* Set up [evbx-product](https://github.com/klindziukp/evbx-product) server using [product-instructions](https://github.com/klindziukp/evbx-product/blob/master/README.md)
* Set up [evbx-graphql](https://github.com/klindziukp/evbx-graphql) server using [graphql-instructions](https://github.com/klindziukp/evbx-graphql/blob/master/README.md)
# Project set up with docker compose
* Execute command from __project root__ directory `docker-compose -f script/docker/service/docker-compose.yml up -d` to start microservices system
* Execute command from __project root__ directory `docker-compose -f script/docker/service/docker-compose.yml down` to stop microservices system and remove containers
## Add ELKB (ElastcicSearch, Logstsash, Kiabana, FileBeat) stack
* Execute command from __project root__ directory `docker-compose -f script/docker/elkb/docker-compose.yml up -d` to start ELKB Stack
* Execute command from __project root__ directory `docker-compose -f script/docker/elkb/docker-compose.yml down` to stop ELKB stack
# Project set up with Kubernetes
* Execute command `minikube ip` to get IP address
* Execute command from __project root__ directory `kubectl create -f k8s/deployment/dev/all-dev.yaml` to start POD with development version.Services will be available at: <br>
  __Resource service:__ `minikubeIp:30802`  __Product service:__  `minikubeIp:30801`  __GraphQL service:__  `minikubeIp:30800`
* Execute command from __project root__ directory `kubectl delete -f k8s/deployment/dev/all-dev.yaml` to stop POD with development version.
* Execute command from __project root__ directory `kubectl create -f k8s/deployment/prod/all-prod.yaml` to start POD with production version.Services will be available at: <br>
  __Resource service:__ `minikubeIp:31802`  __Product service:__  `minikubeIp:31801`  __GraphQL service:__  `minikubeIp:31800`
* Execute command from __project root__ directory `kubectl delete -f k8s/deployment/prod/all-prod.yaml` to stop POD with production version.

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
    
