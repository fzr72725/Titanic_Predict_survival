# Titanic Passenger Survival Prediction
The sinking of the RMS Titanic is one of the most infamous shipwrecks in history.
Only 722 out of 2224 passengers and crew survived.

## Motivation
One of the reasons that the shipwreck led to such loss of life was that there were not enough lifeboats for the passengers and crew. Although there was some element of luck involved in surviving the sinking, some groups of people were more likely to survive than others, such as women, children, and the upper-class.

## Data Set
### General Description
- Training Set:
891 rows, 12 columns

- Testing Set:
418 rows, 11 columns

- NaN values: Yes

### Data Dictionary

Variable	Definition	Key
survival	Survival	0 = No, 1 = Yes
pclass	Ticket class	1 = 1st, 2 = 2nd, 3 = 3rd
sex	Sex
Age	Age in years
sibsp	siblings count / spouses aboard the Titanic
parch	parents count / children aboard the Titanic
ticket	Ticket number
fare	Passenger fare
cabin	Cabin number
embarked	Port of Embarkation	C = Cherbourg, Q = Queenstown, S = Southampton

## Process
### Pre-Processing
- Remove NaN rows in training set.
- Numerize categorical columns
- Fill NaN values in testing set based on data distribution

### Model Development
- Used tree-based models
- Random Forest, Gradient Boosting, AdaBoost
- GridSearch to tune hyperparameters
- VotingClassifier for the final call

### Result
- 0.799 accuracy, ranked 20% in the Titanic Competition
