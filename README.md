# Voting Platform — Spring Boot 3 • Postgres • Flyway • CI • Testcontainers

A production-style voting platform built with **Java 17** and **Spring Boot 3**.  
Supports **multi-election ballots**, **role-based access control (Admin/User)**, and **vote integrity** enforced at the database level.

---

## Features

### Core
- **Authentication & RBAC** (Admin/User)
- **Multi-election voting**
  - `Election` (title, description, start/end window)
  - `Candidate` belongs to an election
  - `Vote` belongs to (user + election + candidate)

### Vote Integrity (Real-world constraints)
- **One vote per user per election** enforced by a DB constraint:
  - `UNIQUE(user_id, election_id)`
- Transactional vote casting (prevents double voting under concurrency)
- Optional audit trail table (`vote_audit`) for traceability

### Production Signals
- **Flyway migrations** for schema + seed data
- **Docker Compose** for local DB setup
- **GitHub Actions CI** (build + tests)
- **Integration tests** using **Testcontainers** (runs against a real Postgres instance)

---

## Tech Stack

- Backend: Java 17, Spring Boot 3 (Web, Security, Data JPA, Validation)
- DB: PostgreSQL
- Migrations: Flyway
- Build: Maven
- Testing: JUnit 5, Spring Test, Testcontainers
- Optional: Thymeleaf UI / REST API (depending on your branch)

