# Predicting Future Price Movements using Neural Networks

This project aims to predict future price movements in a financial market using neural networks. The data used for this project includes the imbalance, the sign of the last 10 transactions, the normalized transaction volume, and the volumes at the best bid and ask. The target variable is the future increase in price (diff(h)) for a given horizon ($h$).

- Data Used : Bouygues Order Book of year 2011.

## Methodology

1. Data Preparation: The data is split into a training set and a test. The input matrix ($X$) and the target matrix ($Y$) are then normalized using the scalers obtained from the training set.
2. Model Building: A neural network with one hidden layer of size 32 and a TanH activation function is used to model the relationship between the input variables and the target variable.
3. Model Evaluation: The performance of the model is evaluated on the test set using R-squared metric.
4. Results Analysis: The results are analyzed to compare the performance of the neural network with that of linear regression.

## Results

1. The features used in the model were found to be good explanatory variables for price movements, and were able to capture the tangent-like shape of the curve.

2. The neural network outperforms linear regression on the training dataset, especially for larger values of $h$. On the test set, the neural network also performed better than linear regression, with a slight advantage for linear regression at $h=1$.

## Future Work

To improve the results, several possibilities were suggested, including finding a better architecture for the neural network, fine-tuning the parameters of the neural network, using stochastic gradient descent with a batch size, adding features from the order book, and performing feature engineering by creating new features.
