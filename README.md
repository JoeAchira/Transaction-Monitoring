# Transaction-Monitoring Outlier Detection Model

### Project Overview
This project builds an unsupervised anomaly detection model designed to identify unusual or suspicious banking transactions for **Transaction Monitoring (TM)** use cases.  
Unlike supervised fraud datasets, TM monitoring often lacks labelled data, making **anomaly detection** essential.

This project simulates a real-world financial crime workflow by profiling customer activity, identifying behavioural outliers, and flagging unusual transactions.

---

### Objectives
- Detect anomalous transactions in an unlabeled dataset  
- Compare different outlier detection algorithms  
- Reduce false positives while preserving true anomaly detection  
- Provide actionable insights for AML/fraud investigation teams  

---

### Methods & Tools
- **Python, scikit-learn, pandas, NumPy, seaborn**
- **Algorithms:**
  - Isolation Forest  
  - DBSCAN (density-based clustering)  
  - Z-Score and statistical anomaly rules  

- **Techniques:**
  - Feature engineering (velocity, value ratios, transaction frequency)  
  - Behaviour profiling at customer and transaction level  
  - Dimensionality reduction for visualization (PCA, t-SNE)

---

### Model Development Steps
1. **Data Preparation & EDA**  
   Explored transaction patterns, distributions, and correlations, identifying behavioural clusters.

2. **Feature Engineering**  
   Created AML-relevant features such as:  
   - Transaction velocity  
   - Daily/weekly spend consistency  
   - Merchant category frequency  
   - Transaction deviation from customer norms  

3. **Anomaly Detection Models**  
   - Isolation Forest as the baseline TM algorithm  
   - DBSCAN for clustering rare/irregular behaviour  
   - Rule-based statistical thresholds as comparison  

4. **Evaluation & SME Review Simulation**  
   Since the dataset is unlabeled, model validation done through:  
   - Cluster separation quality  
   - Percentage of anomalies  
   - Manual investigation of flagged samples  

5. **Visualisation**  
   Mapped clusters and anomalies using PCA to show separation.
---

   <!-- ### Visuals
<!--![Anomaly Clusters](images/anomaly_clusters.png)  
![PCA Projection](images/pca_projection.png) 
  -->


### Results
- Isolation Forest flagged approximately **2.3%** of transactions as anomalies.  
- DBSCAN identified several dense behaviour clusters plus sparse anomalous points.  
- Feature importance indicated transaction value deviation and velocity were key anomaly drivers.

These results demonstrate realistic TM detection patterns often seen in AML systems.

---

### Learning Outcomes
- Applied **unsupervised learning** techniques to real banking AML scenarios  
- Improved understanding of behaviour-based anomaly detection  
- Strengthened skills in feature engineering for financial crime analytics  

---

### Future Improvements
- Add autoencoder-based anomaly detection  
- Build a small Streamlit dashboard for analysts to review flagged transactions  
- Integrate customer segmentation to reduce false positives  
