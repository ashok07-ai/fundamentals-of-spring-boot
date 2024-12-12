# Spring Boot

---

## Spring Boot
Spring Boot is an open-source Java-based framework used to create stand-alone, production-grade Spring-based applications quickly and efficiently. It is build on top of the [**Spring Framework**](https://github.com/ashok07-ai/basics-of-spring-framework) and provides pre-configured setups to simplify the development process by reducing boilerplate code and configuration. <br>
**Spring Boot** = **Spring Framework + Prebuilt Configuration + Embedded Servers**

---

## Spring VS Spring Boot
- **Spring**: Lots of steps involved in setting up, configuration, writing boilerplate code, deployment of the app.
- **Spring Boot**: Offers a set of pre-configured components or defaults, and eliminating the need for a lot of boilerplate code that was involved in setting up a Spring Application.

---

## Components of Spring Boot
- Spring Boot Starters
- Auto Configuration
- Spring Boot Actuator
- Embedded Server
- Spring Boot DevTools

---

## Advantages of Spring Boot
- Stand alone and Quick Start
- Starter Code
- Less Configuration
- Reduced cost and application development time
- Avoids boilerplate code and configurations
- Monitoring and Management
- Microservices Ready

---

## Architecture of Spring Boot
Spring Boot is built on the top of **Spring Framework**, following the layered architecture design. It simplifies and accelerates the development of enterprise-grade Java applications by integrating various components with an opinionated approach.

### 1. Layered Architecture in Spring Boot
Spring Boot applications are typically designed with the following layers.
- **Presentation Layer (Controller Layer)**: Presentation layer represents the data and the application features to the user. This is the layer where in all the controller classes exist.
  - **Purpose**: Handles user interaction (e.g, HTTP requests) and forwards them to the business layer.
  - **Key Components**: Controllers, defined using [@Controller or @RestController](https://docs.spring.io/spring-boot/tutorial/first-application/index.html#getting-started.first-application.code.mvc-annotations). Request Mappings **(@GetMapping, @PostMapping, etc.)**.
  - **Technologies**: Spring MVC, Thymeleaf, REST APIs.
  - **Responsibilities**: Managing HTTP requests and responses. Returning views (e.g, HTML) or serialized JSON response for REST APIs.
<br><br>
- **Business Layer (Service Layer)**: Service Layer is where business logic resides in the application. Tasks such as evaluations, decision-making, processing of data is done at this layer.
  - **Purpose**: Contains the business logic of the application.
  - **Key Components**: Service classes annotated with **@Service**. Encapsulates business rules and interacts with the data access layer.
  - **Responsibilities**: Implements core logic independent of the presentation. Provides reusable methods for various controllers.<br><br>
- **Data Access Layer (Repository Layer)**: Data access layer is the layer where all the repository classes reside.
  - **Purpose**: Manages the persistence of application data.
  - **Key Components**: Repositories or DAOs (Data Access Objects), and annotated with @Repository. Uses Spring Data JPA or JDBC for database interactions.
  - **Responsibilities**: CRUD operations on the database. Converts business objects to database entities and vice versa.
<br><br>
- **Database Layer**:
  - **Purpose**: The physical database where application data is stored.
  - **Technologies**: Relational Databases (MySQL, PostgreSQL, Oracle), NoSQL Databases (MongoDB).
  - **Responsibilities**: Stores application data. Handles schema and Query Optimizations.

![Spring Boot Architecture](./src/images/architecture.png)

---

## Spring Initializer
The Spring Initializer is a web-based tool provided by the Spring team to quickly generate and bootstrap Spring Boot projects. It simplifies the process of creating a new Spring Boot application by providing a graphical interface to configure the project’s dependencies, settings, and structure. <br>
Click the link to redirect in Spring Initializer website: [Spring Initializer](https://start.spring.io/)

---

## Database Management System (DBMS)
It is a software application that enables users to efficiently create, access, manage, and manipulate databases. DBMS serves as an interface between the database and its users or application programs, ensuring that data is consistently organized and easily accessible.

### Key features of DBMS
- Data Storage and Retrieval
- Data Integrity
- Data Security
- Data Independence
- Backup and Recovery
- Transaction Management

### Types of DBMS
- [**Relational DBMS (RDBMS)**](https://www.oracle.com/database/what-is-a-relational-database/#:~:text=The%20software%20used%20to%20store,storage%2C%20access%2C%20and%20performance.)
  - Example: MySQL, PostgreSQL, Oracle, SQL Server.
- [**Hierarchical DBMS**](https://www.geeksforgeeks.org/hierarchical-model-in-dbms/)
  - Example: IBM Information Management System (IMS)
- [**Network DBMS**](https://www.geeksforgeeks.org/network-model-in-dbms/)
  - Example: Integrated Data Store (IDS)
- [**Object-Oriented DBMS (OODBMS)**](https://www.geeksforgeeks.org/definition-and-overview-of-odbms/)
  - Example: ObjectDB.
- [**NoSQL DBMS**](https://www.mongodb.com/resources/basics/databases/nosql-explained)
  - Example: MongoDB, Cassandra, CouchDB.

---

## Object Relational Mapping (ORM)
It is a programming technique that allows developers to interact with a database using object-oriented concepts. ORM simplifies the process of mapping data between relational databases and object oriented programming languages, eliminating the need to write complex SQL queries.

### Key Features
- Abstraction
- Automatic Query Generation
- Cross-Database Compatibility
- Lazy and Eager Loading.

---

## JPA (Java Persistence API)
[**JPA**](https://spring.io/projects/spring-data-jpa) is a specification in Java for managing relational data in applications. It defines a standard way to map Java objects (entities) to database tables and to perform database operations such as CRUD (CREATE, READ, UPDATE, DELETE).

### Key features of JPA
- Object-Relational Mapping (ORM)
- Entity Management
- Querying
- Annotations
- Transactions

## Data Layer
Data Layer is a software architecture refers to the part of an application responsible for handling all interactions with the database or other data storage systems. It serves as an abstraction layer between the application logic (business layer) and the data storage mechanisms.

### Presentation Layer
Presentation layer presents the data and the application features to the user. This is the layer where in all the controller classes exist.

### Service Layer
Service layer is where business logic resides in the application. Tasks such as evaluations, decision-making, processing of data is done at this layer.

### Data Access Layer
Data access layer is the layer where all the repository classes reside.

---

## H2 Database
It is an open-source, lightweight, relational database management system written in Java. It is designed to be fast, portable, and easy to use, making it an excellent choice for development, testing, and small-scale production applications.

### Key features of H2 Database
- In-Memory and Persistent Modes
- Lightweight
- Embedded and Server Modes
- SQL Compatibility
- GUI Console
- Java Integration

---

## Entities in JPA
In **JPA**, entities are the primary way of representing tables in a relational database. An entity is a lightweight, persistent domain object that maps a Java class to a database table. Each instance of an entity represents a row in the corresponding table.

### Key features of JPA entities
- **Object-Relational Mapping (ORM)**: The fields of the entity class map the columns of a database table.
- **Annotations**: Use annotations like **@Entity**, **@Table**, and **@Column** to specify how the java class maps to the database table.
- **Persistence Context**: Entities are managed by the JPA persistence context, enabling CRUD operations and transactions.

---

## Types of Generation Strategies
In JPA, the generation types for entities determine how the primary key values are generated for the database table. These are defined using the **@GeneratedValue** annotation in combination with the **@Id** annotation.
- **GenerationType.AUTO**: 
  - JPA chooses the strategy based on the underlying database and the persistence provider (e.g., Hibernate).
  - It is database-independent and a good default choice.
  - Example: <br>@Id <br>@GeneratedValue(strategy = GenerationType.AUTO)<br>private Long id;
  - Behaviour: May use SEQUENCE, IDENTITY, or a table-based strategy, depending on the database.<br><br>
- **GenerationType.IDENTITY**:
  - Relies on the database to auto-generate the primary key, typically using an auto-increment column.
  - Suitable for databases like MySQL or PostgreSQL that support auto-increment fields.
  - Example: <br>@Id <br>@GeneratedValue(strategy = GenerationType.IDENTITY)<br>private Long id;
  - Behaviour: Each entity is inserted into the database immediately to obtain the generated ID.<br><br>

-  **GenerationType.SEQUENCE**:
  - Uses a database sequence to generate primary key values. 
  - Suitable for databases like Oracle, PostgreSQL, and H2 that support sequences. 
  - Example: <br>@Id <br>@GeneratedValue(strategy = GenerationType.SEQUENCE, generator = "product_seq") <br>@SequenceGenerator(name = "product_seq", sequenceName = "product_sequence", allocationSize = 1)
  <br>private Long id;
  - Behaviour: Uses the specified sequence to fetch IDs..<br><br>
- **GenerationType.TABLE**:
  - Simulates a sequence by using a table in the database to maintain the generated values.
  -Database-independent and can be used when SEQUENCE is not supported.
  - Example: <br>@Id <br>@GeneratedValue(strategy = GenerationType.TABLE, generator = "table_gen") <br>@TableGenerator( <br>
    name = "table_gen", <br>
    table = "id_generator",<br>
    pkColumnName = "gen_name",<br>
    valueColumnName = "gen_value",<br>
    pkColumnValue = "product_id",<br>
    allocationSize = 1<br>
    )
    <br>private Long id;
  - Behaviour: Uses a dedicated table to store the next value of the primary key.<br><br>

---

## Comparison of Generation Strategies
| Strategy   | Database Dependency  | Batch Inserts | Performance | Example Databases     |
|------------|-----------------------|---------------|-------------|-----------------------|
| `AUTO`     | Depends on provider  | Yes           | Varies      | Any                   |
| `IDENTITY` | Auto-increment support | No          | Good        | MySQL, PostgreSQL     |
| `SEQUENCE` | Sequence support      | Yes           | Best        | Oracle, PostgreSQL, H2 |
| `TABLE`    | None                  | Yes           | Slow        | Any                   |

---

## Lombok
Lombok is a Java library that helps reduce boilerplate code in your Java classes. It achieves this by automatically generating common methods like getters, setters, constructors, toString, equals, and hashCode at compile time, using annotations. This makes your code cleaner and more maintainable.

### Key features and annotations of Lombok
Lombok is a library that helps reduce boilerplate code in Java by generating common methods like getters, setters, constructors, etc., at compile time using annotations. Below is a quick reference for some commonly used Lombok annotations and their purposes.

| **Annotation**              | **Purpose**                                                                                     |
|-----------------------------|-------------------------------------------------------------------------------------------------|
| `@Getter`                   | Automatically generates a getter for each field.                                               |
| `@Setter`                   | Automatically generates a setter for each field.                                               |
| `@ToString`                 | Generates a `toString` method including all fields (or specified fields).                      |
| `@EqualsAndHashCode`        | Generates `equals` and `hashCode` methods.                                                     |
| `@NoArgsConstructor`        | Generates a no-argument constructor.                                                           |
| `@AllArgsConstructor`       | Generates a constructor with arguments for all fields.                                         |
| `@RequiredArgsConstructor`  | Generates a constructor for `final` or `@NonNull` fields only.                                 |
| `@Data`                     | Combines `@Getter`, `@Setter`, `@ToString`, `@EqualsAndHashCode`, and `@RequiredArgsConstructor`. |
| `@Builder`                  | Implements the Builder pattern for creating objects.                                           |
| `@Value`                    | Makes a class immutable by marking fields as `final` and providing a private constructor.      |
| `@Slf4j`                    | Adds a logger field (using SLF4J) for logging purposes.                                        |

### Installation

### Maven Dependency
Add the following to your `pom.xml`:
```xml
<dependency>
    <groupId>org.projectlombok</groupId>
    <artifactId>lombok</artifactId>
    <version>1.18.28</version>
    <scope>provided</scope>
</dependency>
```

---

## Validations
Validation in software development refers to the process of ensuring that the data provided by a user, system, or application meets the defined rules, constraints, and requirements. It is used to verify that input or data is both correct and meaningful before it is processed, stored, or transmitted.
Bean Validation (e.g., `javax.validation.constraints`) is used to enforce constraints on Java fields or methods. Lombok annotations can be combined with validation annotations for clean, maintainable code.

### Common Validation Annotations

| **Annotation**             | **Purpose**                                                                                     |
|----------------------------|-------------------------------------------------------------------------------------------------|
| `@NotNull`                 | Ensures the value is not `null`.                                                               |
| `@NotEmpty`                | Ensures the value is not `null` or empty (for strings, collections, etc.).                     |
| `@NotBlank`                | Ensures the value is not `null` and trimmed length > 0 (for strings).                          |
| `@Size(min, max)`          | Specifies the size of a string, collection, or array.                                          |
| `@Min(value)`              | Specifies the minimum value for a numeric field.                                               |
| `@Max(value)`              | Specifies the maximum value for a numeric field.                                               |
| `@Email`                   | Validates that a string is a valid email address.                                              |
| `@Pattern(regexp)`         | Validates a string against a regular expression.                                               |
| `@Positive`                | Ensures the value is positive (greater than 0).                                                |
| `@Past` / `@Future`        | Ensures the value is in the past/future (used for `Date` or `LocalDate`).                      |

---

## **Validation Example**

Here's an example of how to use Lombok with validation:

### Entity with Validation
```java
import lombok.Data;

import javax.validation.constraints.*;

@Data
public class User {

    @NotNull(message = "ID cannot be null")
    private Long id;

    @NotBlank(message = "Name cannot be blank")
    @Size(min = 3, max = 50, message = "Name must be between 3 and 50 characters")
    private String name;

    @NotBlank(message = "Email cannot be blank")
    @Email(message = "Email must be valid")
    private String email;

    @Min(value = 18, message = "Age must be at least 18")
    @Max(value = 65, message = "Age must be no more than 65")
    private int age;

    @Pattern(regexp = "^\\d{10}$", message = "Phone number must be 10 digits")
    private String phoneNumber;
}
```