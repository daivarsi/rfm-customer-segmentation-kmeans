# Customer Segmentation Using RFM Analysis and K-Means Clustering

This project applies real-world customer transaction data to segment customers based on Recency, Frequency, and Monetary (RFM) value using K-Means clustering. The goal is to identify high-value customer groups and enable strategic targeting for marketing, loyalty programs, and churn prevention.

## 🔍 Objective
To help businesses identify:
- Which customers are the most valuable?
- Who is at risk of churn?
- Where to direct promotional efforts and premium offers (e.g., travel perks, elite memberships)

## 🧾 Dataset
- Source: [UCI Online Retail Dataset](https://archive.ics.uci.edu/ml/datasets/online+retail)
- One year of transactional data from a UK-based e-commerce retailer
- Features: `InvoiceNo`, `CustomerID`, `InvoiceDate`, `Quantity`, `UnitPrice`

## 🧮 Methodology
1. **Data Cleaning**
   - Removed nulls and cancelled orders
   - Calculated `TotalPrice = Quantity * UnitPrice`
2. **RFM Calculation**
   - `Recency`: Days since last purchase
   - `Frequency`: Number of transactions
   - `Monetary`: Total money spent
3. **Normalization**
   - Standardized RFM features using `StandardScaler`
4. **Clustering**
   - K-Means clustering with 4 segments
5. **Visualization**
   - Boxplots for RFM metrics
   - t-SNE 2D projection to visualize cluster separation

## 📊 Results & Business Insight

| Cluster | Description | Actionable Strategy |
|---------|-------------|---------------------|
| **Cluster 2** | 💎 Small group of **high spenders** | Reward with premium offers (e.g., Platinum card perks, exclusive loyalty points) |
| **Cluster 3** | 📦 **Largest group**, average spend | Cost-sensitive group — automate low-cost engagement |
| **Cluster 1** | ⚠️ Low engagement & low spend | Reactivation campaign or cut spend |
| **Cluster 0** | 💼 Stable, mid-value customers | Upsell opportunities with relevant offers |

### 💡 Insight:
**Value is not in volume alone** — Cluster 2 (the smallest) brings in the highest monetary value. Smart segmentation = smart targeting.

## 📈 Visuals

- 📦 RFM boxplots by cluster
- 🧠 t-SNE 2D projection of customer groups

## 🛠 Tools Used
- Python (pandas, numpy)
- Scikit-learn (KMeans, StandardScaler, t-SNE)
- Seaborn & Matplotlib

## 📁 How to Run
Clone the repo and run `rfm_analysis.ipynb` in Jupyter or Google Colab. No API keys required.

## 📬 Contact
Feel free to reach out if you'd like to collaborate or have feedback.
