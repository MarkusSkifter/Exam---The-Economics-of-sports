# CLAUDE.md — Exam Project: The Economics of Sports (KAN-CGMAV1006U, Spring 2026)

## Project Overview

This is an individual take-home exam paper for the CBS course "The Economics of Sports" (Cand.merc.mat., student number S160645). The paper analyses rider abandonment (DNF) in Grand Tour cycling (Tour de France, Giro d'Italia, Vuelta a España, 2010–2025) using Cox proportional hazard models. The research question is: **How do proxy measures of economic incentives and continuation costs explain rider abandonment in Grand Tours?**

The goal is a **10-page** research paper written in LaTeX that earns a **12 on the Danish grading scale** (the highest standard grade, equivalent to 13 on the old scale). This means the paper must demonstrate excellent command of course theory, rigorous empirical methodology, careful interpretation of results, and clear academic writing.

---

## Exam Requirements (from Exam_Project_2026.pdf)

The exam description by Battista Severgnini (bs.eco@cbs.dk) specifies:

1. **Research paper** on a specific and relevant research question in Sport Economics.
2. **Must use research methods in economics and/or econometrics.**
3. **Required structure:** Front Page and Title, Content (Introduction, Chapters, Conclusion, References, Appendixes if necessary).
4. **Introduction must:** present the research question, explain why it is important, discuss the literature considered, the material (data) used, and the research methods.
5. **Chapters** perform the analysis of the research question.
6. **References** must follow CBS's "Acknowledging sources in written work" — failure to cite properly constitutes plagiarism.
7. **Page limit:** papers exceeding the maximum number of standard pages (check CBS formal requirements) may not be accepted.

**Optional:** A research proposal can be sent to the instructor during week 17 (April 20–26, 2026) via CBS mail. Comments returned before April 23rd.

---

## Folder Structure

```
Eksamen/
├── Exam_Project_2026.pdf                  # Exam description and rules
├── Forelæsninger/                         # Lecture slides (F1–F7)
│   ├── F1 - Intro.pdf
│   ├── F2 - Sport Clubs as Profit-Maximizing Firms.pdf
│   ├── F3 - Advertisement and TV rights..pdf
│   ├── F4 - labour markets pt 1.pdf
│   ├── F5 - labour markets pt 2.pdf
│   ├── F6 - Managers, Coaches and team performance.pdf
│   └── F7 - Predicting match outcomes and betting markets.pdf
├── Kilder/                                # Source papers from the course
│   ├── Rosen-EconomicsSuperstars-1981.pdf
│   ├── 2010-the-sports-business-as-a-labor-market-laboratory.pdf
│   ├── Long Term Contracts and Compensation in Major League Baseball.pdf
│   ├── The italian job.pdf
│   ├── Match riging and the career.pdf
│   ├── Racial Discrimination Among NBA Referees,.pdf
│   ├── 2006-some-economics-of-ticket-resale.pdf
│   └── 2010-the-economics-of-sports-facilities-and-their-communities.pdf
├── Economics_of_sport_Exam/               # Data + Python analysis pipeline
│   └── grand_tour_attrition/
│       ├── scripts/  (01_scrape → 05_robustness)
│       ├── data/     (raw + processed CSVs, panel.csv, panel_time_varying.csv)
│       ├── figures/  (fig1–fig8 PNG files)
│       └── tables/   (table1–table6 CSV + LaTeX)
└── Exam---The-Economics-of-sports/        # LaTeX project (THIS IS THE PAPER)
    ├── main.tex                           # Master document
    ├── Afsnit/                            # Section files
    │   ├── 1. INTRODUCTION.tex            ✅ FULLY WRITTEN
    │   ├── 2. THEORETICAL FRAMEWORK AND LITERATURE.tex  ✅ FULLY WRITTEN
    │   ├── 3. DATA.tex                    ✅ FULLY WRITTEN
    │   ├── 4. EMPIRICAL STRATEGY.tex      ❌ STILL BULLET-POINT OUTLINE
    │   ├── 5. RESULTS.tex                 ❌ STILL BULLET-POINT OUTLINE
    │   ├── 6. ROBUSTNESS CHECKS AND EXTENSIONS.tex  ❌ STILL BULLET-POINT OUTLINE
    │   ├── 7. CONCLUSION.tex              ❌ STILL BULLET-POINT OUTLINE (also in Outline.tex)
    │   ├── Appendix.tex                   📋 Contains variable table (done)
    │   ├── Outline.tex                    📋 Full structural outline with reasoning (commented out)
    │   ├── Litteratur.bib                 ✅ COMPLETE (30 references)
    │   └── Billeder/                      # All 8 figures (PNG)
    ├── cbs-forside.pdf / cbs-forside.sty  # CBS front page template
    └── fonts/                             # CBS custom fonts
```

---

## Current Writing State — What Is Done vs. What Needs Writing

### DONE (Sections 1–3 are fully written in prose):
- **Section 1 (Introduction):** Complete. Opens with Wiggins 2013 Giro example, states research question, previews approach and findings, outlines paper structure. Contains Figure 2 (DNF by race/year). ~2 pages.
- **Section 2 (Theoretical Framework and Literature):** Complete. Three subsections: economics of rider abandonment (tournament theory, team as firm), labour markets and contracts (Kahn 2000, signalling, DNF as negative signal), related empirical work (gap in literature). ~2.5 pages.
- **Section 3 (Data):** Complete. Three subsections: data collection (scraping pipeline), variable definitions with economic interpretations (Table of variables), summary statistics (Table 1 + KM curves figure + DNF by year figure). ~2.5 pages.

### NEEDS WRITING (Sections 4–7 are still bullet-point outlines):
- **Section 4 (Empirical Strategy):** Outline only. Must be converted to flowing prose. Three subsections: Cox PH model justification and equation, time-varying extension, PH assumption testing. Should reference Table 4 (Schoenfeld test) and Figure 6 (Schoenfeld residuals). ~1.5 pages.
- **Section 5 (Results):** Outline only. Must be converted to flowing prose. Three subsections: basic Cox model (Table 2, Figure 5), time-varying Cox model (Table 3), economic interpretation. ~1.5 pages.
- **Section 6 (Robustness Checks and Extensions):** Outline only. Must be converted to flowing prose. Two subsections: sub-sample analysis (Tables 5a/5b, Figure 7), GC counterfactual analysis (Table 6, Figure 8). ~1.5 pages.
- **Section 7 (Conclusion):** Outline only. Must be converted to flowing prose. Restate findings, limitations, extensions, closing sentence. ~0.5–1 page.

---

## Writing Rules — STRICTLY FOLLOW THESE

### Language and Style
1. **Write in simple, understandable language.** Sentences should be clear and direct. Avoid unnecessarily complex or flowery academic phrasing. A reader unfamiliar with survival analysis should be able to follow the reasoning.
2. **NO dashes ("-") in the text.** Do not use hyphens for parenthetical remarks (e.g., do not write "riders — especially GC contenders — tend to..."). Use commas, parentheses, or restructure the sentence instead. Note: this applies to the text body, not to LaTeX commands, citations, or mathematical notation.
3. **Write in full prose paragraphs.** Never use bullet points or numbered lists in the final text. Every section must be written as connected, flowing sentences and paragraphs. The bullet-point outlines in Sections 4–7 are a planning tool, not the final form.
4. **Use hedged language when interpreting results.** Because the dataset has no direct financial variables, always use phrases like "consistent with," "suggests," "can be interpreted as," "proxies for." Never overclaim causality. This is critical for the grade.
5. **Keep existing text that is already well-written.** Sections 1–3 are largely good. They can be improved or tightened, but do not rewrite them from scratch unless there is a clear problem.

### Figures and Tables
6. **Keep all relevant plots and tables.** The figures and tables already generated by the Python scripts are important analytical outputs. The mapping of which figure/table goes in which section is documented in the Outline.tex comment block.
7. **Figure/table placement:** Include figures and tables in the sections where they are discussed, not in a separate appendix dump. The appendix should only hold supplementary material.
8. **Fix figure captions.** Several figures currently have `\caption{Caption}` as placeholder. Every figure and table must have a descriptive caption that tells the reader what it shows.
9. **Fix figure label references.** Some figures use `\label{fig:placeholder}` instead of proper labels. Each figure must have a unique, descriptive label (e.g., `\label{fig:km_curves}`, `\label{fig:dnf_by_year}`).

### Figure and Table Mapping (from Outline.tex)
| Output | Section |
|---|---|
| Table 1 (summary stats) | Section 3.3 |
| Table 2 (basic Cox) | Section 5.1 |
| Table 3 (time-varying Cox) | Section 5.2 |
| Table 4 (Schoenfeld test) | Section 4.3 |
| Tables 5a/5b (subsamples) | Section 6.1 |
| Table 6 (counterfactual) | Section 6.2 |
| Figure 1 (KM curves) | Section 3.3 |
| Figure 2 (DNF by race/year) | Section 1 (already placed) and Section 3.3 |
| Figure 3 (DNF by stage type) | Appendix |
| Figure 4 (cumulative DNF) | Appendix |
| Figure 5 (hazard ratio forest) | Section 5.1 |
| Figure 6 (Schoenfeld residuals) | Section 4.3 or Appendix |
| Figure 7 (GC vs non-GC forest) | Section 6.1 |
| Figure 8 (counterfactual GC) | Section 6.2 |

### Academic Quality for Grade 12
10. **Connect everything to economic theory.** Every empirical finding must be tied back to the course concepts: tournament theory (Rosen 1981, Lazear & Rosen 1981), labour market signalling (Kahn 2000), team as profit-maximising firm (Lecture F2), advertisement and media value (Lecture F3). This is the single most important thing for the grade.
11. **Show awareness of limitations.** The paper must explicitly acknowledge what the data cannot say (no financial variables, coarse GC proxy, unobserved team strategy, selection bias). Self-awareness signals maturity.
12. **Cite course material.** The examiner wants to see that you engaged with the lectures and readings. Reference specific lectures (F2 on firms, F3 on TV rights, F4/F5 on labour markets, F6 on managerial tenure as a survival process) and the assigned papers.
13. **Methodology must be justified, not just described.** Explain why a Cox PH model is appropriate (semi-parametric, handles censoring, duration dependence) and why the time-varying extension is needed (stage difficulty varies within a race).

---

## What Lectures and Sources Are Relevant (and What Is NOT)

### RELEVANT — use these in the paper:
- **F2 (Sport Clubs as Profit-Maximizing Firms):** teams make resource-allocation decisions about riders; the team-as-firm framing for domestique withdrawal.
- **F3 (Advertisement and TV rights):** media exposure and sponsor visibility differ between races; explains why Tour de France has lower abandonment.
- **F4 (Labour Markets pt 1):** Kahn (2000) on sports as labour market laboratory; Rosen (1981) on superstars and tournament theory; sports produce observable performance data.
- **F5 (Labour Markets pt 2):** performance signals, contract implications, discrimination framework (for context on how observable outcomes affect wages).
- **F6 (Managers, Coaches and team performance):** managerial tenure modelled as a survival process (parallel to rider abandonment as a survival process). Boeri & Severgnini (2008) on career concerns in Italian football.
- **Rosen (1981) — The Economics of Superstars:** tournament theory, convex prize structures.
- **Kahn (2000) — The Sports Business as a Labor Market Laboratory:** core framework for the paper.
- **Boeri & Severgnini (2008) — The Italian Job:** career concerns and strategic behaviour inference.

### NOT RELEVANT — do not use these:
- **F1 (Intro):** too general, no specific theory applicable.
- **F7 (Predicting match outcomes and betting markets):** not related to abandonment or cycling.
- **Courty (2003) ticket resale:** not relevant.
- **Coates & Humphreys (2010) sports facilities:** not relevant.
- **Price & Wolfers (2010) NBA referee discrimination:** not relevant.
- **Duggan & Levitt (2002) sumo wrestling corruption:** not relevant (though match-fixing methodology is tangentially interesting, it is not used in this paper).

These irrelevant sources are already in the .bib file but should NOT be cited in the paper text. Only cite what is directly relevant to the argument.

---

## The Python Analysis Pipeline

The data and figures are already generated. The scripts are in `Economics_of_sport_Exam/grand_tour_attrition/scripts/` and produce all outputs in `figures/` and `tables/`. The pipeline runs sequentially:

1. **01_scrape.py** — Scrapes ProCyclingStats for rider data, stage results, stage metadata (2010–2025). Resumable with checkpoint.
2. **02_clean.py** — Cleans data, constructs features (age, experience, prev DNF rate, GC contender flag, team covariates), builds panel.csv and panel_time_varying.csv.
3. **03_descriptive.py** — Generates Table 1 (summary stats), Figure 1 (KM curves), Figure 2 (DNF by race/year), Figure 3 (DNF by stage type), Figure 4 (cumulative DNF by stage).
4. **04_cox_model.py** — Fits basic Cox PH model (Table 2) and time-varying Cox PH model (Table 3). Tests PH assumption via Schoenfeld residuals (Table 4). Generates Figure 5 (hazard ratio forest plot) and Figure 6 (Schoenfeld residual plots).
5. **05_robustness.py** — Fits sub-sample Cox models for GC contenders (Table 5a) and non-GC riders (Table 5b). Runs GC counterfactual analysis (Table 6). Generates Figure 7 (GC vs non-GC forest plot) and Figure 8 (counterfactual GC positions).

**Important:** The figures are already copied into `Exam---The-Economics-of-sports/Afsnit/Billeder/`. The LaTeX files reference them from that location. The `.tex` table files are in `Economics_of_sport_Exam/grand_tour_attrition/tables/` and can be `\input{}` directly or their contents can be adapted.

---

## Key Results to Discuss (from the Python outputs)

### Basic Cox Model (Table 2):
- Previous DNF rate: HR = 1.549, p < 0.001 (strongest predictor; 55% higher hazard)
- GC contender: HR = 1.156, p = 0.008 (counterintuitive positive; strategic withdrawal + physical exposure)
- Tour de France: HR = 0.865, p = 0.002 (lower hazard; higher event value)
- Age, experience, team controls, year trend: insignificant

### Time-Varying Cox Model (Table 3):
- Mountain stages: HR = 1.034, p = 0.025 (marginal cost of effort)
- Previous DNF rate: marginally significant (p = 0.05), smaller coefficient
- GC contender and race dummies lose significance (absorbed by stage-level variation)

### Sub-sample Analysis (Tables 5a/5b):
- GC contenders: DNF rate HR = 2.28, p = 0.001 (much stronger effect)
- Non-GC riders: DNF rate HR = 1.47, p < 0.001 (significant but weaker)
- Tour de France protective effect: significant only for non-GC riders (HR = 0.866, p = 0.005), not for GC contenders

### Counterfactual GC Analysis (Table 6):
- Estimates reshuffled standings if abandoned GC contenders had continued
- Illustrates economic consequences: redistribution of prize money, UCI points, signal value

---

## LaTeX Specifics

### Compilation
The project uses `biblatex` with `biber` backend (`authoryear` style). Compile with: `pdflatex → biber → pdflatex → pdflatex`.

### Header Issue
The header currently says "Household behaviour over the lifecycle" in main.tex line 159. **This must be changed** to the actual paper title or a short version of it (e.g., "Economics of Sports — Exam Paper" or "Rider Abandonment in Grand Tour Cycling").

### Section Numbering
The main.tex file has custom section numbering that removes chapter prefixes (article-style numbering: 1, 1.1, 1.1.1 instead of 0.1, 0.1.1). This is already configured and should not be changed.

### The Conclusion Section
The file `7. CONCLUSION.tex` exists and contains bullet-point outline. It is also partially duplicated in `Outline.tex`. The actual conclusion should be written in `7. CONCLUSION.tex`. Note that `7. CONCLUSION.tex` is NOT currently `\input` in main.tex (the main.tex goes from Section 6 directly to bibliography). The conclusion section should be added to main.tex before the bibliography.

### Missing from main.tex
- `\input{Afsnit/7. CONCLUSION}` is not in main.tex. Must be added before `\printbibliography`.
- The Appendix file exists but is not `\input` in main.tex either. If an appendix is desired, it must be added.
- The `\label{sec:conclusion}` referenced in the introduction's outline needs to exist in the conclusion file.

---

## Checklist Before Submission

- [ ] All sections written in full prose (no bullet points remaining)
- [ ] No dashes ("-") used for parenthetical remarks in text
- [ ] All figures have descriptive captions (no "Caption" placeholders)
- [ ] All figures have unique labels (no "fig:placeholder" duplicates)
- [ ] Header in main.tex fixed (not "Household behaviour over the lifecycle")
- [ ] Section 7 (Conclusion) is \input in main.tex
- [ ] Every empirical finding is tied to economic theory from the course
- [ ] Hedged language used throughout results discussion
- [ ] Only relevant sources cited (not the full bib file)
- [ ] All cross-references (\ref) resolve correctly
- [ ] Paper compiles without errors
- [ ] Paper is approximately 10 pages (excluding front page, ToC, references, appendix)
- [ ] The paper reads as a coherent, flowing academic argument, not a collection of sections
