# deep_learning_challenge
Module 21 homework

Questions and Answers:
1.  Overview of the analysis: Explain the purpose of this analysis. Analysis was to build an neural network model with various attempts to improve the accuracy and loss rate of the model. The subject matter was to use the features in the provided dataset to create a binary classifier that can predict whether applicants will be successful if funded by Alphabet Soup.

Data Preprocessing

2.  What variable(s) are the target(s) for your model? The target variable is the 'IS_SUCCESSFUL' column from application_df

3.  What variable(s) are the features for your model? The feature variables are every other column from application_df --> this was defined by dropping the 'IS_SUCCESSFUL' column from the original dataframe.

4. What variable(s) should be removed from the input data because they are neither targets nor features? Both 'EIN' and 'NAME' columns were dropped/removed, because they were neither targets nor features for the dataset.
   
Compiling, Training, and Evaluating the Model

5. How many neurons, layers, and activation functions did you select for your neural network model, and why?
a.  Starter model reported 0.7322 accuracy and 0.5607 loss. Model had 2 layers with 8 and 5 units each and used 'relu' for activation.
b.  Attempt #1 reported 0.7319 accuracy and 0.5718 loss. Model had 3 layers with 80 units each and used 'relu' for activation.
c.  Attempt #2 reported 0.7310 accuracy and 0.5668 loss. Model had 3 layers with 120 units each and used 'rbf' for activation.
d.  Attempt #3 reported 0.7315 accuracy and 0.5770 loss. Model X factors were regrouped to reduce the number of unique application and class types. Model had 4 layers with 120 units each and used 'rbf' for activation.
e.  Attempt #4 was supervised machine learning that used XGBClassifier and reported 0.7301 accuracy. The f1-score was 0.70 for the 0 group and 0.76 for the 1 group. Precision scores were 0.73 for both groups and recall scores were 0.67 and 0.78 respectively.

6. Were you able to achieve the target model performance? No, i was not able to achieve an accuracy score of higher than 73% on any of the attempts.
   
7. What steps did you take in your attempts to increase model performance? - see Answer #5

8. Summary: Summarize the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and then explain your recommendation.
a.  Including the starter model, all attempts reported accuracy within a tight range of 0.7310 to 0.7322 and loss rates ranged from 0.5607 to 0.5770. It did not appear that increasing the number of hidden layer or number of neurons increased the accuracy of the model. Furthermore, it appeared that the 'relu' activation was nominally a better fit than the rbf activation for the model. Attempt #4 showed that the accuracy between group 0 and group 1 varied by 0.06, and group 1 reported a recall score 0.12 higher than group 0. This suggests that the data itself is the key to achieving a higher accuracy score. Plotting and understanding the relationship between the parts of the data set with the largest number of data points could perhaps yield a model design that produces an accuracy score in excess of 73%.

References: 
1.  Class materials
2.  Github used as a reference to check my work: https://github.com/JLeigh101/deep-learning-challenge/blob/main/AlphabetSoupCharity.ipynb, accessed 10/29/23
