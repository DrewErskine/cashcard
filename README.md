# Spring Boot Web Application

## Project Overview

This project is a web application built using Spring Boot. The backend is implemented with Spring Boot version 3.1.5, incorporating various components such as controllers, repositories, and security configurations. The frontend leverages Bootstrap's AdminLTE template for a responsive and modern UI, utilizing HTML, JavaScript, and CSS.

## File Descriptions

### Backend Files

- **build.gradle**
  - Contains the Gradle build configuration, including dependencies and plugins required for the project. This file configures the project to use Spring Boot, Spring Data JPA, Spring Security, and other necessary libraries.

- **CashCardApplication.java**
  - The main class that bootstraps the Spring Boot application.

- **CashCard.java**
  - Represents the entity model for the Cash Card, defining its attributes and methods.
  - **Attributes:**
    - `id`: Unique identifier for the cash card.
    - `holderName`: Name of the card holder.
    - `balance`: Current balance of the cash card.
  - **Methods:**
    - Getters and setters for `id`, `holderName`, and `balance`.
    - `toString()`: Returns a string representation of the Cash Card.

- **CashCardController.java**
  - Contains RESTful endpoints for managing Cash Card resources.
  - **Endpoints:**
    - `getAllCashCards()`: Retrieves all cash cards.
    - `getCashCardById(Long id)`: Retrieves a specific cash card by its ID.
    - `createCashCard(CashCard cashCard)`: Creates a new cash card.
    - `updateCashCard(Long id, CashCard cashCard)`: Updates an existing cash card.
    - `deleteCashCard(Long id)`: Deletes a cash card by its ID.

- **CashCardRepository.java**
  - Provides CRUD operations for the Cash Card entity using Spring Data JPA.
  - **Methods:**
    - `findAll()`: Retrieves all cash cards.
    - `findById(Long id)`: Retrieves a cash card by its ID.
    - `save(CashCard cashCard)`: Saves a cash card (create or update).
    - `deleteById(Long id)`: Deletes a cash card by its ID.

- **SecurityConfig.java**
  - Configures security settings for the application, including authentication and authorization.
  - **Methods:**
    - `configure(AuthenticationManagerBuilder auth)`: Configures in-memory authentication with user details.
    - `configure(HttpSecurity http)`: Configures security settings, such as request authorization and form login.

- **CashCardApplicationTests.java**
  - Contains unit tests for the Cash Card application to ensure functionality.
  - **Test Methods:**
    - `contextLoads()`: Verifies that the Spring application context loads successfully.

- **CashCardJsonTest.java**
  - Includes tests for JSON serialization and deserialization of the Cash Card entity.
  - **Test Methods:**
    - `testSerialize()`: Tests JSON serialization of a Cash Card.
    - `testDeserialize()`: Tests JSON deserialization of a Cash Card.

- **schema.sql**
  - SQL script for setting up the database schema.
  - **Contents:**
    - SQL statements to create the `cash_card` table with columns for `id`, `holder_name`, and `balance`.

- **data.sql**
  - SQL script for populating the database with initial data.
  - **Contents:**
    - SQL statements to insert sample data into the `cash_card` table.

### Frontend Files

- **advanced.html**
  - Contains advanced form elements and functionalities using the AdminLTE template.

- **general.html**
  - Includes general form elements and layout using the AdminLTE template.

- **editors.html**
  - Provides various text editors and related functionalities within the AdminLTE template.

## Dependencies

- **Spring Boot 3.1.5**
  - Core framework for the backend application.
  
- **Spring Data JPA**
  - Provides the repository abstraction for database operations.
  
- **Spring Security**
  - Manages authentication and authorization.

- **Bootstrap (AdminLTE)**
  - Frontend framework for responsive design and UI components.

## Database

- The application uses an H2 in-memory database for development and testing purposes. The database schema is initialized using the `schema.sql` file, and initial data is populated using the `data.sql` file.

## Additional Information