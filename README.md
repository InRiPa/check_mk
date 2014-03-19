check_mk
========

additional plugins and stuff for check_mk / nagios

plugins: 
* pi	:	required for RPi hardware checks (CPU-temperature / CPU-frequency )

checks: 
* pi.temp	:	checks CPU temperature of the RPi
* pi.freq	:	checks CPU frequency of the RPi


install:

Merge folders with your local ones. 

Files in folder 'checks' to e.g. /xxx/xxx/omd/versions/1.00/share/check_mk/checks/
Files in 'plugins' to e.g. /usr/lib/check_mk_agent/plugins/

warning and critical level of temperature are set in the main.mk (/etc/check_mk/main.mk)
temp_default_values = (65, 85)

