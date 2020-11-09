#### Exercise 1

**Introduction**
The goal of this exercise is to evaluate the familiarity with pandas in order to discover how confident is the subject applying data transformations and manipulations.

You have to build a transformation pipeline that will look as follows:

**read features -> read normative -> join normative with features -> add a gender name based in in the scores of the normative -> calculate the standard deviation of the features into a new column -> save results ** 

The duration of the exercise is 1.5h not being necessary to complete the exercise in this time but to explain the approach and the ideas to the reviewer in a pair programming exercise.

The approach must be object oriented and full tested using the unittest framework or any other testing framework on which you feel comfortable.

#### Setup environment
Clone the code, Source a python 3.6+ environment and create a feature branch in order to PR this exercise later.
Install the requirements in requirements.txt using pip.

#### Tasks

Design and implement an abstract class called BaseTask based in the fact that we are going to execute tasks sequentially and the output of one will be the intput of the next one. 

#### Join Task

**Step1**

In the data directory you'll find two CSV files: features.csv and normative.csv.
Create a data access class that reads these CSVs via pandas and retrieves DataFrames per each file.

**Step2**

Create a Join class called JoinTask which responsability is to merge the normative and the features DataFrames

#### Add descriptions


The JoinTask have retrieved a DataFrame on which one of the columns is gender. This columns is based in probas on which if is > 0.5 is a male and if is <=0.5 is a female.
Create a LabelTask class that will build a column called gender_name wich values will be male or female based in previous criteria.

#### Calculate standard deviation

Based in the previous results build a new task class, StdTask, that will create a new column  in th DataFrame called features_std. This column must contain the standard deviation of the features feature_0 to feature_15.

#### Save results

**Step1**

Modify the data access class to be capable to persist a dataframe into a CSV 

**Step2**

Create a PersistTask that wil receive the resultant dataframe  and will save it using the data access class.

#### Run script

Build an entry script that will run these tasks sequentially and run this script.

 

 


