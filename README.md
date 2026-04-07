# Playwright + TypeScript QA Automation Framework

A small portfolio-ready UI automation framework using Playwright, TypeScript, layered architecture, fixtures, flows, page objects, environment-based config, and GitHub Actions CI.

## Tech Stack
- Playwright
- TypeScript
- Node.js
- GitHub Actions

## Folder Structure
```text
src/
  assertions/   # reusable validations
  config/       # env and routes
  constants/    # ui messages and constants
  data/         # test users and inputs
  fixtures/     # custom Playwright fixtures
  flows/        # business actions / reusable user journeys
  pages/        # page objects
tests/
  ui/           # ui test specs
.github/
  workflows/    # ci pipeline
```

## Why this structure?
- **Pages** keep selectors and page-level actions together.
- **Flows** represent business actions like login/logout.
- **Assertions** keep verification logic reusable and clean.
- **Fixtures** reduce duplication in tests.
- **Config + env** make local and CI execution easier.

## Setup
```bash
npm ci
cp .env
npx playwright install
npm run test:ui
```

## Available Scripts
```bash
npm test
npm run test:ui
npm run test:smoke
npm run test:headed
npm run report
```

## CI / GitHub Actions
This repo includes a workflow at `.github/workflows/playwright.yml`.

Add these GitHub repository secrets:
- `BASE_URL`
- `API_URL`
- `USER_EMAIL`
- `USER_PASSWORD`

## Current Coverage
- valid login
- invalid login
- required field validation
- logout after login

## Good next improvements
- add API tests
- add reusable components layer
- add test tagging strategy by smoke/regression
- add Allure reporting
- add parallel browser matrix later if needed
