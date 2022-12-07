# Spring boot + React boilerplate

## How to create
1. Create Spring Boot app using Spring Initializr.
2. Create React project.
3. Avoid Cors modifying package.json adding proxy property.
4. Add "frontend-maven-plugin" to prepare frontend build during "maven clean install".
5. Add "maven-resources-plugin" to copy /build directory to the jar during "maven clean install".

## Build jar
```bash
./mvnw clean install
```

## Run jar
```bash
java -jar target/backend-0.0.1-SNAPSHOT.jar
```

## Url
```bash
http://localhost:8080/
```

## Docker & Jib
Prerequisites:
- Install docker-desktop
- Add Jib to maven and configure
- Having account in Dockerhub

Known problems:
- I had problems with 401 Http error. I fixed executing this command:
```bash
docker login registry.hub.docker.com
docker login registry-1.docker.io
```

How to build & deploy:
```bash
mvnw clean install -P build-frontend -P jib-push-to-dockerhub -Dapp.image.tag=latest
mvnw clean install -P build-frontend -P jib-push-to-local -Dapp.image.tag=latest
```