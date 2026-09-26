# Task Den

A single-page task tracker with a GitHub-style activity heatmap, four themed
sections (Work, Admin, Life, Play), subtasks, and mood-driven mascots per
section. Pure HTML/CSS/JS, no build step.

Data is stored in a shared Supabase project (Postgres) with no login —
anyone who opens the page sees and edits the same tasks and progress log.

## Usage

Open `index.html` in a browser and start adding tasks.

## Supabase project

- Project: `task-den-tracker` (`ap-southeast-1`)
- Tables: `tasks`, `subtasks`, `progress_log`, with RLS policies open to
  anyone holding the anon key (no per-user separation)
- The anon key embedded in `index.html` is meant to be public; do not treat
  data in these tables as private.
