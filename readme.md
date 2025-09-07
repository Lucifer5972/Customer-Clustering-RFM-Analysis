# Online Retail Data Clustering

This project performs customer segmentation for an online retail business using **unsupervised machine learning**. By analyzing customer transaction data, we identify distinct customer groups based on their purchasing behavior. These segments enable more targeted marketing strategies and provide deeper insights into the customer base.

***

## Dataset

The dataset used is the **Online Retail II dataset** from the UCI Machine Learning Repository. It contains transaction data from a UK-based online retail store between **December 2009 and December 2011**.  

Key features include:

- **InvoiceNo**: Invoice number of each transaction  
- **StockCode**: Product code  
- **Description**: Product description  
- **Quantity**: Number of products purchased  
- **InvoiceDate**: Date and time of the transaction  
- **UnitPrice**: Price per unit  
- **CustomerID**: Unique identifier for each customer  
- **Country**: Customer’s country  

***

## Methodology

The project follows a standard machine learning pipeline:

### Data Cleaning and Preprocessing
- Handle missing values and correct data types  
- Remove irrelevant/anomalous entries (e.g., canceled orders, negative quantities, missing CustomerIDs)  

### Feature Engineering (RFM Model)
- **Recency**: Days since the last purchase  
- **Frequency**: Number of purchases  
- **Monetary Value**: Total spending  

### Customer Segmentation (K-Means)
- Features scaled with **StandardScaler**  
- Apply **K-Means clustering**  
- Use **Elbow Method** and **Silhouette Score** to determine the optimal number of clusters  

### Cluster Analysis
Each cluster is interpreted based on RFM scores:
- Average **Recency**  
- Average **Frequency**  
- Average **Monetary Value**  

***

## Expected Outcomes and Business Impact

The analysis identifies distinct customer segments:

- **High-Value Customers**: Loyal, frequent buyers who generate the most revenue. Prioritize for loyalty programs and exclusive offers.  
- **Recent but Low-Value Customers**: Newly acquired, low-spending customers. Engage with targeted campaigns to boost spending.  
- **At-Risk Customers**: Valuable historically but haven’t purchased recently. Re-engage with discounts or personalized offers.  
- **Churned Customers**: Low-value, inactive customers. Generally not cost-effective to win back.  

This segmentation supports **personalized marketing**, **customer retention**, and **improved targeting strategies**.  

***

## Visualizations

The project produces the following visualizations:  

- **Cluster Distribution**: Bar plot showing customer counts in each cluster  
- **Average Feature Values**: Line plot of average Recency, Frequency, and Monetary values per cluster for behavioral profiling  

***

## Usage

### Requirements
Install the required Python libraries:
```bash
pip install pandas matplotlib seaborn scikit-learn
```

### Running the Analysis
Open the Jupyter Notebook and execute the workflow:
```bash
jupyter notebook online-retail-data-clustering.ipynb
```

This will preprocess the data, perform clustering, and generate visualizations.
