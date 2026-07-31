# Fraser Health NEO Tracker

A lightweight, browser-based tool for tracking New Employee Orientation (NEO) checklist completion in compliance with WorkSafeBC OHS Regulation §3.23.

> **Disclaimer:** This is an unofficial open-source prototype and is not an official Fraser Health Authority product. It is provided as a reference implementation for demonstration and educational purposes.

## Overview

The NEO Tracker replaces spreadsheet-based tracking with a centralized register that:

- Automatically calculates 14-day NEO completion deadlines from each employee's hire date
- Flags overdue, due-soon, and incomplete records with clear visual cues
- Requires an uploaded checklist file at the point of confirmation, creating an audit-defensible trail
- Provides tamper-evident revision controls with full audit logging

## Live Demo

Open `index.html` in any modern browser. That's it. No build step, no server, no dependencies. The tool runs entirely client-side and uses browser `localStorage` to persist data.

## Features

- **Live dashboard** — three stat cards (Total Employees, NEO Complete %, Action Required)
- **Employee register** — sortable table with facility, status, and cost centre filters
- **Confirm Completion** — required file upload with drag-and-drop
- **Revise Submission** — audit-tracked revisions with mandatory reason
- **File Attachment column** — clickable links to uploaded checklists
- **CSV export** — one-click compliance reporting
- **In-app Help** — comprehensive reference including WorkSafeBC §3.23 regulation

## Tech Stack

- Plain HTML, CSS, and JavaScript
- No frameworks, no build step
- System fonts (no external dependencies)
- `localStorage` for persistence

## Configuration

Open `index.html` and find these constants near the top of the `<script>` block:

- `DAYS = 14` — NEO completion window from hire date
- `LAUNCH_DATE = '2026-06-01'` — cutoff date for pre-system hires

Modify to match your organization's policy.

## Regulatory Context

Built around **WorkSafeBC OHS Regulation Section 3.23** — Young or New Worker Orientation and Training. See the in-app Help for the full list of required orientation topics.

## License

MIT License — see `LICENSE` for details.

## Contributing

This is an open prototype. Contributions welcome via GitHub issues and pull requests.

---

*Disclaimer: This is an unofficial open-source prototype and is not an official Fraser Health Authority product. WorkSafeBC and Fraser Health Authority are referenced for regulatory context only and have no affiliation with this project.*
