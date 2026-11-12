# TokenChain Tickets

**TokenChain Tickets** is an academic and portfolio project exploring a safer, more transparent way to issue, verify, and manage event tickets. It combines a conventional web application with blockchain-backed ticket ownership and traceability.

The project is oriented toward cultural and sports events in Latin America. Its goal is to make the attendee and organizer experience familiar while using verifiable digital assets where they add value.

> This repository is the public project overview. The complete application source code is maintained separately in a private repository and is not included here.

## What the platform is intended to do

- Let attendees discover events, manage their accounts, and access purchased tickets.
- Give organizers tools to create and administer events and ticket inventory.
- Represent eligible tickets as NFTs so ownership and transfers can be independently verified.
- Support QR-based ticket presentation and validation at event entry.
- Explore controlled peer-to-peer resale and marketplace workflows.
- Connect web-based payments and asynchronous processing with the ticket lifecycle.

These are project goals and areas represented in the application. Their implementation and readiness vary; this overview does not claim that a production service or public smart contract is deployed.

## How it fits together

1. Attendees and organizers use a React web application.
2. The application communicates with a FastAPI service for accounts, events, tickets, and operational workflows.
3. PostgreSQL stores application records; Redis and Celery are used for background work.
4. Payment providers handle payment flows, while blockchain integrations target Polygon Amoy during development.
5. Ticket presentation and validation connect the application record to the attendee's ticket and, where enabled, its on-chain representation.

See [Architecture overview](docs/architecture.md) for a component view and boundaries.

## Technology

| Area | Technologies |
|---|---|
| Web client | React, TypeScript, Vite |
| API | Python, FastAPI, SQLAlchemy |
| Data and background work | PostgreSQL, Redis, Celery |
| Smart contracts | Solidity, Hardhat, OpenZeppelin |
| Development and operations | Docker Compose, Nginx, Alembic |

The exact versions and operational configuration are defined in the private source repository and may change as the project evolves.

## Project status

This is a work in progress developed in an academic and portfolio context. Polygon Amoy is a test network, not a production deployment. Payment, wallet, email, and blockchain integrations require environment-specific configuration and must be reviewed before use.

No credentials, private keys, deployment instructions, or application source code are published in this overview repository.

## Documentation

- [Architecture overview](docs/architecture.md) — components, responsibilities, and data flow.
- [Guide for AI-assisted review](docs/ai-review-guide.md) — how to review the project responsibly and produce useful next steps.

## Source code

The complete source repository is private: [nicoprog4/tokenchain-web3-ticketing](https://github.com/nicoprog4/tokenchain-web3-ticketing). Access requires authorization from its owner.

## Language

The project and its working documentation are primarily in Spanish. This overview is written in English to make the project easier to discover; the private source repository contains the detailed project documentation.
