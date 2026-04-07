# Playwright Clean Architecture Framework

Playwright + TypeScript automation framework using clean architecture, page objects, flows, fixtures, assertions, environment-based config, and GitHub Actions CI.

## Tech Stack

- Playwright
- TypeScript
- GitHub Actions

## Framework Highlights

- Clean folder structure
- Page Object Model
- Flow layer for reusable business actions
- Fixtures for test setup
- Assertions layer
- Environment-based configuration
- CI-ready with GitHub Actions

## Run Locally

```bash
npm install
npx playwright install
npm run test:ui

## Reports

This framework generates:
- Playwright HTML Report
- Allure Report

Both reports are uploaded as GitHub Actions artifacts after every workflow run.