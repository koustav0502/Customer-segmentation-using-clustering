<!-- # Customer-segmentation-using-clustering
Customer segmentation using KMeans Clustering  
-->

# Mall Target Customer Segmentation

Technology, libraries and tools used in this project:  
Python, pandas, matplotlib, seaborn, KMeans Clustering

## 1. Introduction

The analysis aims to segment a mall’s customer base to better understand and target the most valuable shopping groups for its upcoming marketing campaign. By breaking down the market based on demographics (age and income) and behavioral metrics (mall shopping score), the analysis supports the marketing team in designing targeted strategies.

## 2. Problem Statement & Context

**Problem Statement:**  
Identify a suitable target customer segment most relevant for the upcoming marketing strategy. The goal is to create approachable and distinct groups that enable tailored marketing actions.

**Context:**  
Stakeholders require insights on:
- The most important shopping groups.
- An ideal number of clusters that best represent customer differences.
- Appropriate labeling of these clusters to assist with strategy formulation.

**Objective:**  
- Divide the overall market into well-defined subsets.
- Use demographic and behavioral metrics to create distinct segments.
- Enable targeted marketing strategies based on customer profiles.

## 3. Methodological Approach

A systematic approach has been adopted to cater to the requirements of the stakeholders. The approach comprises:

### 3.1 Exploratory Data Analysis (EDA)
- **Data Inspection and Preparation:**  
  The notebook starts by loading the dataset and examining its structure. This includes checking for missing values, outlier detection, and ensuring the variables (income, age, shopping score) are in the correct format for analysis.

- **Initial Visualizations:**  
  The use of histograms, scatter plots, and other visual tools helps understand the distribution and relationships between the key variables, setting the stage for clustering. A pairplot was used to check the preliminary relationships between labels.

### 3.2 KMeans Clustering
- **Algorithm Rationale:**  
  KMeans clustering was selected for its efficiency and interpretability. The algorithm clusters the data based on Euclidean distance, grouping similar customer profiles together.

- **Clustering Approaches Considered:**  
  Univariate, bivariate, and multivariate clustering were performed during the exploratory phase. It was determined that bivariate clustering—focusing on annual income and spending points—best captured the primary factors in deciding the top target cluster.

- **Determining the Ideal Number of Clusters:**  
  The elbow method was employed to assess the number of clusters that best represent the data. This ensures that the chosen number of clusters provides meaningful differentiation among customer groups.
  ![image](https://github.com/user-attachments/assets/1859f784-b8d0-48cf-a8da-9ec70daad2eb)


- **Cluster Labeling:**  
  After clustering, each group was analyzed and assigned a descriptive label. These labels reflect the main characteristics observed (e.g., high-income/high-shopping score, younger/moderate income) to make them easily interpretable for marketing purposes.

### 3.3 Summary Statistics and Visualization
- **Descriptive Statistics:**  
  Summary measures (mean, median, variance) for each cluster are computed. These statistics offer insights into the central tendencies and spread of the demographic and behavioral data in each group.

- **Visual Interpretation:**  
  Multiple visualizations are used to present the clustering results:
  - **Scatter Plots:** Display the distribution of customers across the clusters in two dimensions.
  - **Centroid Visualization:** Plots the centroids of clusters to highlight the average profile of each segment.
  - **Comparative Charts:** Additional visualizations (such as box plots, kdeplots for comparison and heatmaps for corelation) help compare key features across clusters.

## 4. Key Findings

Based on the notebook’s comprehensive analysis, several important insights were obtained:

1. **Distinct Customer Segments Identified:**  
   The KMeans algorithm successfully segregated the customer base into clearly distinct groups, with each cluster showing unique patterns in age, income, and shopping behavior. In the analysis it was identified that cluster 1 is the target cluster for the marketing team. This cluster highlights the customers with high annual income and high spending points in the mall. This is the ideal target cluster for the following reasons: <br>
   (1) High spending points in the mall implies that this segment of customers regularly spend more or want to spend more in the mall. The high annual income also highlights that the customers of this segment have the means to spend in the mall.<br>
   (2) It was observed that the the average age in this cluster is ~33yrs (32.69yrs) and ~54% (53.84%) of the customers in this segment are female. Hence this segment can be labelled as high income young population. This is an ideal segment because they often have disposable income, are early adopters of trends, and are influential within their social circles, potentially driving broader market adoption.
   ![image](https://github.com/user-attachments/assets/bb03cec0-69aa-4ecb-9800-2b11fd394f6c)

![image](https://github.com/user-attachments/assets/58b6c01d-374a-468e-8a83-6a03cf32d450)

![image](https://github.com/user-attachments/assets/df9612bc-d4fc-4bbc-8221-309ea309f101)


3. **Optimal Cluster Count:**  
   The analysis determined the ideal number of clusters, balancing the need for both interpretability and statistical robustness. The elbow method was used to find the appropriate number of clusters for KMeans Clustering.

4. **Profile of Clusters:**  
   - **High-Income, High-Shopping Score Segment:**  
     Customers in this segment (segment 1 in the scatterplot attached) are characterized by high disposable income and a strong propensity to shop frequently. This group is ideal for premium product offerings and exclusive promotions.
   - **Younger, Emerging Shoppers:**  
     This segment (segment 2 in the scatterplot attached) consists of younger customers with moderate income levels and rising shopping scores. They may be more receptive to trends, social media marketing, and budget-friendly campaigns.
   - **Mid-Income, Consistent Shoppers:**  
     Representing stable shopping behavior (segment 0 in the scatterplot attached), this group can benefit from loyalty programs and consistent engagement strategies.
   - **Additional Niche Segments:**  
     Depending on the dataset, other nuanced clusters are present, each offering a unique combination of demographic and behavioral traits that could be leveraged for more targeted marketing initiatives. <br><br>An interesting segment to note is cluster 4. This segment comprises of customers who have high annual income and low spending points in the mall, the average age of this segment being 42yrs. The low spending characteristics of this segment maybe an indicator that the customers of this segment are purchacing only during sales or buying only big ticket items (for example, TVs, Playstations etc) once in a while from the mall. 

5. **Actionable Marketing Insights:**  
   The segmentation provides a roadmap for targeted marketing. Based on the target segment that was determined in the analysis, the marketing team can:
   - Tailor exclusive offers and high-end products for the high-income customers.
   - Engage younger consumers with digital-first, trend-driven campaigns.
   - Implement loyalty and retention strategies for consistently active shoppers.

## 5. Conclusions and Recommendations

- **Segmentation Value:**  
  By identifying distinct customer clusters, the analysis empowers the marketing team to design data-driven strategies that align with the specific needs and behaviors of each segment.

- **Next Steps:**  
  - **Model Refinement:** Regularly update the clustering model as new customer data becomes available to maintain its relevance.
  - **Deepen the Analysis:** Consider integrating additional variables (like geographic or behavioral data beyond the shopping score) to further refine customer segments.
  - **Strategic Implementation:** Develop tailored marketing campaigns based on the detailed cluster profiles to optimize marketing spend and improve customer engagement.

- **Strategic Impact:**  
  This segmentation not only provides a clearer picture of the mall’s customer base but also offers actionable insights that can drive targeted marketing, enhance customer satisfaction, and ultimately boost sales.
