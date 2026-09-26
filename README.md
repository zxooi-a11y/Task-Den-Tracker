# Task Den

A single-page task tracker with a GitHub-style activity heatmap, four themed
sections (Work, Admin, Life, Play), subtasks, and mood-driven mascots per
section. Pure HTML/CSS/JS, no build step.

Data is stored in Supabase (Postgres + Auth). Each visitor signs in with
email/password; tasks, subtasks, and daily progress points are scoped to
their account via row-level security.

## Usage

Open `index.html` in a browser, create an account (or sign in), and start
adding tasks.

## Supabase project

- Project: `task-den-tracker` (`ap-southeast-1`)
- Tables: `tasks`, `subtasks`, `progress_log`, all with RLS restricting rows
  to `auth.uid() = user_id`
- The anon/publishable key embedded in `index.html` is safe to expose
  client-side; it only grants access permitted by RLS policies.
