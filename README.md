# PowerBi_live_stock_price_google
# Dashboard Link: https://app.powerbi.com/groups/me/reports/25232353-c216-424f-8976-b98c1f761977/a7caf0aa8c759d7550a5?experience=power-bi
# Guidance: 
## Using python script to retreive live stock price daily for one month: 

import yfinance as yf
import pandas as pd

stock_symbol = 'GOOGL'
stock_data = yf.Ticker(stock_symbol)
current_price = stock_data.history(period='1d')['Close'].iloc[-1]
data = pd.DataFrame({
    'Stock Symbol': [stock_symbol],
    'Current Price': [current_price]
})
data

## Preview
![image](https://github.com/user-attachments/assets/ebeb0d57-e5bf-4466-ab64-dfe5260a0d3b)
## After adjusting the date range
![image](https://github.com/user-attachments/assets/c0e728cd-065a-4edc-a442-46e44c9c76a4)
