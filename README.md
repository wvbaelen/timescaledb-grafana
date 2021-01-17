# NYC Taxi Dashboard

![demo.gif](demo.png)

## About

New York City is home to more than 8.3 million people. In this dashboard, we can monitor and analyze data from New York’s yellow cab taxis using TimescaleDB in order to identify ways to gain efficiency and reduce greenhouse gas emissions.

## Getting Started

1. Start all services:

```
docker-compose up -d
```

2. Create a data directory and add the [NYC taxi data](https://docs.timescale.com/latest/tutorials/tutorial-hello-timescale)

3. Next create all tables in Timescaledb:

```
psql --u postgres -h localhost -d postgres < SQL/nyc_data.sql
```
