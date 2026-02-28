# OpenRisk Academy 🎯
### The World's Free Financial Risk Education Platform

> *"A kid in Mumbai. A banker in Nairobi. A quant in Jakarta. Same knowledge. Zero cost."*

[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![GitHub Pages](https://img.shields.io/badge/Deploy-GitHub%20Pages-blue)](https://pages.github.com)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)
[![Questions](https://img.shields.io/badge/Questions-5000%2B-orange)](curriculum/)

---

## 📋 Table of Contents

1. [Vision](#vision)
2. [Certifications Covered](#certifications)
3. [Repo Architecture](#architecture)
4. [Content Format Spec](#content-format)
5. [Tech Stack](#tech-stack)
6. [Build & Deploy](#build-deploy)
7. [How to Contribute](#contributing)
8. [Roadmap](#roadmap)
9. [File Naming Conventions](#conventions)

---

## Vision <a name="vision"></a>

Financial risk education is locked behind:
- $1,000+ exam registration fees
- $500 textbooks that go out of date
- $3,000+ prep course paywalls

This platform tears all of that down. Every concept, every question type, every case study — free, open-source, community-maintained, forever.

**Stack philosophy: static-first, offline-capable, zero server costs.**  
Runs entirely on GitHub Pages. No database. No cloud bill. No single point of failure.

---

## Certifications Covered <a name="certifications"></a>

### Tier 1 — Big Guns
| Code | Full Name | Status | Body |
|------|-----------|--------|------|
| FRM | Financial Risk Manager (Part I & II) | 🟢 **ACTIVE** | GARP |
| CFA | Chartered Financial Analyst (L1, L2, L3) | 🟡 In Progress | CFA Institute |
| PRM | Professional Risk Manager | 🔵 Planned | PRMIA |

### Tier 2 — Specialized Warriors
| Code | Full Name | Status | Body |
|------|-----------|--------|------|
| CAIA | Chartered Alternative Investment Analyst | 🔵 Planned | CAIA Association |
| CIPM | Investment Performance Measurement | 🔵 Planned | CFA Institute |
| ERP | Energy Risk Professional | 🔵 Planned | GARP |

### Tier 3 — Tech-Enabled Finance
| Code | Full Name | Status | Body |
|------|-----------|--------|------|
| CQF | Certificate in Quantitative Finance | 🔵 Planned | Fitch Learning |
| CFP | Certified Financial Planner | 🔵 Planned | CFP Board |
| CERA | Chartered Enterprise Risk Actuary | 🔵 Planned | SOA/CAS |

### Tier 4 — Regulatory & Compliance
| Code | Full Name | Status | Body |
|------|-----------|--------|------|
| CRCM | Certified Regulatory Compliance Manager | 🔵 Planned | ABA |
| CAMS | Certified Anti-Money Laundering Specialist | 🔵 Planned | ACAMS |
| CBCA | Commercial Banking & Credit Analyst | 🔵 Planned | CFI |

---

## Repo Architecture <a name="architecture"></a>

```
openrisk-academy/
│
├── 📁 curriculum/                    # All learning content (Markdown)
│   ├── 📁 frm/
│   │   ├── README.md                # Cert overview, exam structure, tips
│   │   ├── 📁 part-i/
│   │   │   ├── 📁 01-foundations-of-risk/
│   │   │   │   ├── README.md        # Module overview
│   │   │   │   ├── 01-var-and-expected-shortfall.md
│   │   │   │   ├── 02-normal-distribution-in-risk.md
│   │   │   │   └── formulas.md     # Quick-reference formula sheet
│   │   │   ├── 📁 02-quantitative-analysis/
│   │   │   ├── 📁 03-financial-markets/
│   │   │   ├── 📁 04-valuation-and-risk-models/
│   │   │   └── index.json          # Module metadata for nav
│   │   └── 📁 part-ii/
│   │       ├── 📁 01-market-risk-measurement/
│   │       ├── 📁 02-credit-risk/
│   │       ├── 📁 03-operational-risk/
│   │       ├── 📁 04-liquidity-funding-risk/
│   │       └── 📁 05-investment-management/
│   ├── 📁 cfa/
│   │   ├── 📁 level-1/
│   │   │   ├── 📁 01-ethics-professional-standards/
│   │   │   ├── 📁 02-quantitative-methods/
│   │   │   ├── 📁 03-economics/
│   │   │   ├── 📁 04-financial-statement-analysis/
│   │   │   ├── 📁 05-corporate-issuers/
│   │   │   ├── 📁 06-equity-investments/
│   │   │   ├── 📁 07-fixed-income/
│   │   │   ├── 📁 08-derivatives/
│   │   │   ├── 📁 09-alternative-investments/
│   │   │   └── 📁 10-portfolio-management/
│   │   ├── 📁 level-2/
│   │   └── 📁 level-3/
│   ├── 📁 prm/
│   ├── 📁 caia/
│   ├── 📁 cqf/
│   ├── 📁 cfp/
│   ├── 📁 cera/
│   ├── 📁 cipm/
│   ├── 📁 erp/
│   ├── 📁 crcm/
│   ├── 📁 cams/
│   └── 📁 cbca/
│
├── 📁 question-bank/                 # The exam question arsenal
│   ├── 📁 frm/
│   │   ├── 📁 past-exams/
│   │   │   ├── 2023-nov.json
│   │   │   ├── 2023-may.json
│   │   │   └── ...
│   │   ├── 📁 practice-sets/
│   │   │   ├── market-risk-easy.json
│   │   │   ├── market-risk-hard.json
│   │   │   └── ...
│   │   └── 📁 by-topic/
│   │       ├── var-questions.json
│   │       └── credit-risk-questions.json
│   ├── 📁 cfa/
│   └── 📁 ...
│
├── 📁 case-studies/                  # Historical financial disasters
│   ├── ltcm-1998.md
│   ├── gfc-2008.md
│   ├── barings-bank-1995.md
│   ├── enron-2001.md
│   ├── archegos-2021.md
│   ├── ftx-2022.md
│   ├── lehman-brothers-2008.md
│   ├── orange-county-1994.md
│   ├── knight-capital-2012.md
│   ├── mf-global-2011.md
│   ├── svb-2023.md
│   └── 📁 interactive/               # Decision-tree simulations
│       ├── ltcm-simulation.json
│       └── gfc-2008-simulation.json
│
├── 📁 tools/                         # Browser-based modeling tools
│   ├── var-calculator/
│   │   ├── index.html
│   │   └── var.js
│   ├── stress-test-engine/
│   │   ├── index.html
│   │   └── stress.js
│   ├── monte-carlo-simulator/
│   │   ├── index.html
│   │   └── montecarlo.js
│   ├── yield-curve-builder/
│   ├── credit-model-sandbox/
│   └── portfolio-optimizer/
│
├── 📁 notebooks/                     # Pyodide Python notebooks
│   ├── var-from-scratch.py
│   ├── black-scholes-model.py
│   ├── credit-risk-montecarlo.py
│   └── yield-curve-models.py
│
├── 📁 _layouts/                      # Jekyll/Eleventy templates
│   ├── default.html
│   ├── lesson.html
│   ├── question.html
│   └── case-study.html
│
├── 📁 _includes/                     # Reusable template components
│   ├── quiz-engine.html
│   ├── progress-tracker.html
│   ├── formula-display.html
│   └── case-simulation.html
│
├── 📁 assets/
│   ├── 📁 css/
│   ├── 📁 js/
│   │   ├── quiz.js                   # Adaptive quiz engine
│   │   ├── progress.js               # LocalStorage progress tracking
│   │   ├── spaced-repetition.js      # SM-2 algorithm
│   │   └── case-simulator.js         # Interactive case study engine
│   └── 📁 img/
│
├── 📁 .github/
│   ├── 📁 workflows/
│   │   ├── validate-questions.yml    # CI: validate JSON question format
│   │   ├── check-links.yml           # CI: dead link checker
│   │   └── deploy.yml                # CD: auto-deploy to GitHub Pages
│   ├── 📁 ISSUE_TEMPLATE/
│   │   ├── question-error.md
│   │   ├── new-content.md
│   │   └── bug-report.md
│   └── PULL_REQUEST_TEMPLATE.md
│
├── _config.yml                       # Jekyll config
├── sw.js                             # Service worker (offline PWA)
├── manifest.json                     # PWA manifest
├── CONTRIBUTING.md                   # How to contribute
├── CODE_OF_CONDUCT.md
├── LICENSE                           # MIT
└── README.md                         # This file
```

---

## Content Format Spec <a name="content-format"></a>

### Lesson Markdown Format

Every lesson file follows this frontmatter schema:

```markdown
---
title: "Value at Risk (VaR) — Core Concepts"
cert: frm
part: 1
module: 4
topic: market-risk
difficulty: intermediate
exam_weight: high            # low / medium / high
prerequisites:
  - normal-distribution
  - standard-deviation
formulas:
  - name: "Historical VaR"
    latex: "VaR_\\alpha = -\\text{Quantile}_\\alpha(R)"
tags: [var, market-risk, quantitative, portfolio]
last_updated: 2024-11-01
contributors: [github_username]
---

## Introduction
[Content here]

## Key Concepts
[Content here]

## Worked Example
[Content here]

## Common Exam Traps
[Content here]

## Practice Questions
→ See [question bank](/question-bank/frm/by-topic/var-questions)
```

### Question JSON Format

```json
{
  "id": "FRM-MR-2023-Q047",
  "cert": "frm",
  "part": 1,
  "topic": "market-risk",
  "subtopic": "var",
  "year": 2023,
  "session": "november",
  "difficulty": "hard",
  "stem": "A portfolio has a daily VaR of $1M at the 95% confidence level...",
  "options": {
    "A": "...",
    "B": "...",
    "C": "...",
    "D": "..."
  },
  "answer": "B",
  "explanation": "Full worked solution here...",
  "formula_used": "VaR = z * sigma * sqrt(T)",
  "traps": ["Don't forget to scale by sqrt(T)", "95% CI uses z=1.645, not 1.96"],
  "related_questions": ["FRM-MR-2022-Q031", "FRM-MR-2021-Q055"],
  "source": "GARP FRM Part I November 2023",
  "contributor": "github_username",
  "verified": true
}
```

### Case Study Format

```markdown
---
title: "Long-Term Capital Management (1994–1998)"
type: case-study
category: [market-risk, liquidity-risk, model-risk, leverage]
loss_amount: "$4.6 billion"
year: 1998
interactive: true
simulation_file: ltcm-simulation.json
certs_relevant: [frm, prm, cfa]
difficulty: advanced
---

## Background
[Company overview]

## The Strategy
[What they were doing]

## The Trigger
[What set off the collapse]

## The Collapse — Timeline
[Chronological breakdown]

## The Rescue
[Fed-orchestrated bailout details]

## Risk Failures — Annotated
[Each failure mapped to a risk concept]

## Exam Connections
[Which FRM/CFA topics this illustrates]

## Decision Points
[For interactive simulation JSON]

## Further Reading
[Free sources only]
```

---

## Tech Stack <a name="tech-stack"></a>

### Hosting & Deployment
- **GitHub Pages** — Free, global CDN, custom domain support
- **GitHub Actions** — CI/CD pipelines (validate, build, deploy)
- **Cloudflare** (optional) — Additional CDN layer for performance

### Static Site Generation
```yaml
# _config.yml (Jekyll)
title: OpenRisk Academy
baseurl: ""
url: "https://openrisk.academy"
markdown: kramdown
highlighter: rouge
plugins:
  - jekyll-feed
  - jekyll-sitemap
  - jekyll-seo-tag
```
Or use **Eleventy (11ty)** — faster builds, more flexible templating, better for large content sites.

### Interactive Layer (Browser-Side)
```
Vanilla JS         → Quiz engine, progress tracking, navigation
Pyodide            → Full Python runtime in browser (numpy, scipy, pandas)
Chart.js / D3.js   → Risk visualization (VaR charts, yield curves, etc.)
MathJax 3          → LaTeX formula rendering
Marked.js          → Client-side Markdown rendering for dynamic content
```

### Offline & PWA
```javascript
// sw.js — Service Worker Strategy
// Cache-first for content, network-first for questions
const CACHE_VERSION = 'v1.2.0';
const STATIC_ASSETS = ['/curriculum/', '/tools/', '/question-bank/'];
```

### CI/CD — GitHub Actions
```yaml
# .github/workflows/validate-questions.yml
name: Validate Question Format
on: [pull_request]
jobs:
  validate:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - name: Validate JSON schemas
        run: python scripts/validate_questions.py
      - name: Check for required fields
        run: python scripts/check_required_fields.py
```

---

## Build & Deploy <a name="build-deploy"></a>

### Local Development
```bash
# Clone the repo
git clone https://github.com/YOUR_USERNAME/openrisk-academy.git
cd openrisk-academy

# Install Jekyll
gem install bundler jekyll
bundle install

# Serve locally
bundle exec jekyll serve --livereload
# → http://localhost:4000

# OR with Eleventy
npm install
npm run dev
```

### Deploy to GitHub Pages
```bash
# Enable GitHub Pages in repo settings → Pages → Source: GitHub Actions
# Push to main branch → auto-deploys via .github/workflows/deploy.yml
git push origin main
```

---

## How to Contribute <a name="contributing"></a>

### Types of Contributions We Love
1. **New questions** — Add questions to `question-bank/` using the JSON schema above
2. **Curriculum content** — Write or improve lesson Markdown files
3. **Case studies** — Add new historical cases or improve existing ones
4. **Tool improvements** — Enhance the JS modeling tools
5. **Translations** — Translate content to other languages
6. **Bug fixes** — Fix errors in solutions, formulas, or explanations

### Contribution Workflow
```bash
# 1. Fork the repo
# 2. Create a feature branch
git checkout -b add/frm-credit-risk-questions

# 3. Add your content following the format specs above

# 4. Run local validation
python scripts/validate_questions.py

# 5. Commit with a descriptive message
git commit -m "add: 25 FRM credit risk questions (2019-2023)"

# 6. Push and open a PR
git push origin add/frm-credit-risk-questions
```

### PR Review Checklist
- [ ] Questions use correct JSON schema
- [ ] Answer explanation is thorough
- [ ] Sources cited (where applicable)
- [ ] No copyright violations (original content only)
- [ ] Difficulty level is accurate
- [ ] CI checks pass

---

## Roadmap <a name="roadmap"></a>

| Phase | Timeline | Deliverable |
|-------|----------|-------------|
| 1 — Launch | Month 1–2 | FRM Part I curriculum + 300 questions + 5 case studies |
| 2 — FRM Complete | Month 3–5 | FRM Part II + adaptive quiz engine + PWA |
| 3 — CFA L1 | Month 6–8 | CFA Level 1 + interactive case simulator |
| 4 — Quant Track | Month 9–12 | CFA L2/L3 + CQF + Python notebooks via Pyodide |
| 5 — Full Arsenal | Month 13–24 | All 12 certifications + 5,000+ questions + multilingual |

---

## File Naming Conventions <a name="conventions"></a>

```
Lessons:         kebab-case.md              → var-and-expected-shortfall.md
Questions:       CERT-TOPIC-YEAR-Q###.json  → FRM-MR-2023-Q047
Case studies:    company-name-year.md       → ltcm-1998.md
Tools:           tool-name/index.html       → var-calculator/index.html
Notebooks:       concept-name.py            → black-scholes-model.py
```

---

## License

MIT License. Free as in freedom. Free as in beer.

Copy it. Fork it. Deploy it. Share it. Just don't paywall it.

---

*Built by the community. For the community. For everyone who was ever locked out.*
