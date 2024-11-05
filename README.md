
# Spring Boot Project Setup and Deployment Workflow

## Table of Contents
- [Introduction](#introduction)
- [Getting Started](#getting-started)
- [Project Structure](#project-structure)
- [Installation and Setup](#installation-and-setup)
- [Build and Run](#build-and-run)
- [Version Control Workflow](#version-control-workflow)
- [Branching Strategy](#branching-strategy)
- [Contributing](#contributing)
- [License](#license)

## Introduction
This is a Spring Boot application created using Spring Initializr, designed to demonstrate a complete workflow from setup to deployment, including branching for `master`, `prod`, `preprod`, and `dev` environments. This project also includes REST API functionality and utilizes Maven for build automation.

## Getting Started
This guide will help you set up, build, and deploy this project in a structured manner, ensuring code versioning and environment separation.

## Project Structure
The core components of the project include:
- **Controller**: Contains REST API methods.
- **Service**: (Optional) Handles business logic.
- **Repository**: (Optional) Interfaces for data access.
- **Application**: The main entry point for the Spring Boot application.

## Installation and Setup

1. **Clone the Repository**:
   ```bash
   git clone <repository-url>
   ```
2. **Workspace Setup**:
   - Create a folder named `myworkspace` on your local machine (e.g., `C:\myworkspace`).
   - Extract the project into `myworkspace`.

3. **Dependencies**:
   - Maven and Java (JDK 11 or later) should be installed.

## Build and Run

To build and run the application, use the following Maven commands:

```bash
mvn clean compile       # Compile the project
mvn clean package       # Package the project as a JAR
mvn spring-boot:run     # Run the Spring Boot application
```

After running, verify the application is live by accessing `http://localhost:8080`.

## Version Control Workflow

### 1. **Connect to GitHub**
   - Set up a GitHub repository and push the initial code:
     ```bash
     git add --all
     git commit -m "Initial commit"
     git push origin master
     ```

### 2. **Create and Fetch Branches**
   - Create the necessary branches (`prod`, `preprod`, and `dev`) locally:
     ```bash
     git branch prod
     git branch preprod
     git branch dev
     ```
   - Fetch all branches from the remote repository:
     ```bash
     git fetch origin
     ```

### 3. **Work on `dev` Branch**
   - Switch to `dev` branch:
     ```bash
     git checkout dev
     ```
   - Make changes, stage, commit, and push:
     ```bash
     git add .
     git commit -m "Initial commit on dev branch"
     git push origin dev
     ```

### 4. **Merge `dev` into `preprod`**
   - Go to GitHub and open a Pull Request (PR) to merge `dev` into `preprod`.
   - Review and merge the PR.

## Branching Strategy
The branching strategy for this project is designed for different environments:
- **master**: Main branch, typically for stable production-ready code.
- **prod**: For production deployment.
- **preprod**: For testing before production.
- **dev**: Active development branch.


