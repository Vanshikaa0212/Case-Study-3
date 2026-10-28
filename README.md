# Customer_Segmentation
# Customer Segmentation Using Machine Learning

## 📌 Project Overview

This project focuses on customer segmentation using unsupervised machine learning techniques. It analyzes customer purchasing behavior to identify groups of customers based on their shopping activity and spending patterns.

The project uses **RFM Analysis (Recency, Frequency, and Monetary Value)** along with clustering algorithms to segment customers.

## 🎯 Objectives

- Analyze customer purchasing behavior.
- Clean and preprocess the retail transaction dataset.
- Calculate RFM metrics for each customer.
- Apply clustering algorithms to identify customer segments.
- Visualize customer groups using dimensionality reduction techniques.
- Generate insights that can help businesses improve their marketing strategies.

## 📂 Project Structure

```text
Customer-Segmentation/
│
├── Dataset/
│   └── OnlineRetail.csv
│
├── Customer_Segmentation.ipynb
│
├── results/
│   ├── customer_segments.csv
│   ├── cluster_summary.csv
│   ├── pca_clusters.png
│   └── tsne_clusters.png
│
└── README.md
```

## 📊 Dataset

The project uses the **Online Retail dataset**, which contains retail transaction records.

The dataset includes information such as:

- Invoice number
- Product description
- Quantity purchased
- Invoice date
- Unit price
- Customer ID
- Country

The dataset is used to analyze purchasing patterns and calculate customer-level RFM metrics.

## 🛠️ Technologies Used

- Python
- Jupyter Notebook
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn

## ⚙️ Methodology

### 1. Data Cleaning and Preprocessing
- Identify and remove duplicate records.
- Handle missing customer IDs.
- Remove cancelled invoices.
- Filter invalid quantities and unit prices.
- Convert invoice dates into datetime format.

### 2. RFM Analysis

Three metrics are calculated for each customer:

- **Recency:** Number of days since the customer's most recent purchase.
- **Frequency:** Number of distinct invoices associated with the customer.
- **Monetary:** Total amount spent by the customer.

### 3. Feature Transformation and Scaling

Log transformation is applied to reduce skewness in the RFM features, followed by standardization using `StandardScaler`.

### 4. K-Means Clustering

K-Means is applied to group customers based on their RFM characteristics. The Elbow Method and Silhouette Score are used to evaluate different cluster counts.

### 5. DBSCAN Clustering

DBSCAN is used as an additional clustering method to identify customer groups and detect noise points.

### 6. Data Visualization

- RFM distribution plots
- Elbow Method plot
- Silhouette Score plot
- K-Means cluster visualization
- DBSCAN cluster visualization
- PCA visualization
- t-SNE visualization

### 7. Customer Segment Analysis

Cluster summaries are generated to compare customer counts, average recency, frequency, and monetary value.

## 📈 Results and Outputs

The notebook generates:

- Customer-level RFM metrics
- K-Means cluster assignments
- DBSCAN cluster assignments
- Cluster summary statistics
- PCA and t-SNE visualizations
- CSV files containing customer segmentation results

These outputs help explore customer behavior and identify groups with different purchasing patterns.

## 🚀 How to Run the Project

### Step 1: Clone the repository

```bash
git clone YOUR_REPOSITORY_URL
```

Replace `YOUR_REPOSITORY_URL` with your GitHub repository URL.

### Step 2: Open the project folder

```bash
cd Customer-Segmentation
```

### Step 3: Install the required libraries

```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
```

### Step 4: Add the dataset

Place `OnlineRetail.csv` inside the `Dataset` folder.

Ensure that the dataset path matches the path used in the notebook:

```python
df = pd.read_csv("Dataset/OnlineRetail.csv", encoding="latin1")
```

### Step 5: Run the notebook

Open `Customer_Segmentation.ipynb` in VS Code with the Jupyter extension installed, and execute the cells in order.

## 💡 Applications

Customer segmentation can help businesses:

- Develop targeted marketing campaigns.
- Understand customer purchasing behavior.
- Identify high-value customers.
- Improve customer retention strategies.
- Make data-driven marketing decisions.

## 🔮 Future Improvements

- Experiment with additional clustering algorithms.
- Improve cluster selection and evaluation.
- Develop an interactive customer segmentation dashboard.
- Create more detailed customer personas.
- Explore personalized marketing recommendations.
