# Spring Boot API Testing Project

This is a simple Spring Boot project focused on API testing. The application provides basic CRUD (Create, Read, Update, Delete) operations for managing customers. It demonstrates how to build a RESTful API using Spring Boot and integrates with a PostgreSQL database.

## Features

1. **RESTful API**: The project exposes RESTful API endpoints to interact with the customer data. The API supports the standard HTTP methods: GET, POST, PUT, and DELETE.

2. **Data Persistence**: The application uses JPA (Java Persistence API) with Hibernate as the implementation to interact with the PostgreSQL database. The `Customer` entity is mapped to the `customer` table in the database.

3. **Dockerized PostgreSQL**: The project utilizes Docker Compose to set up and run a PostgreSQL database container. The database container is configured in the docker-compose.yml file.

## Development

Throughout the development of this Spring Boot project, several key concepts and technologies were learned and utilized:

1. **Spring Boot Basics**: This project provided hands-on experience with Spring Boot, its annotations, and auto-configuration. The `@SpringBootApplication` annotation sets up the application, enabling the auto-configuration and component scanning.

2. **Controller and REST Endpoints**: By annotating the `Main` class with `@RestController`, it becomes the controller for the REST API. The various endpoints (`@GetMapping`, `@PostMapping`, `@PutMapping`, and `@DeleteMapping`) are mapped to HTTP methods and handle the corresponding API operations.

3. **Dependency Injection**: Spring Boot promotes the use of dependency injection for loose coupling and easier unit testing. The `CustomerRepository` is injected into the `Main` class constructor, allowing seamless interaction with the underlying database.

4. **Data Persistence with JPA and Hibernate**: The `Customer` class is annotated with `@Entity`, and its properties are mapped to columns in the `customer` table using annotations such as `@Id`, `@GeneratedValue`, `@SequenceGenerator`, and `@Column`. JPA's `JpaRepository` interface simplifies CRUD operations.

5. **Docker and Docker Compose**: Docker Compose is utilized to orchestrate the PostgreSQL database container, making it easy to set up and run the database locally. This enables a consistent development and testing environment.

## MVC (Model-View-Controller) Architecture

The project follows the MVC (Model-View-Controller) architectural pattern, a widely-used design pattern in web development. Here's how the MVC components are implemented:

1. **Model**: The `Customer` class represents the model in this application. It encapsulates customer data and provides getter and setter methods for accessing and modifying the data. The `CustomerRepository` interface serves as the model's data access layer, allowing the application to interact with the underlying database.

2. **View**: As this is a RESTful API, there is no traditional view component involved. Instead, the views are represented by the JSON responses that the API returns to clients.

3. **Controller**: The `Main` class acts as the controller in the MVC pattern. It receives incoming HTTP requests and delegates the processing to appropriate methods based on the requested endpoints (`/api/v1/customers`). The controller is responsible for handling the business logic and invoking the necessary services to fulfill the client's request.


