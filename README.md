# Reminders — Mobile

## Template copy

This repository is one of the name-substituted Ionic React + Vite template copies in `bookchaowalit-mobile`.
The canonical template is
[`bookchaowalit-mobile/marketing-seo-analyzer-mobile`](https://github.com/bookchaowalit-mobile/marketing-seo-analyzer-mobile).
Consolidation or archiving of the copies is pending owner decision D5 (BD-033), per
`repository-catalog/portfolio/MOBILE-CONSOLIDATION-2026-10.md` in solo-empire.
There is no Capacitor native project here: it builds a Vite web app only, not an Android or iOS binary.

Ionic + React cross-platform mobile app for **Reminders**.

Part of [Chaowalit Greepoke](https://bookchaowalit.com)'s 101 Portfolio Projects.

## Features

- **Reminders** (Home tab): add a reminder with a date/time and optional
  daily/weekly/monthly repeat. Reminders are grouped into Overdue, Today,
  Upcoming and Done, saved in `localStorage`, and completing a repeating
  reminder rolls it to its next occurrence (monthly repeats clamp to month end).
- Reminder logic lives in `src/lib/reminders.ts` (pure TypeScript, unit-tested).

## Tech Stack

- **Framework:** Ionic 8 + React 18
- **Language:** TypeScript
- **Build Tool:** Vite
- **UI:** Ionic Components + Ionicons

## Getting Started

```bash
npm install
npm run dev
```

## Scripts

```bash
npm run dev         # Vite dev server
npm run typecheck   # tsc (noEmit)
npm run lint        # ESLint flat config (typescript-eslint + react-hooks)
npm test            # vitest unit tests for src/lib
npm run build       # tsc && vite build
```

CI (`.github/workflows/ci.yml`) calls the shared `bookchaowalit/platform-ci-workflows` v1.1.1
(`ci-node.yml` + `security.yml`, pinned by SHA): `npm ci`, lint, typecheck, tests, `npm run build`, and the
gitleaks / Semgrep / OSV-Scanner / Trivy scans. Failures are not masked.

## Build

```bash
npm run build
# Static web build in dist/. A native app would need a Capacitor project, which does not exist yet.
```

## Related

- **Frontend:** [bookchaowalit-website/reminders-frontend](https://github.com/bookchaowalit-website/reminders-frontend)
- **Portfolio:** [bookchaowalit.com](https://bookchaowalit.com)

## License

MIT
