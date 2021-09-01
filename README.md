# Spring-Docker-Deploy-Example
spring boot로 개발된 웹서버를 K8s환경에 배포하기위해 Docker 빌드를 테스트한다.

## Description
1. docker build with Dockerfile
```bash
docker build -t skaghzz/spring-boot-docker .   
docker run -p 8080:80 skaghzz/spring-boot-docker
```

1. docker build with gradle
```
./gradlew bootBuildImage --imageName=skaghzz/spring-boot-docker-practice
docker run -p 8080:80 skaghzz/spring-boot-docker
```
- build without installing docker, gradle

## Reference
https://spring.io/guides/gs/spring-boot-docker/