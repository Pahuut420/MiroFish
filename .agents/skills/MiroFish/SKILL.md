```markdown
# MiroFish Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches the core development patterns and conventions used in the MiroFish TypeScript codebase. It covers file naming, import/export styles, commit message conventions, and testing patterns. While no specific frameworks or CI workflows are detected, this guide provides clear steps and commands to help you contribute effectively to MiroFish.

## Coding Conventions

### File Naming
- Use **camelCase** for all file names.
  - Example: `userProfile.ts`, `fishTankManager.ts`

### Imports
- Use **relative imports** for referencing other modules.
  - Example:
    ```typescript
    import { getFish } from './fishUtils';
    ```

### Exports
- Use **named exports** rather than default exports.
  - Example:
    ```typescript
    // fishUtils.ts
    export function getFish(id: string) { /* ... */ }
    export function feedFish(id: string) { /* ... */ }
    ```

### Commit Messages
- Follow the **Conventional Commits** specification.
- Use the `chore` prefix for maintenance and non-feature changes.
  - Example:  
    ```
    chore: update dependencies to latest versions
    ```
- Average commit message length: ~76 characters.

## Workflows

### Committing Changes
**Trigger:** When making any change to the codebase  
**Command:** `/commit-changes`

1. Stage your changes with `git add`.
2. Write a commit message using the Conventional Commits format, primarily with the `chore` prefix.
   - Example: `chore: refactor fish feeding logic for clarity`
3. Commit your changes with `git commit -m "<message>"`.
4. Push your changes to the repository.

### Adding a New Module
**Trigger:** When creating a new feature or utility module  
**Command:** `/add-module`

1. Name your new file using camelCase (e.g., `newFeature.ts`).
2. Use named exports for all functions and constants.
   - Example:
     ```typescript
     export function newFeature() { /* ... */ }
     ```
3. Use relative imports to include this module elsewhere.
   - Example:
     ```typescript
     import { newFeature } from './newFeature';
     ```
4. If applicable, create a corresponding test file (see Testing Patterns).

## Testing Patterns

- Test files follow the pattern: `*.test.*` (e.g., `fishUtils.test.ts`).
- Testing framework is **unknown**; check existing test files for patterns.
- Place test files alongside or near the modules they test.
- Example test file structure:
  ```typescript
  // fishUtils.test.ts
  import { getFish } from './fishUtils';

  describe('getFish', () => {
    it('returns the correct fish object', () => {
      // test implementation
    });
  });
  ```

## Commands
| Command          | Purpose                                      |
|------------------|----------------------------------------------|
| /commit-changes  | Guide for committing code using conventions  |
| /add-module      | Steps for adding a new module                |
```
