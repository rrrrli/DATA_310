## Project 2 ##

### Using the R script provided, split and sample your DHS persons data and evaluate the AUC - ROC values you produce. Which "top_model" performed the best (had the largest AUC)? ###
Below is the chart containing the information of the best 15 models: 

![.](auc_chart.png)

According to AUC graphs, slice 1-15 performed relatively similarly and have essentially identical AUC graphs. Below is a few randomly selected examples.

Slice 7:
![.](lr_auc_7.png)  
Slice 10:
![.](lr_auc_11.png) 
Slice 15:
![.](17.png) 

While slice 1-15 look familiar, models after 15 start to perform worse. Below is slice 19:
![.](15.png) 
And when I reached slice 26, it is obvious that this is not an accurate model, especially as shown in graph 1: 
![.](26.png) 

### Are you able to use the feature selection penalty to tune your hyperparameter and remove any potentially irrelevant predictors? 

I think so, as the penalty values in models from 1-15 indeed provided larger AUC compared to the ones in the subsequent models. However, since model 1-15 differed very slightly in their AUC, it is hard to say which model is the best. 

### Provide justification for your selected penalty value? ###

I chose model 10 because it has the largest mean value (0.602). Among the four models (model 10, 11, 12, 13) that have a mean value of 0.602, model 10 has the smallest penalty value (0.00174). 

### How effective is your penalized logistic regression model at predicting each of the five wealth outcomes. ###
(ROC plots have been shown above) 

Here is the five wealth outcomes predicted by model 10:
![.](lr_auc_11.png) 

The model seems to be able to differentiate 1, 4, and 5 from each other and from 2 and 3, but the model could not differentiate between 2 and 3 very well because these two graphs looked very similar. This may be because 2 and 3 represent the middle-income families with relatively similar wealth status and therefore the model couldn't distinguish between them. Overall, 1-4 did not perform well because the area under the curve is not large for all of these graphs. This may be that since Tajikstan is a authoritarian dictatorship and a low-income economy, the majority of the people are low income (even the "middle class") compared to developing and developed nations. Therefore it was hard for the model to distinguish among wealth group 1-4. In comparison, the model distinguished the fifth wealth group, which represents the wealthiest class in the nation. 
