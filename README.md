# Car Rental Service - Installation Guide

This guide will help you set up and run the Car Rental Service CRUD web application.

## Prerequisites

Ensure you have the following installed on your system:

- [Java 17+](https://adoptium.net/)
- [Maven](https://maven.apache.org/download.cgi) (Ensure it's added to your `PATH`)
- [PostgreSQL](https://www.postgresql.org/download/) (Ensure pgAdmin 4 is installed)
- [Postman](https://www.postman.com/downloads/) (For testing API endpoints)
- [IDE](https://www.jetbrains.com/idea/download/) (For example Jetbrains IntelliJ IDEA)

## Step 1: Clone the Repository

```sh
  git clone https://github.com/Kapprikorn/backend-spring-carpark.git
  cd backend-spring-carpark
```
#### Or use the IntelliJ GUI:

1. In the top left click on your current project name
2. Select `Clone Repository...`
3. Paste `https://github.com/Kapprikorn/backend-spring-carpark.git`
4. Press `clone`

## Step 2: Configure PostgreSQL Database

1. Open **pgAdmin** and create a new database.
2. Ensure your pgAdmin runs on localhost:5432
3. Name it `car_rental_db` or update the `application.properties` accordingly.
4. Ensure PostgreSQL is running.

## Step 3: Configure Application Properties

Create `src/main/resources/application-local.properties` with your PostgreSQL credentials:

```properties
    spring.datasource.username=<your_pg_username>
    spring.datasource.password=<your_pg_password>
```

Open run configuration and add `local` to your active profile.

## Step 4: Build and Run the Application

Use Maven to build and run the application:

```sh
    mvn clean install
    mvn spring-boot:run
```

## Step 5: Verify API Endpoints

1. Open Postman.
2. Import the API collection or manually test endpoints.
3. Access the API at:
    - Swagger UI (if enabled): `http://localhost:8080/swagger-ui.html`

## Additional Commands

- Run tests:

    ```sh
    mvn test
    ```

- Stop the application:

  ```sh
  CTRL + C
  ```

## Troubleshooting
- **Getting a Database connection error?** Ensure PostgreSQL is running and credentials are correct.
