# NYC Public High School Equity Analysis — Detailed Findings

## Executive Summary
[1-2 paragraphs: What you analyzed, why it matters, headline findings]

## Data Overview
- **Dataset**: 1,834 NYC public high schools
- **Time Period**: [Year of data]
- **Variables Analyzed**:
  - Total enrollment
  - Percent students with disabilities
  - Percent English language learners (ESL)
  - Percent students in poverty
  - School name (identifier)
- **Data Source**: [NYC Dept of Education / Kaggle / etc.]

## Methodology
### Statistical Approach
- Descriptive statistics (mean, median, quartiles)
- Distribution analysis (histograms, skewness assessment)
- Correlation matrix (Pearson coefficients)
- Outlier identification

### Tools & Libraries
- Python 3.x
- Pandas (data manipulation)
- NumPy (numerical computing)
- Plotly (interactive visualizations)

---

## Key Findings

### 1. Enrollment Distribution
**Finding**: Right-skewed distribution with mean (588.3) > median (476.7)

**Interpretation**: 
- Most schools are mid-sized (~477 students, median)
- 30 specialized schools (1.6%) exceed 2,000 enrollment
- Some very large schools pull the average higher

**Implication**: NYC maintains diverse school models—comprehensive schools coexist with specialized programs.

---

### 2. Students with Disabilities
**Finding**: Mean 21.9%, median 19.3%; narrow IQR (15.0–24.4%)

**Interpretation**:
- Clustering around 20% is notable
- NYC's median (19.3%) exceeds national average (~14–15%)
- 57 schools (3.1%) serve 90%+ students with disabilities (specialized IEP programs)

**Implication**: NYC either has higher identification rates, serves more students with disabilities, or has robust specialized school infrastructure.

---

### 3. English Language Learners (ESL)
**Finding**: Right-skewed; mean 13.3% > median 9.1%

**Interpretation**:
- Most schools serve low proportions of ESL students (median 9.1%)
- 48 schools (2.6%) have extreme ESL concentrations (>50%)
- Right tail indicates geographic/demographic clustering

**Implication**: ESL students are concentrated in specific schools rather than dispersed system-wide.

---

### 4. Poverty Distribution
**Finding**: Left-skewed; mean 75.0%, median 79.7%; narrow IQR (68.1–88.6%)

**Interpretation**:
- **Critical insight**: 948 schools (52%) cluster tightly in 68–89% poverty band
- Only 20.5 percentage-point spread in middle 50% of schools
- Indicates consistent, systemic high poverty across nearly all schools

**Implication**: Poverty is not concentrated in a few schools—it's a **system-wide challenge**. Most NYC high schools serve predominantly low-income populations.

---

### 5. Relationships Between Variables

#### Poverty ↔ ESL Correlation: **r = 0.3155**
- **Strength**: Weak-to-moderate positive relationship
- **Variance explained**: r² ≈ 10% (poverty explains ~10% of ESL variation)
- **Interpretation**: Poverty and ESL co-occur more than chance, but most variation is explained by other factors

#### Other Correlations (all < 0.18):
- Enrollment vs. Poverty: r = −0.14 (negligible)
- Enrollment vs. Disability: r = −0.18 (negligible)
- Enrollment vs. ESL: r = 0.03 (essentially none)
- Disability vs. ESL: r = 0.02 (essentially none)

**Implication**: School characteristics are **largely independent**. You cannot predict one metric from another. Schools are multidimensional.

---

### 6. Compounded Disadvantage
**Finding**: 212 schools (11.6%) have both >85% poverty AND >20% ESL

**Interpretation**: These schools face intersecting challenges on multiple fronts.

**Implication**: Targeted policy should identify and support these high-needs schools with coordinated ESL + poverty interventions.

---

## What This Means for Educational Equity

### Systemic vs. Concentrated
- Poverty is **systemic** (widespread across 52% of schools in 68–89% band)
- ESL and disabilities are **concentrated** (right-skewed distributions)
- Schools cannot be ranked on a single "need" scale

### Resource Allocation Implications
1. **One-size-fits-all won't work**: Each school requires individualized assessment
2. **Targeted support needed**: 212 schools with compounded needs require multi-pronged intervention
3. **ESL programs uneven**: 48 schools serve 50%+ ESL students; most serve <20%
4. **Specialized infrastructure**: 57 schools serve 90%+ students with disabilities

### Policy Recommendations (Speculative)
- Conduct equity audit of 212 high-need schools
- Strengthen ESL capacity in concentrated schools
- Ensure comparable resources across all high-poverty schools
- Support specialized school models without creating separate tiers

---

## Limitations & Caveats

1. **Correlational, not causal**: Relationships identified here do not establish causation
2. **Cross-sectional snapshot**: Data reflects one point in time, not trends
3. **Aggregated metrics**: School-level averages mask within-school variation
4. **Missing context**: Variables like funding, staffing, curriculum quality not included
5. **Unmeasured factors**: Geography, school type, grades served not in dataset
6. **Sample limitations**: NYC-specific; findings may not generalize nationally

---

## Conclusion

NYC's public high school system serves predominantly low-income students with considerable diversity in specialization, language needs, and disability status. Rather than a single "equity problem," the system exhibits multiple independent challenges requiring multidimensional policy responses. The concentration of both poverty (systemic) and ESL/disability (clustered) suggests that while resource challenges are widespread, targeted interventions could address specific school populations effectively.

---

## Data & Code
- Full analysis: `M6_NYC_Schools.ipynb`
- Data source: `datasets/schools.csv`
- Visualizations: See `visualizations/` folder
- Dependencies: `requirements.txt`
