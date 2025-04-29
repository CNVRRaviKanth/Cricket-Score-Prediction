# 🏏 Live Cricket Score Prediction using Machine Learning

This project aims to predict the final score of a T20 cricket innings using machine learning regression models based on real-time match features. It considers various match parameters like current run rate, wickets left, performance in the last 5 overs, and more to estimate the final score effectively.



## Problem Statement
The goal is to predict the final score of a T20 cricket innings using real-time match data. Accurate score prediction can help commentators, coaches and analysts take  decisions during a match.



## Dataset Description 
The dataset has been taken from kaggle. It contains the information of various parameters such as: 

1. powerPlay: Indicates if the current over is part of the powerplay (1 for yes, 0 for no). 

2. AverageScore: Historical average final score on the same ground/city. 

3. battingTeam: Name of the team currently batting. 

4. bowlingTeam: Name of the team currently bowling. E

5. city: The location where the match is being played. 

6. delivery_left: Number of deliveries (balls) remaining in the innings. 

7. score: Current total score of the batting team.

8. CurrentRunRate: Runs scored per over till the current point. Calculated as score / (total overs faced so far).

9. wicketsLeft: Number of wickets remaining .

10. Run_In_Last5: Number of runs scored in the last 5 overs.
 
11. Wickets_In_Last5: Number of wickets lost in the last 5 overs. 
  
12. Final_Score: The actual final score achieved by the batting team .
   
13. innings: Indicates whether it’s the 1st or 2nd innings. 

Where the shape of the dataset is (40,000,14). Initially there were 14 columns but 1 column is unnamed therefore it has been removed.

Out of these 13 parameters Final_Score is our target/independent variable which is a continuous value.




## Data Preprocessing
1. Outliers have been handled using IQR (Interquartile Range).

   Before outlier removal
   
   ![image](https://github.com/user-attachments/assets/5f4b3e20-d6c4-45ad-ae6f-b32d6045d263)

   After outlier removal

   ![image](https://github.com/user-attachments/assets/3886448c-48c6-4939-9912-cb8055861943)


3. Splitting the data for training and testing.

4. Feature encoding for features such as city, battingTeam and bowlingTeam is done using OneHotEncoder.

5. Scaling the data using MinMaxScaler to normalize the feature values to a [0,1] range.




## Models
As the data is a continous value therefore regression models have been employed to solve the problem. The following regression models are used:

1. Linear regression
2. Support Vector Regressor
3. Decision Tree Regressor
4. Random Forest Regressor
5. Gradient Boosting Regressor
6. XGBoost Regressor
7. AdaBoost Regressor
## Model Evaluation
To evaluate the model performance several evaluation metrics are applied such as:
1. r-square
2. mean square error
3. root mean square error
4. mean absolute error
## Results
1. Linear Regression:
r-square: 0.64, mse: 283.40, mae: 12.80, rmse: 16.83

2. Support Vector Regressor:
r-square: 0.60, mse: 314.49, mae: 13.27, rmse: 17.73

3. Decision Tree Regressor:
r-square: 0.80, mse: 159.46, mae: 4.98, rmse: 16.83

4. Random Forest Regressor:
r-square: 0.91, mse: 71.01, mae: 5.22, rmse: 8.42

5. Gradient Boosting Regressor:
r-square: 0.67, mse: 263.40, mae: 12.21, rmse: 16.22

6. XGBoost Regressor:
r-square: 0.84, mse: 125.23, mae: 8.19, rmse: 11.19

7. AdaBoost Regressor:
r-square: 0.57, mse: 343.56, mae: 14.40, rmse: 18.53




## Conclusion
By considering all parameter we can say that Random Forest Regressor is the top performer compared to all other models.
## Tech Stack
**Programming Language:** Python

**Libraries:** Numpy, Pandas, Matplotlib, Seaborn, Sikit-learn




## Installation

Command to install libraries

```bash
pip install ~ requirements.txt
```
    
## Authors

- [@Ravikanth Chivukula](https://github.com/CNVRRaviKanth)

