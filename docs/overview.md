# Project Overview

This project uses the following stack:

## Core Technologies
- **Language**: TypeScript 5.9+
- **Runtime**: Node.js 20+
- **Package Manager**: pnpm 10.16.1

## Build Configuration
- **TypeScript**: Strict mode enabled, ESNext target
- **Module System**: ESM modules
- **Module Resolution**: Bundler

## Testing
- **Test Runner**: Vitest 3.2.4
- **Coverage**: V8 (@vitest/coverage-v8)
- **In-source Testing**: Enabled with import.meta.vitest

## Code Quality
- **Type Checking**: TypeScript strict mode
- **Test Scripts**: `pnpm test`, `pnpm test:cov`
- **Validation**: `pnpm check` (combines typecheck and tests)

## CI/CD
- **Platform**: GitHub Actions
- **Node Version**: 24
- **Workflow**: Automated testing on push and pull requests to main branch

---

*This project was bootstrapped from [ts-guide](https://github.com/mizchi/ts-guide) and ejected on 2025-09-14.*