# Wells Fargo Software Engineering Job Simulation – Task 2

## Overview

This repository contains my solution for **Task 2** of the Wells Fargo Software Engineering Job Simulation hosted on Forage.

The objective of this task was to design and implement a financial advisory data model using **Spring Boot**, **Java Persistence API (JPA)**, and **Maven**. The system models how financial advisors manage clients, portfolios, and investment securities through well-structured entity relationships.

---

## Objectives

* Design an Entity Relationship Diagram (ERD) for a financial advisory system
* Convert the ERD into JPA entity classes
* Implement correct database relationships using JPA annotations
* Build and manage the project using Maven
* Practice version control using Git and GitHub

---

## Technologies Used

* Java
* Spring Boot
* Java Persistence API (JPA)
* Maven
* Git
* GitHub
* IntelliJ IDEA / VS Code

---

## System Architecture

The application models the relationship between:

* Advisors
* Clients
* Portfolios
* Securities

### Entity Relationship Flow

```text
Advisor
   │
   ├── One Advisor → Many Clients
   │
Client
   │
   ├── One Client → One Portfolio
   │
Portfolio
   │
   ├── One Portfolio → Many Securities
   │
Security
```

---

## Entity Descriptions

### Advisor

Represents a financial advisor responsible for managing multiple clients.

**Fields**

* advisorId (Auto Generated)
* firstName
* lastName
* address
* phone
* email

**Relationship**

* One Advisor → Many Clients (`@OneToMany`)

---

### Client

Represents an individual client assigned to an advisor.

**Fields**

* clientId (Auto Generated)
* firstName
* lastName
* address
* phone
* email

**Relationship**

* Many Clients → One Advisor (`@ManyToOne`)
* One Client → One Portfolio (`@OneToOne`)

---

### Portfolio

Represents the investment portfolio owned by a client.

**Fields**

* portfolioId (Auto Generated)
* totalValue

**Relationship**

* One Portfolio → One Client (`@OneToOne`)
* One Portfolio → Many Securities (`@OneToMany`)

---

### Security

Represents an investment asset held within a portfolio.

**Fields**

* securityId (Auto Generated)
* name
* category
* purchaseDate
* purchasePrice
* quantity

**Relationship**

* Many Securities → One Portfolio (`@ManyToOne`)

---

## Entity Relationship Summary

| Relationship         | Type        |
| -------------------- | ----------- |
| Advisor → Client     | One-to-Many |
| Client → Advisor     | Many-to-One |
| Client → Portfolio   | One-to-One  |
| Portfolio → Security | One-to-Many |
| Security → Portfolio | Many-to-One |

---

## Project Structure

```text
src/
└── main/
    └── java/
        └── com/
            └── wellsfargo/
                └── counselor/
                    └── entity/
                        ├── Advisor.java
                        ├── Client.java
                        ├── Portfolio.java
                        └── Security.java
```

---

## Building the Project

### Prerequisites

* Java JDK installed
* Maven installed
* Git installed

### Clone Repository

```bash
git clone <repository-url>
cd wells-fargo-task-2
```

### Build Project

```bash
mvn clean install
```

### Windows (If JAVA_HOME is not configured)

```bash
set JAVA_HOME=C:\Program Files\Java\jdk-22
mvnw.cmd clean install
```

### Expected Output

```text
BUILD SUCCESS
```

---

## Key Learning Outcomes

Through this simulation, I gained practical experience in:

* Database modeling and design
* Entity Relationship Diagram (ERD) creation
* JPA entity mapping
* Spring Boot project structure
* Maven build management
* Object-relational mapping (ORM)
* Version control with Git and GitHub

---

## Accomplishments

✔ Designed a complete financial advisory data model

✔ Implemented entity relationships using JPA annotations

✔ Created maintainable and scalable entity classes

✔ Successfully built the project using Maven

✔ Managed source code using Git and GitHub

---

## About the Simulation

This project was completed as part of the **Wells Fargo Software Engineering Job Simulation** provided through Forage, where participants gain practical experience solving real-world software engineering tasks inspired by industry workflows.

---

## Author

**Moram Navadeep**

* Computer Science Student
* Aspiring AI Researcher & Software Engineer
* Passionate about Backend Development, AI Systems, and Financial Technology
