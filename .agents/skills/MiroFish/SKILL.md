```markdown
# MiroFish Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches the core development patterns, coding conventions, and workflows used in the MiroFish TypeScript codebase. It covers file naming, import/export styles, commit message conventions, and testing patterns to ensure consistency and maintainability across the project.

## Coding Conventions

### File Naming
- Use **camelCase** for all file names.
  - Example: `miroFishEngine.ts`, `userSettings.test.ts`

### Import Style
- Use **relative imports** for all modules.
  - Example:
    ```typescript
    import { getUserSettings } from './userSettings';
    ```

### Export Style
- Use **named exports** only.
  - Example:
    ```typescript
    // userSettings.ts
    export function getUserSettings() { ... }
    ```

### Commit Message Convention
- Use **Conventional Commits** with the following prefixes:
  - `feat`: For new features
  - `docs`: For documentation changes
- Keep commit messages concise (average ~55 characters).
  - Example:
    ```
    feat: add fish movement algorithm
    docs: update README with setup instructions
    ```

## Workflows

### Conventional Commit Workflow
**Trigger:** When making a commit
**Command:** `/conventional-commit`

1. Stage your changes.
2. Write a commit message using the allowed prefixes (`feat`, `docs`).
3. Keep the message concise and descriptive.
4. Commit your changes.

### Add New Feature
**Trigger:** When implementing a new feature
**Command:** `/add-feature`

1. Create a new TypeScript file using camelCase naming.
2. Use relative imports to include dependencies.
3. Use named exports for all functions or constants.
4. Write or update corresponding test files (`*.test.ts`).
5. Commit your changes using the `feat` prefix.

### Update Documentation
**Trigger:** When updating or adding documentation
**Command:** `/update-docs`

1. Edit or create documentation files as needed.
2. Commit your changes using the `docs` prefix.

## Testing Patterns

- Test files follow the pattern: `*.test.*` (e.g., `miroFishEngine.test.ts`)
- Testing framework is **unknown**; check existing test files for structure.
- Place test files alongside the code they test or in a dedicated test directory.
- Example test file name: `userSettings.test.ts`

## Commands
| Command               | Purpose                                      |
|-----------------------|----------------------------------------------|
| /conventional-commit  | Guide for writing conventional commit messages|
| /add-feature          | Steps to add a new feature                   |
| /update-docs          | Steps to update documentation                |
```
