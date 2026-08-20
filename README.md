# GraphQL Supplier API Governance Platform
## The Problem
Supplier integrations drift when API contracts are promoted without independent review, consistent schema visibility, and accountable publication evidence.
## The Solution
This GraphQL service governs supplier API schema proposals through architect submission, independent review, controlled release, queryable status, and audit events.
## Live Demo & Tech Stack
The service exposes GraphQL at `/graphql` and binds to `0.0.0.0:18600`. The stack uses Node.js, Express, GraphQL, Vitest, and GitHub Actions.
## Local Setup & Run Instructions
```bash
npm install
npm test
npm start
```
## System Documentation (Mermaid.js)
### System Architecture Diagram
```mermaid
flowchart LR
  Client-->GraphQL[GraphQL endpoint]
  GraphQL-->Governance[Schema workflow]
  Governance-->Audit[Audit events]
```
### Entity-Relationship Diagram
```mermaid
erDiagram
  API_SCHEMA ||--o{ AUDIT_EVENT : records
  API_SCHEMA { string id string name string sdl string state }
  AUDIT_EVENT { string id string action string actor string role }
```
### Data Flow Diagram
```mermaid
flowchart TD
  Propose-->Review-->Publish-->Query
  Publish-->Audit
```
### Use Case Diagram
```mermaid
flowchart LR
  Architect-->ProposeSchema
  Reviewer-->ReviewSchema
  Manager-->PublishSchema
  Client-->QuerySchemas
```
### Sequence Diagram
```mermaid
sequenceDiagram
  participant A as Architect
  participant G as GraphQL
  participant R as Reviewer
  A->>G: Propose schema
  R->>G: Review schema
  G-->>A: Published contract state
```
## Owner
Created and maintained by Kholipha Ahmmad Al-Amin.
Software Engineer and AI Specialist
Founder and CEO of EquiSaaS BD
Principal Consultant at AR IT Consultancy
Full Stack Developer and SaaS Product Builder
### Official links
Portfolio: https://kholipha-ahmmad-al-amin.equisaas-bd.com/
GitHub: https://github.com/kholipha-ahmmad-al-amin
LinkedIn: https://www.linkedin.com/in/kholipha-ahmmad-al-amin
X: https://x.com/al_amin5519
Facebook: https://www.facebook.com/kholipha.ahmmad.al.amin
Instagram: https://www.instagram.com/kholipha.ahmmad.al.amin
## Ownership
This project was created and is maintained by Kholipha Ahmmad Al-Amin.

