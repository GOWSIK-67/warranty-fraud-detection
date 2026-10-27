# Warranty Claim Fraud Detector

A Spring Boot application for managing device ownership, warranty claims, and fraud detection.

## Prerequisites

- Java 17 or higher
- Maven 3.6+
- MySQL 8.0+

## Database Setup

1. Create MySQL database:
```sql
CREATE DATABASE warranty;
```

2. Create MySQL user (or use existing root user):
```sql
CREATE USER 'root'@'localhost' IDENTIFIED BY 'root';
GRANT ALL PRIVILEGES ON warranty.* TO 'root'@'localhost';
FLUSH PRIVILEGES;
```

## Running the Application

1. Clone/download the project
2. Navigate to project directory
3. Run the application:
```bash
mvn spring-boot:run
```

The application will start on port 9004 (or the port specified in `application.properties`).

## API Documentation

Once the application is running, access Swagger UI at:
http://localhost:9004/swagger-ui/index.html (or http://localhost:9004/swagger-ui.html)

## Testing

Run the TestNG test suite:
```bash
mvn test
```

## Endpoints

- **Health Check**: GET /health
- **Authentication**: POST /auth/register, POST /auth/login
- **Devices**: /api/devices/*
- **Claims**: /api/claims/*
- **Stolen Devices**: /api/stolen-devices/*
- **Fraud Rules**: /api/fraud-rules/*
- **Fraud Alerts**: /api/fraud-alerts/*

## Database Configuration

The application is configured to connect to:
- Database: warranty
- Username: root
- Password: root
- Host: localhost:3306

Update `application.properties` if your database configuration differs.