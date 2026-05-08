# Kubernetes Infrastructure for Microservices

This directory contains Kubernetes manifests for deploying a microservices stack in **Minikube**

## Required Secrets Configuration

The system relies on two main **SealedSecret** objects:

### `postgres-credentials`

| Key | Description |
| :--- | :--- |
| `postgres-password` / `postgres-user` | Credentials for the primary database |
| `auth-db-password`, `user-db-password`, `order-db-password` | Service-specific DB credentials |
| `mongodb-root-username` / `mongodb-root-password` | MongoDB Administrative access |
| `kafka-user` / `kafka-password` | SASL/SCRAM credentials for Kafka auth |

### `app-secrets`

| Key | Description |
| :--- | :--- |
| `jwt-secret` | Key used for signing JWT tokens |
| `gateway-internal-secret` | Secret for inter-service Gateway authentication |
| `admin-bootstrap-password` | Default administrator password |
