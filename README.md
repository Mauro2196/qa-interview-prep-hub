# Interview Prep Hub

A single-page, fully responsive study app for preparing a **Senior QA Automation Engineer**
interview in English — technical, leadership and system design.

Built with **HTML + Tailwind CSS (CDN) + Vanilla JavaScript**. No build step, no dependencies,
no server required: it is one self-contained file.

---

## Run it locally

Open `index.html` in any modern browser. That's it.

```bash
# optional: serve it instead of using file://
npx serve .
```

---

## What's inside

### 1 · Header & overview
- Title, subtitle and a live **progress tracker** (overall completion %).
- Stat tiles for topics prepared, questions mastered and questions needing review.

### 2 · Four interactive modules

| Module | Focus |
| --- | --- |
| **Technical & Automation Architecture** | Selenium / W3C / BiDi, Cypress execution model, WebdriverIO, CI/CD pipelines, parallel execution vs sharding, flaky-test management, reporting frameworks, locator strategy, cross-browser & visual regression — plus deep **Playwright** coverage: execution model, locators & web-first assertions, `playwright.config` projects & sharding, tracing & UI mode, network interception, and fixtures |
| **Coding & Algorithms** | Log/string parsing, grouping & dedup, deep equality, a **custom test runner**, retry with exponential backoff, concurrency limiter, debounce + fake timers, a test-tagging DSL, and **Playwright-style helpers** (a web-first polling assertion, a storage-state session helper) — each with **JavaScript/TypeScript ⇄ Python** toggles, syntax highlighting and copy-to-clipboard |
| **Behavioral & Leadership** | 12 STAR prompts: production bugs, pushing back on deadlines, mentoring juniors, defining a test strategy from scratch, rebuilding trust in a flaky suite, disagree-and-commit, a **Selenium/Cypress → Playwright migration**, and **cutting CI feedback below 10 minutes** |
| **Mock Interview Simulator** | 25 flashcards with model answers in professional technical English (including fixtures, shared auth, `page.route` traps and CI-vs-local diagnosis), reveal-on-demand, **Mastered / Needs Review** grading, filters, and a **Generate Random Mock Question** spotlight |

**Totals:** 37 checkable topics across the first three modules, 12 STAR prompts, 13 dual-language
code snippets and 25 mock questions.

### 3 · Key features
- Check/uncheck topics → progress bar and per-module badges update instantly.
- Everything persists in `localStorage` (`senior-qa-prep-hub.v1`) — checkboxes, grades and the active module survive a reload.
- Live topic search, expand/collapse all, bulk check/clear.
- Press **`R`** anywhere on the page to generate a surprise mock question.
- Dark developer-dashboard UI, animated gradient-mesh background, `prefers-reduced-motion` respected.

---

## Project structure

```
.
├── index.html      # the entire application (markup, styles, data, logic)
├── prueba.html     # earlier, simpler draft of the app
├── README.md
└── .gitignore
```

---

## Deploy

This repo is published with **GitHub Pages**:

1. Push to `main`.
2. Repository → **Settings → Pages → Source: Deploy from a branch → `main` / root**.
3. The site appears at `https://<user>.github.io/qa-interview-prep-hub/`.

Because Tailwind and the fonts load from a CDN, the page needs internet access once; everything
else (including saved progress) works offline afterwards.
