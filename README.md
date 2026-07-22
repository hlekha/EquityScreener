# Equity Screener
During winter break of my sophomore year, I participated in the UBS Stock Pitch Competition, which was an ehilirating experience as I had no knowledge in the finance world whatsoever. Nevertheless, after weeks of research on stock valuation, this project was made as an attempt to combine the quantitative skills I know I had, and the qualitative skills I had just learned, and served as a supplement for my investment thesis on APA Corporation (NASDAQ: APA). 

## Purpose
For the competition, I was tasked with filtering through a universe of stocks (about 500) of various sectors, and picking the firm that showed the greatest undervaluation, and soforth, the greatest potential for a long oppurtunity. I realized that at its core a great investment thesis needs an absolute valuation, and a relative valuation, and that a Python script that does parses through these tickers, fetched the financial data of each company, computed respective metrics for each company, and then compare the metrics to each other, would be a perfect way to relatively value each of the 500 companies, while also narrowing down the universe of stocks into a manageable list of 5-10 stocks that I could further assess with an absolute valuation. 

## Prerequisites 
This project utilizes the numpy, and pandas library, as well as the yfinance API. The numpy library helps with the normalization calculations (talked about in [Key Features](##key-features)), while the pandas library organizes and outputs those beautiful tables. The yfinance API is used to retrieve the financial data for each equity including income statements, cash flow data, and other company insights that assist with calculating the metrics.

```shell
pip install numpy
pip install pandas
pip install yfinance
```

## Usage
By inputting a list of equity tickers, the system outputs a pandas table displaying the top 10 most undervalued companies based their "long score". This is a customized metric that is cumulative of all metrics for each company in the universe, where each metric is weighted based on how much the metric impacts a companies valuation. The companies are ranked from highest score to lowest (higher long score being a better long oppurtunity); the metrics involved in the calculation are then shown respective to each company. 
<p align="center">
  <img width="562" height="359" alt="image" src="https://github.com/user-attachments/assets/7fb678b1-a766-4a35-a065-0a5b89baccec" />
</p>
Keep in mind that this script only regards long oppurtunities; there is no limit to how much tickers you can enter, but of course, the more tickers you enter the longer it will take to process. 

## Key Features
Along with a long score for the top 10 firms, and their respective metrics. There is a second cell, which acts like a second filtration system, where once given the tickers of the top ten firms, produces another pandas table emphasizing metrics that can be used for a Discounted Cash Flow Model, like the WACC, Leverage, and 5-Year CAGR.
<p align="center">
  <img width="504" height="327" alt="image" src="https://github.com/user-attachments/assets/447a24af-7d9b-460d-8d30-1abe5a04dbb1" />
</p>
Observe that the metrics in both features (the initial and secondary filter), are not raw, but a normalization. It is normalized by taking the z-score of each stock respective to their industry's mean, then calculating how far the raw metric of the company is from the meean, and dividing it by the average distance away from the mean of the equities belonging to that industry - the standard deviation. 

## License
Distributed under the MIT License. See LICENSE for more information.

## Contact 
My LinkedIn: linkedin.com/in/hayden-lekha
My Email: haydenlekha@gmail.com
Project Link: https://github.com/hlekha/EquityScreener
