# NEO Checklist Tracker — Fraser Health

A single-page tool for tracking New Employee Orientation (NEO) completion against WorkSafeBC OHS Regulation §3.23 (Young or New Worker Orientation and Training).

## What it does

- Tracks each employee's NEO due date against a 14-day window from hire date
- Auto-flags status as **Complete**, **Incomplete**, **Due Soon**, **Overdue**, or **Pre-System Complete** (for employees hired before the tracker's launch date)
- Lets managers confirm completion with a date and uploaded file
- Supports revising a completed submission — correcting the date, replacing the file, removing the file, or undoing the submission entirely — with every change written to an audit log and prior files kept in a version history rather than overwritten
- Filterable/searchable employee register (leader, facility, status, cost centre, active/inactive)
- CSV export
- Delegate Access panel for sharing view/edit access
- Built-in Help panel covering statuses, file requirements, and the underlying §3.23 regulation text

## Running it

This is a self-contained static HTML file — no build step, no server required.

**Locally:** open `index.html` directly in a browser.

**On GitHub Pages:**
1. Push this repo to GitHub.
2. In the repo, go to **Settings → Pages**.
3. Under **Build and deployment**, set **Source** to "Deploy from a branch," pick the `main` branch and `/ (root)` folder, then save.
4. GitHub will publish the site at `https://<your-username>.github.io/<repo-name>/` within a minute or two.

## Data storage

All employee data is stored in the browser's `localStorage` — there is no backend or database. This means:

- Data is local to whichever browser/device is used to enter it; it does **not** sync across devices or between users automatically.
- Clearing browser data/cache will erase the saved records.
- The file ships with a set of seed/test employees on first load. If you want to start clean for production use, clear the site's local storage (or open the page in a private/incognito window) before entering real data.

## File

- `index.html` — the entire application (HTML, CSS, and JavaScript in one file)
