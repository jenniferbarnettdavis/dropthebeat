# Drop the Beat — NETA 2026 Music Trivia

A mobile-first, single-page music trivia game for NETA 2026. Players sign in with Google, play one round per session, and compete on a live leaderboard. Answers are hidden until a reveal time set by the admin.

## Files

- `index.html` — player app (sign in, pick round, play, leaderboard, review)
- `admin.html` — admin dashboard (round schedule, reveal time, admins, stats)
- `assets/` — NETA logo + fonts used by both pages

## Tech

- **Frontend:** static HTML + React via CDN (no build step)
- **Backend:** Supabase (Postgres + Auth + RLS)
- **Auth:** Google OAuth via Supabase
- **Hosting:** GitHub Pages (static)

## Running locally

```bash
python3 -m http.server 5173
# then open http://localhost:5173/
```

For OAuth to work locally, `http://localhost:5173` must be an allowed origin in both Supabase (Auth → URL Configuration) and Google Cloud Console (Credentials → OAuth client → Authorized JavaScript origins).

## Deployment

This repo is served via GitHub Pages from the `main` branch. After pushing to `main`, changes go live at the Pages URL within a minute.
