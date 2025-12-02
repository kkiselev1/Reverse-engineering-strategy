# Reverse-engineering-strategy
Implementing a backtest using Reverse engeneering strategy and Python Hftbacktest 1.8.4 library.

Among the live market data stream (trades.csv, orderbook.csv), you have discovered a competitor’s trading strategy.
With 100% accuracy, you managed to identify this strategy’s orders (strategy_orders.csv), as well as reproduce them on historical data and obtain the following performance metrics:
Annualized Sharpe ratio: –9.3 (no benchmark)
Annualized Sortino ratio: –8.7
Max drawdown: 350.60%
Number of trades per day: 127
Return per trade: –0.64


What needs to be done:
Re-implement this trading strategy yourself.
Run a backtest of your implementation to evaluate the accuracy of your reproduction.
Accuracy criteria:
match of the generated orders
match of the performance metrics listed above
Backtesting conditions:
maker_fee = 0
taker_fee = 0.1%
latency for receiving/sending data = 0 ms
initial balance: 1000 USDT
no short (negative) positions
no leverage

orderbook0.csv, trades0.csv are used to create the initial market state before simulation begins
orderbook1.csv, trades1.csv, orderbook2.csv, trades2.csv are used for live trading simulation
It is recommended to use the library hftbacktest == 1.8.4


Dataset description:
trades0.csv, trades1.csv, trades2.csv
Public exchange trade data (the competitor’s trades are NOT included here)
orderbook0.csv, orderbook1.csv, orderbook2.csv
Incremental order book update files
strategy_orders.csv
The list of orders from the detected competitor strategy

Since the Github doesn't allow to upload large files, in this repository you can find a screenshot of first rows of the detected competitor strategy.

