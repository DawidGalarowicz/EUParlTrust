# Trusting the EU begins at home
## Building a classification model to predict which voters trust the EU Parliament

This repository contains the data and Jupyter notebooks which underpin the article that I have published on Medium on the 29th of June 2020.

Link: https://medium.com/@dawidgalarowicz/trusting-the-eu-beings-at-home-bf49c022be83

## Table of Contents  
[Installation](#installation)  
[Project Motivation](#motivation)  
[File Descriptions](#files)  
[Results](#results)  
[Licensing & Acknowledgements](#licensing)  

<a name="installation"/></a>
## Installation

The following libraries have been used inside Google Colab's Python environment:

```bash
pandas
numpy
shap
xgboost
sklearn
time
hyperopt
defragTrees
pickle
matplotlib
google.cloud
```

The code should run with no issues using Python 3.6.9.

Make sure that all your packages are up-to-date if you want to use my code!

<a name="motivation"/></a>
## Project Motivation

This code has been written to complete the capstone assignment of Udacity's Data Science Nanodegree.

I have defined the problem statement myself. This required looking for the data, selecting an appropriate modelling strategy and analysing outputs.

The aim of the project was twofold:
- to verify whether a Machine Learning model can accurately distinguish between voters who trust the EU Parliament and those who do not
- to identify what factors would drive such model
                           
Please note that the repository DOES NOT contain the API key used to make translations in EES - Data Cleaning.ipynb due to security/privacy reasons.

<a name="files"/></a>
## File Descriptions
Apart from the README file, there is a number of files in this repository:

```bash
- EES - Data Cleaning.ipynb # A notebook used to process the Stata file in EES2019 Voter Study early release.zip.
- EES - Modelling.ipynb # A notebook used to apply Machine Learning models on the outputs of EES - Data Cleaning.ipynb
- NUTS2.csv # A mapping table to link NUTS codes to regions' names
- cleandata_noparty.csv # 1 of 2 datasets produced by EES - Data Cleaning.ipynb (uploaded for convienience of others who want to simply run EES - Modelling.ipynb)
- cleandata_parties.zip # .zip with 2 of 2 datasets produced by EES - Data Cleaning.ipynb (uploaded for convienience of others who want to simply run EES - Modelling.ipynb)
- defragTrees.py # A Python package released by Hara and Hayashito, 2018
- EES2019 Voter Study early release.zip # .zip with the Stata file published by Schmitt et al., 2019
- README.md
```

<a name="results"/></a>
## Results
To prepare all files needed by the app, run the commands in the following order:

```bash
# In the "data" folder:
python process_data.py disaster_messages.csv disaster_categories.csv DisasterResponse.db
python discover_languages.py

# In the "models" folder:
python train_classifier.py ../data/DisasterResponse.db classifier.pkl
```

Your data is now ready and your pickled model has been created!

Finally, you can run the app!

<a name="licensing"/></a>
## Licensing & Acknowledgements
Feel free to use the code here as you would like!
