# Multilabel-Classification-PDD
This is a repository for CS 598 DL4H that attempts to replicate recently published work in deep learning for healthcare with a focus on Multi-label classification for psychotic disorder diseases.

The main goal of this repository is to attempt to replicate some of the findings by implementing baseline and proposed models stated in the paper "*Application of deep and machine learning techniques for multi-label classification performance on psychotic disorder diseases*"[[1](https://www.sciencedirect.com/science/article/pii/S2352914821000356)]. All the work is done in the single Jupyter Notebook file.

## Data
The data that was used is provided as supplementary data. This dataset can be located [here](https://www.sciencedirect.com/science/article/pii/S2352340917303487) under Appendix A of the paper "*Quantitative exploration of factors influencing psychotic disorder ailments in Nigeria.*"[[2](https://www.sciencedirect.com/science/article/pii/S2352340917303487)].

## Data Processing
The original data has some invalid characters present for the UTF-8 decoder. To avoid running into problems later, manually remove the invalid characters and additional spaces present in rows `[2,3,4,5,10,14,17]`. The remaining data processing steps are all handled in the [jupyter notebook](multilabel_classification_PDD.ipynb). 

## Implementation Steps Taken
1. Converted multi-label classification problem into conventional multi-classification problem
2. Perfomed One-hot-vector encoding of the categorical variables
3. Implemented SMOTE for generating synthetic samples for dataset without class imbalance
4. Created, trained, and evaluated ML models (MLP, RF, SVM, DT) for both balanced and imbalanced datasets 
6. Created, trained, and evaluated DNN-MLP model using Keras function API for both balanced and imbalanced datasets
7. Performed ablation study for hidden layers of DNN-MLP model evaluating the impact of each hidden layer on the accuracy of the model
8. Created our own DNN-MLP model using PyTorch Neural Network Modules for training of both balanced and imbalanced datasets: Model prediction and comparison

## Steps to Replicate
1. Requires `python >= 3.7`
2. Clone the repo or download the files
3. Install the requirements if needed. `pip install -r requirements.txt`
4. Obtain the data and remove the special characters manually.
5. Add the data file named as `PDD_data.csv` into the same directory.
6. Run the jupyter notebook.

## Table of Results
A pdf file is included which holds all the results obtained from our replication study and can be viewed [here](table_results.pdf).

### References
[[1](https://www.sciencedirect.com/science/article/pii/S2352914821000356)] Israel Elujide, Stephen G. Fashoto, Bunmi Fashoto, Elliot Mbunge, Sakinat O. Folorunso, and Jeremiah O. Olamijuwon. 2021. Application of deep and machine learning techniques for multilabel classification performance on psychotic disorder diseases. Informatics in Medicine Unlocked, 23:100545

[[2](https://www.sciencedirect.com/science/article/pii/S2352340917303487)] O Adejumo Adebowale, Nehemiah A Ikoba, Suleiman Esivue A, Okagbue Hilary I, Oguntunde Pelumi E, Odetunmibi Oluwole A, Job Obalowu. Quantitative exploration of factors influencing psychotic disorder ailments in Nigeria. Data in Brief 2017;14:175–85. 
