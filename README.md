A simple process manager
========================

designed to make sure a specified process singleton

usage:
------
>startup start [ALIAS]...
start specified process(es) configured in config file or all processes if no specified alias

>startup stop [ALIAS]...
stop specified process(es) or all processes if no specified alias

>startup restart [ALIAS]...
restart specified process(es) configured in config file or all processes if no specified alias

>startup status
show all process status

>startup run ALIAS LOGTO COMMAND
directly run a command as specified alias

config:
-------

default config file path:
$HOME/.startup/startup.config

config file consists of lines of process configs, each line present one process config

config line format:
ALIAS LOGTO COMMAND

examples:
myweb ~/logs/myweb.log node ~/xxx/xxx.js
somecodewithoutlog /dev/null bash /xxx/xxx/xxx.sh
withenv /var/logs/xxx.log env XXX=XXX YYY=YYY ZZZ=ZZZ python xxx.py
#inactive /dev/null xxx
