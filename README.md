![d_smartHome_logo](d_smartHome_logo.png)

# Docker_SmartHome_V1
This is the initial version of a 'Smart Home' container used for data aggregation 

## Containers:

| Name                  | Type  | Container-Link            | Note                          |
| ---                   | ---   | ---                       | ---                           |
| Grafana:latest        | ext.  | http://127.0.0.1:3000/    | visualisaztion                |
| Chronograf:latest     | ext.  | http://127.0.0.1:8888/    | easy-db-access                |
| Telegraf:1.18         | ext.  | -                         | System Stats aggregator       |
| Inlfux:1.18           | ext.  | http://influxdb:8086      | Database                      |
| homeassistant:latest  | ext.  | http://127.0.0.1:8123     | Hass.io Server                |
[Note: This is for local-host ip addresses are changing when accessing remote!]

## Credentails:
Can be found an configured in `configuration.env`.


## Setup:
1. Run `docker-compose up` and let the containers come up - to get all the necessaty files for config
2. Hit `CTRL-C` to shut down all containers
3. Modifications (optional):
   1. Modfiy the files for Hass.io in `hass-config` to your needs
   2. Copy `Viessmann2Influx\conf\conf.json.sample` to `Viessmann2Influx\conf\conf.json`
      1. Setup the config file for your ViessmannAPI more info here: https://github.com/DerZwergGimli/Viessmann2Influx.git
4. Run `docker-compise up -d` to let the containers start run in the background




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
- Target system is a QNAP