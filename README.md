# Spring Boot Hello World API

This is a small Spring-Boot Hello World application to demonstrate a quick and simple API.

It has one endpoint which returns a JSON response containing the hostname and IP of the server and an obligatory hello world message. 

## Requirements
 * Java 1.8
 * Maven
 
## Using the API
Simply start the app and make a HTTP GET request to http://localhost:8080/ and you will get a JSON response.

## Docker Build
The application has been built and packaged in a Docker container and published to DockerHub: https://hub.docker.com/repository/docker/ravina1002/hello-world-spring-boot/

## How To

#### Clean and Build
```
mvn clean package
```

#### Run
```
mvn spring-boot:run
open http://localhost:8080/
```
Or
```
java -jar ./target/spring-boot-hello-world-1.0.0-SNAPSHOT.jar
```

#### Test
```
mvn verify
```

#### Docker Build
```
mvn package docker:build
```
Or

```
mvn package docker:build -Dmaven.test.skip=true
```

#### Docker Push
```
docker login
docker tag hello-world-spring-boot ravina1002/hello-world-spring-boot
docker push ravina1002/hello-world-spring-boot
```

#### Helm commands
```
helm create spring-application-0.1.0
helm lint spring-application
helm package spring-application
helm install spring-application-0.1.0.tgz
```