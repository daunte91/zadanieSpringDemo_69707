
# Zadanie Spring Demo - Case Study

## Overview
This project demonstrates a simple Spring Boot application that includes essential elements like a REST controller, application configuration, and dependency management through Maven. It is designed for educational purposes and serves as a starting point for building more complex systems.

---

## Project Structure

### Key Components:

1. **`pom.xml`**  
   - Manages project dependencies and build lifecycle.  
   - Includes dependencies for Spring Boot and other required libraries.

2. **Main Application Class** (`zadanieSpringDemoApplication.java`)  
   - The entry point of the application.  
   - Annotated with `@SpringBootApplication`, enabling auto-configuration, component scanning, and other Spring Boot features.

3. **Controller Class** (`HelloController.java`)  
   - Defines a simple REST endpoint.  
   - Handles HTTP GET requests and returns a predefined response.

4. **`application.properties`**  
   - Contains configuration settings for the application, such as the server port.

---

## Detailed Breakdown

### 1. `pom.xml`
The `pom.xml` file specifies the Maven configuration for this project. Key dependencies include:
- **`spring-boot-starter-web`**: Provides the web framework and embedded server.
- **`spring-boot-starter-test`**: Includes libraries for unit and integration testing.

---

### 2. Main Application Class
The main class initializes and launches the Spring Boot application:

```java
@SpringBootApplication
public class zadanieSpringDemoApplication {
    public static void main(String[] args) {
        SpringApplication.run(zadanieSpringDemoApplication.class, args);
    }
}
```

---

### 3. Controller Class
The controller defines a RESTful endpoint accessible at `/api/hello`. It handles HTTP GET requests and returns a simple message:

```java
@RestController
@RequestMapping("/api")
public class HelloController {

    @GetMapping("/hello")
    public String sayHello() {
        return "Hello, Vistula!";
    }
}
```

---

### 4. `application.properties`
The configuration file provides essential settings for the application. Here, it specifies the default server port:

```properties
server.port=8080
```

---

## Running the Application
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/zadanie-spring-demo.git
   cd zadanie-spring-demo
   ```
2. Build and run the project:
   ```bash
   ./mvnw spring-boot:run
   ```
3. Access the application in your browser at:
   ```
   http://localhost:8080/api/hello
   ```

---

## Example Response
When you access the endpoint `/api/hello`, you should see the following response in your browser:
```
Hello, Vistula!
```

---

## Conclusion
This demo Spring Boot application provides a foundational understanding of building RESTful services with Spring. It is ideal for beginners looking to explore the basics of Spring Boot and REST API development.

---


