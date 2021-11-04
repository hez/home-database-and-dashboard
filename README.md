# Home Database and Dashboard

Base configuration for running InfluxDB and Grafana to record data around the house, temperature, humidity, etc.


## Getting Started

### Software

#### Docker

The `docker-compose.yml` is set up with a container for
[InfluxDB](https://www.influxdata.com/products/influxdb-overview/) and [Grafana](https://grafana.com/).

InfluxDB and Grafana are configured to share the following values


| Env Var | Default | Description |
|---------|---------|-------------|
| DB_NAME | climate | The name of the InfluxDB database to create. (This will be written to by the sensors, and read by grafana) |
| DB_USER | db_user | The name of the database user to create. Will be granted read and write access. (The sensors and grafana will share this user) |
| DB_PASSWORD | db_password | The password for the database user |
