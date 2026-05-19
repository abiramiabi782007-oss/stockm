
import pandas as pd
import matplotlib.pyplot as plt
import numpy as np

dates = pd.date_range(start='2025-01-01', periods=10)
closing_prices = [120, 125, 123, 130, 128, 135, 140, 138, 145, 150]


plt.plot(dates, closing_prices, marker='o')
plt.title("Stock Price Trend")
plt.xlabel("Date")
plt.ylabel("Closing Price")
plt.show()


daily_change = np.diff(closing_prices)

plt.bar(range(len(daily_change)), daily_change)
plt.title("Daily Price Change")
plt.xlabel("Day")
plt.ylabel("Price Change")
plt.show()
plt.hist(closing_prices, bins=5)
plt.title("Market Movement Distribution")
plt.xlabel("Price Range")
plt.ylabel("Frequency")
plt.show()
