# Weather Microservice – Technical Assignment

## Overview
This project implements a **Weather Microservice** designed using a **Backend-for-Frontend (BFF) microservice architecture**.  
The system exposes REST APIs that allow clients to retrieve weather information, manage alert subscriptions, and export weather data.

The solution focuses on **clean architecture, scalability, and maintainability**, following standard enterprise backend development practices.

---

# Architecture

The system follows a **layered microservice architecture**:

Client → API Controller → Service Layer → Repository Layer → Database

### Components

**WeatherService.API**
- REST API service that exposes weather endpoints.

**Service Layer**
- Handles business logic related to weather retrieval and alert subscriptions.

**Repository Layer**
- Manages data persistence and retrieval.

**Database Layer**
- Uses Entity Framework DbContext for storing weather data and subscriptions.

**Utility Components**
- CSV Export functionality for weather reports.

---

# Tech Stack

- **C#**
- **.NET Web API**
- **Entity Framework Core**
- **Docker**
- **REST APIs**
- **GitHub Actions CI/CD**

---

# Project Structure

WeatherService.API
├── Controllers
│ └── WeatherController.cs
│
├── Services
│ └── WeatherService.cs
│
├── Repositories
│ └── WeatherRepository.cs
│
├── Models
│ ├── WeatherData.cs
│ └── AlertSubscription.cs
│
├── Data
│ └── WeatherDbContext.cs
│
├── Utils
│ └── CsvExporter.cs
│
└── Program.cs


---

# Features

- Retrieve weather information via API
- Subscribe to weather alerts
- Export weather data to CSV
- Clean layered architecture
- Dockerized application
- CI/CD pipeline with GitHub Actions

---

# API Endpoints

### Get Weather Data

GET /api/weather


Returns current weather information.

### Subscribe to Weather Alerts

POST /api/weather/subscribe


Creates a weather alert subscription.

### Export Weather Data

GET /api/weather/export


Exports weather data in CSV format.

---

# Running the Project

### 1. Clone Repository

git clone <repository-url>


### 2. Navigate to project


cd WeatherService.API


### 3. Run the application


dotnet run


The API will start locally.

---

Running with Docker

Build image:

docker build -t weather-service .

Run container:
docker run -p 5000:5000 weather-service

CI/CD

GitHub Actions workflow is included in:
.github/workflows/github-actions.yml

The pipeline performs:
- Build
- Dependency restore
- Test execution
- CI validation

Design Documentation

Additional documentation is included:

- **BFF Architecture Diagram**
- **Design Document**

These explain:
- System architecture
- API design decisions
- Data flow

---

Assumptions

- Weather data source can be extended to external APIs.
- Persistence layer can be replaced with a production database.
- Authentication can be added for secure API access.

---

Improvements (Future Work)

- Integrate real weather APIs
- Add caching (Redis)
- Add authentication (JWT)
- Implement message queue for alert notifications
- Add unit and integration tests

---
