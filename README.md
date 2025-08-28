# Internet Banking With Java Spring Boot Microservices

#### Docker Containers

Container | IP | Port Mapping |
--- | --- | --- |
openzipkin_server | 172.25.0.12 | 9411
keycloak_web | 172.25.0.11 | 8080
keycloak_postgre_db | 172.25.0.10 | 5432(Closed Port)
mysql_java_app | 172.25.0.9 | 3306
internet-banking-config-server | 172.25.0.8 | 8090
internet-banking-service-registry | 172.25.0.7 | 8081
internet-banking-api-gateway | 172.25.0.6 | 8082
internet-banking-user-service | 172.25.0.5 | 8083
internet-banking-fund-transfer-service | 172.25.0.4 | 8084
internet-banking-utility-payment-service | 172.25.0.3 | 8085
core-banking-service | 172.25.0.2 | 8092

### Microservices Inside This Project

Here this project consist of mainly 6 microservices and those are,

- User service (banking-core-user-service) – This service includes all the operations under the User such as registrations and retrieval. Additionally, this API consumes keycloak REST API to register and manage the user base while using the local PostgreSQL database as well.
- Fund transfer service (banking-core-fund-transfer-service) – This is the service that handles all the fund transfers between accounts and this API will push messages to a centralized RabbitMQ queue to use from the Notification service.
- Payment service (banking-core-payments-service) – This service will include all the API endpoints to process Utility payments in this project and that will push notification messages to RabbitMQ as well.
- Notification service – This API is registered under the service registry but consumes all the messages from RabbitMQ and pushes necessary notifications to the end users. - PENDING Development
- Banking core service – This is the banking core service that acts as a dummy banking core with accounts, users, transaction details, and processors for banking transactions.

### Technology Stack

1. Java 21
2. Spring Boot 3.2.4
3. Spring Cloud 2023.0.0 
4. Netflix Eureka Service Registry
5. Netflix Eureka Service Client
6. Spring Cloud API Gateway
7. Spring Cloud Config Server
8. Zipkin
9. Spring Cloud Sleuth
10. Open Feign
11. RabbitMQ
12. Prometheus 
13. MySQL 
14. Keycloak 
15. Docker / Docker Compose 
16. Kubernetes 
17. Keycloak

#### Author

<h1 align="center">Hi 👋, I'm Ujjwal Garg</h1>
<h3 align="center">A Passionate Java Fullstack Developer from India</h3>
