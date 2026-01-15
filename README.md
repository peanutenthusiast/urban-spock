# Used Car Pricing Guide for Dealers

## Data-Driven Insights for Smarter Inventory Decisions

## Executive Summary

I built a predictive model that analyzed hundreds of thousands of used car sales to identify price drivers. The model achieves +/- $7k prediction accuracy and reveals a clear hierarchy of value drivers.

**Primarily**: brand reputation adn vehicle type are dominant price factors, followed by age and mileage. Prioritize strong manufacturers in popular vehicle categories.

## Key Findings

### Price Drivers

**1. Manufacturer & Brand (Highest Impact)**

- Brand reputation drives baseline value
- Lesser-known brands can struggle regardless of condition or mileage

**2. Vehicle Type and category**

- SUVs and trucks command market premiums

**3. Age/Year (Moderate Impact)**

- Prioritize Newer Cars
- Newer vehicles from weak brands can underperform older vehicles from strong brands

**4. Mileage (Lower Impact)**

- Lower mileage adds value but doesn't overcome weak brand/type

## Business Recommendations

### 1. Acquisition Strategy

**Model Selection**
Vehicle model, manufacturer, and type contribute a significant percentage to resale value. What's this mean?

- Popular models and brands hold value, more so than minor condition differences
- Build inventory around proven high-value models, not just "good deals"

**Action Items:**

- Create a list of 10-15 brand-type combinations to target
- Allocate 70-80% of acquisition budget to these combinations


### 2. Pricing Strategy

1. Start with manufacturer/brand specific market averages
2. Adjust for age (newer = higher premium)
3. Small adjustments (+/- 5%) for:

- Mileage (low miles = higher price)
- Transmission type
- Regional market differences

## Top Recommendations for Dealers

### Immediate Actions

1. **Audit current inventory**

- Identify strong performing models
- Flag weak models for quick sale, even at lower margins
- Ignore poor performing models, even if lauded as "good deals"

2. **Update pricing strategy**

- Price based on manufacturer, brand, model specific market data first
- Adjust for age second
- Use mileage/features for tweaks

## Technical Analysis for Data Scientists, R&D

### Model Performance Summary

| Approach | RMSE | Key Strengths | Key Weaknesses |
|----------|------|---------------|----------------|
| PCA + Ridge | 6,978 | Best accuracy, handles multicollinearity | Complex interpretation |
| RFE + Linear | ~7,030 | Interpretable coefficients | Slightly lower accuracy |
| Permutation Importance | N/A | True feature impact | Computationally expensive |

![Top Prices for Different Used Vehicle Drivers](/images/prices_via_category.png)

![Correlation Matrix for Various Car Drivers](/images/correlation_matrix.png)
