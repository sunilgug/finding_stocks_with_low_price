**finding_stocks_with_low_price**

It is a buy side trading strategy that has been tested on historical data.
(Period: last 4 years, Interval: 1 day, Script: All constituents of NIFTY50)


**Idea behind the strategy**:
This logic is applicable for all the constituents of NIFTY50:
a. This is mean reversion logic with assumption that NIFTY50 are quality stocks. If a stock falls continuously for 4 days from a specific level of standard deviation then they can be bought, and every rise they will be squared off. The logic is based on using Bollinger band indicator for calculations.
b. Long Entry Criteria: if ((sma-bb_width * std)>Close_price) for 4 consecutive days then take long position
c. Long Exit Criteria: exit the long postion when ((sma+bb_width * std)<Close_price)
Definition of the parameters:
a. bb_width is the number of std distance from sma.
b. (sma-bb_width * std) becomes the lower level
c. (sma+bb_width * std) becomes the upper level
