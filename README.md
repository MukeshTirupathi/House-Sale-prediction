# House-Sale-prediction
Data Loading and Preprocessing  We consider the same notebook used in the labs, containing house sale prices for King County, which includes Seattle. It includes homes sold between May 2014 and May 2015.  https://www.kaggle.com/harlfoxem/housesalesprediction  For each house we know 18 house features (e.g., number of bedrooms, number of bathrooms, etc.) plus its price, that is what we would like to predict.

Neural Networks
Let's learn the best neural network with 1 hidden layer and between 1 and 9 hidden nodes, choosing the best number of hidden nodes with cross-validation.

k-Nearest Neighbours
You will now explore the k-Nearest Neighbours (kNN) method for regression. In order to do this, you will need to use load the scikit-learn package *neighbors.KNeighborsRegressor* 

k-Nearest Neighbours for regression works as follows: the predicted value $h(\textbf{x})$ for an instance $\textbf{x}$ is obtained by first finding the $\ell$ instances *in the training set* that are clostest to $\textbf{x}$; the predicted value $h(\textbf{x})$ is then the mean of the targets of such $\ell$ instances. $\ell$ is a parameter of the method. The targets of the $\ell$ instances used for prediction can be weighted by the (inverse of) their distance to $\textbf{x}$.

load the package for kNN regression, learn the model with default parameters using the training and validation scaled data, and print the error (1-R^2) on the data used to train the model and on the test data.

Clustering and "Local" Linear Models
  
  You are now going to explore the use of clustering to identify groups of *similar* instances, and then learning models that are specific to each group.

Once you have clustered the data, and then learned a model for each cluster, the prediction for a new instance is obtained by using the model of the cluster that is the closest to the instance, where the distance of a cluster to the instance is defined as the distance of the *center* of the cluster to the instance.
 
*compute* the error (1 - R^2) on the data not used to learn the models.
For each instance not used to learn the model, the prediction is done by:
- finding the cluster C whose center is the closest to the instance
- use the model learned for cluster C to make the prediction
