# Grill: PulseForge project direction
Date: 2026-11-16

## Intent
Build a portfolio learning project that teaches Java backend engineering, system design, AI integration, and DevOps by processing simulated operational telemetry and helping investigate incidents.

## Constraints
- Keep sessions realistic for about 30 minutes per day over a 90-day learning plan.
- The user is the developer; default to mentoring rather than implementing.
- No real external services are required; use a simulator and repeatable scenarios.
- Demonstrate scale through controlled measurements, not unsupported claims.

## Key decisions
- Decision: Name the project PulseForge. Reason: A concise name suited to a platform processing service signals and shaping operational response. Alternative considered: keeping OpsDesk, an incident/change CRUD-oriented project.
- Decision: Include metrics and structured logs in the first version. Reason: The AI assistant needs both operational trends and error details to form useful explanations.
- Decision: Use a bounded five-minute pre-alert context window. Reason: Keep investigation relevant and limit the data provided to AI.
- Decision: AI summaries must reference supporting telemetry and present likely causes as hypotheses. Reason: Make conclusions inspectable rather than asking users to trust generated text.
- Decision: AI recommends actions for human review and does not execute remediation in v1. Reason: Keep operational authority with the user while learning safe AI integration.
- Decision: Simulated services generate known failure scenarios. Reason: Make detection, evaluation, and demos repeatable without live services.
- Decision: Begin with a modular Spring Boot application and add asynchronous processing and infrastructure as learning goals justify them. Reason: Learn system boundaries without premature service sprawl.

## Surfaced assumptions
- A project can demonstrate capacity and system design through a documented workload and reproducible benchmarks without claiming a large real user base.
- Logs improve AI investigations only when they are structured, bounded, and correlated with relevant metrics.

## Open questions
- Which AI provider/model and exact integration library to use; decide when implementation begins after checking current official documentation.
- Which local load profile and performance targets are meaningful; establish a baseline before setting targets.

## Out of scope
- Autonomous remediation in the first version.
- Requiring real production services or real user traffic.
- Adding specialized storage, many microservices, or a frontend before a demonstrated need.
