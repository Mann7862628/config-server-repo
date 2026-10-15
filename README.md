# config-server-repo

Configuration for the microservices, served by Spring Cloud Config Server.

| File | Used by |
|---|---|
| `application.yml` | all services (Eureka, JPA, tracing, actuator) |
| `order-service.yml` | order-service (port 8081, database, inventory/payment URLs) |
| `inventory-service.yml` | inventory-service (port 8082, database) |
| `payment-service.yml` | payment-service (port 8083, database, payment limits) |

Naming rule: `{spring.application.name}.yml`, plus `{name}-{profile}.yml` for a profile
(for example `order-service-prod.yml`).

Check what a service receives: http://localhost:8888/order-service/default
