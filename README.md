# Intrusion-Detection-With-Spark

In this notebook, I replicated the Spark-Chi-SVM model proposed in the paper "Intrusion detection model using machine learning algorithm on Big Data environment" (S. M. Othman, F. M. Ba-Alwi, N. T. Alsohybe, and A. Y. Al-Hashida, 2018).

The goal of this project is to detect network intrusions into a computer from unauthorized users. The KDD99 data set (10% subset) is used. The data set consists of 494,021 instances with 41 attributes and a class attribute. The two classes are a 'normal' connection and an 'attack'.

The notebook was run in PySpark in a Databricks notebook. The flow of the notebook is summarized in the following table, except that I used a linear support vector machine (SVM) model without the stochastic gradient descent (SGD). 

Additionaly, since there is an imbalance of classes in the data set, I assigned a higher weight to the minority class and a lower weight to the majority class, based on the class ratio, to penalize the misclassification.

![image](https://github.com/quincyho/Intrusion-Detection-With-Spark/blob/main/Images/Model%20Flow.JPG)

A test ROC of 99.48% was achieved by this Spark-Chi-SVM model.
