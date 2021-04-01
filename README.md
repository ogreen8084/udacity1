<h1>Problem Statement</h1>
This dataset contains banking marketing results.  We seek to predict customers that can be successfully marketed to based 
off of past information in the dataset. 

<h2>Best Model</h2>
The best model was a Voting Ensemble Model. 
<p align="center">
  <img src="https://github.com/ogreen8084/udacity1/blob/main/Screen%20Shot%202021-04-01%20at%201.14.48%20PM.png" width="350" title="Pipeline">
</p>


<h3>Sklearn-Pipeline</h3>
The sci-kit learn model was a logistic regression model. Regularization was used to optimize the model by penalizing errors. 
The bandit policy with a slack amount stopped the iteration if an AUC less than the best performer minus the slack amount of 0.1. 


<h3>AutoML</h3>
The AutoML model generated about 50 different models automatically within the 30 minute experiment window. 
It utilized many XGBoost and Random Forest models with different scaling methods. Ultimately a voting ensemble model fit the data best. 
The model utilized 'AUC_weighted' as the primary evaluation method to balance between high precision and recall. 

<h3>Comparison</h3>
With manually setting hyperparameters for the sci-kit learn model I achieved an accuracy of about 91%. By utilizing AutoML and letting it
pick the best combination of models and standardizations I achieved an accuracy of 94.95%. AutoML performed better because it utilized more powerful
models and was not restricted by model choice or one standardization method. 

<h3>Future Work</h3>
In the future to improve this model we could address the issue with class balancing. 



