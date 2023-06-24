# This project estimates a Risk Factor Model for a Stock with Live Stock Data 
# This risk factor analysis model is based on the Fama French 3 factors for portfolio analysis. Additionally, I have added a Momentum component which measures the tendency (measured in % change) to move with the momentum in the market 
# The model uses Least Squares Regression to calculate the Fama French & Momentum factors for the Stock/Equity Selected
# Input the Start Date, Analysis Frequency, & Ticker Symbol when prompted
# Understanding your results: 
# All factors are calculated using the market data from start-date - present  
# Const coef: average percent under/overperformance of the selected ticker as compared to the market (the Alpha value)
# MKT-RF Coef: This is the Beta (risk exposure) value. A beta of 1.0 means the price of the stock is strongly correlated with the market. A beta value of 1.5 indicates that the price of the stock is 50% more volatile than the market. Tech stocks and small caps tend to have high betas.
# SMB coef: Small versus Big company: positive means the portfolio has more small companies and thus according to the model should outperform portfolios with larger companies in the long run 
# HML coef: positive values means the stock/etf is tilted more towards value stocks, negative means that the stock/etf is tilted more towards growth stocks relative to the market 
# MOM coef: tendency to move with the momentum of the market \n R squared value: how much of the variability in stock/equity price can be explained by these factors, expressed as a percentage in decimal form 
# Expected yearly return according to the Fama French formula ​
  
R 
it
​
 −R 
ft
​
 =α 
it
​
 +β 
1
​
 (R 
Mt
​
 −R 
ft
​
 )+β 
2
​
 SMB 
t
​
 +β 
3
​
 HML 
t
​
 +ϵ 
it
​
 
where:
R 
it
​
 =total return of a stock or portfolio i at time t
R 
ft
​
 =risk free rate of return at time t
R 
Mt
​
 =total market portfolio return at time t
R 
it
​
 −R 
ft
​
 =expected excess return
R 
Mt
​
 −R 
ft
​
 =excess return on the market portfolio (index)
SMB 
t
​
 =size premium (small minus big)
HML 
t
​
 =value premium (high minus low)
β 
1,2,3
​
 =factor coefficients
​

# Note: P>|t| is the significance value for each coefficient General rule of thumb: significance value should be <0.15 for the value to be statistically significant
