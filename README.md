## EECS 731 Project 5: Time Series Forecasting by Matthew Taylor

### Overview

This project is meant to serve as an introduction to time series forecasting. Time-dependent data will be processed using different statistical models in order to predict what might happen in the future.

### Approach

I began by downloading [this dataset](https://www.kaggle.com/felixzhao/productdemandforecasting). This dataset contains the demand of many products over many years. I chose one of the products that had the most available data and decided to focus on the one in particular that had a rather clear trend. After removing all of the extraneous information from the dataset, I grouped the product demand figures by day. Once the data had been prepared, I performed an 80-20 train-test split. Then, I used linear regression and ARIMA models to forecast the prepared time series. I employed plots to visually confirm the results and mean-squared-error to quantitatively compare the two models.

### How to Run

This project was written in a Jupyter Notebook running Python 3.7.2. This project relies on a small number of modules, which can be installed by running this command:
```
pip3 install -r requirements.txt
```

Once the requirements are installed, each of the cells in the Jupyter Notebook can be executed. However, this is not required as each cell has already been executed and the results are shown.

### Results

Forecasts for each of the two models were plotted against the true trends to qualitatively illustrate their accuracies. At a glance, both models seem fairly similar. After inspecting the decomposition models, the reason behind this becomes apparent. There's hardly any fluctuation in the trend. The original chart spikes between values near zero and values above 200,000. However, the trend has a range of only about 15,000. In other words, this time series is fairly constant, albeit noisy. To effectively compare the two models, I decided  to utilize mean-squared-error. As expected, the more complex ARIMA model had a lower MSE value and is therefore marginally more accurate than the simple linear regression model.

### Future Work and Optimizations

Given more time to work on this project, I would look for other products in the dataset with more interesting trends. Most of the examples I looked at were very similar. They had average values that hardly fluctuated with copious amounts of noise throughout. Once I found a product with a more interesting trend, I would implement other forecasting models. Although rather complex, recurrent neural networks like LSTMs have been used by others to predict time-dependent data with surprising results.
