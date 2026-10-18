# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

This is the marketing website for Ashland Skateland, a roller rink in Ashland, VA. It is a static site with no build process, no package manager, and no JavaScript framework — just hand-written HTML files with inline CSS served directly.

## Structure

- `index.html` — the main landing page (schedule, party packages, building rental, fundraisers, classes, contact info)
- `menu/index.html` — a separate standalone page for the snack bar menu, served at `/menu/`
- `.htaccess` — Apache config; sets `DirectoryIndex index.html` for static hosting

Each HTML file is fully self-contained: all CSS lives in a `<style>` block in the `<head>`, and there is no shared stylesheet, build step, or templating. Both pages duplicate the same CSS custom properties (color palette, fonts) at the top of their `<style>` blocks — when changing the visual theme, update both files.

## Development

There is no build, lint, or test tooling. To preview changes, open the HTML files directly in a browser or serve the directory with any static file server (e.g. `python3 -m http.server`).

## Conventions

- Dark theme using CSS custom properties: `--bg-black-magic`, `--card-bg`, `--neon-pink`, `--neon-cyan`, `--neon-lime`, `--border-color`, defined in `:root`.
- Booking/contact actions use `tel:`, `sms:`, and `mailto:` links directly (e.g. `sms:8047986550?&body=...`) rather than a contact form; pre-filled SMS bodies are URL-encoded inline in the `href`.
- External booking forms (party booking, job applications) link out to Google Forms.
- Pricing and schedule data (public skate hours, party packages, rental rates, fundraiser rates) is hardcoded directly in the HTML tables/cards — there is no CMS or data file, so updates mean editing the markup in place.
