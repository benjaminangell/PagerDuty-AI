# Kaluza PagerDuty Best Practice Standards

> **Owner:** Ben Angell
> **Source of Truth:** [Ownership Repository](https://github.com/ovotech/ownership)
> **PagerDuty Instance:** [ovo-tech.pagerduty.com](https://ovo-tech.pagerduty.com)

---

## Table of Contents

1. [Guiding Principles](#1-guiding-principles)
2. [Taxonomy: Naming Conventions](#2-taxonomy-naming-conventions)
3. [Service Severity Tiers](#3-service-severity-tiers)
4. [On-Call Schedule Standards](#4-on-call-schedule-standards)
5. [Escalation Policy Structure](#5-escalation-policy-structure)
6. [Business Services](#6-business-services)
7. [User & Access Standards](#7-user--access-standards)
8. [Responsibilities](#8-responsibilities)
9. [Anti-Patterns Reference](#9-anti-patterns-reference)
10. [Getting Help](#10-getting-help)

---

## 1. Guiding Principles

- **Team names in PagerDuty must match the ownership repo** (`team/*.json` → `TeamName` field). This is the canonical source of truth.
- **Services are named after what they monitor**, not the team or monitoring tool.
- **Schedules are never empty.** Every on-call rotation must have at least a primary responder at all times.
- **Individuals are never assigned directly to escalation policies** — always use a schedule.
- **Every engineer must configure their own notification preferences** and be reachable within 15 minutes during on-call hours.

---

## 2. Taxonomy: Naming Conventions

### 2.1 Teams

Teams map 1:1 to the ownership repo `TeamName`. The table below defines the canonical PagerDuty team names across all value streams:

| Value Stream | PagerDuty Team Name | Jira Key | Region |
|---|---|---|---|
| **Core Billing & Scalability** | | | |
| | Ledger and Finance | LAF | UK |
| | Exception Management | EX | UK |
| | Billing Coordinator | BC | UK |
| | Billing Australia | BAUS | AUS |
| **Energy Commerce** | | | |
| | EnCom Core 1 | ECFS | UK |
| | EnCom Core 2 | — | UK |
| | EnCom Sales Management | ECC | AUS |
| | EnCom Tariffs and Charging Aus | TCAUS | AUS |
| **Payments & Credits** | | | |
| | PAC EU 1 | PAC1 | UK |
| | PAC EU 2 | PAC2 | UK |
| | PAC EU 3 | PACEU3 | UK |
| | PAC EU 4 | PACEU4 | UK |
| | PAC AUS 1 | PAC3 | AUS |
| | PAC AUS 2 | PACAUS2 | AUS |
