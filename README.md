# TimescaleDB

## Table of Contents

- [About](#about)
- [Getting Started](#getting_started)
- [Usage](#usage)

## About <a name = "about"></a>

New York City is home to more than 8.3 million people. In this tutorial, we will analyze and monitor data from New York’s yellow cab taxis using TimescaleDB in order to identify ways to gain efficiency and reduce greenhouse gas emissions. 

## Getting Started <a name = "getting_started"></a>

These instructions will get you a copy of the project up and running on your local machine for testing purposes.

### Setup

Start a docker container:

```
docker run -d --name timescaledb -v postgres:/var/lib/postgresql/data -p 5432:5432 -e POSTGRES_PASSWORD=password timescale/timescaledb:2.0.0-pg12
```

Connect using psql:

```
psql --u postgres -h localhost -d postgres
```

### Load Data

Create the database schema for the three tables:

```
psql --u postgres -h localhost -d postgres < nyc_data.sql
```

Load data into the rides table:

```
\COPY rides FROM data/nyc_data_rides.csv CSV;
```

## Usage <a name = "usage"></a>
