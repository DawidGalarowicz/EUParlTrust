# "Trusting the EU begins at home" - Supporting Code
This repository contains the data and Jupyter notebooks which underpin the article that I have published on Medium on the 29th of June 2020.

** Link: https://medium.com/@dawidgalarowicz/trusting-the-eu-beings-at-home-bf49c022be83 **

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

To find out more about the study and the questionnaire, visit http://europeanelectionstudies.net/european-election-studies/ees-2019-study/voter-study-2019.

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
- party-list-appendix.csv # A .csv with party mappings used in EES - Data Cleaning.ipynb created by Schmitt et al., 2019
- README.md
```

<a name="results"/></a>
## Results
You can view the outputs in Jupyter notebooks and read my intepretation of the results in my Medium article.

If you would like to replicate the study, start from unpacking EES2019 Voter Study early release.zip (zipped to reduce its size) to get the Stata file. Next, run EES - Data Cleaning.ipynb to obtain cleandata_noparty.csv and cleandata_parties.csv. Finally, run EES - Modelling.ipynb to apply classification models.

If you have issues with running hyperparameter optimisation in EES - Modelling.ipynb, make sure that you are using Google Colab's GPU or adjust the code to utilise your local CPU.

<a name="licensing"/></a>
## Licensing & Acknowledgements
Feel free to use this code for educational purposes and to experiment with it.

If you are sharing this work, please reference the Medium article that describes my study.
