# M-Pesa Merchant Settlement Service 

A lightweight, production-ready backend component built in **Kotlin** designed to ingest, validate, and settle real-time mobile money payment notifications originating from Safaricom's M-Pesa API gateways.

##  System Architecture & Mechanics
- **Webhook Ingestion:** Exposes an isolated service architecture to securely receive incoming JSON validation strings from external payment processing arrays.
- **Data Integration:** Utilizes explicit data serialization modeling to securely abstract transactional identifiers, customer billing details, and platform resolution codes.
- **Idempotency Protection:** Intended to align with robust ledger architectures to prevent duplicate transaction accounting over unstable network states.

##  Key Framework Capabilities
- Evaluates Safaricom transaction response parameters asynchronously.
- Isolates failed codes (`ResultCode != 0`) instantly to prevent premature resource provisioning.
- Separates network payload transfers cleanly from downstream application business logic.
