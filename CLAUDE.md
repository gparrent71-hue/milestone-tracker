# HOU SE Milestone Tracker

## What it is
A single-file web app for tracking TxDOT engineering projects across three districts: Houston, Beaumont, and Bryan.

## File location
`/Users/rp-mac/Documents/Projects/milestone-tracker/index.html`

## GitHub
- Repo: https://github.com/gparrent71-hue/milestone-tracker (private)
- Logged in as: gparrent71-hue
- Default branch: main

## Tech stack
- Vanilla HTML, CSS, JavaScript — no frameworks, no build step
- Data stored in browser `localStorage` under key `txdot-projects`
- Just open `index.html` in a browser to run it

## Data model
Each project has:
- `id`, `name`, `csj` (CSJ number), `district`, `contact`, `notes`
- `milestones` — array of 10 fixed milestones, each with: `planned`, `actual`, `status`, `notes`

Fixed milestones (in order):
1. Traffic Methodology
2. Traffic Forecasts
3. Draft Schematic
4. Traffic Operations Analysis
5. Final Schematic
6. Prepare Public Meeting Material
7. Submit Public Meeting Material
8. Revise per TxDOT Comments
9. Advertise Public Meeting
10. Conduct Public Meeting

## Pushing changes to GitHub
After any change to index.html, run:
```
git add index.html
git commit -m "description of change"
git push
```
Or just ask Claude Code to do it.

## Working across multiple Macs
- The code (index.html) syncs via GitHub — pull on each Mac to get latest
- The data (entered projects) does NOT sync automatically — use Export/Import buttons
- Workflow: finish work on Mac A → Export data → copy JSON to Mac B → Import on Mac B

## Planned improvements
- [x] Export all projects to a JSON file
- [x] Import projects from a JSON file
