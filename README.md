# PulseForge

An AI-assisted observability and incident response learning project built with Java.

## Project overview

PulseForge will monitor simulated services. The simulator will send health checks, performance metrics such as response time and error rate, and structured logs. This lets the project demonstrate monitoring without requiring existing services.

When PulseForge detects a problem, it will create an incident and gather the relevant metrics and logs from the five minutes before the alert. AI will use that evidence to summarize what may have happened and suggest investigation steps. The summary will link to its supporting evidence, and a person will decide what action to take. PulseForge will not automatically change or restart services.

## Planned features

- Generate normal service activity and repeatable failure scenarios.
- Receive and validate health checks, metrics, and structured logs.
- Detect problems using rules and create incident notifications.
- Show an AI-assisted summary with likely causes, recommended investigation steps, and links to relevant evidence.
- Let a person review the incident and decide what to do.
- Measure PulseForge's own health and behavior under controlled load.

## Technologies and topics to learn

**Backend:** Java, Spring Boot, Maven, PostgreSQL, and database migrations.

**Messaging and testing:** RabbitMQ, JUnit, Mockito, integration testing, and Testcontainers.

**DevOps:** Docker, Docker Compose, GitHub Actions CI/CD, Kubernetes, Helm, and Argo CD.

**Operations and system design:** Spring Actuator, Micrometer, Prometheus, Grafana, load testing, event processing, and distributed-system fundamentals.

**AI:** provider-neutral integration, evidence-grounded summaries, evaluation, and safe handling of failures and sensitive data.

This is a learning project. The simulator and planned features will be built incrementally; performance results will be reported with their test conditions.
