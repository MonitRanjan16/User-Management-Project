# Spring Boot Developer Internship Assignment

## Features
- User Registration & Login (JWT Auth)
- CRUD operations for Users & Countries
- External API Integration from restcountries.com
- Docker & Docker Compose support
- Swagger UI Documentation

## Setup Instructions

### Docker Build & Run
```bash
docker-compose up --build
```

### Access Application
- App URL: http://localhost:8080
- Swagger UI: http://localhost:8080/swagger-ui.html

### Postman Collection
Import `postman_collection.json` (provided separately)

### Endpoints
- `/auth/register` - Register
- `/auth/login` - Login (returns JWT)
- `/countries/fetch` - Fetch and save countries
- `/countries` - CRUD on countries
- `/countries/search?name=india` - Search by name (partial match)

## Notes
- Default DB: MySQL on port 3307
- Update environment vars in `docker-compose.yml` if needed

---

## ✅ JWT Setup (Behind the Scenes)
- `SecurityConfig.java` for password encoder, JWT filter, role-based access
- `User.java`, `UserRepository.java`, `Role.java` enum
- `AuthenticationController.java` for login/register
- `JwtService.java`, `JwtAuthFilter.java`, `JwtUtils.java` for token generation/validation

---

## ✅ Docker Setup
- `Dockerfile` and `docker-compose.yml` included
- MySQL image with root/user, password and db name pre-configured
