# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

@AGENTS.md

## Commands

- `npm run dev` — start dev server (http://localhost:3000)
- `npm run build` / `npm start` — production build / serve
- `npm run lint` — ESLint (flat config in `eslint.config.mjs`)
- No test runner is configured yet.

## Project state

Currently a fresh `create-next-app` scaffold (Next.js 16, React 19, Tailwind v4, TypeScript; only `app/layout.tsx`, `app/page.tsx`, `app/globals.css`). The planned build is an pixel-faithful Instagram clone, driven step by step by the numbered prompts in `prompts/` (01 overview → 10 stories). Execute only the prompt the user points to, and wait for confirmation between prompts.

## Project rules (from `prompts/01- Project Overview.prompt.md`)

- Allowed stack only: Next.js 16 App Router, TypeScript, React, Tailwind, shadcn/ui, Clerk (auth), Prisma + PostgreSQL, Zod, UploadThing. Do not suggest other libraries/frameworks or extra features.
- Prisma schema must never exceed 6 models.
- Required screens: landing page with sign-in, sign-up, feed (stories etc.), search modal, notifications modal, create post modal, profile page (own and other users').
- Every route must include `error.tsx` and `loading.tsx`.
- Prefer server components, derived state, and event-driven logic; avoid `useEffect` unless unavoidable.
- `screenshots/` is the primary reference for UI/UX/layout/behavior — consult it before building any screen.
- If unsure about something, say "I don't know" rather than guessing.
