# Bank-Customer-Segmentation
## AllLife Bank Customer Segmentation
### Business Case
AllLife Bank aims to grow its credit card customer base by improving market penetration.
- **Marketing Team:** Run personalized campaigns for new and existing customers.
- **Operations Team:** Enhance customer support by upgrading the service model.
- **Data Science Team (this project):** Deliver actionable customer segmentation using clustering algorithms to guide both marketing and operations strategies.

### Objective  
To identify distinct customer segments based on *spending patterns* and *past interactions with the bank*, and provide *business recommendations* that improve targeting, service efficiency, and customer satisfaction.

### Data Profile
- **Features:**
  - Avg_Credit_Limit
  - Total_Credit_Cards
  - Total_visits_bank
  - Total_visits_online
  - Total_calls_made
- **Observations:** ~660 customers
- **Nature:** Mix of continuous (credit limit) and discrete count features (cards, visits, calls).

## Data Cleaning & Preparation
- Removed irrelevant identifiers (Sl_No, Customer Key).
- Handled skewness in Avg_Credit_Limit via log transformation.
- Applied StandardScaler to normalize all features for fair contribution in clustering.
- Verified distributions with histograms and boxplots.

## Exploratory Data Analysis (EDA)
- **Correlation Heatmap:** Identified strong relationships (e.g., credit limit ↔ number of cards).
- **Pairplots:** Visualized feature interactions and outliers.
- **Boxplots per cluster:** Validated spread and cluster-specific behavior.

## Dimensionality Reduction
- Applied **t-SNE** (2D & 3D) to visualize high-dimensional data.
- Experimented with multiple perplexity values, finalized **perplexity = 50** for optimal separation.
- Clear visual separation of clusters observed.

## Modelling – K-Means Clustering
- Used **Elbow Method** to identify optimal k.
- Validated with **Silhouette Score** for cluster quality.
- Final model chosen with **k = 3 clusters.**

![Final Clusters](https://github.com/MissSamyuktha/Bank-Customer-Segmentation/blob/main/Screenshot_20260105-232141.Chrome~2.png)

## Cluster Profiling
### Cluster 0 – Mid-tier Branch Loyalists (≈58.5%)
- Moderate credit limits (~₹33k), ~5–6 cards.
- High branch visits, low online usage.
- **Recommendation:** Promote digital adoption, hybrid campaigns, branch service bundles.

### Cluster 1 – Mass Market Support-Heavy (≈34%)
- Lowest credit limits (~₹12k), ~2–3 cards.
- Moderate online usage, very high call dependency.
- **Recommendation:** Improve call center efficiency, credit-builder programs, incentivize app usage.

### Cluster 2 – Digital Elites (≈7.5%)
- Very high credit limits (~₹141k), ~9 cards.
- High online usage, minimal branch visits and calls.
- **Recommendation:** Premium digital perks, loyalty rewards, personalized dashboards.

## Approach Followed:
1. Data Cleaning & Transformation
2. EDA & Visualization
3. Feature Scaling
4. Dimensionality Reduction (t-SNE)
5. K-Means Modelling
6. Cluster Validation (Elbow + Silhouette)
7. Cluster Profiling & Business Recommendations

## Tools & Environment
- **IDE:** Google Colab Jupyter Notebook
- **Languages:** **Python** (pandas, numpy, scikit-learn, seaborn, matplotlib), t-SNE
- **Visualization:** **t-SNE**, scatterplots, histograms, boxplots, heatmaps, pairplots
- **Clustering: K-Means**, silhouette analysis

## Impact
This segmentation empowers AllLife Bank to:
- **Marketing:** Deliver personalized campaigns, increase penetration, and upsell products.
- **Operations:** Reduce support load, improve customer satisfaction, and optimize service channels.
- **Strategy:** Focus resources on high-value digital elites while nurturing mid-tier and support-heavy customers.

## Conclusion
This project demonstrates **industry-ready data science capabilities with business approach** through:
- Rigorous preprocessing and scaling.
- Robust clustering validation.
- Clear visualization and profiling.
- Actionable business recommendations.

I approached this as a confident data professional delivering insights that directly drive business growth.
