# Applied Machine Learning Group Project
# Credit Card Fraud detection 

This is a readme file for our group project codes. We hope this will help to navigate the different files and codes. 

--------------------------------------------------------------

## Table of contents

- [Folder contents](#contents)
- [Setup](#setup)
- [Execution](#execution)

--------------------------------------------------------------

## Folder contents
The contents of this group project submission folder should contain 2 folders and 2 ipynb files.
- Inside the 'Fraud dataset' folder, it should contain 3 files. 2 csv files and 1 ipynb file.
- Inside the 'Feature generated dataset' folder, it should contain 3 files. 2 csv files and 1 ipynb file.
- The main file that will be used is the 'Model with Coefficients.ipynb' file as it is the latest version of our model file.
```
The structure should be organised as follows:
├── README.md                       # Project overview and setup instructions
├── Fraud dataset                   # Dataset source file
│   ├── EDA.ipynb                   # Jupyter notebook containing EDA codes
│   ├── fraudTest.csv               # Fraud test dataset downloaded from kaggle
│   └── fraudTrain.csv              # Fraud train dataset downloaded from kaggle
├── Feature generated dataset       # Feature generation
│   ├── Feature generation.ipynb    # Jupyter notebook containing feature engineering codes
│   ├── test_dataset.csv            # Fraud test dataset with generated features
│   └── train_dataset.csv           # Fraud train dataset with generated features
├── Model with Coefficients.ipynb   # Updated models code that shows coefficient scores
└── Models.ipynb                    # Initial models code
```
--------------------------------------------------------------

## Setup
Our models were made to work using Kaggle. 
However, our feature generation file was made to work locally to save the feature generated dataset. 
Also, our EDA ipynb was made to work on Google colab. 

Upon downloading the repository, please leave the files as they are as much as possible.
Please also note that this repository do not contain the original datasets and feature engineered dataset.

You may download the original dataset from kaggle at this link and place it in the correct folders according to the structure above:
[Dataset](https://www.kaggle.com/datasets/kartik2112/fraud-detection)

### Feature generated dataset Setup
If you wish to recreate our feature generated dataset you will have to run the 'Feature generation.ipynb' file located in the 'Feature generated dataset' folder.

We ran this file locally so as to save the feature generated dataset.
- If you have kept the file structure as it is, you may just run all the cells.
- If you encounter any errors, please check the path of the dataset.

Once all the cells have been run, the feature generated dataset should be in the same directory as this 'Feature generation.ipynb'. They should be named `train_dataset.csv` and `test_dataset.csv` respectively.

### Model Setup
To get the models to run on Kaggle, upload the model file which you wish to use. Then upload the `train_dataset.csv` and `test_dataset.csv` from the `Feature generated dataset` folder.

**NOTE**: **DO NOT** use the file from the `Fraud dataset` folder as this contains only the raw dataset without our new features. 

### EDA Setup (Optional)
If you wish to recreate our EDA results you will have to run the `EDA.ipynb` file located in the `Fraud dataset` folder.

We ran this file on Google Colab. So please ensure that after you have mounted your drive, the file path is according to how you have it set up on your drive.

please change this cell accordingly: 
```
%cd /content/drive/MyDrive/MITB/Applied Machine Learning/Group Project Submission/Fraud dataset
```

If you encounter any errors, please check the path of the dataset. You can just run all the cells to recreate our EDA findings.

--------------------------------------------------------------

## Execution
As mentioned, the main file to run will be the 'Model with Coefficients.ipynb' file. Please ensure you have set it up on Kaggle accordingly.
Also ensure that under Accelerator > please select the GPU T4 x2.

To recreate our results, please run all the cells. 

**NOTE**: The whole run time of our file might take 1 hour 30 mins. This is mostly due to the hyper parameter tuning section. 

If you wish to have a faster run time, please comment out the hyper parameter tuning models and ensure that you comment out these lines in the 5th last cell:
```
model_metrics_list.append(rf_tuned_model_metrics)
model_names.extend('Tuned Random Forest')
model_metrics_list.append(lgr_tuned_model_metrics)
model_names.extend('Tuned Log Regression')
```

The team also understands that the parts for the model coefficient is rather messy. This is due to the structure of how we saved the coefficients for the tuned models.

The current version is the one that best outputs all the coefficients, other methods have led to bugs that do not show the coefficients nicely.

We seek your understanding for this inconvenience. 


