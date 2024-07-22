# CSV File Processor

## Overview

This Spring Boot application is designed to process CSV files by applying transformation rules and generating reports. The application includes functionalities for reading input and reference CSV files, applying transformation rules, and generating output CSV files. 

## Features

- Ingest CSV files for processing.
- Apply configurable transformation rules.
- Generate output CSV files based on the transformations.
- Support for scheduled report generation.
- REST API endpoint for manual trigger of report generation.

## Technologies Used

- Spring Boot 3.x
- Spring Batch
- Spring Data JPA
- OpenCSV
- H2 Database (for testing)
- Mockito (for unit testing)

## Project Structure

- `src/main/java/com/csvfile`
  - `controllers/` - REST controllers for exposing endpoints.
  - `models/` - Data models for input, output, and reference records.
  - `services/` - Services for file processing and transformation.
  - `utils/` - Utility classes for CSV operations.
- `src/test/java/com/csvfile`
  - `services/` - Unit tests for service classes.

## Configuration

### Application Properties

Configure your application by updating the `src/main/resources/application.properties` file.

```properties
# DataSource configuration for H2 Database
spring.datasource.url=jdbc:h2:mem:testdb
spring.datasource.driverClassName=org.h2.Driver
spring.datasource.username=sa
spring.datasource.password=password
spring.h2.console.enabled=true
spring.jpa.hibernate.ddl-auto=update
spring.jpa.database-platform=org.hibernate.dialect.H2Dialect

# Scheduling configuration
# Define your scheduled tasks here
