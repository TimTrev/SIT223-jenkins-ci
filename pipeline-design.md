# Pipeline Design – SIT223 Part 1 Task 1

This document describes a 7-stage Jenkins pipeline for continuous integration and deployment.  
Each stage specifies its purpose and a commonly used tool.

---

### Stage 1: Build
- **Purpose**: Compile and package the application code.  
- **Tool**: Maven (for Java), Gradle (alternative).

### Stage 2: Unit and Integration Tests
- **Purpose**: Run unit tests to confirm individual components work, and integration tests to check components work together.  
- **Tools**: JUnit (Java unit tests), Mocha/Jest (JavaScript), TestNG (integration).

### Stage 3: Code Analysis
- **Purpose**: Analyse code for style, standards compliance, and maintainability.  
- **Tools**: SonarQube or ESLint (JavaScript), Checkstyle (Java).

### Stage 4: Security Scan
- **Purpose**: Identify vulnerabilities in code and dependencies.  
- **Tools**: OWASP Dependency-Check, Snyk, or Trivy.

### Stage 5: Deploy to Staging
- **Purpose**: Deploy the build to a staging environment that mimics production.  
- **Tools**: AWS EC2, Docker Compose, Kubernetes (for containerised apps).

### Stage 6: Integration Tests on Staging
- **Purpose**: Validate the deployed application works correctly in a staging environment.  
- **Tools**: Postman (API tests), Selenium (UI tests), Cypress (web end-to-end).

### Stage 7: Deploy to Production
- **Purpose**: Promote the application from staging to production for end users.  
- **Tools**: AWS EC2, Kubernetes, or Ansible for automated deployment.

---
