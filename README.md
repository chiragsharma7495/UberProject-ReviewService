# UberReviewService

A Spring Boot REST API for managing ride reviews in the Uber project ecosystem. The service uses Spring Data JPA, Flyway migrations, and MySQL for persistence.

## Features

- REST endpoints for creating, listing, fetching, updating, and deleting reviews
- Spring Boot 3.2.x with Java 17
- JPA/Hibernate persistence layer
- Flyway database migrations
- Gradle build with JUnit 5 test support
- Actuator for application health and runtime insights

## Tech Stack

- **Framework:** Spring Boot
- **Language:** Java 17
- **Build Tool:** Gradle
- **Database:** MySQL
- **Persistence:** Spring Data JPA, Hibernate
- **Database Migration:** Flyway
- **Testing:** Spring Boot Test, JUnit Platform

## Project Structure

```text
src/main/java/com/example/uberreviewservice
├── adapters
├── controllers
├── dtos
├── models
├── repositories
└── services

src/main/resources
└── db/migration
```

## Prerequisites

Before running the application, make sure you have:

- Java 17 installed
- MySQL running locally
- A database created for the service
- Gradle wrapper support (included in the repo)

## Configuration

The application reads its database settings from `src/main/resources/application.properties`.

Update the datasource values there to match your local environment:

- database URL
- username
- password
- port if needed

The app is configured to run on port `7474` by default.

## Running the Application

### Windows

```powershell
.\gradlew.bat bootRun
```

### macOS / Linux

```bash
./gradlew bootRun
```

## Running Tests

### Windows

```powershell
.\gradlew.bat test
```

### macOS / Linux

```bash
./gradlew test
```

## Build the Project

### Windows

```powershell
.\gradlew.bat build
```

### macOS / Linux

```bash
./gradlew build
```

## API Overview

Base path: `/api/v1/reviews`

| Method | Endpoint | Description |
| ------ | -------- | ----------- |
| `POST` | `/api/v1/reviews` | Create and publish a new review |
| `GET` | `/api/v1/reviews` | Get all reviews |
| `GET` | `/api/v1/reviews/{reviewId}` | Get a review by ID |
| `PUT` | `/api/v1/reviews/{reviewId}` | Update a review |
| `DELETE` | `/api/v1/reviews/{reviewId}` | Delete a review |

## Notes

- Flyway migrations are located in `src/main/resources/db/migration`.
- JPA is configured to validate the schema rather than auto-create it.
- The project includes a basic Spring Boot context test to confirm the application loads successfully.

## License

No license file is currently included.

