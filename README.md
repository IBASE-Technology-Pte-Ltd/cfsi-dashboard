# CFSI Dashboard

**Condo Financial Stress Index (CFSI) Dashboard** — an AI-powered financial intelligence tool for condominium estate management in Singapore.

Built by **Qornerstone** / **IBASE Technology Pte Ltd**.

---

## What This Project Does

The CFSI Dashboard helps condominium management boards and property managers assess the **financial health** of their residential estate. It calculates a **Condo Financial Stress Index (CFSI)** score (0–100) based on key financial and asset inputs, then surfaces actionable insights and warnings.

### Key Capabilities

- **CFSI Score Calculation** — A weighted risk formula combining reserve funding, arrears, asset age, maintenance history, and special levies.
- **Visual Dashboard** — Interactive gauge, health bars, and signal cards that make risk levels immediately understandable.
- **AI Signals & Recommendations** — Severity-rated insights (Reserve Risk, Collections Risk, Asset Age Risk, Execution History Risk) with numbered action cards.
- **Estate Comparison** — Two pre-loaded sample estates (Example A and Example B) plus a live-input mode for custom data.
- **Print / Export** — One-click browser print to share the dashboard as a PDF report.

---

## CFSI Risk Formula

The score is calculated as a weighted sum across six risk dimensions:

| Dimension | Weight | Driver |
|---|---|---|
| Reserve Risk | 35% | Sinking fund vs 10-year capex projection |
| Arrears Risk | 20% | Owner payment delinquency rate |
| Lift Age Risk | 15% | Lift age (>25 years = 100% risk) |
| Repainting Risk | 10% | Years since last repainting (>10 years = 100% risk) |
| Special Levy Risk | 10% | Number of special levies in the past 5 years |
| Failed Work Risk | 10% | Number of postponed major works |

**Risk Classification:**

| CFSI Score | Rating | Meaning |
|---|---|---|
| ≥ 65 | 🔴 Stressed | High risk of special levy |
| 40 – 64 | 🟡 Watchlist | Moderate funding stress |
| < 40 | 🟢 Stable | Low financial risk |

---

## Technology Stack

This is a **zero-dependency, single-file web application**:

- **HTML5 / CSS3 / Vanilla JavaScript** — all code lives in `index.html`
- No build tools, no npm packages, no frameworks
- Deployable to any static web host (GitHub Pages, Netlify, Vercel, S3, etc.)

---

## Getting Started

### Open Locally

```bash
# Clone the repository
git clone https://github.com/IBASE-Technology-Pte-Ltd/cfsi-dashboard.git
cd cfsi-dashboard

# Open in your browser
open index.html          # macOS
start index.html         # Windows
xdg-open index.html      # Linux

# Or serve via a simple HTTP server
python -m http.server 8000
# then visit http://localhost:8000
```

### How to Use

1. **Browse examples** — Click **Example A** or **Example B** to load pre-populated sample estates.
2. **Enter your data** — Click the **Settings** tab and fill in your estate's financial and asset details.
3. **Calculate** — Click the **Calculate** button to run the CFSI assessment.
4. **Review results** — The Dashboard tab updates with the CFSI score, risk rating, AI signals, and recommended actions.
5. **Export** — Click the **Export / Print** button to open the browser print dialog and save the dashboard as a PDF.

---

## Project Structure

```
cfsi-dashboard/
└── index.html    # Entire application — HTML, CSS, and JavaScript in one file
```

---

## License

© IBASE Technology Pte Ltd. All rights reserved.