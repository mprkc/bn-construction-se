# Bayesian network construction in software engineering

Supplementary material for **Building Bayesian Networks in Software Engineering: A Checklist and Catalog of Methods for Expert-Based and Hybrid Models**, by Thiago Rique, Emilia Mendes, Mirko Perkusich, Danyllo Albuquerque, Kyller Gorgônio, and Angelo Perkusich.

The resources connect BN construction activities to methods and examples reported in software engineering studies. They support consultation and documentation; they are not a prospectively evaluated construction protocol or a ranking of model quality.

## Start here

- [Companion document (PDF)](supplement/bn-supplement.pdf): mapping and agreement records (S1), full method descriptions and application examples (S2), and the activity-indexed catalog, scoring tables, and reference studies (S3).
- [LaTeX source](supplement/bn-supplement.tex) and [figures](supplement/figures): editable sources for the companion document.
- [BNs in SE - Data extraction.xlsx](data/current/BNs%20in%20SE%20-%20Data%20extraction.xlsx): current author-provided snapshot of the rubric, assessment results, method extraction with supporting excerpts, and retained study set.
- [Checklist Application.xlsx](data/review/Checklist%20Application.xlsx): the assessment and extraction workbook.
- [BN Methodologies - Review.xlsx](data/review/BN%20Methodologies%20-%20Review.xlsx): the cross-domain methodology review and mapping records.
- [Parsifal Report.xls](data/review/Parsifal%20Report.xls): the review-management export.

## Study identifiers and scores

P identifiers in Supplement S1 refer to the cross-domain methodology review. S1–S118 in Supplement S2 refer to the assessed SE studies. PS1–PS66 in Supplement S3 identify the retained catalog studies; the `Final set` worksheet links them to the S identifiers. Paper IDs inside the SE workbook are a separate identifier namespace from the P identifiers of the cross-domain review.

The conceptual checklist has eight activities. The operational assessment uses seven scored questions because expert-based and data-driven validation are assessed together under Q3.1. Each scored question receives 0, 0.5, or 1. The aggregate is:

`0.25 × (Q1.1 + Q1.2 + Q1.3 + Q1.4) + 0.5 × (Q2.1 + Q2.2) + Q3.1`

Each phase contributes at most 1, giving a maximum total of 3. The catalog retains studies with a total of at least 1.5. Scores characterize what studies report, not independently established construction quality, predictive performance, or decision usefulness.

## Data and documentation

The `data/review/` directory contains the methodology-review, checklist-application, and review-management records. The `data/current/` directory provides the current assessment-workbook snapshot. The [data inventory](DATA.md) lists their contents, file sizes, and checksums.

Workbook labels, including references to a “protocol,” are retained as recorded. The current resource is presented as a checklist and catalog. The companion provides detailed method descriptions and study-level tables separately from the main article.

One reference-list inconsistency has been corrected in the companion: PS17 (S25, *Scenario-based assessment of nonfunctional requirements*) is not listed as a maximum-score model-validation reference study, because its recorded Q3.1 score is 0.0. Its other catalog entries and all original workbook scores are unchanged.

## Building the companion

From the `supplement` directory, compile `bn-supplement.tex` with pdfLaTeX and BibTeX:

```sh
pdflatex bn-supplement.tex
bibtex bn-supplement
pdflatex bn-supplement.tex
pdflatex bn-supplement.tex
```

Alternatively, import the contents of `supplement/` into an Overleaf project and set `bn-supplement.tex` as the main document. All required figures and cited bibliography entries are included. The source uses a passthrough `\added` command so that retained revision markup does not affect the companion's appearance.

## Licensing

The three files in `data/review/` retain their [Creative Commons Attribution 4.0 International](https://creativecommons.org/licenses/by/4.0/) license. This repository does not assign a new license to the additional companion text or figures. Third-party publications and quoted excerpts remain subject to their respective rights.
