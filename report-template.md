# Report: Predict Bike Sharing Demand with AutoGluon Solution
#### Sarthak Gupta

## Initial Training
### What did you realize when you tried to submit your predictions? What changes were needed to the output of the predictor to submit your results?
Intitially when I tried submitting the predictions I realised that the negative outputs were not allowed. Thus I changed all the negative outputs to 0 so I could be accepted by Kaggle.

### What was the top ranked model that performed?
WeightedEnsemble_L2 was the top ranked model every time.

## Exploratory data analysis and feature creation
### What did the exploratory analysis find and how did you add additional features?
Exploratory analysis found the patterns in the dataset, as it plotted the histogram for the relation between output and the input label.
Additional Features were found in date time as we could see there was no major contribution by the datetime but after EDA we found strong correlation between month and year and count .

### How much better did your model perform after adding additional features and why do you think that is?
It performed bad afterwards as it's performance decreased by 26.3% than the original model.
I thought that day didnt play any role in the model and it was not needed but later I found that it had a small contribution and might have improved the score a bit.Also after better EDA, we might be able to find a better new feature which might have a good impact on the model.

## Hyper parameter tuning
### How much better did your model preform after trying different hyper parameters?
It performed better than model after adding parameters but still worse than original model.
It's Performance increased by 0.423% than model after adding hyperparameters but it is 26% worse than original model.

### If you were given more time with this dataset, where do you think you would spend more time?
If I was given more time, I would I have spent more time in EDA to understand the dataset and its's correlations and explore more hyperparameters that might have helped in increasing the accuracy of the model.

### Create a table with the models you ran, the hyperparameters modified, and the kaggle score.
|    model   |num_trials|num_bag_folds006|num_stack_levels| score |
|------------|----------|----------------|----------------|-------|
|   initial  |   1024   |        0       |        0       |1.79341|
|add_features|   1024   |        0       |        0       |1.32137|
|     hpo    |   2048   |        6       |        1       |1.32696|

### Create a line plot showing the top model score for the three (or more) training runs during the project.

TODO: Replace the image below with your own.

![model_train_score.png](img/model_train_score.png)

### Create a line plot showing the top kaggle score for the three (or more) prediction submissions during the project.

TODO: Replace the image below with your own.

![model_test_score.png](img/model_test_score.png)

## Summary
Original model was the most accurate one as it didnt change the parameters while making prediction without date and time and thus performed much better. 
The additional parameter required more time dedicated towards eda for getting better results.
HPO was helped the model by a little bit because the increased optimisation made it easier for the model to improve the accuracy within the time limit of 10 minutes.
 