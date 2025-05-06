#FROM registry.ocp4.example.com:8443/redhattraining/ocpdev-ubi8-openjdk-17-base:1.16 
FROM registry.access.redhat.com/ubi8/openjdk-17:1.1

COPY pom.xml .
RUN mvn dependency:go-offline

COPY src .
RUN mvn clean package

CMD ["java", "-jar", "target/expense-service-1.0.0-SNAPSHOT-runner.jar"]
