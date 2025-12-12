# QuantumCart Microservices

A robust e-commerce microservices architecture built with Spring Boot 3.2 and Java 17.

## Services Overview
- **Discovery Server** - Service registry and discovery (Eureka).
- **Order Service** - Manages order placement and retrieval.
- **Inventory Service** - Tracks product stock and availability.
- **Notification Service** - Asynchronous notification handling via Kafka.

## Tech Stack
The technologies used in this project are:
- **Spring Boot 3.2**
- **Java 17**
- **Spring Cloud Netflix Eureka**
- **Spring Data JPA**
- **MySQL**
- **Apache Kafka**
- **Resilience4j**
- **Micrometer Tracing & Zipkin**
- **Docker & Kubernetes**

## How to build the backend services
Run the following command to build and package the backend services:

```bash
mvn clean install -DskipTests
```

## How to run the backend services
Make sure you have the following installed on your machine:
- Java 17
- Docker
- Maven

### Local Setup (Standalone)
You can run each service individually using Maven:

1. **Discovery Server**: `cd discovery-server && mvn spring-boot:run`
2. **Order Service**: `cd order-service && mvn spring-boot:run`
3. **Inventory Service**: `cd inventory-service && mvn spring-boot:run`
4. **Notification Service**: `cd notification-service && mvn spring-boot:run`

### Kubernetes Deployment
To deploy the services to a Kubernetes cluster:

```bash
# Apply all manifests
kubectl apply -f k8s/
```
