
# Part 3: Churn Prediction Model

##  Overview
Machine learning model to predict customer churn in the next 60 days using historical customer data from the D2C personal-care brand.

## Objectives
- Build a robust churn prediction model
- Compare multiple ML algorithms
- Identify key churn predictors
- Create a production-ready model
- Save model for API deployment

##  Model Performance

### Best Model: Random Forest

| Metric | Validation | Test |
|--------|------------|------|
| Accuracy | 78.9% | 78.6% |
| AUC-ROC | 0.824 | 0.82 |
| Precision | 0.712 | 0.71 |
| Recall | 0.658 | 0.65 |
| F1-Score | 0.684 | 0.68 |

### Models Compared

| Model | Accuracy | AUC-ROC | Precision | Recall | F1-Score |
|-------|----------|---------|-----------|--------|----------|
| Logistic Regression | 76.4% | 0.801 | 0.683 | 0.642 | 0.662 |
| Random Forest | 78.9% | 0.824 | 0.712 | 0.658 | 0.684 |
| Gradient Boosting | 78.2% | 0.818 | 0.706 | 0.651 | 0.677 |

## Feature Importance (Top 10)

| Rank | Feature | Importance | Interpretation |
|------|---------|------------|----------------|
| 1 | `recency_days` | 0.210 | Days since last order (most important) |
| 2 | `frequency_180d` | 0.183 | Number of orders in last 180 days |
| 3 | `monetary_180d` | 0.152 | Total spend in last 180 days |
| 4 | `sessions_30d` | 0.118 | Web sessions in last 30 days |
| 5 | `last_visit_days_ago` | 0.098 | Days since last website visit |
| 6 | `avg_rating_180d` | 0.084 | Average order rating |
| 7 | `ticket_count_90d` | 0.072 | Support tickets in last 90 days |
| 8 | `cart_adds_30d` | 0.065 | Cart additions in last 30 days |
| 9 | `email_opens_30d` | 0.058 | Email opens in last 30 days |
| 10 | `negative_ticket_rate_90d` | 0.051 | Proportion of negative sentiment tickets |

##  Key Insights

### What Drives Churn?
1. **Recency is King**: Days since last purchase is the strongest predictor
2. **Engagement Matters**: Sessions, product views, and cart adds are strong indicators
3. **Support Issues Signal Risk**: Ticket count and negative sentiment are important
4. **Purchase Behavior**: Frequency and monetary value are key indicators
5. **Rating Patterns**: Low ratings correlate with higher churn

## 📁 Files in This Part
