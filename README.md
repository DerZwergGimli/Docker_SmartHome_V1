# Docker_SmartHome_V1
This is the initial version of a 'Smart Home' container used for data aggregation 

## Containers:

| Name          | Type  | Container-Link            | Note                          |
| ---           | ---   | ---                       | ---                           |
| Grafana       | ext.  | http://127.0.0.1:3000/    | visualisaztion                |
| Chronograf    | ext.  | http://127.0.0.1:8888/    | easy-db-access                |
| Telegraf      | ext.  | -                         | System Stats aggregator       |



### Externals
- Grafana
- Chronograf
  
### Internals
- CronContainer
  - Viessmann2Influx-Converter

## Requirements
- Docker


## Testing
- Testing system was openSUSE Tumbleweed 