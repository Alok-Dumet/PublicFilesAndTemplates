# CORE

## Stack
OS: Linux (WSL)
Version Control: Git + GitHub
Frontend: Next.js + TypeScript + Tailwind CSS
Backend: FastAPI
Database: Supabase + Postgres + Prisma ORM
Auth: Clerk
Payments: Stripe
Email: Resend
Cache: Upstash Redis
DNS / CDN / Security: Cloudflare
Deployment: Vercel
Error Tracking: Sentry
Analytics: PostHog
CI/CD: GitHub Actions
Package Manager: pnpm
Linting: Ruff (Python) + Prettier (JS/TS)

## Directives
We are Rewriting the ParroTavern project that exists in the old directory. The new ParroTavern will use the modern stack as described in this doc. We will optimize, make better, remove unecessary or old features and practice, and improve.

---

## Project Structure

```
ai/
├── core.md
├── tasks.md
├── issues.md
└── completed/
    └── <YYYY-MM-DD-slug>/
        ├── task.md OR issue.md
        └── explanation.md
```

---

## Procedure

Do NOT archive automatically. Only archive when the user explicitly tells you to (e.g. "archive that," "log it," "move it to completed"). On every other completion, just finish the work and stop.

### Task — only when explicitly told to archive
1. Do the work
2. Remove the entry from `tasks.md`
3. Create `completed/<YYYY-MM-DD-slug>/task.md` — copy the original task description verbatim
4. Create `completed/<YYYY-MM-DD-slug>/explanation.md` — follow Explanation Format below

### Issue — only when explicitly told to archive
1. Do the work
2. Remove the entry from `issues.md`
3. Create `completed/<YYYY-MM-DD-slug>/issue.md` — copy the original issue description verbatim
4. Create `completed/<YYYY-MM-DD-slug>/explanation.md` — follow Explanation Format below

---

## Slug Format

`YYYY-MM-DD-short-description` in kebab-case. 2–5 words. Derived from the task or issue title.

---

## Explanation Format

```
# Explanation: <title>

## What was the task / issue?
## What changed?
## Why this approach?
## Anything to watch for?
```

---

## tasks.md Format

```
# Tasks

## <Task Title>
<Description>
```

---

## issues.md Format

```
# Issues

## <Issue Title>
<Description>
```

---

## Documentation

File: `zdocs/project-map.md`

Update only when told a push is happening or explicitly asked. Not after every task or issue.

When updating, cover:
- What the project does
- Folder structure and responsibilities
- Pages, components, and where they live
- API routes and route handlers
- Key classes, hooks, and utilities
- Database schema and models
- Environment variables
- Conventions and gotchas

Remove anything that no longer exists. Write for a developer who is new to the codebase.

---

## Rules

- One task or issue at a time unless told otherwise
- Work is not done until `completed/` is updated
- Never modify anything inside `completed/`
- Ask before starting anything ambiguous
- No new libraries without asking first

---

## Context Hygiene

- Only read files relevant to the current task or issue
- Never read inside `completed/`
- Never read `zdocs/project-map.md` unless the task involves documentation or you are told to
- Read `tasks.md` and `issues.md` only to locate the current item — do not summarize or reflect back the full contents
- Read `core.md` once at the start of a session — do not re-read it mid-session
