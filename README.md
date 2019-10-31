## EECS 731 Project 5: Time Series Forecasting by Matthew Taylor

### Overview

This project is meant to serve as an introduction to time series forecasting. Time-dependent data will be processed using different statistical models in order to predict what might happen in the future.

### Approach

I began by downloading [this dataset](https://www.kaggle.com/felixzhao/productdemandforecasting). This dataset contains the demand of many products over many years. I chose the product that had the most available data and decided to focus on that one in particular. After removing all of the extraneous information from the dataset, I grouped the product demand figures by month. The served a dual-purpose of reducing the number of samples the models would have to process while also creating a uniform temporal distribution of exactly one month between samples. Once the data had been prepared, I performed an 80-20 train-test split. Then, I created moving average and ARIMA models to predict future product demand.

### How to Run

This project was written in a Jupyter Notebook running Python 3.7.2. This project relies on a small number of modules, which can be installed by running this command:
```
pip3 install -r requirements.txt
```

Once the requirements are installed, each of the cells in the Jupyter Notebook can be executed. However, this is not required as each cell has already been executed and the results are shown.

### Results

Forecasts for each of the two models were plotted against the true trends to qualitatively illusrate their accuracies. With only a glance, the moving average model is far more accurate than

### Future Work and Optimizations

Possible optimizations include tweaking model parameters. There likely exists some combination of settings that would increase the performance of these models. Future work might also include utilizing many more regression models to see exactly which one performs the best. Neural networks are said to have state-of-the-art performance, so it may be interesting to see how they perform relative to these two models.
