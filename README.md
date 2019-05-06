# MAT-400-Final-Project

For our final project, we decided to look at NBA shot logs and to predict if a shot will be made or not based on other variables such as distance from the closest defender, total time in the game, and distance from net, among others.d
	The first step was to clean the data by removing unnecessary variables and making the data easier to read. For example, player identification was removed because we wanted to keep the prediction general. The game clock was also changed from HH:MM:SS to total time in seconds. This made it easier to read and work with.
	After cleaning the data, some initial exploratory visualization was performed to predict the most important variables. This led to the prediction that CLOSE_DEF_DIST and SHOT_DIST would be the most important variables.
	Next, the data was split into training and testing sets, but because it had so many rows (more than 120,000), we split the training set even smaller so we could test the code. All final results were found using the full set.
	For this classification problem, the models that were used were elastic net, tree, and svm. All the misclassification rates were around 39 - 40%.

We weren’t able to get a very low misclassification rate with the data set we were using at, so we decided to try looking at one specific player, enabling us to use more predictors. We found a dataset with 25697 of Kobe Bryant’s shots, including where he was on the court, and the type of shot he made, as well as the same predictors from the first dataset. 
The first thing we did was clean the dataset. Some of the predictors were irrelevant like the date, and the game id and other data was the same as other columns or all zero, so we removed these columns.
With the cleaned data, we fit multiple models, including GLM, logistic regression, LDA, classification trees, and xgboost. We used 5-fold cross validation where applicable. All the misclassification rates were between 38% and 40%, with logistic regression performing the best.

In the future it would be interesting to try predicting other variables, like shot location or shot type using their appropriate predictors.



We split the datasets into two parts. The first dataset analysis is in Basketball.Rmd and the one that focuses on Kobe Bryant is in KobeBryant.Rmd