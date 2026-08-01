# Istanbul Shopping Customer Segmentation Analysis

### *Uncovering Shopping Patterns and Customer Behaviors through Data Science*

![Python](https://img.shields.io/badge/Python-3.9%2B-blue)
![Data Science](https://img.shields.io/badge/Data-Science-green)
![Machine Learning](https://img.shields.io/badge/Machine-Learning-orange)
![Clustering](https://img.shields.io/badge/Clustering-Unsupervised-red)
![Status](https://img.shields.io/badge/Status-Active-success)

---

## 🎯 Project Overview

### Business Problem

Understanding customer behavior is crucial for retail success. This project analyzes shopping data from Istanbul to identify distinct customer segments, enabling:
- **Targeted marketing campaigns** - Reach the right customers with the right message
- **Personalized customer experiences** - Tailor offerings to specific customer needs
- **Optimized inventory management** - Stock products based on customer preferences
- **Strategic business decisions** - Data-driven insights for growth

### What This Project Does

- Performs exploratory data analysis on Istanbul shopping data
- Identifies customer segments using clustering algorithms
- Analyzes shopping patterns and trends
- Provides actionable business insights
- Visualizes customer behavior patterns

### Key Insights Delivered

- 🛍️ **Customer purchasing patterns** - Understanding what drives purchases
- 💰 **Spending behavior analysis** - Identifying high-value customers
- 📊 **Demographic segmentation** - Targeting by age, gender, and income
- 🕐 **Temporal shopping trends** - Peak times and seasonal patterns
- 🎯 **Customer lifetime value estimation** - Predicting long-term value

---

## 📊 Dataset Description

**Source:** Istanbul Shopping Mall Customer Data

### Features

**Customer Demographics:**
- Age
- Gender
- Income level
- Location

**Shopping Behavior:**
- Purchase amount
- Product categories
- Shopping frequency
- Payment methods
- Visit duration

**Temporal Data:**
- Purchase date/time
- Seasonal patterns
- Day of week trends

**Dataset Characteristics:**
- Comprehensive customer transaction records
- Multiple demographic and behavioral variables
- Suitable for segmentation and pattern analysis

---

## 🧠 Methodology

### 1. Data Preparation
```python
# Data cleaning and preprocessing
- Handling missing values
- Feature engineering
- Outlier detection and treatment
- Data normalization/standardization
```

### 2. Exploratory Data Analysis (EDA)
- Univariate analysis (distributions)
- Bivariate analysis (relationships)
- Correlation analysis
- Statistical testing
- Visualization of patterns

### 3. Feature Engineering
- **RFM Analysis** (Recency, Frequency, Monetary)
- Customer lifetime value calculation
- Shopping pattern indicators
- Temporal features
- Derived metrics

### 4. Segmentation Techniques
- **K-Means Clustering**: Identify natural customer groups
- **Hierarchical Clustering**: Understand segment relationships
- **DBSCAN**: Detect outliers and dense regions
- **PCA**: Dimensionality reduction and visualization

### 5. Segment Profiling
- Demographic characteristics
- Shopping behavior patterns
- Value contribution
- Growth potential
- Marketing recommendations

---

## 🛠️ Technologies & Tools

### Programming & Libraries

```
Python 3.9+
├── Data Manipulation
│   ├── pandas
│   ├── numpy
│   └── scipy
├── Machine Learning
│   ├── scikit-learn
│   └── yellowbrick
├── Visualization
│   ├── matplotlib
│   ├── seaborn
│   ├── plotly
│   └── folium (for maps)
└── Jupyter
    └── jupyter notebook
```

---

## 📦 Installation & Setup

### Prerequisites
- Python 3.9 or higher
- pip package manager
- 4GB RAM minimum

### Quick Start

```bash
# Clone the repository
git clone https://github.com/Ghulam-Mustafa-Keerio/Customer-Segmentation-Analysis.git
cd Customer-Segmentation-Analysis

# Create virtual environment (recommended)
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Launch Jupyter Notebook
jupyter notebook

# Open Customer_Segmentation_Analysis.ipynb
```

---

## 🚀 Usage

### Running the Analysis

**1. Load and Explore Data:**
```python
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

# Load dataset
df = pd.read_csv('data/istanbul_shopping_data.csv')

# Quick overview
print(df.head())
print(df.info())
print(df.describe())
```

**2. Perform RFM Analysis:**
```python
# Calculate RFM scores
# Recency: Days since last purchase
# Frequency: Number of transactions
# Monetary: Total spending amount

rfm_df = calculate_rfm(df, 
                       customer_id='CustomerID',
                       date='InvoiceDate',
                       amount='TotalAmount')
```

**3. Apply Clustering:**
```python
from sklearn.cluster import KMeans
from sklearn.preprocessing import StandardScaler

# Prepare features
features = ['Recency', 'Frequency', 'Monetary']
X = rfm_df[features]

# Standardize
scaler = StandardScaler()
X_scaled = scaler.fit_transform(X)

# Apply K-Means
kmeans = KMeans(n_clusters=4, random_state=42)
rfm_df['Segment'] = kmeans.fit_predict(X_scaled)
```

**4. Visualize Segments:**
```python
import plotly.express as px

# 3D scatter plot of segments
fig = px.scatter_3d(rfm_df, 
                     x='Recency', 
                     y='Frequency', 
                     z='Monetary',
                     color='Segment',
                     title='Customer Segments')
fig.show()
```

---

## 📈 Key Findings

### Customer Segments Identified

#### 💎 Champions (Segment 1)
- **Characteristics:** High frequency, recent purchases, high spending
- **Action:** VIP treatment, loyalty rewards, exclusive access
- **Business Value:** Highest lifetime value customers

#### ⭐ Loyal Customers (Segment 2)
- **Characteristics:** Regular purchasers, moderate to high spending
- **Action:** Engagement programs, upselling, personalized offers
- **Business Value:** Stable revenue stream

#### 🎯 Potential Loyalists (Segment 3)
- **Characteristics:** Recent customers, growing purchase frequency
- **Action:** Nurture with offers, build loyalty programs
- **Business Value:** High growth potential

#### 💤 At-Risk (Segment 4)
- **Characteristics:** Previously active, now declining engagement
- **Action:** Win-back campaigns, incentives, feedback surveys
- **Business Value:** Retention opportunity

### Shopping Trends
- 📅 **Peak shopping periods** identified for optimal marketing timing
- 🕐 **Time-of-day patterns** for staffing and promotions
- 💳 **Payment preferences** for checkout optimization
- 🛒 **Average basket analysis** for upselling strategies
- 📈 **Seasonal variations** for inventory planning

---

## 📊 Visualizations

The project includes comprehensive visualizations:

### 1. Customer Distribution
- Age and gender demographics
- Income level distribution
- Geographic heat maps

### 2. Shopping Patterns
- Purchase frequency over time
- Spending trends
- Category preferences
- Time-of-day analysis

### 3. Segmentation Results
- 3D cluster visualization
- Dendrogram (hierarchical clustering)
- Elbow curve for optimal K
- Silhouette analysis

### 4. Business Insights
- Revenue by segment
- Customer lifetime value
- Churn risk indicators
- Growth opportunities

---

## 💼 Business Recommendations

### For Champions
- ✅ Exclusive early access to new products
- ✅ Premium customer service
- ✅ Referral incentive programs
- ✅ Personalized communication

### For Loyal Customers
- ✅ Points-based loyalty program
- ✅ Special birthday offers
- ✅ Community building initiatives
- ✅ Product recommendations

### For Potential Loyalists
- ✅ Welcome series emails
- ✅ Educational content
- ✅ First purchase follow-ups
- ✅ Incentivized repeat purchases

### For At-Risk Customers
- ✅ Re-engagement campaigns
- ✅ Limited-time offers
- ✅ Feedback surveys
- ✅ Win-back discounts

---

## 📂 Project Structure

```
Customer-Segmentation-Analysis/
├── Customer_Segmentation_Analysis.ipynb    # Main analysis notebook
├── data/                                   # Data directory (if applicable)
│   ├── raw/                               # Raw data files
│   └── processed/                         # Processed data files
├── requirements.txt                        # Python dependencies
├── .gitignore                             # Git ignore rules
├── README.md                              # This file
├── CONTRIBUTING.md                        # Contribution guidelines
└── LICENSE                                # MIT License
```

---

## 🔍 Methodology Details

### RFM Analysis
- **Recency (R):** Days since last purchase
- **Frequency (F):** Number of transactions
- **Monetary (M):** Total spending amount

### Scoring System
- Each metric scored 1-5
- Combined RFM score (111-555)
- Segment assignment based on scores

### Clustering Validation
- Elbow method for optimal K
- Silhouette score analysis
- Davies-Bouldin index
- Calinski-Harabasz score

---

## 🎓 Learning Outcomes

### Skills Demonstrated

**Technical Skills:**
- ✅ Data cleaning and preprocessing
- ✅ Exploratory data analysis
- ✅ Feature engineering
- ✅ Unsupervised learning (clustering)
- ✅ Statistical analysis
- ✅ Data visualization
- ✅ Python programming

**Business Skills:**
- Customer behavior analysis
- Marketing strategy development
- Data-driven decision making
- Retail analytics
- Customer relationship management

---

## 🔬 Technical Highlights

**Advanced Techniques:**
- Dimensionality reduction (PCA, t-SNE)
- Multiple clustering algorithms comparison
- Hyperparameter tuning
- Statistical significance testing
- Time series analysis for trends

---

## 🌟 Unique Features

- 🗺️ Geographic analysis of Istanbul shopping zones
- 📱 Product category deep-dive
- 💡 Actionable marketing recommendations
- 📊 Interactive visualizations
- 📈 Customer lifetime value analysis
- 🎯 Churn prediction indicators

---

## 🚀 Future Enhancements

**Planned Improvements:**
- [ ] Predictive modeling for customer churn
- [ ] Real-time dashboard with Streamlit
- [ ] A/B testing framework
- [ ] Integration with CRM systems
- [ ] Recommendation engine
- [ ] Market basket analysis
- [ ] Cohort analysis
- [ ] Customer journey mapping

---

## 🤝 Contributing

Contributions are welcome! Ways to contribute:
- Add new clustering algorithms
- Improve visualizations
- Enhance documentation
- Add more business metrics
- Optimize code performance

See [CONTRIBUTING.md](CONTRIBUTING.md) for details.

---

## 📚 References & Resources

### Tools & Libraries
- [Scikit-learn Documentation](https://scikit-learn.org/)
- [Pandas User Guide](https://pandas.pydata.org/)
- [Seaborn Gallery](https://seaborn.pydata.org/)
- [Plotly Python](https://plotly.com/python/)

### Topics
- Customer Segmentation
- RFM Analysis
- Clustering Algorithms
- Retail Analytics

---

## 📜 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 🙏 Acknowledgments

- Istanbul shopping mall data providers
- Data science community
- Open-source contributors
- Researchers and analysts using this project

---

## 👨‍💻 Author

**Ghulam Mustafa Keerio**
- GitHub: [@Ghulam-Mustafa-Keerio](https://github.com/Ghulam-Mustafa-Keerio)
- Specialization: Data Science, Machine Learning, Business Analytics
- Focus: Turning data into actionable insights

---

## 📧 Contact & Feedback

Have questions or suggestions?
- Open an [Issue](https://github.com/Ghulam-Mustafa-Keerio/Customer-Segmentation-Analysis/issues)
- Submit a Pull Request
- Connect on LinkedIn

---

## 📊 Project Status

- [x] Data collection and cleaning
- [x] Exploratory data analysis
- [x] Feature engineering
- [x] Clustering implementation
- [x] Visualization and reporting
- [ ] Dashboard development
- [ ] Deployment

---

**"Data is the new oil, but insights are the refined fuel that drives business growth."**

---

*This project serves as a valuable resource for researchers, data analysts, and machine learning enthusiasts who want to gain insights into shopping trends and patterns in Istanbul.*
