# Multilabel-Classification-PDD
This is a repository for CS 598 DL4H that attempts to replicate recently published work in deep learning for healthcare with a focus on Multi-label classification for psychotic disorder diseases.

The main goal of this repository is to attempt to replicate some of the findings by implementing baseline and proposed models stated in the paper "*Application of deep and machine learning techniques for multi-label classification performance on psychotic disorder diseases*"[[1](https://www.sciencedirect.com/science/article/pii/S2352914821000356)]. All the work is done in the single Jupyter Notebook file.

## Data
The data that was used is provided as supplementary data. This dataset can be located [here](https://www.sciencedirect.com/science/article/pii/S2352340917303487) under Appendix A of the paper "*Quantitative exploration of factors influencing psychotic disorder ailments in Nigeria.*"[[2](https://www.sciencedirect.com/science/article/pii/S2352340917303487)].

## Data Processing
In the original dataset, replace P with 1 and N with 0 for all the dependent variables, and combine all the dependent variables to create a combined target converting a multi-label classification to conventional multi-classification problem where there is only one target but there are more than two classes.
Once complete, create two identical files for the data. The first copy of the data will remain as is, but for the second copy, remove rows with target value combinations of 11100, 01111, 10011, 00110, 00010, 10100, 10111. The first copy will have 500 records, and the second copy of the data will have 484 records of patients.

## Steps
1. Converted multi-label classification problem into conventional multi-classification problem
2. Perfomed One-hot-vector encoding of the categorical variables
3. Implemented SMOTE for generating synthetic samples for dataset without class imbalance
4. Machine Learning techniqus MLP, RF, SVM and DT for both balanced and imbalanced datasets: Model training, prediction and comparison
5. Implemented DNN-MLP model using Keras function API for both balanced and imbalanced datasets: Model training, prediction and comparison
6. Performed ablation study for hidden layers of DNN-MLP model evaluating the impact of each hidden layer on the accuracy of the model
7. Created our own DNN-MLP model using PyTorch Neural Network Modules for training of both balanced and imbalanced datasets: Model prediction and comparison

## Table of Results
A pdf file is included which holds all the results obtained from our replication study and can be viewed [here](table_results.pdf).

### References
[[1](https://www.sciencedirect.com/science/article/pii/S2352914821000356)] Israel Elujide, Stephen G. Fashoto, Bunmi Fashoto, Elliot Mbunge, Sakinat O. Folorunso, and Jeremiah O. Olamijuwon. 2021. Application of deep and machine learning techniques for multilabel classification performance on psychotic disorder diseases. Informatics in Medicine Unlocked, 23:100545

[[2](https://www.sciencedirect.com/science/article/pii/S2352340917303487)] O Adejumo Adebowale, Nehemiah A Ikoba, Suleiman Esivue A, Okagbue Hilary I, Oguntunde Pelumi E, Odetunmibi Oluwole A, Job Obalowu. Quantitative exploration of factors influencing psychotic disorder ailments in Nigeria. Data in Brief 2017;14:175–85. 
