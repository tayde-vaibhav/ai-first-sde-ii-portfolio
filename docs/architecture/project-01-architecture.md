# Project 1: AI-Powered Banking Knowledge Assistant
## Initial System Architecture

### 1. Architecture Objective

Define the initial architecture for a full-stack application that
searches a curated collection of synthetic banking knowledge documents.

The architecture will evolve incrementally as new requirements
and capabilities are implemented.

### 2. Architectural Style

The initial application will use a layered backend architecture
and a separate frontend application.

Backend layers:
- Controller: handles HTTP requests and responses.
- Service: implements application and business logic.
- Repository: abstracts database access.
- Database: persists knowledge documents and related data.

Frontend:
- React components render the user interface.
- TypeScript provides static type checking.
- An API client communicates with the Spring Boot backend.

AI capabilities will be introduced after the core application
and its tests are established.

### 3. Logical Architecture

User
 |
 v
React + TypeScript Frontend
 |
 | HTTP / JSON
 v
Spring Boot REST Controllers
 |
 v
Service Layer
 |
 v
Repository Layer
 |
 v
PostgreSQL Database

Future AI extension:

Service Layer
 |
 v
Retrieval and AI Orchestration
 |
 +--> Knowledge Retrieval
 |
 +--> LLM Provider
 |
 v
Answer with Supporting Sources

The AI extension is a planned capability, not an implemented component.

### 4. Component Responsibilities

#### 4.1 Frontend

Responsibilities:
- Display the search interface.
- Accept user queries.
- Call backend REST endpoints.
- Display search results and application errors.
- Provide loading and empty-result states.

Technology:
- React
- TypeScript
- HTML and CSS
- npm

#### 4.2 REST API

Responsibilities:
- Expose documented HTTP endpoints.
- Validate request parameters.
- Return structured JSON responses.
- Apply consistent error handling.

Technology:
- Java
- Spring Boot
- Spring Web

#### 4.3 Service Layer

Responsibilities:
- Implement search and retrieval use cases.
- Enforce application rules.
- Coordinate repository operations.
- Provide a suitable boundary for future AI orchestration.

The service layer must not depend on frontend implementation details.

#### 4.4 Repository Layer

Responsibilities:
- Read and persist application data.
- Isolate database access from business logic.

Planned technology:
- Spring Data JPA
- PostgreSQL

#### 4.5 Database

Responsibilities:
- Persist knowledge documents and associated metadata.
- Enforce appropriate data constraints.
- Support reliable querying.

Schema and migration scripts will be introduced in a later milestone.

#### 4.6 AI Extension

Planned responsibilities:
- Retrieve relevant passages from the knowledge base.
- Provide retrieved context to an LLM.
- Generate answers grounded in available evidence.
- Return supporting source references.
- Support repeatable evaluation of answer quality.

AI output must not automatically be treated as correct.

### 5. Initial API Contract

The following endpoints are planned.

#### GET /api/v1/health

Purpose:
Return the application's health status.

Expected initial response:
{
  "status": "UP"
}

#### GET /api/v1/documents

Purpose:
Retrieve available knowledge documents.

The response structure will be finalized before implementation.

#### GET /api/v1/documents/search?q={query}

Purpose:
Search the knowledge base using a query parameter.

The behavior for empty queries, invalid parameters, and no matches
will be defined and tested during implementation.

#### Future AI endpoint

POST /api/v1/assistant/ask

Purpose:
Accept a question and return an AI-generated answer with supporting
source references.

This endpoint will be implemented only after retrieval and
evaluation requirements have been established.

### 6. Security Principles

- Do not commit passwords, tokens, API keys, or other secrets.
- Validate user input.
- Return safe error messages without exposing internal details.
- Use synthetic banking documents for development.
- Introduce authentication and authorization when required by
  the application's evolving scope.
- Treat retrieved documents and model-generated content as
  untrusted input.
- Do not execute banking transactions or make financial decisions.

### 7. Testing Strategy

Backend:
- Unit tests for service logic.
- Controller/API tests.
- Integration tests for persistence and database behavior.

Frontend:
- Component tests.
- Tests for loading, success, empty, and error states.
- Tests for backend API interactions.

AI:
- A repeatable evaluation dataset.
- Checks for source attribution and unsupported claims.
- Tests for questions that cannot be answered from the knowledge base.

### 8. Deployment Strategy

Initial development:
- Run the backend locally.
- Run the frontend locally.
- Use the local PostgreSQL installation when persistence is introduced.

Future deployment:
- Containerize the application where appropriate.
- Configure environment-specific settings.
- Run automated quality checks before release.
- Deploy to the planned OCI development instance when available.

Deployment configuration will be finalized after the application
runs successfully in the local environment.

### 9. Architecture Decisions

ADR-001: Use a layered Spring Boot backend.

Reason:
Separate HTTP handling, application logic, and data access.

ADR-002: Use React with TypeScript for the frontend.

Reason:
Build a maintainable frontend while learning React fundamentals.

ADR-003: Use PostgreSQL for persistent application data.

Reason:
Practice relational data modelling, SQL, constraints, and indexing.

ADR-004: Introduce AI capabilities incrementally.

Reason:
Establish a tested, understandable application before adding
retrieval, LLM integration, and AI-specific failure modes.

### 10. Current Status

Architecture status: Initial design documented.

Implementation status: Not started.

The architecture and API contracts may be refined as requirements,
tests, and implementation experience provide additional evidence.
