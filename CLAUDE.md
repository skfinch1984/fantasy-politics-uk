# Fantasy Politics UK

Single-file fantasy-sports-style web app for UK politics. Pick a squad of MPs within a budget, score points as they act in Parliament.

## Structure
- `index.html` — the entire app (HTML + inline CSS + inline JS, ~757 lines, ~55KB). No build step, no dependencies.
- `README.md` — stub.
- Deployed to GitHub Pages via a workflow on the `main` branch (repo: `skfinch1984/fantasy-politics-uk`).

## Pages (SPA tabs)
Navigation is data-attribute driven (`data-page="..."`) with a `navigateTo(page)` function that toggles `.page.active`:
- `dashboard` — points summary + top scorers
- `pick-team` — browse MPs, filter, select within budget
- `my-team` — current squad
- `live` — live scoring
- `rules` — scoring rules

## Design system
Dark theme with gold/red accents. CSS variables at the top of `<style>`:
- `--bg-primary: #0f0f1a`, `--bg-card: #16213e`
- `--accent-red: #e94560`, `--accent-gold: #C9A94E`, `--accent-blue: #0f3460`
- Georgia serif for headings, system sans for body.

## Working on this
- Edit `index.html` directly — everything is inline. Open it in a browser to test; no dev server needed.
- Keep it single-file unless there's a strong reason to split (the appeal is zero-build GitHub Pages deploy).
- Commit to `main` → Pages workflow redeploys.
