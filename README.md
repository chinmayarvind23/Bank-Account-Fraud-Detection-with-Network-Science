# Bank Account Fraud Detection with Network Science

## Project Details

Team Members: Chinmay Arvind, Jerry Fan, Dmitry Kostyukov, Ryan Millar

## Purpose of Project

This project aims to conduct a data-driven & thorough network analysis of bank account applications. This project aims to provide a solution for bank account fraud detection that will find outliers in the dataset to separate non-fraudulent and fraudulent bank account applications. We plan to answer research questions that will be utilizing various network science metrics taught in class, such as Eigenvector centrality, network density, degree centrality, Katz centrality, closeness centrality, local clustering coefficient, cosine similarity, and Jaccard coefficient, and concepts such as strongly connected components and cores,. The idea is to use the above-mentioned metrics along with the other columns in the dataset to classify nodes as either having a higher or lower risk of committing bank account fraud. The network science metrics interpreted in the context of bank fraud detection will provide a better idea of which nodes could be linked and commit bank fraud, potentially identifying criminal organizations that are participating in bank fraud. The other columns in the dataset will allow for creating edges between the nodes based on the similarity of their application details alongside the network metrics, allowing for a complex multigraph to be formed between nodes, providing a bigger picture of different facets of bank account applications to be considered when identifying fraudulent applications. The project will answer the following research questions:

1. Which were the key fraudulent players within the network?

2. Were there any specific fraudulent groups within the network that could be collaborating to defraud the bank?

3. What was the average profile of a fraudulent customer?

4. What differences exist between fraudulent account applications and non-fraudulent account applications?

## Data

This project uses data from the following Kaggle dataset: <https://www.kaggle.com/datasets/sgpjesus/bank-account-fraud-dataset-neurips-2022/data>. There are 32 columns in the dataset, and 6 files of data which we have performed data modeling, cleaning, preparation, dimensionality reduction, feature engineering, data analysis, and visualization on to determine the most important predictors of bank account fraud from the dataset, and use the identified most important columns along with computed network metrics as our final set of predictors to solve the above research questions, and attempt to provide an approximate method of bank account fraud estimation given a dataset with relevant predictors.

## Tech Stack

R, Quarto, Azure Blob Storage, GitHub Pages

## Network Definition

The nodes in this network represent the customers who make applications for accounts with a bank. The edges are connections between nodes (customers) based on the similarity of an attribute such as: the time of the application, credit risk score, etc. The network will be a multigraph connecting nodes based on the similarity of attributes as mentioned above (the similarity score will be computed separately and will have to account for different types of columns in the dataset). The edges will hold information on what type of attribute 2 nodes are linked to each other based on (or color them differently and provide a legend for each different type of relationship based on the attribute) and weighted based on the similarity score computed for the 2 nodes (edges will be created if a certain similarity threshold is exceeded for the attribute in question). This will form a sufficiently complex network (which isn’t disconnected into isolated pieces based on different attributes which would otherwise have not allowed for in-depth network analysis).
