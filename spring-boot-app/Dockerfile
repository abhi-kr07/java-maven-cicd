<<<<<<< HEAD
FROM maven:3.8.3-openjdk-17 AS builder
WORKDIR /app
COPY . /app
RUN mvn clean package -DskipTests=true

FROM openjdk:17-alpine
WORKDIR /app
COPY --from=builder /app/target/*.jar /app/target/app.jar
=======
FROM maven:3.8.3-openjdk-17 AS builder
WORKDIR /app
COPY . /app
RUN mvn clean package -DskipTests=true

FROM openjdk:17-alpine
WORKDIR /app
COPY --from=builder /app/target/*.jar /app/target/app.jar
>>>>>>> 52993af9889cf63bc2b2580ad773e74f4ca695d2
CMD [ "java" , "-jar" , "/app/target/app.jar" ]