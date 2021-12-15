
# Chess Data Science Project - Predicting the winner
Salem Eid.

## Abstract
The goal is to predict the outcome of a chess game under certain conditions. The data i worked with is downloaded from [Kaggles' datasets](https://www.kaggle.com/datasnaek/chess) which is originally an export from [lichess](lichess.com) API,the data is rich with information. Utulized some cleaning and preprocessing technics to get the best usable features.Next, Conducted some analysis and explored the data with visualization.Then, I utulized different classification model to get the best results. I summarized results and findings in slides presentation.  

## Design
The project was inspired by the idea of microsoft predicted all world cup 2014 football matches correctly, and also predicted the final winner, building on top of that , I would like to present a model that is good enough to predict chess matches or any other sports in the future. 


## Data
The dataset contained 20,000 datapoints/matches , with 15 features, 9 of which are categorical. The features are opening moves, opening moves steps, length of games, ratings of players, outcome of the matches, the victory status. All of these features are important in the analysis and modelling process. I ended up with 17 features after preprocessing , and left one feature (moves) out for another type modelling in the near future, which will involves some neural networking.


## Algorithms

*Feature Engineering*
1. Converting unix code time stamps to date-time format and recalcualte the difference between two points of time.
2. Converting categorical features to binary dummy variables.
3. Combining some features to better visualize during EDA

**Models**
  
Due the imporatnce of the project i have decided to apply most of the models that comes into mind and see how they perform, Started with Logistic regression as base model , Random Forest, XGBoost, SVM, K Nearest Neighbor. I would like to have variety between bagging, boosting and distances models and see how they perform.


**Model Evaluation and Selection**

The dataset of 20,000 rows was split into 80% test and 20% test , the cleaned dataset were dummified into 137 feaures up from 17 features. to resolve imbalance issue between targets i utulized imblance library using SMOTE to create virtual datapoints. Due to the variations in value between feautres , i have decided also to scale the dataset, this would be usful when handling distance alghorithims such as KNN.

My main score mertics was accuracy and f1 score , i have also decided to plot confusion matrix for each model to show the prediction rates clearly. The XGBoost model scored the best results. Later ran a GridSearchCV to improve the results,unfortunately, the initial prediction hyperparameters were better. 

**Best Result for XGBoost:** 137 features 
   - Accuracy 0.875
   - F1 0.871 weighted



## Tools
- Numpy and Pandas for data manipulation
- Scikit-learn/XGBoost for modeling
- Matplotlib and Seaborn for plotting


## Communication
A powerpoint presentation maybe found [here]  