# NYC Public High School Educational Equity Analysis

## Overview
Analyzed 1,834+ NYC public high schools to identify equity patterns in poverty, 
English language learner (ESL), and disability populations. This project demonstrates 
data analysis, statistical reasoning, and policy-informed insights.

## Key Findings
- **52% of schools** cluster in high-poverty band (68–89% poverty rates)
- **212 schools (11.6%)** face compounded disadvantages (>85% poverty AND >20% ESL)
- **Poverty-ESL correlation: 0.32** (r² = 10%) — co-occurrence is real but 
  other factors drive most variation
- **48 schools** with extreme ESL concentrations (>50% English learners)
- **30 specialized schools** exceed 2,000 enrollment

## Methodology
- **Tools**: Python (Pandas, NumPy, Plotly), Jupyter Notebook
- **Analysis**: Descriptive statistics, distribution analysis, correlation matrices
- **Sample Size**: 1,834 schools across 5 key metrics

## Key Insights for Policy
Most NYC high schools serve similar high-poverty populations. Resource challenges 
are **systemic, not isolated**. Schools cannot be categorized by a single metric—
equitable policy requires individualized assessment of each school's multidimensional profile.

## Visualizations
- Enrollment distribution (right-skewed with outliers)
- Disability percentage clustering (~20%)
- ESL concentration patterns (highly skewed)
- Poverty band clustering (narrow IQR shows consistency)
- Poverty vs. ESL scatter plot with trend line

## How to Run
1. Clone the repository
2. Install dependencies: `pip install -r requirements.txt`
3. Open `M6_NYC_Schools.ipynb` in Jupyter
4. Run all cells to reproduce analysis

**Or** run interactively on [Kaggle](https://www.kaggle.com/code/robertasumeng/nyc-public-high-school-data-analysis)

## Files
- `M6_NYC_Schools.ipynb` — Full analysis with code, visualizations, and interpretation
- `datasets/schools.csv` — Raw data (1,834 schools × 5 variables)
- `visualizations/` — PNG exports of all key charts

## What I Learned
- Distribution shape matters more than mean alone (left vs. right skew tells different stories)
- Correlation ≠ causation (0.32 suggests pattern, not mechanism)
- NYC schools are multidimensional — need holistic equity lens
- Narrow IQR can be a *feature*, not a bug (shows systemic consistency)
