# Voting-Application

A small Spring Boot web application that demonstrates a simple voting system with user registration, authentication, admin and user dashboards, and candidate management.

## Features

- User registration and login (Spring Security)
- Admin dashboard with vote totals
- User dashboard to view profile and cast a vote
- Candidate management and vote counting (seeded on startup)
- Thymeleaf templates and static assets for UI

## Tech stack

- Java 17
- Spring Boot (parent: 2.6.5)
- Spring Data JPA, Spring Security, Thymeleaf
- MySQL (configured via `application.properties`)
- Maven (wrapper included)

## Prerequisites

- JDK 17
- MySQL server (or change datasource to a different DB)
- Git (optional)
