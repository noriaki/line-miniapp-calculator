<!-- Inclusion Mode: Always -->

# Project Overview and Technical Context

## Project Description

最新のモダンなNext.jsによる四則演算電卓Webアプリケーション。TypeScriptとVitestを使用した堅牢な開発環境で構築。

## Technical Stack

### Core Technologies
- **Framework**: Next.js (最新版)
- **Language**: TypeScript 5.9+ (strict mode enabled)
- **Runtime**: Node.js 20+
- **Package Manager**: pnpm 10.16.1

### Build Configuration
- **Module System**: ESM modules
- **Module Resolution**: Bundler
- **Target**: ESNext
- **TypeScript**: Strict mode with all type checking enabled

### Testing Framework
- **Test Runner**: Vitest 3.2.4
- **Coverage Tool**: @vitest/coverage-v8
- **Testing Approach**: In-source testing enabled via import.meta.vitest

## Development Principles

### Code Quality Standards
1. **Type Safety**: すべてのコードはTypeScriptの厳格モードで記述
2. **Testing**: すべての主要機能にユニットテストを実装
3. **Modern Syntax**: 最新のESNext機能を積極的に使用

### File Organization
```
src/
├── app/          # Next.js App Router
├── components/   # Reusable UI components
├── lib/          # Utility functions and business logic
└── styles/       # Global styles and theme
```

### Component Architecture
- **Component Library**: モダンなReactコンポーネントパターンを使用
- **State Management**: React標準のuseStateとuseReducerを活用
- **Styling**: CSS ModulesまたはTailwind CSSを使用

## Calculator Specific Guidelines

### Calculator Features
1. **基本四則演算**: 加算(+)、減算(-)、乗算(×)、除算(÷)
2. **小数点対応**: 小数点を含む計算をサポート
3. **エラーハンドリング**: ゼロ除算などのエラーケースを適切に処理
4. **キーボード入力**: テンキーとキーボード入力の両方をサポート

### UI/UX Requirements
- **レスポンシブデザイン**: モバイル、タブレット、デスクトップに対応
- **アクセシビリティ**: WCAG 2.1 AA準拠
- **パフォーマンス**: 初回ロード時間を最小化

### Testing Requirements
```typescript
// すべての計算機能にテストを実装
describe('Calculator', () => {
  it('should perform basic arithmetic operations', () => {
    // テスト実装
  });

  it('should handle edge cases properly', () => {
    // エラーケースのテスト
  });
});
```

## CI/CD Configuration

### GitHub Actions
- **Node Version**: 24
- **Workflow Triggers**: push and pull requests to main branch
- **Quality Gates**:
  - TypeScript type checking must pass
  - All tests must pass
  - Coverage threshold: 80%

### Available Scripts
```bash
pnpm test        # Run tests
pnpm test:cov    # Run tests with coverage
pnpm check       # Run typecheck and tests
pnpm dev         # Start development server
pnpm build       # Build for production
```

## Important Notes

1. **Project Origin**: This project was bootstrapped from [ts-guide](https://github.com/mizchi/ts-guide) and ejected on 2025-09-14
2. **Development Approach**: Follow TDD (Test-Driven Development) principles
3. **Code Reviews**: All changes should be reviewed before merging to main

## Next.js Specific Configuration

### App Router
- Use App Router (app directory) for routing
- Server Components by default, Client Components where needed
- Implement proper loading and error boundaries

### Performance Optimization
- Use Next.js Image component for any images
- Implement proper code splitting
- Utilize Next.js built-in optimization features

### SEO and Metadata
- Implement proper metadata for calculator app
- Ensure Open Graph tags are configured
- Add appropriate title and description