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