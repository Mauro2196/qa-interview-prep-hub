# Interview Prep Hub

A single-page, fully responsive study app for preparing a **Senior QA Automation Engineer**
interview in English — technical, leadership, system design and data quality.

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

### 2 · Five interactive modules

| Module | Focus |
| --- | --- |
| **Technical & Automation Architecture** | Selenium / W3C / BiDi, Cypress execution model, WebdriverIO, CI/CD pipelines, parallel execution vs sharding, flaky-test management, reporting frameworks, locator strategy, cross-browser & visual regression — plus deep **Playwright** coverage: execution model, locators & web-first assertions, `playwright.config` projects & sharding, tracing & UI mode, network interception, and fixtures |
| **Coding & Algorithms** | Log/string parsing, grouping & dedup, deep equality, a **custom test runner**, retry with exponential backoff, concurrency limiter, debounce + fake timers, a test-tagging DSL, **next permutation** (the O(n) Palantir classic) and **Playwright-style helpers** (a web-first polling assertion, a storage-state session helper) — each with **JavaScript/TypeScript ⇄ Python** toggles, syntax highlighting and copy-to-clipboard |
| **Behavioral & Leadership** | 12 STAR prompts: production bugs, pushing back on deadlines, mentoring juniors, defining a test strategy from scratch, rebuilding trust in a flaky suite, disagree-and-commit, a **Selenium/Cypress → Playwright migration**, and **cutting CI feedback below 10 minutes** |
| **Mock Interview Simulator** | 31 flashcards with model answers in professional technical English (Playwright fixtures, shared auth, `page.route` traps, CI-vs-local diagnosis, plus ETL, data quality dimensions, masking, reconciliation, schema migrations and idempotent loads), reveal-on-demand, **Mastered / Needs Review** grading, filters, and a **Generate Random Mock Question** spotlight |
| **Data & Database Testing** | 13 topics in 5 groups: test data management & factories, PII masking and compliant environments, synthetic/property-based data, SQL-level assertions, schema migrations & backward compatibility, API-payload vs persisted-row validation, ETL transformation testing, the five data quality dimensions, reconciliation & freshness, streaming/CDC correctness, and data volume & query budgets — with **SQL ⇄ Python ⇄ TypeScript** snippets — plus 2 data-leadership STAR prompts |

**Totals:** 51 checkable topics, 14 STAR prompts, 20 code snippets (JavaScript/TypeScript, Python
and SQL) and 31 mock questions.

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
