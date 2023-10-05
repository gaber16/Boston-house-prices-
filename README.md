# Boston-house-prices-
## we are going to try using a simple sequential model to predict the Boston house prices
## Approach for the dataset:
- Read the data into a Data frame then set the columns right as it has only one column with all the data mixed together
- Get some info from the describe method which showed us that there are outliers
- Use boxplots to check the severity of the outliers, in our case the outliers are not that harmful as they are not that far away from our data which means they are actual data and not noise.
- Using the heatmap we dropped the RAD column as it was correlated with TAX and we would not just benefit from it while training
- We selected 6 columns that are moderately correlated with the MEDV column which is our Y and got the data for these columns in a separate Data frame to try training the model on those 6 columns and then all the columns
- Some data normalization is needed as the X was normalized using MinMax to help with the skewed data and the z-score was applied to the Y to get better results in the training process
- Model construction is pretty simple: 3 hidden layers (2 dense and 1 dropout), 1 output layer of linear activation
- In the model learning rate decay was applied to get a head start, and dropout as we have such a small dataset so we don’t want to over fit.
- We can see that the model trained on all of our dimensions performed so much better than that of only 6 dimensions.
- Finally, we can see from the plots at the end the training loss and validation loss of both models.
## kaggle dataset link: https://www.kaggle.com/datasets/vikrishnan/boston-house-prices/data
