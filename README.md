Wells Fargo – Software Engineering Job Simulation (Task 2)
📌 Overview

This project is part of the Wells Fargo Software Engineering Job Simulation hosted on Forage.
The objective of this task was to design and implement a data model for a financial advisory system using Spring Boot and Java Persistence API (JPA).

The system models how financial advisors manage clients, client portfolios, and securities.

🎯 Objectives

Design an Entity Relationship Diagram (ERD) for the system

Convert the ERD into JPA entity classes

Implement correct entity relationships

Use Maven for build management

Use Git & GitHub for version control

🛠️ Technologies Used

Java

Spring Boot

Java Persistence API (JPA)

Maven

Git & GitHub

VS Code / IntelliJ IDEA

🧩 Data Model (Entities)
1. Advisor

Represents a financial advisor who manages multiple clients.

Key fields:

advisorId (auto-generated)

firstName

lastName

address

phone

email

2. Client

Represents a client managed by an advisor.

Key fields:

clientId (auto-generated)

firstName

lastName

address

phone

email

Relationship:

Many clients belong to one advisor (@ManyToOne)

3. Portfolio

Represents a client’s investment portfolio.

Key fields:

portfolioId (auto-generated)

totalValue

Relationship:

One portfolio belongs to one client (@OneToOne)

4. Security

Represents an investment held within a portfolio.

Key fields:

securityId (auto-generated)

name

category

purchaseDate

purchasePrice

quantity

Relationship:

Many securities belong to one portfolio (@ManyToOne)

🔗 Entity Relationships Summary

Advisor → Client : One-to-Many

Client → Portfolio : One-to-One

Portfolio → Security : One-to-Many

▶️ How to Build the Project
Prerequisites

Java JDK installed

Git installed

Steps
# Navigate to project directory
cd wells-fargo-task-2

# (Temporary workaround for Windows if JAVA_HOME is not set)
set JAVA_HOME=C:\Program Files\Java\jdk-22

# Build the project
mvnw.cmd clean install


Expected output:

BUILD SUCCESS

📂 Project Structure
src/main/java/com/wellsfargo/counselor/entity
 ├── Advisor.java
 ├── Client.java
 ├── Portfolio.java
 └── Security.java

✅ What Was Accomplished

Designed a clean relational data model

Implemented JPA entities with correct annotations

Configured entity relationships

Successfully built the project using Maven

Pushed the completed solution to GitHub

📜 Certificate

This project was completed as part of the Wells Fargo Software Engineering Job Simulation on Forage.

👤 Author

Moram Navadeep
