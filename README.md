# Equity Screener

## Purpose
During winter break of my sophomore year, I participated in the UBS Stock Pitch Competition, which was an ehilirating experience as I had no knowledge in the finance world whatsoever. Nevertheless, after weeks of research on stock valuation, this project was made as an attempt to combine the quantitative skills I know I had, and the qualitative skills I had just learned, and served as a supplement for my investment thesis on APA Corporation (NASDAQ: APA). 

For the competition, I was tasked with filtering through a universe of stocks (about 500) of various sectors, and picking the firm that showed the greatest undervaluation, and soforth, the greatest potential for a long oppurtunity. I realized that at its core a great investment thesis needs an absolute valuation, and a relative valuation, and that a Python script that does parses through these tickers, fetched the financial data of each company, computed respective metrics for each company, and then compare the metrics to each other, would be a perfect way to relatively value each of the 500 companies, while also narrowing down the universe of stocks into a manageable list of 5-10 stocks that I could further assess with an absolute valuation. 

## Usage
By inputting a list of equity tickers, the system outputs a Pandas table displaying the top 10 most undervalued companies based their "long score". This is a customized metric that is cumulative of all metrics for each company in the universe, where each metric is weighted based on how much the metric impacts a companies valuation. The companies are ranked from highest score to lowest (higher long score being a better long oppurtunity); the metrics involved in the calculation are then shown respective to each company. 
<p align="center">
  <img width="562" height="359" alt="image" src="https://github.com/user-attachments/assets/7fb678b1-a766-4a35-a065-0a5b89baccec" />
</p>
Keep in mind that this script only regards long oppurtunities.

## Key Features
Along with a long score for the top 10 firms, and their respective metrics. There is a second cell, which acts like a second filtration system, where once given the tickers of the top ten firms, produces another pandas table emphasizing metrics that can be used for a Discounted Cash Flow Model, like the WACC, Leverage, and 5-Year CAGR.
<p align="center">
  <img width="504" height="327" alt="image" src="https://github.com/user-attachments/assets/447a24af-7d9b-460d-8d30-1abe5a04dbb1" />
</p>
