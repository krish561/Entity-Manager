# Entity Manager

A full-stack application built with Spring Boot and React that provides entity management capabilities. This project demonstrates the implementation of a modern web application with a robust backend and responsive frontend.

## Technology Stack

### Backend

- Java 23
- Spring Boot 3.4.2
- Spring Data JPA
- MySQL/H2 Database
- Lombok
- Maven
- Spring Validation
- SLF4J for Logging

### Frontend

- React
- Vite
- Modern JavaScript/TypeScript

## Project Structure

```
EntityManager-main/
├── src/                    # Backend source code
│   ├── main/
│   │   ├── java/          # Java source files
│   │   │   ├── controller/  # REST controllers
│   │   │   ├── entity/     # JPA entities
│   │   │   ├── model/      # Data models
│   │   │   ├── repository/ # JPA repositories
│   │   │   ├── services/   # Business logic
│   │   │   └── MyfirstappApplication.java
│   │   └── resources/     # Application properties and resources
│   └── test/              # Test files
├── frontend-view/         # Frontend React application
│   ├── src/              # React source code
│   ├── public/           # Static assets
│   └── package.json      # Frontend dependencies
└── pom.xml               # Backend dependencies and build configuration
```

## Features

- RESTful API endpoints for entity management
- Database integration with JPA
- Modern React frontend
- Cross-Origin Resource Sharing (CORS) support
- Comprehensive error handling
- Lombok for reduced boilerplate code
- Input validation
- Soft delete functionality
- Advanced search capabilities
- Proper logging throughout the application
- Transaction management
- API versioning

## Entity Structure

The main entity (`FaEntity`) includes:

- ID (auto-generated)
- Name (2-50 characters, required)
- Phone (10-15 digits, required)
- Email (valid email format, required)
- Active status (for soft delete)

## API Endpoints

The application provides the following REST endpoints:

### Base URL: `/api/v1`

#### Employee Management

- `GET /employees` - Get all active employees
- `GET /employees/{id}` - Get employee by ID
- `POST /employees` - Create new employee
- `PUT /employees/{id}` - Update existing employee
- `DELETE /employees/{id}` - Soft delete employee

#### Search

- `GET /employees/search` - Search employees with filters
  - Query Parameters:
    - `name` (optional): Search by name (case-insensitive)
    - `email` (optional): Search by email (case-insensitive)
    - `phone` (optional): Search by phone number

## Error Handling

The application provides proper error handling for:

- Resource not found (404)
- Validation errors (400)
- Server errors (500)
- Custom error messages

## Prerequisites

- Java 23 or higher
- Node.js and npm
- Maven
- MySQL (or H2 for development)

## Getting Started

1. Clone the repository:

```bash
git clone [repository-url]
```

2. Backend Setup:

```bash
cd EntityManager-main
mvn clean install
mvn spring-boot:run
```

3. Frontend Setup:

```bash
cd frontend-view
npm install
npm run dev
```

The backend server will start on `http://localhost:8080` and the frontend development server will be available at `http://localhost:5173`.

## Database Configuration

The application supports both MySQL and H2 databases. The default configuration can be found in `src/main/resources/application.properties`.

## Validation Rules

- Name: Required, 2-50 characters
- Phone: Required, 10-15 digits, valid phone number format
- Email: Required, valid email format

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- Spring Boot team for the excellent framework
- React team for the frontend framework
