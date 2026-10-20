# shaidan-portfolio

Portfolio and online CV for **Shaidan Shaari Bin Abd Rasep** — Infrastructure &
Security Engineer turned AI Systems Builder. Founder, NusaByte IT Solutions.

Live: https://nusabyte-my.github.io/shaidan-portfolio/

## Contents

| File | Purpose |
|---|---|
| `index.html` | The site. One file, no build step, no framework. |
| `cv.html` | Print-ready A4 CV. Open → Ctrl+P → Save as PDF. |
| `shaidan-shaari-cv.pdf` | Earlier PDF export; use `cv.html` for the current print-ready CV. |
| `resume.json` | Single source of truth — every section renders from this. |
| `dns/README.md` | A records for the shaidan.nusabyte.my custom domain. |

## Editing

All content lives in `resume.json`. The page renders it with template literals —
edit the JSON, save, reload. No `npm install`, no compile.

Deploy: push to `main`, GitHub Pages serves from branch (legacy build, no
Actions — the account's runner is billing-locked). `.nojekyll` is present so
`resume.json` is served verbatim rather than parsed by Jekyll.

## Interactive features

- **Console** — type `help`. Reads the same `resume.json` the page renders, so
  it cannot invent an answer. Commands: `whoami`, `projects [domain]`, `stack`,
  `experience`, `systems`, `proof`, `certifications`, `contact`, `cv`, `clear`.
  Tab completes, arrow keys walk history, `/` focuses input, Ctrl+L clears.
- **Project grid** — filter chips by domain (AI / Commerce / Security /
  Platform / Product / Client). Cyan-bordered cards are the four flagships.
- **Proof bars** — animated before/after for the SEO engine results.
- **Count-up stats** — animate when scrolled into view.
- **Scrollspy** — nav highlights the active section.

All motion respects `prefers-reduced-motion`.

## Design system

Stealth-Dark Tactical, matching NusaByte/JEBAT:

- ink #030303 · surface #0a0b0e · border #1a1d24
- neon cyan #22d3ee · purple #a855f7 · amber #f59e0b · green #34d399
- Space Grotesk (display) · Inter (body) · JetBrains Mono (code)

## Accessibility & performance

- Semantic headings, aria-live on console output, labelled input
- One external request (fonts), no images, no tracking, no analytics
- ~47 KB total, no JavaScript dependencies
