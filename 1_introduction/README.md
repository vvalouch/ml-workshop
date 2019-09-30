# Lesson 1: Introduction (Binary Classification)

This lesson is about creation of **shallow** neural network for **binary classification**.

## Dictionary
**Classic programming vs machine learning**

![1_classic_vs_ml](./images/1_classic_vs_ml.jpg)  
- Classification vs Regression
    - Classification: is the problem of identifying to which of a set of categories (sub-populations) a new observation belongs [wiki](https://en.wikipedia.org/wiki/Statistical_classification)
    - Regression:  is a set of statistical processes for estimating the relationships among variables. [wiki](https://en.wikipedia.org/wiki/Regression_analysis)
- Binary vs Multiclass classification
    - Binary: the result of the classification is a prediction of affinity to one of **2** classes
    - Multiclass: the result of the classification is a prediction of score/probability of affinity to one of **x** classes
- Scikit Learn
    - is a free software machine learning library for the Python programming language [link](https://scikit-learn.org/stable/)


## Practise
### 1a) Setup via Python virtual Env

If you are using MacOS and missing python 3 here is way how to install it.
```bash
brew install python3
```

Optional: The steps bellow will help you to setup your virtual Python environment. 
```bash
pip install pipenv
cd <folder where you are planning to run python>
pipenv --three
pipenv shell
```

Install Scikit Learn framework
```bash
pip install scikit-learn==0.21.2 
pip install pandas
pip install numpy
pip install jupyter
pip install joblib
```

### 1b) Docker style
Install [docker](https://www.docker.com/get-started) client so that you can experiment locally on your computer 
```bash
docker pull jupyter/scipy-notebook
```

### 2) Introduction to Jupyter notebook


Hopefully useful tips:
- `tab` : intellisense
- `shift + tab` : method arguments intellisense
- `ctrl + enter`: execute current line
- `shift + enter` : execute current line and move to next line 

### 3) Playground
Start your `jupyter notebook`
- for python version just run following command in the `1_introduction` folder
```bash
jupyter notebook
```
- for docker run following command and then open the link displayed
```bash
docker run -p 8888:8888 jupyter/scipy-notebook
```

Open/Upload random_sample.ipynb to your running `jupyter notebook` and start to play. You will see that the file contains sample data generator. 

*Try following tasks:*
- change the count of generated sample rows
- change the data generation equation to `y = 1 if x1%5==0 else 0` 
- change the data generation equation to `y = 1 if (x1+x2+x3>x3/3) else 0`
- add new feature `x4` 
- try different classifier like [`tree.DecisionTreeClassifier()`](https://scikit-learn.org/stable/modules/generated/sklearn.tree.DecisionTreeClassifier.html) or [naive bayes Gausian]() and compare their performance
- check and try to use [GridSearchCV](https://scikit-learn.org/stable/modules/generated/sklearn.model_selection.GridSearchCV.html)
 

### 4) ML challenge
Here is a link to repository for [Data Days 2019 challenge](https://github.com/anfibil/dataday19_intro_to_ml)

### 5) Extra:
Check following projects:
- [Ludwig](https://github.com/uber/ludwig)
- [Automl-gs](https://github.com/vvalouch/automl-gs)
- [Google AutoML](https://cloud.google.com/automl/)




