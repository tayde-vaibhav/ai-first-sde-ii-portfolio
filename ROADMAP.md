# AI-First SDE-II Engineering Roadmap

## Purpose

Build a portfolio of ten progressively challenging projects that
demonstrate practical competence in Java, Spring Boot, React,
PostgreSQL, software architecture, and AI engineering.

The objective is not to maximize the number of technologies used.
It is to demonstrate sound engineering decisions, working software,
reliable tests, clear documentation, and the ability to explain
architectural trade-offs.

## Learning Method

Every project follows this lifecycle:

1. Understand the business problem.
2. Define requirements and acceptance criteria.
3. Identify the Java, database, frontend, and AI concepts involved.
4. Design the architecture and data model.
5. Define APIs and important failure scenarios.
6. Implement incrementally.
7. Write and execute automated tests.
8. Review security, maintainability, and performance.
9. Document decisions and setup instructions.
10. Publish a verified release to GitHub.

React and TypeScript concepts will be explained from the beginning.

AI-generated implementations must be reviewed and understood before
being accepted. Build and test results must be observed rather than
assumed.

---

## Project 1 — Team Task and Knowledge Hub

**Level:** Intermediate

**Purpose:** Establish the complete Java-to-React development workflow.

### Business problem

Build an application that allows a small engineering team to manage
tasks, record decisions, and maintain searchable project knowledge.

### Core capabilities

- Create, update, view, and archive tasks.
- Organize tasks by status and priority.
- Record project notes and decisions.
- Search and filter records.
- Validate user input.
- Expose REST APIs.
- Present the data through a React interface.

### Learning objectives

- Java classes, interfaces, collections, exceptions, and generics
- Spring Boot application structure and dependency injection
- REST controllers, services, and repositories
- Spring Data JPA and entity relationships
- PostgreSQL schema design
- Maven lifecycle and dependency management
- React components, props, state, and event handling
- TypeScript fundamentals
- HTTP requests and API error handling
- JUnit, Mockito, and integration testing
- Git branches, commits, and pull-request workflows

### AI extension

Use an LLM to summarize project notes and suggest task descriptions.
Initially, AI functionality should be optional and isolated from the
core CRUD functionality.

### Completion evidence

- Reproducible backend and frontend setup
- Database migrations
- Documented API contracts
- Automated tests
- Architecture diagram
- Screenshots or a demonstration
- Tagged GitHub release

---

## Project 2 — Secure Expense and Approval Workflow

**Level:** Intermediate to Advanced

**Purpose:** Apply software engineering to a familiar BFSI-style
business workflow.

### Core capabilities

- Submit and review expense claims.
- Define approval stages.
- Enforce role-based permissions.
- Maintain an audit trail.
- Validate state transitions.
- Prevent unauthorized updates.
- Track approval history.

### Learning objectives

- Spring Security
- Authentication and authorization
- Role-based access control
- Database transactions
- Validation and exception handling
- Audit logging
- Domain modeling
- Negative testing and security testing

### AI extension

Generate explanations or summaries for submitted claims.
AI must not independently approve financial transactions.

### Completion evidence

- Authorization tests
- Audit-trail verification
- Documented workflow state machine
- Security decisions and threat considerations

---

## Project 3 — Payment Integration and Resilience Simulator

**Level:** Advanced

**Purpose:** Demonstrate reliable integration with external services.

### Core capabilities

- Simulate payment initiation and status tracking.
- Handle duplicate requests safely.
- Implement idempotency.
- Simulate timeouts and service failures.
- Retry only appropriate operations.
- Reconcile uncertain payment outcomes.
- Record transaction lifecycle events.

### Learning objectives

- Idempotency keys
- Transaction boundaries
- Concurrency control
- Resilience patterns
- Timeouts and retries
- Structured logging
- Integration testing
- Failure-mode analysis

### AI extension

Use AI to summarize operational failures and explain diagnostic
evidence without changing payment state.

### Completion evidence

- Failure-scenario tests
- Idempotency verification
- Reconciliation documentation
- Sequence diagrams

---

## Project 4 — Document Intelligence and RAG Workbench

**Level:** Advanced

**Purpose:** Build an evidence-grounded document question-answering system.

### Core capabilities

- Upload supported documents.
- Extract and normalize text.
- Split documents into chunks.
- Generate embeddings.
- Retrieve relevant passages.
- Generate answers grounded in retrieved evidence.
- Return citations to source passages.
- Handle questions with insufficient evidence.

### Learning objectives

- LLM APIs
- Embeddings and vector search
- Chunking strategies
- Retrieval and ranking
- RAG architecture
- Prompt design
- Source attribution
- Retrieval and answer evaluation
- Privacy and document access controls

### AI evaluation

Create a representative question set and evaluate retrieval quality,
citation correctness, answer relevance, and unsupported claims.

### Completion evidence

- Document-processing pipeline
- Retrieval architecture
- Evaluation dataset
- Measured evaluation results
- Documented failure cases

---

## Project 5 — AI Support Triage and Tool-Calling Assistant

**Level:** Advanced

**Purpose:** Demonstrate controlled use of LLMs and tools.

### Core capabilities

- Classify incoming support requests.
- Extract structured fields.
- Suggest priority and routing.
- Retrieve relevant knowledge.
- Invoke explicitly permitted application tools.
- Require approval for consequential actions.
- Record tool inputs, outputs, and errors.

### Learning objectives

- Structured model outputs
- Tool calling
- Workflow orchestration
- Input validation
- Least-privilege tool access
- Human approval gates
- AI failure handling
- Prompt-injection defenses
- Evaluation and auditability

### Completion evidence

- Tool permission model
- Evaluation scenarios
- Human-approval workflow
- Audit records
- Documented safety boundaries

---

## Project 6 — Event-Driven Transaction Monitoring

**Level:** Advanced

**Purpose:** Introduce asynchronous processing and event-driven design.

### Core capabilities

- Publish business events.
- Consume events asynchronously.
- Track processing status.
- Handle duplicate delivery.
- Recover from failed processing.
- Monitor queue or consumer health.

### Learning objectives

- Event-driven architecture
- Messaging fundamentals
- Event schemas
- Eventual consistency
- Idempotent consumers
- Retry and dead-letter strategies
- Observability
- Integration testing

### AI extension

Explore AI-assisted investigation summaries for synthetic transaction
events. Do not present model-generated anomaly assessments as proven
fraud findings.

### Completion evidence

- Event-flow diagrams
- Failure-recovery tests
- Operational metrics
- Documented consistency guarantees

---

## Project 7 — Multi-Tenant SaaS Administration Platform

**Level:** Advanced

**Purpose:** Demonstrate secure application design for multiple customers.

### Core capabilities

- Manage organizations and users.
- Enforce tenant-level access boundaries.
- Apply organization-specific configuration.
- Record administrative changes.
- Provide controlled administrative operations.

### Learning objectives

- Multi-tenant data modeling
- Authorization boundaries
- Secure query design
- Tenant isolation testing
- Database indexing
- API versioning
- Configuration management
- Security threat modeling

### AI extension

Provide tenant-scoped knowledge retrieval with explicit authorization
checks before retrieving or returning any document.

### Completion evidence

- Tenant-isolation tests
- Threat model
- Database design
- Authorization documentation

---

## Project 8 — Production Observability and Incident Assistant

**Level:** Advanced to Expert

**Purpose:** Build operational visibility and evidence-based diagnostics.

### Core capabilities

- Collect application logs and metrics.
- Trace requests across components.
- Define health checks.
- Detect selected error-rate or latency thresholds.
- Record incident timelines.
- Present service-health information.

### Learning objectives

- Structured logging
- Metrics and distributed tracing
- Service-level indicators
- Alerting fundamentals
- Performance diagnostics
- Operational runbooks
- Deployment health checks

### AI extension

Summarize incident evidence and suggest investigation steps.
Recommendations must distinguish observed facts from hypotheses.

### Completion evidence

- Observability dashboard
- Sample incident investigation
- Runbooks
- Demonstration of failure detection

---

## Project 9 — Distributed Workflow and Reliability Platform

**Level:** Expert

**Purpose:** Combine distributed systems, reliability, and architectural
trade-offs.

### Core capabilities

- Coordinate multi-step business workflows.
- Persist workflow state.
- Recover from partial failures.
- Support retries and compensating actions.
- Track execution history.
- Expose operational status through APIs.

### Learning objectives

- Distributed transaction trade-offs
- Saga-style workflows
- Durable state machines
- Concurrency and consistency
- Failure recovery
- Backpressure
- Performance testing
- HLD and LLD documentation

### AI extension

Use AI to summarize workflow failures and assist operators with
diagnosis. Deterministic workflow rules remain authoritative.

### Completion evidence

- Architecture decision records
- Failure-recovery demonstrations
- Load-test results
- Consistency and reliability documentation

---

## Project 10 — AI-First BFSI Operations Intelligence Platform

**Level:** Expert Capstone

**Purpose:** Integrate the strongest capabilities developed across
the portfolio into a coherent, production-oriented system.

### Illustrative capabilities

- Secure operational dashboards
- Workflow and case management
- Document intelligence and RAG
- AI-assisted case summarization
- Controlled tool calling
- Human approval workflows
- Audit trails
- Search and reporting
- Operational observability

The final scope will be selected after the earlier projects reveal
which components can be reused responsibly.

### Learning objectives

- End-to-end system architecture
- Domain-driven modeling where appropriate
- Secure API design
- Database and performance optimization
- AI evaluation and governance
- CI/CD and deployment
- Operational readiness
- Architectural trade-off analysis

### Completion evidence

- System architecture and deployment diagrams
- Threat model
- Automated test suite
- AI evaluation report
- Operational runbooks
- Reproducible deployment
- Demonstration and technical case study

---

## Cross-Project Learning Tracks

These tracks continue alongside the ten projects.

### Java and Spring Boot

Progress from language fundamentals to collections, generics,
exceptions, streams, concurrency, dependency injection, REST APIs,
persistence, security, testing, and production concerns.

### React and TypeScript

Start with HTML, CSS, JavaScript, components, JSX, props, state,
events, and forms. Progress to hooks, routing, API integration,
forms, error states, testing, and maintainable frontend architecture.

### PostgreSQL

Progress through SQL, keys, constraints, joins, normalization,
transactions, indexing, query plans, migrations, and concurrency.

### DSA

Practice arrays, strings, hash maps, linked lists, stacks, queues,
trees, graphs, sorting, searching, recursion, and complexity analysis.

### LLD and HLD

Practice object modeling, interfaces, SOLID, design patterns, API
design, capacity estimates, caching, messaging, availability,
consistency, and failure handling.

### AI Engineering

Progress through model APIs, structured outputs, tool calling,
embeddings, retrieval, RAG, evaluation, agent workflows, security,
and human oversight.

### Engineering Delivery

Use Git, code reviews, automated tests, CI/CD, Docker, configuration
management, secrets handling, observability, and deployment practices.

---

## Release Gates

Each project should pass the following applicable gates before release:

1. Requirements and acceptance criteria reviewed.
2. Architecture and database design documented.
3. Build and automated tests pass.
4. Core workflows verified.
5. Security-sensitive paths tested.
6. Setup instructions validated.
7. Documentation reviewed.
8. Known limitations recorded.
9. Git history and repository contents reviewed.
10. Release tagged and published.

AI-enabled projects additionally require explicit evaluation of
relevant failure modes, retrieval quality, or tool permissions.

## Progress Tracking

For each project, maintain:

- Current phase
- Completed milestones
- Pending milestones
- Known blockers
- Key concepts learned
- Test and quality status
- Important design decisions
- Next actionable task

The central portfolio repository maintains the roadmap. Each project
may have its own repository and dedicated working conversation.

## Deployment Strategy

Development and testing begin locally.

OCI deployment will follow after the target VM is available.
Until then, projects should remain reproducible on the local machine,
with deployment artifacts and instructions prepared where practical.

## Guiding Principle

A credible engineering portfolio demonstrates not only what was built,
but also why it was designed that way, how it was tested, what failed,
and how its reliability and maintainability were improved.
