# Spec Kit Constitution: Payment Gateway

## Product Intent
Stripe and Crypto payment gateway

## Architectural Invariants
- Zero Blast-Radius: Isolated sandbox execution per task.
- Strict TDD: BDD acceptance tests frozen before code development.
- Clean Code & Deterministic Verification: Sole oracle is test runner exit code == 0.
