
# ACC Subscription Backend

A Spring Boot REST API backend for scraping, analyzing, and recommending OTT (Over-The-Top) subscription plans. The system collects plan data from multiple streaming platforms, stores it in a structured dataset, and exposes endpoints to help users compare plans and receive personalized recommendations.

## Features

- **OTT Plan Scraping** — Automated data collection from streaming platform websites using Selenium WebDriver and jsoup
- **Plan Analysis** — Processes and normalizes plan data from a combined CSV dataset (`Combined.csv`)
- **Recommendation Engine** — Suggests optimal OTT plans based on user preferences or usage patterns
- **RESTful API** — Clean JSON endpoints built with Spring Boot Web
- **Hot Reload** — Spring DevTools enabled for faster development iteration

## Tech Stack

| Layer | Technology |
|---|---|
| Language | Java 17+ |
| Framework | Spring Boot 3.3.5 |
| Web Scraping | Selenium 4.26.0 + WebDriverManager 5.5.3 |
| HTML Parsing | jsoup 1.18.1 |
| Data Parsing | Apache Commons CSV 1.10.0 |
| JSON | Jackson Databind |
| Build Tool | Maven (Maven Wrapper included) |

## Prerequisites

- Java 17 or higher
- Maven 3.6+ (or use the included `./mvnw` wrapper)
- A compatible browser (Chrome recommended) — WebDriverManager handles driver setup automatically
- 
## Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/dhruvilad34/acc-subscription-backend.git
cd acc-subscription-backend
```

### 2. Build the project

```bash
./mvnw clean install
```

### 3. Run the application

```bash
./mvnw spring-boot:run
```

The server will start at `http://localhost:8080` by default.

## Project Structure

```
acc-subscription-backend/
├── src/
│   └── main/
│       └── java/com/advance/real/   # Application source code
├── lib/                             # Local library dependencies
├── Combined.csv                     # Aggregated OTT plan dataset
├── words.txt                        # Supporting word/keyword data
├── pom.xml                          # Maven build configuration
└── mvnw / mvnw.cmd                  # Maven wrapper scripts
```

## Data

The `Combined.csv` file contains aggregated OTT subscription plan data collected from various streaming platforms. This dataset is used by the recommendation engine to analyze and compare plans.

## API Overview

Base URL: `http://localhost:8080`

> Detailed endpoint documentation can be added here as the API evolves. Typical endpoints include:

| Method | Endpoint | Description |
|---|---|---|
| `GET` | `/api/plans` | Retrieve all available OTT plans |
| `GET` | `/api/plans/{platform}` | Get plans for a specific platform |
| `POST` | `/api/recommend` | Get a plan recommendation based on user input |
| `GET` | `/api/scrape` | Trigger a fresh scrape of OTT platform data |

## Configuration

Application properties can be configured in `src/main/resources/application.properties`.

Common settings you may want to adjust:

```properties
server.port=8080
spring.devtools.restart.enabled=true
```
## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/your-feature`)
3. Commit your changes (`git commit -m 'Add your feature'`)
4. Push to the branch (`git push origin feature/your-feature`)
5. Open a Pull Request


