# University Management System (UMS)
### Gruppe 08 — Software Architecture Documentation

---

## Project Overview

The University Management System is a web-based platform developed for a regional Austrian university. The system replaces manual administrative processes — including paper-based course enrollment, grade management and fee collection — with a centralized, secure and reliable digital solution.

Developed by a regional software company as an external client project for the university.

---

## Architecture Documentation

This repository contains the complete Arc42 architecture documentation for the UMS, including all diagrams and architectural decisions.

| File | Description |
|---|---|
| `docs/arc42-gruppe08.pdf` | Full Arc42 architecture documentation |
| `diagrams/` | All architecture diagrams (Building Block View, Deployment View, Runtime View etc.) |

---

## System Overview

- **Frontend:** Angular (role-based UI for students, lecturers and administrators)
- **Backend:** Java Spring Boot (microservices architecture)
- **Database:** PostgreSQL (Schema-per-Service pattern)
- **Authentication:** JWT tokens with BCrypt hashing
- **External Integrations:** Stripe (payments), SendGrid (email), Moodle LMS

---

## Microservices

| Service | Responsibility |
|---|---|
| user-service | User management and authentication |
| course-service | Course catalog and capacity management |
| enrollment-service | Atomic course enrollment — prevents double booking |
| grade-service | Grade and exam management |
| finance-service | Fee management and Stripe payment processing |
| notification-service | Asynchronous email and push notifications |

---

## Quality Goals (ISO 25010:2023)

| Priority | Quality Goal |
|---|---|
| 1 | Reliability — stable under peak load, no data loss |
| 2 | Security — role-based access, HTTPS, GDPR compliant |
| 3 | Functional Suitability — all features meet stakeholder needs |
| 4 | Maintainability — independent service deployment |
| 5 | Performance Efficiency — 95% of requests under 2 seconds |

---

## Team

**Gruppe 08** — Software Architecture Course  
Regional software company scenario — client: Austrian regional university

---