# OTT Plan Recommender – Backend 🔧

This is the Spring Boot backend for analyzing uploaded OTT usage files and recommending subscription plans based on pricing and video quality.

---

## Features

- Analyze uploaded text or usage files
- Recommend OTT plans based on:
  - Minimum price
  - Highest video quality
- RESTful APIs for frontend integration
- CORS enabled to support React frontend

---

## Tech Stack

Language: Java  
Framework: Spring Boot  
Build Tool: Maven  
Architecture: REST API  
Port: 8080

---

## Folder Structure

acc-subscription-backend-main-2/  
├── src/  
│   ├── main/  
│   │   ├── java/  
│   │   │   └── com/ott/backend/  
│   │   │       ├── controller/  
│   │   │       ├── model/  
│   │   │       └── service/  
│   │   └── resources/  
│   │       └── application.properties  
├── pom.xml  
└── README.md  

---

## Setup Instructions

1. Clone the repository:

   git clone git@github.com:dhruvilad34/acc-subscription-backend.git  
   cd acc-subscription-backend

2. Build and run the application:

   If using Maven wrapper:  
   ./mvnw spring-boot:run

   Or with global Maven:  
   mvn spring-boot:run

The backend will start on: http://localhost:8080

---

## API Endpoints

- POST /api/analyze-file — Analyze uploaded usage file  
- GET /api/best/price — Get the lowest priced OTT plan  
- GET /api/best/videoquality — Get the plan with the highest video quality

---

## CORS Configuration

This backend is configured to allow requests from http://localhost:3000 for frontend access.

---

## Frontend Repository

Repository Name: ott-subscription-client

---


