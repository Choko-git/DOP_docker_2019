FROM maven:3.5-jdk-8-alpine AS builder

WORKDIR /usr/my_worker_container/

COPY . .

RUN mvn dependency:resolve && mvn package

FROM openjdk:8-jre-alpine

WORKDIR /usr/my_worker_container/

COPY --from=builder /usr/my_worker_container/target/ .

CMD ["java", "-jar", "worker-jar-with-dependencies.jar"]