# Decision Tree Implementation Documentation

This project was completed as part of the semester project for the 4022 course at IUST.
Aidin Asl Zaeim
Student ID: 99400012


## Introduction
This project aims to implement an adaptive decision tree that is not binary and allows each node to have more than two children. The decision tree is designed to handle classification tasks, where the goal is to predict the class label of a given data instance based on its features.

## Data Preprocessing
The project involves several steps of data preprocessing:
1. **Data Cleaning**: Check for missing values (NAN) and remove irrelevant columns.
2. **Feature Customization**: Customize features using techniques such as labeling and clustering. We chose to use k-means clustering to discretize continuous features into categorical ones.

## Decision Tree Implementation
The decision tree is implemented using a Python class called `tree`, which consists of methods for building the tree, printing the tree structure, and validating the accuracy of the tree on test data. Below are the key functionalities of the decision tree implementation:

### Building the Tree
The `build_tree` method recursively constructs the decision tree by selecting the best feature to split the data at each node based on information gain. The tree stops growing when it reaches the maximum depth or when further splitting does not provide significant information gain.

### Information Gain Calculation
The decision tree calculates information gain to determine the best feature for splitting the data. Information gain measures the reduction in entropy (or impurity) achieved by splitting the data based on a particular feature.

### Entropy
Entropy is a measure of impurity in a dataset. The decision tree uses entropy to evaluate the homogeneity of classes within each split. It aims to minimize entropy by choosing the feature that maximizes information gain.

### Traversing the Tree
The `traverse_tree` method allows us to navigate through the decision tree for a given data instance. It moves from the root node to the leaf nodes based on the feature values of the data instance until it reaches a leaf node, where the majority class label is predicted.

## Challenges
1. **Choosing Discretization Method**: Selecting the best method for discretizing numerical values posed a challenge due to the large range of numerical values in the dataset. We experimented with various techniques, including equal frequency and equal length discretization, before settling on k-means clustering.
2. **Learning Curve**: This being the first AI project, there was a learning curve associated with mastering the pandas, matplotlib, and numpy libraries. Additionally, plotting the inertia plot and clusters for each feature required understanding these libraries, which added to the complexity.
3. **Finding the Best Feature for Splitting**: The most complex part of the project was determining the best feature index for each node to enhance the functionality of the tree. This involved implementing the `best_feature` method in the `tree` class, which required careful consideration of information gain and entropy.

## Result
After implementing and testing the decision tree on the provided dataset, we achieved an accuracy of 98% on the test data. This demonstrates the effectiveness of the adaptive decision tree in classifying data instances.


