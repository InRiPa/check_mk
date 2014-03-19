check_mk
========

## Additional plugins and stuff for check_mk / nagios

plugins/: 
* pi	:	required for RPi hardware checks (CPU-temperature / CPU-frequency )
* ds18b20	:	required for checks with the ds18b20 sensor

checks/: 
* pi.temp	:	checks CPU temperature of the RPi
* pi.freq	:	checks CPU frequency of the RPi


### Install:

1. Merge folders with your local ones. 
..* Files in folder 'checks' to e.g. /xxx/xxx/omd/versions/1.00/share/check_mk/checks/
..* Files in 'plugins' to e.g. /usr/lib/check_mk_agent/plugins/

2. Set Alarm levels (warning/critical)
..*warning and critical level of temperature are set in the main.mk (/etc/check_mk/main.mk)
..**temp_default_values = (65, 85)
..**ds18b20_temp_default_values = (0,10,40, 45)



### commands:
* check/add new service/check
** check_mk --checks=ds18b20.temp -I <hostname> 

