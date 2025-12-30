# Configuration Repository for E-commerce Microservices

This directory contains the configuration files that should be pushed to your **remote GitHub repository** for the Config Server.

## Files in this directory:

- `product-service.properties` - Configuration for Product Service
- `order-service.properties` - Configuration for Order Service (includes `mes-config-ms.commandes-last`)
- `frontend-api.properties` - Configuration for Frontend API
- `gateway.properties` - Configuration for Gateway
- `eureka-server.properties` - Configuration for Eureka Server

## How to use:

1. **Create a GitHub repository** for your configuration files
2. **Push these files** to that repository
3. **Update the Config Server** `application.properties` with your GitHub repository URL:
   ```
   spring.cloud.config.server.git.uri=https://github.com/YOUR_USERNAME/YOUR_REPO.git
   ```

## Important Notes:

- The configuration files use `localhost` for local development
- For Docker deployment, environment variables in `docker-compose.yaml` override these values
- The `mes-config-ms.commandes-last=10` property in `order-service.properties` is required by the assignment
