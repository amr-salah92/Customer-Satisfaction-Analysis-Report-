# Customer Satisfaction Analysis Report  
**QuickService Retail Corp**  

---

## Table of Contents  
1. [Project Name](#project-name)  
2. [Project Background](#project-background)  
3. [Project Goals](#project-goals)  
4. [Data Structure & Initial Checks](#data-structure--initial-checks)  
5. [Executive Summary](#executive-summary)  
6. [Insights Deep Dive](#insights-deep-dive)  
7. [Recommendations](#recommendations)  
8. [Technical Details](#technical-details)  
9. [Assumptions and Caveats](#assumptions-and-caveats)  

---

## Project Name  
**QuickService Retail Corp: Branch Customer Satisfaction Comparison**  
Analysis of satisfaction scores across three retail branches (A, B, C) to identify performance trends and operational parity.  

---

## Project Background  
**Company Overview**:  
QuickService Retail Corp operates in the consumer retail sector, with 100+ branches nationwide since 2010. Key metrics include customer satisfaction scores (1-10 scale), average transaction time, and retention rates.  

**Data Context**:  
- **Dataset**: 20 customers rated all three branches (60 total responses) in Q3 2023.  
- **Analyst Role**: Determine statistical differences in satisfaction scores to guide resource allocation and service standardization.  

---

## Project Goals  
1. **Statistical Parity Check**: Use ANOVA and post-hoc t-tests to compare branch performance.  
2. **Operational Benchmarking**: Identify outliers or trends impacting satisfaction consistency.  
3. **Strategic Alignment**: Provide data-driven recommendations for branch managers.  

**Key Focus Area**:  
- Category : Statistical significance of branch differences.  
 

---

## Data Structure & Initial Checks  
**Dataset**: `Customer Satisfaction.csv` (20 rows × 4 columns).  

**Columns**:  
- `Customer_ID`: Unique identifier (1–20).  
- `Branch_A`, `Branch_B`, `Branch_C`: Satisfaction scores (6–9 scale) for each branch.  

**Initial Checks**:  
- **Completeness**: 0 missing values across all columns.  
- **Ranges**: Scores clustered between 6–9 (min=6, max=9).  
- **Central Tendency**: Near-identical means (7.5–7.55) and low variability (std. dev. ~1.1).  

---

## Executive Summary  
**Top Insights**:  
1. **No Statistical Differences**: ANOVA (p=0.987) and pairwise t-tests confirm parity across branches.  
2. **Consistent Performance**: All branches scored ~7.5/10, reflecting uniform service quality.  
3. **Stable Variability**: Tight score distribution (25th–75th percentile: 6.75–8.25).  

---

## Insights Deep Dive  

### Statistical Significance  
- **ANOVA Result**: F(2, 57) = 0.013, p=0.987 – no significant differences.  
- **Pairwise Tests**: All p-values >0.88 (Bonferroni-adjusted), e.g., Branch A vs. B: p=0.889.  

---

## Recommendations  
1. **Centralized Training**: Invest in uniform training programs to elevate all branches.  
2. **Quarterly Re-Analysis**: Monitor for emerging trends using larger samples.  
3. **Qualitative Feedback**: Supplement scores with open-ended survey questions.  

---

## Technical Details  
**Tools**:  
- **Python**: `pandas` (data wrangling), `pingouin` (ANOVA/t-tests), `matplotlib` (visualization).  

**Rationale**:  
- `pingouin` streamlined hypothesis testing with built-in p-value adjustments.  
- `pandas` enabled efficient data transformation (e.g., melting for ANOVA).  

---

## Assumptions and Caveats  
1. **Independent Groups Assumption**: Analysis treated branches as independent, though customers rated all three (potential pseudoreplication).  
2. **Small Sample Size**: 20 customers per branch may limit power to detect subtle differences.  
3. **Timeframe Limitation**: Data reflects a single quarter; seasonal variations unaccounted for.  
