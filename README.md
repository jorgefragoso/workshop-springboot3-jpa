Course Application

This is a Spring Boot project named CourseApplication. The application is designed to manage categories, products, users, and orders in an e-commerce-like context. It provides a RESTful API and uses Hibernate for ORM and H2 as the database for testing and development purposes.

Features

User management (CRUD operations)

Product management (CRUD operations)

Category management (CRUD operations)

Order and Order Items management (CRUD operations)

H2 Console for database visualization

Technologies Used

Java: Version 21.0.4

Spring Boot: Version 3.4.0

Spring Data JPA: For data persistence

H2 Database: In-memory database for testing and development

Hibernate: ORM framework

Tomcat: Embedded server

Maven: Build tool

Project Structure

src/
  main/
    java/
      com/
        educandoweb/
          course/
            controllers/    # REST controllers
            entities/       # Entity classes (JPA)
            repositories/   # Spring Data JPA repositories
            services/       # Business logic
    resources/
      application.properties  # Configuration file
  test/
    java/
      com/
        educandoweb/
          course/           # Unit and integration tests

Getting Started

Prerequisites

Java 21 or higher

Maven 3.8 or higher

Running the Application

Clone the repository:

git clone https://github.com/your-repository-url
cd course

Build the project:

mvn clean install

Run the application:

mvn spring-boot:run

Access the application:

API: http://localhost:8080

H2 Console: http://localhost:8080/h2-console

H2 Database Credentials:

JDBC URL: jdbc:h2:mem:testdb

Username: SA

Password: (leave empty)

Database Schema

The following tables are created by Hibernate:

tb_category

tb_product

tb_user

tb_order

tb_order_item

tb_payment

tb_product_category

Relationships:

tb_order -> tb_user (Many-to-One)

tb_order_item -> tb_product and tb_order (Many-to-Many)

tb_product_category -> tb_product and tb_category (Many-to-Many)

Endpoints

Users

GET /users - List all users

GET /users/{id} - Get user by ID

POST /users - Create a new user

PUT /users/{id} - Update user

DELETE /users/{id} - Delete user

Products

GET /products - List all products

GET /products/{id} - Get product by ID

POST /products - Create a new product

PUT /products/{id} - Update product

DELETE /products/{id} - Delete product

Categories

GET /categories - List all categories

GET /categories/{id} - Get category by ID

POST /categories - Create a new category

PUT /categories/{id} - Update category

DELETE /categories/{id} - Delete category

Orders

GET /orders - List all orders

GET /orders/{id} - Get order by ID

POST /orders - Create a new order

PUT /orders/{id} - Update order

DELETE /orders/{id} - Delete order

Notes

The H2 Console is enabled for testing purposes only.

By default, the application runs in the test profile.

Data is initialized at startup for demonstration purposes.

Author

Developed by Jorge Fragoso. For inquiries, please contact [alvesjorge06@gmail.com].

