# Portfolio — Rifah Nazar

A fast, static portfolio site optimized for engineering-first hiring (built with a 1QLabs-style audience in mind). No build step — just HTML, one CSS file, and a small JS file.

## Structure

```
Portfolio/
├── index.html                    Landing page + featured projects
├── workflow.html                 "My AI Development Workflow" page
├── projects/
│   ├── inbox-copilot.html         ⭐ Hero case study
│   ├── booked-ai.html             Engineering case study (no confidential code)
│   └── llm-observability.html     Case study (real project details)
├── css/style.css                 Shared design system (dark + light themes)
├── js/main.js                    Theme toggle + reveal-on-scroll
├── assets/                       Drop screenshots / resume.pdf here
└── README.md
```

## Run locally

It's static, so just open `index.html` — or serve it:

```bash
python3 -m http.server 8000
# open http://localhost:8000
```

## Deploy (GitHub Pages)

1. Push this folder to a repo (e.g. `rifahnazar.github.io` or any repo).
2. Settings → Pages → deploy from branch → `/root`.
3. Done. (For a custom stack later, this maps cleanly onto Vercel too.)

## What to fill in before sharing

This is a full scaffold with placeholder content in the right structure. Replace:

- **Links** — search for `https://github.com/` and `https://linkedin.com/` and set your real URLs. Resume links use `data-resume` (`href="#"`); point them at `assets/resume.pdf` (or a hosted URL).
- **Screenshots** — every `<figure class="shot">` has a placeholder frame. Drop a real image in `assets/` and replace the `<div class="frame">…</div>` with `<img src="../assets/your-shot.png" alt="…">`.
- **Booked AI contributions** — the "I designed / I implemented / I owned" lines are framing; make them precisely true to your scope.
- **Booked AI "biggest challenge"** — write the real story using the setup → investigation → resolution → takeaway shape provided.
- **Metrics** — anywhere you have real numbers (accuracy, cost saved, latency, eval pass rates), add them; specifics beat adjectives.

## Design notes

- Dark-first, with a light theme via the toggle (persisted in `localStorage`).
- Every case study answers the senior-engineer questions: *What problem? Why this architecture? What tradeoffs? How was it tested? What would I improve?*
- `REPO-README-TEMPLATE.md` is a starting point for the READMEs of your individual project repos.
