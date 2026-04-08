# causalGBKMR — Software Paper (EHP version)

**Target journal:** Environmental Health Perspectives (EHP), NIEHS — Linda's first choice (2026-04-08).
- Higher impact, broader environmental-health audience than EH/BMC.
- No dedicated software track, but Methods/Software papers are accepted as **Research Articles**.
- Submission portal: <https://ehp.niehs.nih.gov>
- Author guidelines: <https://ehp.niehs.nih.gov/authors/research-articles>
- **No official LaTeX template** — authors submit Word or PDF. We will use a clean `article` class for Overleaf and convert to Word at submission time if needed.

## EHP Research Article requirements

| Item | Limit |
|---|---|
| Main text | ≤ 7,000 words (excluding abstract, references, tables, figure captions, acknowledgements, supplemental) |
| Structured abstract | ≤ 300 words |
| Abstract headings | **Background · Objectives · Methods · Results · Discussion** |
| Main text structure | **Introduction · Methods · Results · Discussion** (IMRD) |
| Reference style | EHP / AMA-like (numeric superscripts) |

Required declarations: funding, data availability, **code availability**, ethics, author contributions, competing interests, acknowledgements.

## This paper (≠ Arce's `gBKMR_Nature.docx`)

This is **Yanran Li's first-author dissertation paper** introducing the **causalGBKMR R package**, distinct from the Arce-led methodology/application paper (`gbkmr_mi/gBKMR_Nature.docx`).

**Three use cases for the Results section:**
1. **g-BKMR simulation** — re-run Chai et al. (2025) simulation with the new package to validate that point estimates and CIs match the original within Monte Carlo error.
2. **g-BKMR application** — Strong Heart Study metals → fasting glucose (using the 0311 results from `gbkmr_mi/log_glucose/`).
3. **fast BKMR simulation** — computational efficiency comparison from `gbkmr3/` Scenario 3c (BKMR vs. fastBKMR per-model wall time at $n=6{,}000$).

## File map

- `main.tex` — single-file Overleaf source
- `references.bib` — bibliography
- `figures/` — figure files (to populate)
- `application/` — symlinks/copies of figures from `gbkmr_mi/log_glucose/`
- `simulation/` — figures from validation runs (TBD)
- `fastbkmr/` — figures from `gbkmr3/` Scenario 3c (TBD)

## Overleaf workflow

1. Create new Overleaf project → "Upload Project" → upload this folder zipped
2. Set `main.tex` as main document
3. Connect Overleaf → GitHub via Overleaf's git integration
4. From local: `git clone https://git.overleaf.com/<project-id> causalGBKMR_EHP_overleaf`
5. Subsequent updates: `git pull` from the Overleaf remote

## Status of the OTHER paper directory

The earlier `/burg-archive/biostats/users/yl5465/causalGBKMR_paper/` directory was set up for **Arce-led** application paper (originally targeted at EH). Since user is only writing the Application section there and Linda+Arce handle the rest, that directory mostly exists for reference. **This `causalGBKMR_EHP/` directory is the active workspace for the dissertation/software paper.**
