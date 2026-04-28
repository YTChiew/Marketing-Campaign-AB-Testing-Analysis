## Project Overview

This project analyzes the effectiveness of three marketing campaigns conducted by a fast-food chain to promote a new product. The goal is to evaluate which promotion strategy generates the highest sales performance and provide data-driven recommendations.

The analysis follows an end-to-end workflow including data cleaning, SQL-based querying, statistical testing, and business interpretation.

## Objectives
Evaluate the performance of three promotion strategies
Analyze sales trends across time (4-week period)
Assess impact of market size on campaign effectiveness
Perform statistical testing to validate differences between groups
Provide actionable business recommendations

## Tools & Technologies
- Python (Pandas, SciPy) — data cleaning & statistical analysis
- SQL (SQLite) — data querying and aggregation
- Tableau — data visualization (dashboard)

## Dataset
- Source: Kaggle (Fast Food Marketing Campaign A/B Test)
- Structure: MarketID, LocationID, Promotion (1, 2, 3), Week (1–4). SalesInThousands, and MarketSize (Small, Medium, Large)

## Methodology
1. Data Preparation
- Cleaned dataset using Python (handled missing values, validated data types)
- Loaded structured data into SQL database

2. Data Analysis (SQL)
- Calculated average sales by promotion
- Analyzed weekly sales trends
- Segmented performance by market size

3. Statistical Testing
A. ANOVA test 
- Conducted ANOVA test to compare mean sales across promotion groups
- Result:
     --> F-statistic: 21.95
     --> p-value: 6.77e-10
- Interpretation:
The extremely low p-value (p < 0.05) indicates that there are statistically significant differences in average sales between at least one pair of promotion groups.

B. Post-hoc Analysis (Tukey’s HSD Test)
- To identify which specific groups differ, Tukey’s Honestly Significant Difference (HSD) test was performed.
- Interpretation:
  --> Promotion 1 performs significantly better than Promotion 2
  --> Promotion 3 performs significantly better than Promotion 2
  --> No statistically significant difference between Promotion 1 and Promotion 3

## Key Insights
- Promotion Performance
Promotion 1 achieved the highest average sales (~58K)
Promotion 3 showed moderate performance (~55K)
Promotion 2 significantly underperformed (~47K)

- Time Trend (4 Weeks)
Performance ranking remained consistent across all weeks
Promotion 1 consistently outperformed others
Minimal fluctuation → stable campaign effectiveness

- Market Size Impact
Large markets: highest sales (~60K–77K)
Small markets: moderate (~50K–60K)
Medium markets: lowest (~39K–47K)

- Statistical Validation
ANOVA results confirm statistically significant differences between promotions
Differences are unlikely due to random variation

## Business Recommendations
- Prioritize Promotion 1 as the primary campaign strategy
- Re-evaluate or redesign Promotion 2 due to consistent underperformance
- Focus marketing efforts on large markets for maximum impact
- Investigate structural issues in medium-sized markets

## Conclusion

