# Project 1: AI-Powered Banking Knowledge Assistant

## 1. Project Overview

Build a full-stack application that answers questions about a
curated collection of synthetic banking policies and educational
documents.

The application will progressively introduce Java, Spring Boot,
React, TypeScript, PostgreSQL, automated testing, and AI engineering.

This is an educational software engineering project. It is not
intended to provide financial advice or execute banking transactions.

## 2. Problem Statement

Banking policies and procedures can be difficult to search and
understand. Users need a convenient way to ask questions and find
relevant information from a controlled knowledge base.

The application will provide a structured foundation for searching
banking documents and, in later stages, generating AI-assisted answers
grounded in retrieved content.

## 3. Target Users

- Learners exploring banking concepts.
- Users seeking information from the application's sample documents.
- Developers evaluating a full-stack application with AI capabilities.

## 4. Initial Functional Requirements

FR-01: The application shall expose a health-check endpoint.

FR-02: The backend shall provide a REST API for retrieving available
       knowledge documents.

FR-03: The backend shall support searching the knowledge base.

FR-04: The frontend shall display a search interface and search results.

FR-05: The frontend shall communicate with the backend through HTTP APIs.

FR-06: The application shall validate incoming requests and return
       consistent error responses.

FR-07: The application shall use PostgreSQL for persistent storage
       when database integration is introduced.

FR-08: The application shall support automated backend tests.

FR-09: The project shall document local setup and execution instructions.

FR-10: AI-assisted question answering and source attribution shall be
       introduced in a later milestone.

## 5. Non-Functional Requirements

NFR-01: Code shall be readable, maintainable, and organized into
        appropriate layers.

NFR-02: Configuration shall be externalized where appropriate.

NFR-03: Secrets and credentials shall not be committed to Git.

NFR-04: The application shall provide useful logs and error messages.

NFR-05: Automated tests shall cover important application behavior.

NFR-06: The project shall have reproducible build and setup instructions.

NFR-07: AI-generated answers shall not be presented as verified facts
        without appropriate supporting evidence.

NFR-08: Synthetic data shall be used; real customer information shall
        not be included.

## 6. Initial Technology Stack

Backend:
- Java
- Spring Boot
- Maven
- Spring Web
- JUnit

Database:
- PostgreSQL
- SQL migrations, introduced in a later milestone

Frontend:
- React
- TypeScript
- HTML and CSS
- npm

Engineering:
- Git and GitHub
- Automated tests
- API documentation
- Docker and CI/CD, introduced progressively

AI:
- LLM integration
- Retrieval-Augmented Generation (RAG)
- Source attribution and evaluation

## 7. Acceptance Criteria

AC-01: The backend can be built using Maven.

AC-02: The backend starts successfully in the local development
       environment.

AC-03: The health-check endpoint returns a successful response when
       the application is healthy.

AC-04: Backend API behavior is covered by automated tests.

AC-05: The frontend can be installed and started using documented
       npm commands.

AC-06: The frontend can retrieve and display results from the backend.

AC-07: Database operations work correctly when PostgreSQL integration
       is implemented.

AC-08: AI-assisted answers can be evaluated against a documented set
       of test questions before release.

AC-09: Setup, testing, configuration, and deployment instructions
       are documented.

AC-10: The repository contains no committed secrets or credentials.

## 8. Implementation Milestones

Milestone 1: Requirements, architecture, and development environment.

Milestone 2: Java and Spring Boot fundamentals; health-check API.

Milestone 3: Knowledge-document REST APIs and automated tests.

Milestone 4: PostgreSQL schema, migrations, and persistence.

Milestone 5: React and TypeScript fundamentals; search interface.

Milestone 6: Backend/frontend integration and error handling.

Milestone 7: AI integration, retrieval, and source attribution.

Milestone 8: Security, quality checks, Docker, and CI/CD.

Milestone 9: Deployment preparation and release documentation.

## 9. Scope Boundaries

The initial version will not:
- Execute financial transactions.
- Access real banking systems.
- Process real customer data.
- Make autonomous financial decisions.
- Treat unsupported AI-generated statements as authoritative.

## 10. Status

Current status: Requirements drafted.

Implementation has not yet started.
