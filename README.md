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
