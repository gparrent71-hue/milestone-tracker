# HOU SE Milestone Tracker

## What it is
A single-file web app for tracking TxDOT engineering projects across three districts: Houston, Beaumont, and Bryan.

## File location
`/Users/rp-mac/Documents/Projects/milestone-tracker/milestone-tracker.html`
Note: Documents folder is synced to iCloud Drive automatically — visible in Finder under iCloud Drive → Documents → Projects

## GitHub
- Repo: https://github.com/gparrent71-hue/milestone-tracker (public)
- Live URL: https://gparrent71-hue.github.io/milestone-tracker/milestone-tracker.html
- Logged in as: gparrent71-hue
- Default branch: main

## Tech stack
- Vanilla HTML, CSS, JavaScript — no frameworks, no build step
- Data stored in **Firebase Firestore** (cloud database) — shared in real time across all users
- Firebase project: `milestone-tracker-955f4`
- Just open `milestone-tracker.html` in a browser to run it

## Data model
Each project has:
- `id`, `name`, `csj` (CSJ number), `district`, `contact`, `notes`
- `milestones` — array of milestones, each with: `planned`, `actual`, `status`, `notes`

Milestones are managed in Firebase under `settings/milestones` and can be added, removed, and reordered directly in the app via the **Manage Milestones** button — no code change needed.

Default milestones:
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
After any change to milestone-tracker.html, run:
```
git add milestone-tracker.html
git commit -m "description of change"
git push
```
Or just ask Claude Code to do it.

## Firebase / Data
- Data lives in Firebase Firestore — all users see the same projects in real time
- No export/import needed to sync between computers or team members
- Export button available as a backup in case of accidental data loss (Import button removed)
- Firestore security rules set: `projects` and `settings` collections accessible, project writes are validated
- Milestone list stored in Firebase under `settings/milestones` — editable in the app

## Working across computers
- The code syncs via GitHub — run `git pull` to get the latest version on any machine
- Data syncs automatically via Firebase — no manual steps needed

## Toolbar buttons
- **+ Add Project** — opens form to add a new project
- **Expand All / Collapse All** — show or hide milestone tables
- **Export** — downloads all projects as a JSON backup file
- **Manage Milestones** — add, remove, reorder milestones via drag and drop
