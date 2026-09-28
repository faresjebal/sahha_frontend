# Sahha frontend

React and TypeScript frontend for the [Sahha healthcare platform](https://github.com/faresjebal/sahha_backend). This repository contains a frontend-only export. The implementation source of truth is the [`frontend/` directory on the backend's `feature/organisation-service` branch](https://github.com/faresjebal/sahha_backend/tree/feature/organisation-service/frontend), where frontend and backend contracts are developed together.

The current internship scope covers organisation administration, patient registration, scheduling, clinical encounters, protected files, messaging, referrals, and limited patient workflows. Some broader demonstration screens and adapters exist as references; their presence does not mean the corresponding backend feature is complete.

## Run locally

Use Node 22 and install the locked dependencies:

```bash
npm ci
npm run dev
```

The browser calls the API Gateway at `http://localhost:8079/api/v1` by default. Copy `.env.example` to an ignored `.env.local` if you need to change local settings. Real Gateway adapters are the default; mock adapters are opt-in for isolated development and demonstrations.

## Validate

```bash
npm run typecheck
npm test
npm run build
```

The complete live patient journey and clean-machine acceptance are still being verified. The [backend implementation plan](https://github.com/faresjebal/sahha_backend/blob/feature/organisation-service/docs/INTERNSHIP_PLAN.md) records the latest results and remaining work. This frontend is not a deployed clinical product. Use synthetic or properly anonymised data only.

`FRONTEND_INTEGRATION.md` is an earlier integration snapshot; use the source-of-truth branch and implementation plan for current status.
