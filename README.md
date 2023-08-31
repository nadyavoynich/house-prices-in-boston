# Boston in the '70s: A Residential Pricing Model using Multivariable Regression
<img src=https://i.imgur.com/WKQ0nH2.jpg height=350>

## Project Description
This project takes you on a journey back to Boston, Massachusetts, in the 1970s. 
Its central aim is to construct a model that offers a price estimation based on various home attributes, such as:
* The number of rooms
* The distance to employment centres
* Socio-economic status of the neighborhood
* Student-to-teacher ratio in nearby schools, among others.

Steps to achieve this objective:
1. Analyse and explore the Boston housing price dataset. 
2. Partition the dataset into training and testing sets. 
3. Run a Multivariable Regression. 
4. Assess the model through its coefficients and residuals. 
5. Enhance model performance via data transformations. 
6. Utilize the model for property price estimations.

## Dataset Overview
### Source
This dataset is a replica of the UCI ML housing dataset.
It originates from the StatLib library, hosted by Carnegie Mellon University.
The original research paper associated with it can be accessed [here](https://deepblue.lib.umich.edu/bitstream/handle/2027.42/22636/0000186.pdf?sequence=1&isAllowed=y). 

### Dataset Structure
Number of Instances: 506

Number of Attributes: 13 numeric/categorical predictive. The Median Value (attribute 14) is the target.

    Attribute Information (in order):
        1. CRIM     per capita crime rate by town
        2. ZN       proportion of residential land zoned for lots over 25,000 sq.ft.
        3. INDUS    proportion of non-retail business acres per town
        4. CHAS     Charles River dummy variable (= 1 if tract bounds river; 0 otherwise)
        5. NOX      nitric oxides concentration (parts per 10 million)
        6. RM       average number of rooms per dwelling
        7. AGE      proportion of owner-occupied units built prior to 1940
        8. DIS      weighted distances to five Boston employment centres
        9. RAD      index of accessibility to radial highways
        10. TAX      full-value property-tax rate per $10,000
        11. PTRATIO  pupil-teacher ratio by town
        12. B        1000(Bk - 0.63)^2 where Bk is the proportion of blacks by town
        13. LSTAT    % lower status of the population
        14. PRICE     Median value of owner-occupied homes in $1000's
        
    Missing Attribute Values: None

    Creator: Harrison, D. and Rubinfeld, D.L.

## Setup & Requirements
Follow these steps to get the data analysis project up and running on your local machine.

### Prerequisites
1. **Python**: This project requires Python 3.9 or higher.
If you don't have Python installed, [download and install](https://www.python.org/downloads/) the latest version.
2. **Jupyter Notebook**: Jupyter Notebook is used for the interactive analysis. If you don't have it, install it using pip:
``pip install jupyter``

### Setting Up a Virtual Environment (Recommended)
It's recommended to set up a virtual environment to avoid any package conflicts.
1. Install `virtualenv` if not installed: ``pip install virtualenv``
2. Navigate to the project directory and create a virtual environment: ``virtualenv venv``
3. Activate the virtual environment:
    - **Windows**: ``.\\venv\\Scripts\\activate``
    - **macOS/Linux**: ``source venv/bin/activate``

### Installing Required Libraries
With the virtual environment activated, install the necessary libraries using:
``pip install -r requirements.txt``

Python libraries used:
* pandas
* numpy
* seaborn
* plotly
* matplotlib
* sklearn (LinearRegression, train_test_split)


### Getting the Data
This project uses the `UCI ML housing` dataset.
1. Download the dataset from [this link](https://github.com/nadyavoynich/house-prices-in-boston/blob/main/boston.csv).
2. Place the downloaded dataset in the same directory.

### Running the Notebook
With everything set up, start the Jupyter Notebook server: ``jupyter notebook``
Navigate to the desired notebook and you're ready to start your analysis!

## Methodology
* Exploratory data analysis 
* Descriptive statistics
* Multivariable regression
* Regression model improvement using a log data transformation

## Results
The equation for the constructed model is as follows:

$$ \log (PR \hat ICE) = \theta _0 + \theta _1 RM + \theta _2 NOX + \theta_3 DIS + \theta _4 CHAS + ... + \theta _{13} LSTAT $$

* Training data R-squared: 0.79
* Test data R-squared: 0.74.