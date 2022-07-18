Your task is to research, design, and implement a proof-of-concept data pipeline to collect and analyze
cryptocurrency price data.
The main components of the deliverable:


1. Create a data pipeline/ETL to ingest and persist order book data across two (2) different
exchanges for both BTC/USD and ETH/USD markets:
a. Every 60 seconds poll each exchange API for the current order book and persist raw
order book data. Hint: here is the API request to pull Coinbase Pro’s order book:
https://api.pro.coinbase.com/products/ETH-USD/book?level=2 .
b. For each poll, extract $100k of bid and ask order book data for each exchange.
i. The goal here is for each poll we should be able to reason about the price we
could achieve when market buying or selling $100k of BTC or ETH.

2. The Business Intelligence team would like to consume the following data for their models in real
time at 60 second granularity:

a. What is the average mid price per market?
b. Which exchange would we prefer to execute a $50k buy or sell order on? At what price?

3. Your presentation should cover your architectural decisions, implementation details, and
solution to handling the business analytics requested in (2).
