# CLAUDE.md

## Project Overview

Personal CV/portfolio website for Andrew Sutherland. A static site with no build tools or frameworks.

## Files

- `index.html` — Main website. Single-page HTML with all CSS inlined. Sections: header, profile summary, key capabilities, experience timeline, technical skills, education. Has scroll animations and responsive design.
- `cv_print.html` — Print-optimized CV layout. A4-sized (`210mm × 297mm`), designed for PDF export via browser print. Shares the same design tokens but uses `pt`-based sizing for print fidelity.
- `andrew_h_sutherland.pdf` — PDF export of the CV (generated from `cv_print.html`).

## Design System

- **Fonts**: Playfair Display (headings), Inter (body) — loaded from Google Fonts
- **Color palette** (CSS custom properties):
  - `--bg: #F7F4EF` (warm cream background)
  - `--navy: #1B3A5C` (accent/headings)
  - `--text: #1C1C1C`, `--text-mid: #444`, `--text-soft: #6B6560`
  - `--border: #D9D3CB`
- **No external CSS or JS dependencies** — everything is inlined

## Working with this project

- All styling is inline in `<style>` tags within each HTML file. There are no external stylesheets.
- The two HTML files share design tokens but are independently styled — changes to one don't automatically propagate to the other.
- `cv_print.html` has `@media print` rules for clean PDF output. Test print changes by using browser Print Preview.
- Both files have `<meta name="robots" content="noindex">` set.
- The PDF is generated manually from `cv_print.html` via browser print-to-PDF — it is not auto-generated.

## Content guidelines

- Keep both HTML files in sync when CV content (experience, skills, education) changes.
- `index.html` is the richer, web-friendly version with animations and more detail.
- `cv_print.html` is the condensed, A4-printable version — be mindful of page length when adding content.
