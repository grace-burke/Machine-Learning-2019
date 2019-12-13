# Boston Housing Machine Learning and Statistics Assignment 2019 #

The main body of the project can be found in the BostonDataset.ipynb notebook.

## To Run Notebook ##
- The notebook can be run sequentially from start to finish using the run button at the top of the page.
- To adjust the neural network, ammend the values in the parameter cell as required.
- When re-running neural network the notebook can be re-run from the "Neural Network" heading down only in order to save time and processing power.
- The error values of each model for the parameters specified will be given at the end of the notebook.

## Description of Dataset ##

The first section of the notebook gives a description of the Boston Housing Dataset. <br/>
The dataset is imported from the sklearn library and a description of each parameter is given. The data is then manipulated into a dataframe including the input variables and the target variable. The dataframe is checked for null or missing values and then descriptive statistics for each parameter are given.<br/>
Following this the relationships between the parameters are examined. Pairplots are used to plot each parameter against each other, and show the frequency distribution of each parameter. A heatmap shows the correlation coefficient between the parameters. A larger histogram show the frequency distribution of the target variable only, MEDV.<br/>

## Inferential Statistics Between Properties Bordering the Charles River and Those Not ##
The second section of the notebook calculates inferential statistics between MEDV values where CHAS = 1 and MEDV values where CHAS does not = 1. <br/>
MEDV and CHAS are first plotted against each other. MEDV is then plotted, categorised by whether CHAS = 1 or CHAS = 0. Box plots are shown for MEDV of properties bordering the river and properties not bordering the river, showing medians that are close but not equal.<br/>
An independent t test is used to test the null hypothesis that the means of the datasets from which these samples were taken are equal. The p value produced is  0.0074%, below the threshold of 5%. This suggests that we can reject the null hypothesis and assume that the mean value of properties bordering the river is not equal to the mean value of properties not bordering the river.<br/> 

## Neural Network ##

The final section of the notebook deals with the building and testing a neural network to predict MEDV using the other variables.<br/>
The parameters required for the model are set out at the beginning of this section. The Keras model is then built using a selection of the input variables. The data is split into training and testing segments. The model is trained on the training dataset for a specified number of epochs and batch size. The model then makes predictions for the outputs of the testing dataset. These predictions are evaluated, giving mean absolute error and mean absolute percentage error. The predicted values are graphed against the actual values.<br/>
Following this another model is created using the same inputs afer they are scaled. The data is scaled so that all variables have a mean of 0, deviation of 1 and Gaussian distribution.<br/>
A final model is created in which the data is whitened. Whitening data removes interdependencies between variables, reducing the dimension of the data. <br/>
The results of one run of the notebook are as follows:<br/>
* Original mean absolute error value = 4.55<br/>
* Original mean absolute percentage error value =  20.95 %<br/>
* Scaled mean absolute error value =  2.64<br/>
* Scaled mean absolute percentage error value =  13.59 %<br/>
* Whitened mean absolute error value =  7.41<br/>
* Whitened mean absolute percentage error value =  40.38 %<br/>
<br/>It is clear that the scaled data gives the best model.