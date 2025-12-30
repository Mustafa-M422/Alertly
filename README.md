# Alerlty – Subscription & Bill Reminder Platform

## CI Information
**Build Status:** GitHub Actions (lint + tests on every pull request)

---

## Project Summary

**Alerlty** is a **local-first web application** that helps users track recurring subscriptions and bills, receive timely reminders, and analyze spending patterns over time.

Unlike many commercial personal finance tools, Alerlty avoids bank integrations and third-party financial services. Instead, it emphasizes **transparency, privacy, and explicit user control**. Users manually define subscriptions and billing cycles, making costs, renewals, and reminder logic easy to understand and verify.

A key innovation of the project is its **Synthetic Data Engine**, which generates realistic subscription and billing activity (including churn, payment failures, and retries). This enables robust testing, analytics, and demonstrations without using real financial data.

This project is developed as part of **SOEN 490 (Capstone Software Engineering Project)** at Concordia University and is intended to demonstrate **engineering design and implementation for a complex, open-ended problem**, in accordance with CEAB requirements.

---

## Motivation & Problem Statement

Recurring subscriptions and bills are easy to forget and difficult to reason about over time. Existing tools often:
- Require invasive bank integrations
- Hide billing and reminder logic behind opaque automation
- Add unnecessary features that increase complexity

Alerlty addresses this problem by providing a **simple, user-managed system** where users explicitly define, track, and understand their recurring financial commitments.

---

## Key Features

- **Subscription Management**  
  Create and manage subscriptions with service name, category, cost, billing frequency, and lifecycle dates.

- **Bill Generation & Tracking**  
  Generate bill occurrences and track payment status (paid, late, failed).

- **Reminder & Retry Logic**  
  Detect upcoming renewals, overdue bills, and retry failed payments.

- **Spending Analytics**  
  Dashboards showing monthly totals, upcoming obligations, and top cost drivers.

- **Synthetic Data Engine**  
  Deterministic, seeded simulations of subscriptions, churn, and billing behavior for testing and experimentation.

---

## Engineering Design Philosophy

This project is intentionally **engineering-driven**, not feature-driven.

### Design Principles
- Local-first and privacy-friendly architecture
- Clear separation of concerns
- Fail-fast, risk-driven development
- Deterministic behavior for testing
- Continuous integration and structured logging from day one

The system is designed to be **understandable, testable, and maintainable**, even with a small team.

---

## Technology Stack

### Frontend
- React
- Vite
- TypeScript

### Backend
- Node.js
- Express
- TypeScript

### Database
- PostgreSQL
- Prisma ORM

### Infrastructure & Tooling
- Docker & Docker Compose
- JWT-based authentication
- Zod (input and environment validation)
- Pino (structured logging)
- Jest & Supertest (testing)
- GitHub Actions (CI)

---

## Developer Getting Started Guide

### Prerequisites
- Docker
- Docker Compose
- Git
- Node.js (optional for local development)

---

### Quick Setup

git clone <repository-url>
cd alerlty
docker compose up --build

## Environment Configuration

The project uses environment variables for configuration and secret management.

- Create a `.env` file in the `backend` directory using `.env.example` as a template
- Environment variables include database connection details, JWT secrets, and application ports
- No secrets are committed to the repository

If required environment variables are missing, the application will fail fast during startup.

---

## Contributors

| Name | Student ID | GitHub |
|------|------------|--------|
| Ava Samimi | 40048117 | GitHub username |
| Mostafa Mohamed | 40201893 | Mustafa-M422 |

---

## License

This project is licensed under the MIT License.  
See the `LICENSE` file for details.
