# Production-Grade FastAPI Backend (Auth, SQLAlchemy 2.0, Alembic)

[![Python](https://img.shields.io/badge/Python-3.12-blue.svg)](https://www.python.org/)
[![FastAPI](https://img.shields.io/badge/FastAPI-Latest-teal)](https://fastapi.tiangolo.com)
[![SQLAlchemy](https://img.shields.io/badge/SQLAlchemy-2.0-red)](https://www.sqlalchemy.org/)
[![CI/CD](https://github.com/stevencesario/xecution.ai-api-demo/actions/workflows/ci.yml/badge.svg)](https://github.com/stevencesario/xecution.ai-api-demo/actions/workflows/ci.yml)

> **Portfolio Context:** This repository serves as supporting **Proof of Work** for my core Meta CAPI architecture. While the *domain* (behavioral AI) is different, it demonstrates my mastery of the exact production-grade stack required to build secure, multi-tenant SaaS applications: **FastAPI**, **SQLAlchemy 2.0**, **Pydantic V2**, **Alembic migrations**, and **secure JWT Authentication**.

---

## ⚡ Architectural Proof of Work

This repository showcases the following high-leverage technical competencies:

* **Modern & Robust Backend:** Built with **FastAPI** for high-performance, async-ready API endpoints.
* **Modern ORM:** Uses **SQLAlchemy 2.0** for a fully type-annotated, modern data access layer.
* **Rigorous Data Validation:** Leverages **Pydantic V2** for clear API contracts and declarative `computed_field` responses.
* **Secure Authentication:** Implements stateless, secure user sessions using **JWT** and `passlib` for password hashing.
* **Safe Database Migrations:** Managed via **Alembic** to ensure reliable and repeatable schema changes.
* **Clean Architecture:** Demonstrates a clear separation of concerns (API endpoints `main.py`, business logic `services.py`, data access `crud.py`, and database `models.py`).
* **Atomic Transactions:** Uses atomic endpoints for critical state changes, ensuring data integrity across multiple tables.
* **Fully Tested & Automated:** Includes a comprehensive **Pytest** suite and a **GitHub Actions CI/CD pipeline**.

## 🏗️ System Architecture
```text
User Client (Web/Mobile App)
       │
       ▼ (HTTPS API Requests)
+---------------------------------+
|      FastAPI Application        |
|  (main.py - Endpoint Layer)     |
+---------------------------------+
       │
       ▼ (Business Logic Delegation)
+---------------------------------+
|      Service Layer              |
|  (services.py - Business Logic) |
+---------------------------------+
       │
       ▼ (Database Operations)
+---------------------------------+
|      Data Access Layer          |
|  (crud.py - Read/Write Logic)   |
+---------------------------------+
       │
       ▼ (ORM Mapping)
+---------------------------------+
|      Database Models & Schema   |
|  (models.py, schemas.py)        |
+---------------------------------+
       │
       ▼
+---------------------------------+
|      PostgreSQL Database        |
|  (Migrations via Alembic)       |
+---------------------------------+
```
