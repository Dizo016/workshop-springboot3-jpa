# 🛠️ Course Project – Spring Boot Backend API

This project is a backend API developed with **Spring Boot**, **Spring Data JPA**, and an **H2 in-memory database**, designed for educational purposes. It simulates a simple e-commerce system with full CRUD operations for entities like `User`, `Order`, `Product`, `Category`, `OrderItem`, and `Payment`.

---

## 🚀 Technologies Used

- Java 17  
- Spring Boot 3.3.3  
- Spring Data JPA  
- H2 Database (in-memory)  
- Maven  

---

## 🗂️ Directory Structure

```bash
course/
├── src/
│   └── main/
│       ├── java/com/educandoweb/course/
│       │   ├── config/
│       │   │   └── TestConfig.java
│       │   ├── entities/
│       │   │   ├── Category.java
│       │   │   ├── Order.java
│       │   │   ├── OrderItem.java
│       │   │   ├── Payment.java
│       │   │   ├── Product.java
│       │   │   ├── User.java
│       │   │   ├── enums/
│       │   │   │   └── OrderStatus.java
│       │   │   └── pk/
│       ├── repositories/
│       │   ├── CategoryRepository.java
│       │   ├── OrderItemRepository.java
│       │   ├── OrderRepository.java
│       │   ├── ProductRepository.java
│       │   └── UserRepository.java
│       ├── resources/
│       │   ├── CategoryResource.java
│       │   ├── OrderResource.java
│       │   ├── ProductResource.java
│       │   └── UserResource.java
│       ├── services/
│       │   ├── CategoryService.java
│       │   ├── OrderService.java
│       │   ├── ProductService.java
│       │   ├── UserService.java
│       │   └── exceptions/
│       │       ├── DataBaseException.java
│       │       └── ResourceNotFoundException.java
│       ├── exceptions/
│       │   ├── ResourceExceptionHandler.java
│       │   └── StandardError.java
│       └── CourseApplication.java
│
└── resources/
    ├── application.properties
    └── application-test.properties
pom.xml  
README.md
```
---

✅ Features
- Layered architecture (Controller, Service, Repository)
- CRUD operations for all main domain entities
- Enum-based order status system (OrderStatus)
- Exception handling for resource not found and database violations
- Test configuration with H2 in-memory database
- Formatted SQL output and access to H2 web console

⚙️ H2 Database Configuration
    spring.datasource.url=jdbc:h2:mem:testdb  
    spring.datasource.driverClassName=org.h2.Driver  
    spring.datasource.username=sa  
    spring.datasource.password=  
    spring.jpa.database-platform=org.hibernate.dialect.H2Dialect  
    spring.jpa.show-sql=true  
    spring.jpa.properties.hibernate.format_sql=true  
    spring.h2.console.enabled=true  
    spring.h2.console.path=/h2-console  

Access the H2 console at:
http://localhost:8080/h2-console

▶️ How to Run
# Using Maven wrapper
./mvnw spring-boot:run

# Or manually on Windows with javac
mkdir bin 2>$null
javac -d bin src\application\*.java src\boardgame\*.java src\chess\*.java src\chess\pieces\*.java
java -cp bin application.Program

🧪 Running Tests
# Run automated tests
./mvnw test

🎯 Purpose
This project was created as part of a Spring Boot learning path.  
It helps developers understand how to structure backend applications with JPA,  
RESTful APIs, in-memory databases, service-layer abstraction, and exception handling.  
It is not intended for production use but as a foundation for more complex systems.

📌 Notes
- No authentication or frontend is included in this version.
- Can be extended with features like JWT authentication, pagination, DTOs, and frontend integration.

📎 License
This project is for educational use only. No license attached.
