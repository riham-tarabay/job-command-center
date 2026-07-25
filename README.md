# Job Search Command Center

An executive-style dashboard to run a job search like a pipeline — built as **one single `index.html` file** with zero dependencies, zero build step, and zero backend.

**Live demo:** https://riham-tarabay.github.io/command-center/?demo=1

## Features

- **Application pipeline tracker** — company, role, posting link, status, date applied, follow-up date, notes; inline status changes, add/edit dialog, search and status filter
- **Analytics** — applications-per-week bar chart (last 8 weeks), response rate, active pipeline count, and an Applied → Screening → Interview → Offer status funnel, all rendered with hand-rolled inline SVG (no chart libraries)
- **Follow-up reminders** — surfaces anything due today or overdue, with day counts
- **Privacy by design** — all data lives in the browser's `localStorage`; nothing is ever uploaded
- **CSV export** — one click, Excel-safe (UTF-8 BOM, quoted fields, Arabic-friendly)
- **Bilingual** — full English/Arabic UI with proper RTL layout flip
- **Dark / light themes**, responsive down to 390px, keyboard accessible (skip link, focus rings, ARIA labels)

## Usage

Open `index.html` in any modern browser — that's the whole install.

| URL parameter | Effect |
|---|---|
| `?demo=1` | Loads sample data (in memory only — does not overwrite your saved data) |
| `?lang=ar` / `?lang=en` | Force language |
| `?theme=dark` / `?theme=light` | Force theme |

On the empty state you can also click **Load sample data** to seed the dashboard.

## Tech notes

- Single-file vanilla HTML/CSS/JS — no frameworks, no build, no network calls
- Charts drawn as inline SVG generated from the data at render time
- Theming via CSS custom properties (`data-theme` attribute); RTL via `dir` attribute + logical CSS properties
- State persisted under the `rt-jobs`, `rt-lang`, and `rt-theme` localStorage keys

## Author

**Riham Tarabay** — AI & Data Solutions

- Portfolio: https://riham-tarabay.github.io
- GitHub: https://github.com/riham-tarabay
- LinkedIn: https://www.linkedin.com/in/rihamtarabay/
- Email: rihamtarabay.rt@gmail.com
