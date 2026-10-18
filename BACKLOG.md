# Backlog

Future work, not yet scheduled.

## Content

- **Reviews section testimonials** — `index.html` `#reviews` currently shows only the
  Google (4.4★ / 707 reviews) and Facebook (4.5★ / 80 reviews) rating summaries with
  links out. Add 2–3 real customer quote snippets (with attribution) once they're
  picked out — do not fabricate quotes.
- **Saturday Morning classes photo** — the reference site (ashland-skate.netlify.app)
  includes a photo of skaters practicing in the `#classes` section. Add a real photo
  if/when one is available.

## Engineering

- **Modernize JS syntax** — the inline `<script>` in `index.html` currently uses `var`
  throughout. Refactor to `const`/`let`.
- **Separate concerns** — `index.html` and `menu/index.html` currently inline all CSS
  (`<style>`) and JS (`<script>`) in the HTML file itself, per current convention
  documented in `CLAUDE.md`. Consider splitting into separate `.css`/`.js` files
  (shared where the two pages duplicate rules) once a decision is made to move off the
  single-file-per-page pattern. Note this is a deliberate departure from the current
  "no build process" static-site convention, so confirm hosting/caching setup still
  works with multiple requested files before doing this.
