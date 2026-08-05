# Phase 2 — Level 1 Data Flow Diagram

## Objective

The Level 1 Data Flow Diagram provides a high-level view of the banking platform by illustrating how users interact with the system and how data flows between major components.

It serves as the foundation for identifying trust boundaries, sensitive assets, and attack surfaces in subsequent phases of the threat modeling process.

---

## Components

- Customer
- Internet
- Cloudflare
- Load Balancer
- API Gateway
- Backend
- PostgreSQL
- Redis
- Amazon S3
- AWS KMS
- Amazon CloudWatch

---

## Data Flow

1. Customer sends requests through the Internet.
2. Cloudflare filters and forwards traffic.
3. Requests pass through the Load Balancer.
4. API Gateway routes requests to the Backend.
5. Backend communicates with:
   - PostgreSQL
   - Redis
   - Amazon S3
6. S3 uses AWS KMS for encryption.
7. Backend sends logs and metrics to CloudWatch.

---

## Security Significance

This DFD establishes:

- Primary entry points
- Critical system components
- Sensitive data stores
- External services
- Future trust boundaries


<img width="933" height="870" alt="SecureBank - Digital Banking Platform Threat Modeling drawio (1)" src="https://github.com/user-attachments/assets/4e7b66ee-90a2-450d-a493-e3d17815a7c7" />
