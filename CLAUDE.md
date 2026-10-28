# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project

Arcade Vault: online gaming platform where users play and compete for points. Scaffolded with `create-next-app`, still at starter-template state (default `app/page.tsx`/`app/layout.tsx` content not yet replaced).

## Commands

```bash
npm run dev     # start dev server (Turbopack)
npm run build   # production build
npm run start   # run production build
npm run lint    # eslint
```

No test runner is configured yet.

## Next.js version warning

This repo uses Next.js 16.4.2 (`app/` router) — **not** the Next.js in your training data. Before writing Next.js code, read the relevant guide under `node_modules/next/dist/docs/` (`01-app/`, `02-pages/`, `03-architecture/`, `04-community/`). Heed deprecation notices. See `AGENTS.md` for the enforced version of this rule.

Notable config in `next.config.ts`:
- `experimental.agentFeedback`, `cacheComponents`, `partialPrefetching` are enabled — check the docs above for what these change about rendering/caching semantics before assuming standard Next.js behavior.
- CSS is processed via `@tailwindcss/turbopack` loader (Tailwind v4, no `tailwind.config.js`).

## Workflow: Spec Driven Design

This project follows spec-driven design using the `/spec` and `/spec-impl` commands from the `fernando-skills` package:

```bash
npx skills@latest add Klerith/fernando-skills
```

Follow practices from https://github.com/Klerith/fernando-skills when adding features — write/update a spec before implementation.

## Skills
usa siempre /frontend-design para diseñar la interfaz del usuario.

## Stack

- Next.js 16 (App Router) + React 19 + TypeScript (strict mode)
- Tailwind CSS v4 (Turbopack loader, no separate config file)
- Path alias `@/*` → repo root (`tsconfig.json`)
