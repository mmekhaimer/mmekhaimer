# GitHub Portfolio Strategy — Mohamed Mekhaimer

Supporting plan behind the `README.md` profile: repository structure, naming, a 20-repo backlog, a 12-month rollout, and branding assets. Built from your CV (empirical corporate finance/governance/microstructure research, Purdue MSBA, and applied ML/NLP work referenced in our prior sessions — the CEO-characteristics pipelines, Fog Index/conference-call NLP, overconfidence embeddings, Dash and Gradio teaching apps).

---

## 1. Repository Organization

Use a small number of **topic-based repos**, not one repo per script — recruiters and collaborators judge depth, not repo count. Organize conceptually as:

```
Research/
├── ceo-overconfidence-nlp        # transformer embeddings, anchor-phrase scoring
├── internal-governance-innovation # subordinate-executive / governance empirics
├── disclosure-political-risk      # narrative disclosure & obfuscation NLP
└── liquidity-microstructure       # commonality-in-liquidity replications

Apps/
├── ceo-crash-risk-dashboard
├── ibm-workforce-segmentation
├── airbnb-price-mlr-app
└── corporate-finance-calculator

Teaching/
├── mba-business-analytics
├── financial-accounting-seminar   # syllabus, labs, replication assignments
└── data-viz-storytelling-mba

Pipelines/
├── wrds-controls-pipeline         # Stata/SAS → Stata controls construction
└── conference-call-fog-index

NLP/
└── earnings-call-embeddings

Datasets/  (documentation + access instructions only — never raw WRDS data)
Python-Libraries/  (small reusable packages, e.g. a WRDS-query helper)
```

**Rules of thumb:**
- Never commit raw WRDS/Compustat/CRSP/ExecuComp data (licensing) — commit pull scripts, variable dictionaries, and synthetic/sample data instead.
- Each research repo gets a `README.md` stating the research question, data sources (by name, not raw files), method, and a link to the working paper if public.
- Keep teaching and research repos separate — different audiences (students vs. journal editors/collaborators) want different things up front.

---

## 2. Repository Naming Convention

Lowercase, hyphenated, descriptive of *method + topic* rather than course code or internal filename:

| Good | Avoid |
|---|---|
| `ceo-overconfidence-nlp` | `CC_Variables_pipeline` |
| `internal-governance-innovation` | `Do_Files_v3` |
| `disclosure-political-risk` | `project2` |
| `earnings-call-embeddings` | `nlp_stuff` |
| `wrds-controls-pipeline` | `build_controls_Do` |
| `crash-risk-ncskew-replication` | `ncskew` |
| `financial-accounting-seminar` | `syllabus2026` |

---

## 3. Suggested Repositories (20)

| # | Repository | Objective | Audience | Tech | Complexity | Popularity potential |
|---|---|---|---|---|---|---|
| 1 | `ceo-overconfidence-nlp` | Transformer-embedding overconfidence scoring on earnings-call transcripts | Academics, financial NLP researchers | Python, HuggingFace, Stata export | High | Medium–High |
| 2 | `wrds-controls-pipeline` | Reusable Stata pipeline for firm-quarter controls from Compustat/CRSP (CIZ format) | Empirical finance/accounting PhDs | Stata | Medium | Medium |
| 3 | `crash-risk-ncskew-replication` | Clean, documented NCSKEW/DUVOL crash-risk construction | PhD students, replicators | Stata/Python | Medium | High (classic replication demand) |
| 4 | `discretionary-accruals-toolkit` | Modified-Jones/Dechow accrual-quality estimators | Accounting researchers, students | Stata/Python | Medium | High |
| 5 | `internal-governance-innovation` | Replication companion to *JBF* 2023 paper | Governance researchers | Stata | Low–Medium | Medium |
| 6 | `disclosure-political-risk` | NLP pipeline for political-risk/obfuscation measures in filings | Accounting/disclosure researchers | Python (spaCy/transformers) | High | Medium–High |
| 7 | `liquidity-commonality-toolkit` | Commonality-in-liquidity estimation across markets | Market microstructure researchers | Stata/Python | Medium | Low–Medium |
| 8 | `ceo-crash-risk-dashboard` | Interactive dashboard linking CEO characteristics to crash risk | Recruiters, seminar audiences | Python, Dash/Plotly | Medium | Medium |
| 9 | `sec-edgar-lab-toolkit` | Free-data (EDGAR/yfinance) labs for students without WRDS | PhD/MBA students, instructors | Python | Low–Medium | High (broad utility) |
| 10 | `financial-accounting-seminar` | Full graduate seminar: syllabus, labs, replication assignments | Instructors, PhD students | Markdown, Python, Stata | Medium | Medium–High |
| 11 | `ibm-workforce-segmentation` | K-Means clustering on IBM HR analytics case | MBA students, analytics recruiters | Python, Dash, scikit-learn | Low | Medium |
| 12 | `airbnb-price-mlr-app` | Interactive MLR case study app | MBA students | Python, Gradio | Low | Medium |
| 13 | `earnings-call-fog-index` | Readability/Fog Index extraction from conference calls | Disclosure researchers | Stata/Python | Medium | Low–Medium |
| 14 | `corporate-finance-calculator` | Teaching calculators (NPV/WACC/valuation) | Undergrad/MBA students | Python (Streamlit) | Low | High (evergreen teaching tool) |
| 15 | `execucomp-ceo-variables` | ExecuComp-based CEO tenure/cohort/hiring-type constructors | Governance/compensation researchers | Stata | Low–Medium | Medium |
| 16 | `bad-news-withholding-toolkit` | EAR/NEAR + info-asymmetry PCA pipeline | Disclosure researchers | Stata | Medium–High | Low–Medium |
| 17 | `lending-club-credit-risk` | Credit-risk modeling case (Indiana-focused framing) | Business analytics students | Python | Low–Medium | Medium |
| 18 | `wrds-python-helpers` | Lightweight Python package for common WRDS queries | Empirical researchers | Python (packaged) | Medium | Medium–High (reusable tool = stars) |
| 19 | `market-microstructure-notes` | Curated notes + code on liquidity/microstructure methods | PhD students | Markdown, Python | Low | Low–Medium |
| 20 | `finance-research-starter-template` | Cookiecutter-style repo template (Stata+Python+README structure) for new empirical projects | Junior researchers, PhD students | Template repo | Low | High (templates travel well) |

---

## 4. 12-Month Portfolio Roadmap

**Phase 1 (Months 1–3) — Foundation & credibility**
Publish repos that are low-effort but establish research legitimacy fast: `finance-research-starter-template`, `wrds-controls-pipeline`, `execucomp-ceo-variables`, `crash-risk-ncskew-replication`. These showcase your empirical infrastructure and are the easiest to clean up from existing pipelines.

**Phase 2 (Months 4–6) — Teaching visibility**
Publish `sec-edgar-lab-toolkit`, `financial-accounting-seminar`, `corporate-finance-calculator`, `ibm-workforce-segmentation`. These are highly shareable, low-risk (no proprietary data), and useful to a broad student/instructor audience — good for early stars and forks.

**Phase 3 (Months 7–9) — Flagship research/ML work**
Publish `ceo-overconfidence-nlp`, `disclosure-political-risk`, `discretionary-accruals-toolkit`, `bad-news-withholding-toolkit`. These are your most differentiated, highest-effort repos — release once documentation and a sample dataset are solid, since this is what journal editors and AI-in-finance researchers will scrutinize most.

**Phase 4 (Months 10–12) — Tools & synthesis**
Publish `wrds-python-helpers` (packaged, pip-installable), `ceo-crash-risk-dashboard`, `airbnb-price-mlr-app`, `liquidity-commonality-toolkit`, `market-microstructure-notes`, `lending-club-credit-risk`, `earnings-call-fog-index`, `internal-governance-innovation`. By this point your profile has enough history that a reusable package (`wrds-python-helpers`) and a polished dashboard make the strongest closing impression.

---

## 5. Profile Design Recommendations

- **Color scheme:** one accent color used consistently across badges (`#0e75b6`, a professional academic blue, is used in the README above) rather than rainbow badges.
- **Badges:** shields.io "for-the-badge" style for tech stack (bold, scannable); flat style for links/contact (less visually loud).
- **GitHub Stats widgets:** `github-readme-stats`, `github-readme-streak-stats`, `github-readme-activity-graph` — all shown above, theme set to `default`/`minimal` with `hide_border=true` to avoid clutter.
- **Contribution snake:** optional; set up via the `platane/snk` GitHub Action in a dedicated repo (commented placeholder included in the README) — skip if you'd rather keep the profile strictly research-focused.
- **Trophies:** `github-profile-trophy` can be added under GitHub Stats if you want gamified badges, but for an academic audience it can read as slightly informal — optional, not included by default.
- **Visitor counter:** `komarev.com/ghpvc` badge included at the top; unobtrusive and common on academic profiles.
- Keep total profile length to one scroll-and-a-half on desktop — the stats/trophy section is where profiles usually get cluttered, so cap it at the three widgets already included.

---

## 6. Branding

**Short bio (160 characters):**
> Empirical finance researcher — corporate governance, disclosure & microstructure. Building reproducible research tools & financial ML/NLP. UVM.

**Longer profile summary (for LinkedIn/website "About" reuse):**
> Mohamed Mekhaimer is the Elizabeth and David Daigle Professor of Finance at the Grossman School of Business, University of Vermont. His research spans corporate governance, subordinate-executive incentives, disclosure, and market microstructure, published in outlets including *The Accounting Review*, *Journal of Corporate Finance*, and *Journal of Banking and Finance*. His current work extends this empirical toolkit with machine learning and NLP methods — applied to executive overconfidence, disclosure obfuscation, and political risk — and he builds open, reproducible research and teaching tools in Python and Stata.

**Pinned repository recommendations (choose 6):**
`finance-research-starter-template` · `ceo-overconfidence-nlp` · `wrds-controls-pipeline` · `sec-edgar-lab-toolkit` · `crash-risk-ncskew-replication` · `financial-accounting-seminar`

*(This mix signals: reusable infrastructure, flagship ML research, and teaching impact — the three things the target audiences in the brief care about most.)*

**Discoverability keywords (GitHub bio/topics):**
`empirical-finance` `corporate-governance` `financial-nlp` `machine-learning-finance` `accounting-research` `wrds` `stata` `python` `reproducible-research` `financial-econometrics` `disclosure-analytics` `market-microstructure`
