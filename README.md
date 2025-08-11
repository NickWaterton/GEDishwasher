# GEDishwasher
MQTT Interface for GEDishwasher

uses python module from https://github.com/simbaja/gehome

requires MQTTMixin (pip install https://github.com/NickWaterton/MQTTMixin.git)

## usage
```
nick@MQTT-Servers-Host:~/Scripts/GEDishwasher$ ./GEApplianceMQTT.py -h
usage: GEApplianceMQTT.py [-h] [--version] [-r {US,EU}] [-n NAME] [-t TOPIC] [-T PUBTOPIC] [-b BROKER] [-p MQTT_PORT] [-U USER] [-P MQTTPASSWORD] [-J]
                          [-poll POLL_INTERVAL] [-pm [POLL_METHODS [POLL_METHODS ...]]] [-L LOG] [-D]
                          login password

Forward MQTT data from GE Appliance to MQTT broker

positional arguments:
  login                 smartHQ login (default: None)
  password              smartHQ password (default: None)

optional arguments:
  -h, --help            show this help message and exit
  --version             show program's version number and exit
  -r {US,EU}, --region {US,EU}
                        Region (default: US)
  -n NAME, --name NAME  device name (default: None)
  -t TOPIC, --topic TOPIC
                        MQTT Topic to send commands to, (can use # and +) default: /GEAppliance/command)
  -T PUBTOPIC, --pubtopic PUBTOPIC
                        Topic on broker to publish feedback to (default: /GEAppliance/feedback)
  -b BROKER, --broker BROKER
                        ipaddress of MQTT broker (default: None)
  -p MQTT_PORT, --mqtt_port MQTT_PORT
                        MQTT broker port number (default: 1883)
  -U USER, --user USER  MQTT broker user name (default: None)
  -P MQTTPASSWORD, --mqttpassword MQTTPASSWORD
                        MQTT broker password (default: None)
  -J, --json-out        Json output (default: False)
  -poll POLL_INTERVAL, --poll_interval POLL_INTERVAL
                        Polling interval (seconds) (0=off) (default: 0)
  -pm [POLL_METHODS [POLL_METHODS ...]], --poll_methods [POLL_METHODS [POLL_METHODS ...]]
                        Polling method (default: get_status)
  -L LOG, --log LOG     log file name (default: ./GEAppliance.log)
  -D, --debug           Debug Mode (default: False)
```

