# Sahha frontend

A React and TypeScript frontend prototype for Sahha, a healthcare platform concept. This repository contains the UI, role-based demonstration workflows, and integration code for the authentication journey. Most domain workflows currently use typed mock implementations; they are not connected to completed Spring services.

## Run locally

Prerequisites: Node.js and npm. From the repository root:

```bash
npm ci
npm run dev
```

Use `npm run build`, `npm run typecheck`, and `npm test` to check the project. The environment settings are described in `.env.example` and `FRONTEND_INTEGRATION.md`.

## Integration status

The frontend supports an authentication adapter through API Gateway and a separate mock mode for domain workflows. The documented hybrid setup uses `VITE_USE_MOCKS=true` and `VITE_USE_AUTH_MOCKS=false`; a running Auth service and Gateway are required for that mode. Use the mock auth option for a standalone UI demonstration. See `FRONTEND_INTEGRATION.md` for the precise environment settings, API contract, and which role flows are demo-only.

This is a learning project in progress. Do not use mock workflows or UI role checks as evidence of a production healthcare backend. The [backend repository](https://github.com/faresjebal/sahha_backend) currently contains documentation rather than runnable service code.
