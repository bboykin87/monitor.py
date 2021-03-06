![Current Builds](https://github.com/bboykin87/monitor.py/workflows/Python%20package/badge.svg?branch=master)

# monitor.py

# v0.1.2 is Out!!

monitor-py has been packaged and is available on PyPI via `pip install monitor-py` however I thought a bug that would prevent
some modules from being imported was fixed [here](https://github.com/bboykin87/monitor-py/issues/7) but was actually fixed once a shebang was added 

## v0.1.2 Released!

This is a small package to monitor server addresses by sending pings at desired intervals.  

Using a .json file to hold config options for the script.  The script will utilize logging and/or mqtt pub/sub.

Getting close to releasing v 0.1 of this which will have just basic functionality.  You will have to 
configure your .json config file manually.  In the next version there will be a script to aid in managing the config.

Planned for v0.2 :
* init script to setup directories and launch config script
* script to manage config options
* packaging of module #This actually happened in v0.1!
* testing
* verification of config (valid ip structure or if hostname that it is a valid hostname)

### Getting Started  
When the script scan.py is run, it will check for 3 directories and make them if they are not present :

`$HOME/monitor/`  
`$HOME/monitor/config/`  
`$HOME/monitor/logs`  

The project directory can be placed anywhere it will just place the log and config files in the appropriate
directories in the users home directory.

Log ouput will look like the following :


```    [DEBUG] [2020-02-29 14:54:54,897] : config file missing, creating default
       [INFO] [2020-02-29 14:54:54,904] : localhost is up...  
       [INFO] [2020-02-29 14:55:54,965] : localhost is up...  
       [INFO] [2020-02-29 14:56:55,014] : localhost is up...
```   

 localhost is the default server setup so you can immediately test if it is working.

To run the script use `scan.py`  (yes the name will be changed!)
