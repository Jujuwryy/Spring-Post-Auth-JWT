# Spring-Post-Auth-JWT / Job Post Management API

A Spring Boot application that manages job posts and user authentication using a dual-database architecture. The application uses MongoDB for storing job posts and PostgreSQL for user management. [Use any api tool for testing. Ideally Postman]

## Technologies Used

- **Spring Boot**: Core framework
- **MongoDB**: For storing job posts data
- **PostgreSQL**: For user management
- **Spring Security**: Authentication and authorization
- **JWT**: Token-based authentication
- **Swagger/OpenAPI**: API documentation
- **AOP**: For logging and monitoring
- **JUnit & Mockito**: Testing framework

## Architecture

- **Dual Database Setup**
  - MongoDB for flexible job post storage
  - PostgreSQL for secure user data management
- **Layered Architecture**
  - Controllers: Handle HTTP requests
  - Services: Business logic
  - Repositories: Data access
  - Models: Data structures
  - Security: Authentication and authorization

## Key Features

- CRUD operations for job posts
- Full-text search capabilities for job posts
- User authentication with JWT
- Role-based access control
- Global exception handling
- Comprehensive logging using AOP
- Swagger UI documentation
- Automated testing suite

## API Endpoints

### Job Posts
- `GET /posts`: Retrieve all posts
- `GET /posts/{id}`: Get post by ID
- `GET /posts/search/{text}`: Search posts by text
- `POST /post`: Create a new post
- `POST /posts`: Create multiple posts
- `PUT /updatepost/{id}`: Update a post
- `DELETE /post/{id}`: Delete a post

### Authentication
- `POST /register`: Register new user
- `POST /login`: Authenticate user and get JWT
- `GET /users`: Get all users (admin access)

## Getting Started

### Prerequisites
- JDK 17 or later
- Maven
- MongoDB
- PostgreSQL

### Configuration

1. Configure MongoDB connection in `application.properties`:
```properties
spring.data.mongodb.host=?
spring.data.mongodb.port=?
spring.data.mongodb.database=?
```

2. Configure PostgreSQL connection:
```properties
spring.datasource.url=jdbc:postgresql://localhost:5432/<your_database>
spring.datasource.username=<your_username>
spring.datasource.password=<your_password>
```

### Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/Spring-Post-Auth-JWT.git
```

2. Navigate to project directory:
```bash
cd job-post-management
```

3. Build the project:
```bash
mvn clean install
```

4. Run the application:
```bash
mvn spring-boot:run
```

## 🔒 Security

- JWT-based authentication
- Password encryption using BCrypt
- Role-based authorization
- Protected endpoints
- Token expiration handling

## 📊 Testing

The project includes comprehensive unit tests for controllers and services. Run tests using:

```bash
mvn test
```

## 📝 Documentation

Access the API documentation through Swagger UI:
```
http://localhost:8080/swagger-ui.html
```

## 🏗 Project Structure

```
src/
├── main/
│   ├── java/
│   │   └── com/
│   │       └── g/
│   │           ├── controller/
│   │           ├── model/
│   │           ├── security/
│   │           ├── service/
│   │           ├── exception/
│   │           └── logging/
│   └── resources/
└── test/
    └── java/
```

## Performance Considerations

- MongoDB text indexing for efficient search
- Connection pooling for both databases
- Proper exception handling and logging
- Optimized database queries

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/<Feature>`)
3. Commit your changes (`git commit -m 'Some <Feature>'`)
4. Push to the branch (`git push origin feature/<Feature>`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.
