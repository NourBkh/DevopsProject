# DevOps Project: Stock Management System

This project is a **Stock Management System** developed using **React** (Frontend) and **Spring Boot** (Backend). The system includes advanced functionalities for managing stock entities and services, with automated testing and CI/CD pipelines integrated through **Jenkins**.

## Table of Contents

1. [Project Overview](#project-overview)
2. [Features](#features)
3. [Technologies Used](#technologies-used)
4. [Setup and Installation](#setup-and-installation)
5. [Testing](#testing)
6. [Jenkins Pipeline Workflow](#jenkins-pipeline-workflow)
7. [Dockerization](#dockerization)
8. [SonarQube and Nexus Integration](#sonarqube-and-nexus-integration)
9. [Contributing](#contributing)
10. [License](#license)

---

## Project Overview

The Stock Management System allows users to:
- Perform CRUD operations on stock entities.
- Access advanced stock-related services.
- Benefit from a user-friendly frontend and robust backend.

This project also incorporates continuous integration and delivery using Jenkins to automate builds, testing, and deployments.

---

## Features

- **Frontend (React):**
  - User-friendly interface.
  - State management with modern React practices.
  
- **Backend (Spring Boot):**
  - RESTful APIs for stock operations.
  - MySQL database integration.
  - Advanced service functionalities.

- **Testing:**
  - Backend unit testing with JUnit and Mockito.
  - Code coverage reports using JaCoCo.

- **CI/CD:**
  - Automated builds, tests, and deployments with Jenkins.
  - SonarQube analysis for code quality.
  - Nexus integration for artifact storage.

---

## Technologies Used

- **Frontend:**
  - React
  - Node.js

- **Backend:**
  - Spring Boot
  - MySQL
  - JUnit
  - Mockito

- **DevOps Tools:**
  - Docker
  - Jenkins
  - SonarQube
  - Nexus
  - Trivy (for security scans)

---

## Setup and Installation

### Prerequisites
- **Node.js** (v23+)
- **Maven**
- **MySQL**
- **Docker** (with Compose)
- **Jenkins**

### Steps
1. Clone the repository:
   ```bash
   git clone https://github.com/NourBkh/DevopsProject.git

   ## Testing

- **Frontend Testing:**
  - Run the frontend tests using:
    ```bash
    npm test
    ```

- **Backend Testing:**
  - Run the backend unit tests using Maven:
    ```bash
    mvn test
    ```

- **Code Coverage:**
  - The backend uses JaCoCo for code coverage. After running the tests, check the generated code coverage report.

## Jenkins Pipeline Workflow

This project uses Jenkins to automate the build, test, and deployment processes. The Jenkins pipeline includes:

1. **Build:** Build both the frontend and backend applications.
2. **Test:** Run unit tests for both frontend and backend.
3. **Deploy:** Deploy the applications to a staging environment.
4. **SonarQube Analysis:** Perform static code analysis using SonarQube to ensure code quality.
5. **Nexus Integration:** Store build artifacts in Nexus for further usage.

## Dockerization

The project is Dockerized using Docker Compose for both frontend and backend services. The `docker-compose.yml` file defines the services, networks, and volumes needed to run the application in a containerized environment.

To run the application using Docker:
```bash
docker-compose up --build

## SonarQube and Nexus Integration

- **SonarQube:** The project integrates SonarQube for static code analysis to ensure code quality and maintainability. It performs automatic analysis of the codebase and generates reports, which are integrated into the Jenkins pipeline.
  
- **Nexus:** Nexus is used for storing build artifacts and enabling versioning of software components. Once the build is completed, the artifacts (e.g., JAR files) are pushed to Nexus for future use and deployment.

## Contributing

Contributions are welcome! If you have suggestions or improvements for this project, feel free to open an issue or submit a pull request. When contributing, please make sure to follow the existing coding style and add appropriate tests for new features or bug fixes.

### How to Contribute:
1. Fork the repository.
2. Create a new branch for your feature or bug fix.
3. Make your changes and commit them.
4. Push to your forked repository.
5. Submit a pull request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

