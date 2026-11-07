# Secure-Tenant-Portal

> **Note:** This repository is a personal copy of [Dael777z/Secure-Tenant-Portal](https://github.com/Dael777z/Secure-Tenant-Portal), the original team project. It is kept here to showcase my contributions.

## My contributions (Mohammad)

I served as project manager and forward-deployed engineer for the student team. I did not write the application code; the students built it.

- Answered technical questions from the student developers and mentored the team throughout the project
- Helped the team organize its time and plan its work
- Acted as the bridge between the client and the students, aligning expectations on both sides
- Explained technical concepts to the client in plain terms
- Communicated the client's expectations and priorities to the team

React (Vite) + Express + TypeScript + PostgreSQL resident portal for Summit Property Management (NMSU CSCI 4980 senior project).

## What it does

A web portal for Summit Property Management, built by a student team for a real client. It replaces a mix of RentRedi and spreadsheets with one place for residents and property staff.

**Residents**
- See their unit, balance and full rent ledger
- Pay rent by bank transfer, with a bank account linked through Plaid
- File maintenance requests and follow their status
- Get notices for rent due, payments received and repair updates

**Property managers**
- Dashboard with occupancy, rent collected vs. expected, overdue accounts and open maintenance
- Properties, units, tenants and leases, including residents and cosigners per lease
- Rent roll with filters and search
- Record office payments (check, cash, money order, bank transfer) and change rent or end a lease
- Maintenance queue across all properties

**Maintenance staff** see only the maintenance queue.

Signup is invite-only: the office adds a tenant first, and only that tenant can create an account. Tenants can only reach their own lease, payments, requests and bank accounts, and the manager API is closed to them.

## Stack

| Layer | Tools |
|---|---|
| Frontend | React 19, Vite, TypeScript |
| Backend | Node.js, Express 5, TypeScript |
| Database | PostgreSQL 16 (SQL migrations, seed data) |
| Auth | JWT access and refresh cookies, bcrypt, role-based access control |
| Payments | Plaid Link (bank account linking, sandbox) |
| Logging | pino |
| Testing | Vitest (unit and database integration tests) |
| Tooling | Docker Compose for local Postgres, one-click Windows demo launcher |

**Try it on Windows:** double-click `Start Demo.cmd`, then sign in as a tenant (`tenant@example.com` / `tenant-demo-password`) or the property manager (`manager@example.com` / `manager-demo-password`). Details, the API, and what each teammate's part does: [docs/M1-DATABASE-INTEGRATION.md](docs/M1-DATABASE-INTEGRATION.md).
