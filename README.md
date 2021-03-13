# PROG_MODL_BIG_DATA
Programming Models for Big Data


## Learning Objectives: 
The goal of this course is to introduce the Spark programming model for processing Big Data for discovering patterns and designing predictive models. Several datasets will be made available for labs and mini projects. A cluster computing platform will be made available through ICDS-ACI.  You will learn to use a python-version of Spark (pyspark), and a machine learning library on Spark (MLlib) to develop scalable data analytic solutions and assess their performance. The learning objectives of the course are the following:

* Gain hands-on experience about programming in Spark that are designed to be scalable for handling Big Data.
* Be able to design and implement scalable machine learning algorithms  using pySpark in a cluster environment.
* Be able to choose Spark program design options and choose Spark configurations in a cluster and assess their performance toward the goal of enhancing their scalability.

## [Lab 2: A MapReduce Implementation of Basic WordCount](https://github.com/ljiwoo59/PROG_MODL_BIG_DATA/blob/main/Lab2_wordcount.html)
Basic word count from text file using MapReduce

```python
word_RDD = text_RDD.flatMap(lambda line: line.strip().split(" "))
word_pair_RDD = word_RDD.map(lambda word: (word, 1))
word_count_RDD = word_pair_RDD.reduceByKey(lambda a, b: a + b, 1)
word_count_RDD.collect()
```

## [Lab 3: Filtering and Top Hashtags/Twitters in Tweets](https://github.com/ljiwoo59/PROG_MODL_BIG_DATA/blob/main/Lab3_hashtag.html)
Find top hashtags and top Twitters mentioned in a set of tweets
* Implement filtering of a data stream in Spark
* Reverse a key-value pair
* Sort an RDD by keys

## [Lab 4: Comparing Alternative Solutions Using Spark-submit (local mode)](https://github.com/ljiwoo59/PROG_MODL_BIG_DATA/blob/main/Lab4_hashtag.html)
Implement two alternative ways of finding counts of hashtags and counts of Twitter users mentioned in a set of tweets
* Evaluate the time required using spark-submit (local mode)

## [Lab 7: Decision Tree Learning and Visualization](https://github.com/ljiwoo59/PROG_MODL_BIG_DATA/blob/main/Lab7_DT_plot.html)
* Understand the function of the different steps/stages involved in Spark ML pipeline
* Construct a decision tree using Spark ML machine learning pipeline
* Generate a visualization of Decision Trees
* Compare and evaluate Decision Tree models created using different hyper-parameters (e.g., maximum tree depth).

## [Lab 8: CV Decision Tree Learning and Hyperparameters Tuning Using Cross Validation](https://github.com/ljiwoo59/PROG_MODL_BIG_DATA/blob/main/Lab8_DT_tuning_CV_5.html)
* Understand the goals of hyperpermater tuning include (1) reducing overfitting risk, and (2) high f1 scores for data not used in training.
* Implement hyperparameter tuning in PySpark using ML pipeline
* Evaluate the results of hyperparameter tuning for reducing overfitting risk
* Choose hyperparameters of Decision Trees for reducing overfitting risk
* Understand the value of evaluating and tuning hyperparameters with cross validation and Parameter Grid Search
* Understand the use of parallelism in a cluster.

#### Two methods of hyperparameter tuning
* _CrossValidator_ splits the data into multiple (k) folds (of training, test split) so that we have a more reliable evaluation result
* _ParamGridBuilder_ specifies the set of hyperparameter combinations to use to construct ML model

## [MiniProject 1: DFSQL](https://github.com/ljiwoo59/PROG_MODL_BIG_DATA/blob/main/MiniProject1_DFSQL-Lab-2-1.html)
* Transform columns of Big Data for feature engineering using DataFrame.
* Perform simple data analytics using SQL Spark

## [MiniProject 2: CorrelationOHE](https://github.com/ljiwoo59/PROG_MODL_BIG_DATA/blob/main/MiniProject2_CorrelationOHE-v2.html)
* Compute correlation of Big Data
* Compute the dimensionality of a categorical variable if it is converted to a numerical representation.

## [MiniProject 3: Frequent Service Sets](https://github.com/ljiwoo59/PROG_MODL_BIG_DATA/blob/main/MiniProject3_FrequentServiceSets_Lab.html)
* Identify top k services that are open for scanners in the Darknet dataset
* Identify frequent 2-service sets (based on top 10 services) and identify potentially interesting patterns
* Compute 3-service sets (based on top 10 services) that are open for scanners in the Darknet dataset

## [MiniProject 4: K-Means Clustering](https://github.com/ljiwoo59/PROG_MODL_BIG_DATA/blob/main/MiniProject4_Lab.html)
* Apply k-means clustering to the Darknet dataset
* Intepret the features of the cluster centers generated
* Compare the result of k-means clustering with different value of k



