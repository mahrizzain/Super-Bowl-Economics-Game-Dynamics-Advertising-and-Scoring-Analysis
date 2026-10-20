# Super Bowl Economics & Game Dynamics

**Trends in advertising costs and scoring patterns across Super Bowls I–LII (1967–2018)**

An R / Quarto data analysis examining how the cost of Super Bowl advertising has evolved over five decades, and whether more competitive games tend to be higher scoring.

## Research Questions

1. Is there a relationship between time (year) and the cost of a 30-second Super Bowl advertisement?
2. Is there a relationship between margin of victory and total points scored — do closer games score more?

## Key Findings

| Hypothesis | Result | Interpretation |
|------------|--------|----------------|
| Year → ad cost | **R = 0.931, R² = 0.866** | Very strong positive relationship. The cost of a 30-second ad has risen steadily (and nonlinearly) with time; ~87% of the variation in ad cost is associated with year. The pattern holds across all broadcast networks (ABC, CBS, NBC, Fox). |
| Margin of victory → total points | **R = 0.280, R² = 0.078** | Weak positive association. Margin of victory explains only ~8% of scoring variation — game competitiveness is not a strong predictor of total points scored. |

## Data

- **Source:** [“Super Bowl Game Results”](https://www.kaggle.com/datasets/thedevastator/super-bowl-game-results/) on Kaggle, aggregating NFL records, broadcast networks, and media rating organizations.
- **Coverage:** 52 games, Super Bowl I (1967) through Super Bowl LII (2018), 19 variables covering game outcomes, scoring, attendance, broadcast details, and advertising costs.
- **Engineered variables:** `year` (from game date), `margin_of_victory` (winning − losing points), `total_points` (winning + losing points).
- Full data dictionary: [`data/README.md`](data/README.md).

## Methods

- Cleaned and reshaped the raw Kaggle data in R (`tidyverse`): standardized dates, converted viewership to numeric, dropped non-analytic columns (venue, city, conference, notes, index).
- Visualized trends with `ggplot2`: viewership over time, ad cost over time, ad cost vs. viewership by network, and total points vs. point differential.
- Quantified both hypotheses with correlation and linear regression (`tidymodels`), reporting R, R², and slope.

## Limitations

- Observational data: associations between year, viewership, and ad cost are not causal, and ad costs are not adjusted for inflation.
- The year–cost relationship appears exponential, so a linear model only approximates it.
- One game per year (n = 52) limits generalizability of the scoring analysis.

## Project Structure

```
├── README.md                        # Project overview (this file)
├── LICENSE
├── analysis/
│   ├── super-bowl-analysis.qmd      # Main report: analysis, plots, discussion
│   └── proposal.qmd                 # Project proposal and analysis plan
├── data/
│   ├── README.md                    # Data dictionary
│   ├── super-bowl-dataset-1.csv     # Game results, viewership, ad costs
│   └── super-bowl-dataset-2.csv     # Game results, MVP, stadium
└── presentation.pdf                 # Final presentation slides
```

## Tools

- **R** with `tidyverse`, `tidymodels`, `ggplot2`
- **Quarto** for the reproducible report

## Team

Developed by team *group_by_awesomeness* — Benjamin Palmer, Diya Patel, Julia Libhaber, Priyanka Gupta, and Mahriz Zain — for STA 199: Introduction to Data Science at Duke University.
