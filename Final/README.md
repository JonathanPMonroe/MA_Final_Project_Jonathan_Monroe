# University of Chicago — Final Project Replication Materials
**Jonathan Monroe**

This repository contains the final project deliverables for my Community Notes auditing work, focused on **collective intelligence diagnostics** (e.g., decentralization, independence, topical diversity, and aggregation consistency) using the public X (Twitter) Community Notes data.

## Project Overview

The project builds a reproducible analysis workflow around the Community Notes ecosystem, including:

- **Topic modeling + meta-topic construction** (semantic clustering and consolidation for downstream diagnostics)
- **Independence modeling** (similarity/dependence patterns in rater behavior)
- **Decentralization modeling** (structure/centralization of participation and outcomes)
- **Aggregation diagnostics** (interpretable rule extraction / decision-structure probing)

Outputs include cleaned data artifacts (`.parquet`), final notebooks (`.ipynb`), and exported figures (`.png`) used in the write-up/presentation.

---

## Repository Structure

### `Data/`
Core parquet datasets used across notebooks.

| File | Description |
|------|-------------|
| `notes.parquet` | Community Notes note-level data |
| `ratings.parquet` | Ratings on notes (helpful / not helpful, etc.) |
| `noteStatusHistory.parquet` | Note status transitions over time |
| `userEnrollment.parquet` | User enrollment / participation metadata |

### `Notebooks/`
Primary analysis notebooks (final versions).

| Notebook | What it does |
|----------|--------------|
| `Topic Modeling.ipynb` | Topic modeling pipeline (baseline) |
| `Topic_Modeling_2.ipynb` | Topic modeling iteration / refinements |
| `Topic_Modeling_3.ipynb` | Final topic → meta-topic workflow + downstream-ready outputs |
| `Independence Modeling.ipynb` | Independence diagnostic (rater behavior similarity / dependence) |
| `Decentralization Modeling.ipynb` | Decentralization/centralization diagnostic (participation structure) |
| `Mining_Assoc_Rules.ipynb` | Interpretable aggregation-rule probing via association-rule mining |

### `Figures/`
Exported figures referenced in the final write-up.

| Figure | Description |
|--------|-------------|
| `rating_activity_topics.png` | Rating activity / topical distribution visualization |
| `topic_logistic_curves.png` | Logistic curve visualization for topic/meta-topic effects |
| `dependence_threshold_sensitivity.png` | Sensitivity of dependence results to threshold choices |

---

## How to Run

Recommended environment:
- Python
- PySpark + Spark (big-memory configuration recommended)
- Common scientific stack: `pandas`, `numpy`, `matplotlib` (+ any notebook-specific libs)

General workflow:
1. Start with **Topic Modeling** notebooks to generate topic/meta-topic outputs.
2. Run **Independence Modeling** and **Decentralization Modeling** notebooks.
3. Use **Mining_Assoc_Rules** to probe aggregation structure / interpretable rules.
4. Figures are exported into `Figures/`.

---

## Contact

- **Name:** Jonathan Monroe  
- **Email:** jonathanmonroe@uchicago.edu  
- **GitHub:** github.com/JonathanPMonroe
