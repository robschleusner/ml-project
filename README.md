## Credit Card Fraud Detection

### Introduction / Background:
In the information age, sensitive user data such as payment information has become increasingly digitized. This has created vulnerabilities in data safety. In this project, we intend to implement an automated and intelligent detection system for fraudulent transactions. 

### Problem Definition:
The evolution of physical cash to stored information sacrifices security for speed. According to a Federal Trade Commission 2021 report, 88,354 credit card fraud instances resulted in more than $180 million in losses. By using machine learning to detect fraud, we aim to minimize these financial burdens.

### Data Process & Methods:
Our dataset is simulated consumer information by the MIT Licensed Synthetic Credit Card Transaction generator. It contains 555718 transactions, 22 features, and a single label, fraud vs. normal transactions. To reduce dimensionality of our data, we intend to perform a PCA. Missing values will be filled with the mean. We will scale our features to unit variance using StandardScaler() from sklearn. 

Unsupervised Learning: 

K-Means Clustering:

	Once we have scraped our data, we will cluster based on the transaction amounts; with k = 3, high, medium, and low transaction amounts (Dornadula et al., 2019). We will also run the algorithm with simply 2 clusters and try to compare between the two values of K to see which one performs better, implementing the elbow method. 
  
Local Outlier Factoring (LOF)

	This algorithm is more adept at identifying outlier data points by calculating their density deviation (scikit, 2022). For our purposes, we can consider outliers as cases of fraud under the presumption that card transactions that dramatically deviate from clusters are less likely to be normal. 
  
Supervised Learning: Artificial Neural Networks (ANN)

	We will construct an ANN model to view related patterns between fraudulent credit card transactions, generating a predicted value range of transaction amounts for cases of fraud as a basis for detection. An ANN model is well suited for detecting complex transactional patterns due to its backpropagation algorithm (Mittal et al., 2019).

### Potential Results + Discussion:
We anticipate poor results of the unsupervised, K-Means model. Within current literature, K-Means results in high precision metrics, low negative predictive values, and high specificity values. We infer the K-Mean model will skew towards negative predictions, with most labels resulting as not fraud. From an internal performance metric, the silhouette coefficient, ignoring the ground truth labels, we expect to observe a score closer to 0.  

The LOF model is expected to perform with better accuracy. Current practices show that an LOF algorithm has high positive precision values and negative predictive values. Previous results demonstrated excellent recall with high sensitivity and specificity. Overall, this should be a more effective model for a dataset with a large amount of expected outliers.

Considering the ANN model, we predict a positive performance given our dataset’s size and layered coefficient components. Analyzing this approach will need precision, recall, and accuracy metrics, displayed within a coefficient matrix. We anticipate these metrics to approach 1 after analyzing Abel and Augustin’s model implementing a logistic regression and ANN approach (Abel & Augustin, 2019).

### References:
Abdel, & Augustin, Peter. (2019). Credit Card Fraud Detection Using ANN. 

Dornadula, V. N., & Geetha, S. (2019). Credit card fraud detection using machine learning algorithms. Procedia computer science, 165, 631-641.

Federal Trade Commission. (2022, February 25). Consumer Sentinel Network Data Book 2021. Federal Trade Commission. Retrieved October 4, 2022, from https://www.ftc.gov/reports/consumer-sentinel-network-data-book-2021

Mittal, S., & Tyagi, S. (2019, January). Performance evaluation of machine learning algorithms for credit card fraud detection. In 2019 9th International Conference on Cloud Computing, Data Science & Engineering (Confluence) (pp. 320-324). IEEE. 
Outlier detection with local outlier factor (LOF). scikit. (n.d.). Retrieved October 6, 2022, from https://scikit-learn.org/stable/auto_examples/neighbors/plot_lof_outlier_detection.html#:~:text=The%20Local%20Outlier%20Factor%20(LOF,lower%20density%20than%20their%20neighbors.

Vaishali, Vaishali. (2014). Fraud Detection in Credit Card by Clustering Approach. International Journal of Computer Applications. 98. 29-32. 10.5120/17164-7225.

### Proposed Timeline:

Our Gantt chart can be found [here](https://docs.google.com/spreadsheets/d/1r6GNta5fQibvYkbXJCRdFy63RRoSbyJd/edit?usp=sharing&ouid=117811764220714896416&rtpof=true&sd=true)

### Contribution Table:

| Team Member | Contribution |
|---|---:|
|Samantha Burger|   |
|Olivia Lawson |   |
|Munim Riddhi|   |
|Rob Schleusner |   |
|Samuel Wysocki|   |
