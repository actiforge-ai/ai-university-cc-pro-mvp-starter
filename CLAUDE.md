# CLAUDE.md — [Your Project Name]

> Starter repo for AI University's **MVP to Production (Developer Edition)**
> course. Fill the brackets below once you've named your project in `PRD.md`.

## What this is
[One sentence: what your project does — see PRD.md]

## Stack
- Language: TypeScript
- Framework: Next.js (App Router) + React
- Datastore: Supabase (Postgres)
- Package manager: npm

## Run & test
- Install: `npm install`
- Dev: `npm run dev`
- Typecheck: `npm run typecheck`
- Lint: `npm run lint`

## House convention: keep Supabase calls in lib/data/
Only `lib/data/*` should import from `@supabase/ssr` or `@supabase/supabase-js`.
Routes and components call into `lib/data/` — they never run a query directly.
This keeps your data access swappable and testable as you scope and reshape
the project across the course.

## Coding style
- ES modules / async-await, 2-space indent, descriptive names
- Comment WHY, not WHAT — skip obvious comments

## How to work here
- Read existing code before changing anything
- Small, focused changes — not big rewrites. This course is about scoping
  ruthlessly; resist the urge to build more than the current vertical slice needs.
- Run `npm run typecheck` after changes before saying done
- If a request seems wrong, ask before proceeding

## Security
- Secrets go in `.env.local` only — see SECURITY.md
- `.env.local` is gitignored; never commit it
- `SUPABASE_SERVICE_ROLE_KEY` is server-only — never import `lib/data/supabase-server.ts` from a Client Component

## Project-specific notes
[Anything non-obvious about your specific project: conventions, gotchas, key directories]
