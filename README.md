# Blood Donation Platform Components

Student name: Kavindu Jayasundara
Student number: [add student number before submission]
GCP project ID: `blood-bank-506721`

Spring Cloud infrastructure for the Blood Donation Management System.

## Components

- `config-server` - native Spring Cloud configuration on port `8888`
- `eureka-server` - service registry and dashboard on port `8761`
- `api-gateway` - Eureka-aware gateway on port `8080`

## Technology

Java 25, Spring Boot 3.5, Spring Cloud, Maven and Eureka.

## Build and run

Build an individual component from its directory:

```bash
mvn -DskipTests package
java -jar target/<component>-0.0.1-SNAPSHOT.jar
```

Start Config Server and Eureka before the API Gateway. Set `EUREKA_DEFAULT_ZONE` for deployments where Eureka is not running on `localhost`.

## Deployment

These components run on the private Compute Engine VM `blood-core`, managed by PM2. See the parent deployment guide for GCP commands and IAP access.
