FROM maven:3.8.3-openjdk-17 AS builder
WORKDIR /app
COPY . /app
RUN mvn clean package -DskipTests=true

FROM openjdk:17-alpine
WORKDIR /app
COPY --from=builder /app/target/*.jar /app/target/app.jar
CMD [ "java" , "-jar" , "/app/target/app.jar" ]
