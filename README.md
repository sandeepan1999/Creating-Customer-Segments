# Creating Customer Segments: Project Overview
* Created a tool that separates customers into segments to distinguish them as restaurants or grocery stores,etc.
* Analyzed the relevance of the features for understanding the purchasing behaviours of the customers.
* Transformed features using Principal Component Analysis(PCA).
* Clustered the data using Gaussian Mixture model.

## Code and Resources used
**Python Version:** 3.7

**Packages:** Numpy, Pandas, Matplotlib, Seaborn

## Data
The dataset contains the following features:
* Fresh
* Milk
* Grocery
* Frozen
* Detergents_Paper
* Delicassen

## EDA
I looked at the distributions of the data. Below are a few highlights.

![alt text](https://github.com/sandeepan1999/Creating-Customer-Segments/blob/master/scatter_matrix.png "Scatter-matrix")

![alt text](https://github.com/sandeepan1999/Creating-Customer-Segments/blob/master/correlation%20matrix.png "Correlation Matrix")

## Data Preprocessing
First, I scaled the features using the natural logarithm.

Detected the Outliers using InterQuartile range method and removed the common outliers from the dataframe.

Applied PCA by fitting the good data with the same number of dimensions as features. I also reduced the dimensions by bpplying PCA by fitting the good data with only two dimensions.

## Model Building
The chosen algorithm is **Gaussian Mixture model** because data is not splitted in clear and different clusters, so we do not know how many clusters there are.

Calculated the mean silhouette coefficient for the number of clusters chosen.

## Model Performance
The model with number of clusters = 2, outperformed the other models.
| **Number of clusters:** | **Silhouette score:** |
| :-----------: |:-------------:|
| 2     | 0.42232468264593864  | 
| 3     | 0.3852447193714692   |   
| 4     |  0.3458671375116742  |
| 5     |  0.3314244539434991  |
| 6     |  0.29789067076045    |

## Model Visualisation

![alt text](https://github.com/sandeepan1999/Creating-Customer-Segments/blob/master/clustering.png "Clusters")

