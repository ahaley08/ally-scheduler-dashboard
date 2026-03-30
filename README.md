# Ally Psychiatry — Scheduler Dashboard

Internal scheduling team productivity dashboard for Ally Psychiatry.

## Features

- **Team Overview** — MTD scorecard with tier-based color coding for all 9 schedulers
- **Daily Snapshot** — Search any date, see every scheduler's results
- **Week-to-Date** — Any week's team and individual metrics
- **Month-to-Date** — Full month view with month-over-month trend table
- **Year-to-Date** — YTD leaderboard and appts trend (Jan → Feb → Mar)
- **Scheduler Profile** — Individual drill-down with manager notes
- **Log Entry** — Schedulers enter daily data; auto-updates all views

## Data

- All March 2026 data (180 entries) is pre-seeded from the Daily Tracker xlsx
- New entries persist in the browser's localStorage on each device
- Imported data is protected from accidental overwrite

## Deployment

Hosted as a static site on Render. No server, no database, no build step required.

## Tech Stack

- Pure HTML / CSS / JavaScript — single file, no dependencies
- Data stored in browser localStorage
- Logos and assets embedded as base64

## Access

Deploy URL is set in Render. Share the URL with your scheduling team for log entry, and use it yourself for the manager views.
