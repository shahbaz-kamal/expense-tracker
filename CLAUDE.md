# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Commands

```bash
npm run dev       # Start dev server at http://localhost:5173
npm run build     # Build production bundle to /dist
npm run preview   # Preview the production build
npm run lint      # Run ESLint
```

No test suite is configured.

## Architecture

This is a single-page React + Vite app. All application logic lives in one file:

- **`src/App.jsx`** — contains all state, filtering logic, form handling, and rendering
- **`src/main.jsx`** — entry point that mounts `<App />` in `<React.StrictMode>`
- **`src/App.css`** / **`src/index.css`** — component and global styles

State is managed via `useState` hooks in `App.jsx`:
- `transactions` — array of `{ id, description, amount, type, category }` objects
- form input fields (description, amount, type, category)
- filter fields (filterType, filterCategory)

Categories: `food`, `housing`, `utilities`, `transport`, `entertainment`, `salary`, `other`.

## Context

This is a course starter project from a CodeWithMosh Claude Code tutorial. The codebase **intentionally contains bugs, poor UI, and messy code** meant to be identified and fixed during the course. When exploring the code, expect issues rather than treating existing patterns as correct.
