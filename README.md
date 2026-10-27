# relay

# Relay — Team Operations Coordination

**Status:** Phase 0, backend scaffold only. No scheduling, persistence, authentication, notifications, or user-facing product logic implemented yet.

Relay aims to help organizers collect volunteer availability/preferences, assign work fairly, track acknowledgments, and recover assignments when people decline or miss response deadlines.

## Current stack
- Java 21
- Spring Boot 3.5.0
- Maven
- Spring Web, Validation, Actuator, JUnit / Spring Boot Test

## Run
Requires JDK 21 and Maven 3.9+.

```bash
mvn spring-boot:run
```

Then try:

```bash
curl http://localhost:8080/api/v1/status
curl http://localhost:8080/actuator/health
```

Run tests:

```bash
mvn test
```

## Next steps
1. Define one real pilot workflow and interview potential organizers.
2. Model `Organization`, `Member`, `Task`, `Preference`, `Assignment`, and `Acknowledgment`.
3. Add PostgreSQL + schema migration tool (Flyway) after approving domain model.
4. Implement task creation, preferences, and simple deterministic assignment.
5. Add assignment acknowledgement + timeout recovery with tests.
6. Add AWS/deployment and UI only once the core workflow has been validated.

See [docs/PRODUCT_SPEC.md](docs/PRODUCT_SPEC.md) for the draft contract.
