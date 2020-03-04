# Lesson 2: AutoML introduction

This lesson is about exploration of existing framework for automatic model generation. The lesson tests it out on  **binary classification** & **regression example**.

## Dictionary
Basic machine learning tasks: 
    - Classification: is the problem of identifying to which of a set of categories (sub-populations) a new observation belongs [wiki](https://en.wikipedia.org/wiki/Statistical_classification)
    - Regression:  is a set of statistical processes for estimating the relationships among variables. [wiki](https://en.wikipedia.org/wiki/Regression_analysis)
- Scikit Learn
    - is a free software machine learning library for the Python programming language [link](https://scikit-learn.org/stable/)


## Practise
### 1) Setup via Python virtual Env

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

Connect interactive python kernel to your pipenv
```
pip install ipykernel
python -m ipykernel install --user --name=ml_box
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

### 4) MLBox

Open/Upload lesson_2_mlbox.ipynb to your running `jupyter notebook` and start to play. You will see that the file contains sample data generator. 

*Try following tasks:*
- change the count of generated sample rows
- change the data generation equation to `y = 1 if x1%5==0 else 0` 
- change the data generation equation to `y = 1 if (x1+x2+x3>x3/3) else 0`
- reduce the features count to 4
- !!!change the data generation equation to `y = x1+x2` !!! This is changing the task from binary classification task to regression(value prediction) task


### 5) Ludwig
Open/Upload lesson_2_ludwig.ipynb to your running `jupyter notebook` and start to play. You will see that the file contains sample data generator. 

*Try following tasks:*
- change the count of generated sample rows
- change the data generation equation to `y = 1 if x1%5==0 else 0` 
- reduce the features count to 4
- !!!change the data generation equation to `y = x1+x2` !!! This is changing the task from binary classification task to regression(value prediction) task
-- observe what happens if you do not change the target_column type
-- observe what happens if you change the feature columns type to text
 

### 6) ML challenge
Here is a link to repository for [Data Days 2019 challenge](https://github.com/anfibil/dataday19_intro_to_ml)
- task 1: try to apply any AutoML solution that you tried today

### 7) Extra:
More information about the projects:
- [Ludwig](https://github.com/uber/ludwig)
- [MLBox](https://mlbox.readthedocs.io/en/latest/)
Other AutoML solutions:
- [Google AutoML](https://cloud.google.com/automl)
- [AWS Sagemaker](https://aws.amazon.com/sagemaker/)
- [Datarobot](https://www.datarobot.com/)

### 8) Cleanup
Remove ipykernel
```bash
jupyter kernelspec uninstall <name of your kernel>
```
Remove pipenv
```bash
pipenv --rm
```












