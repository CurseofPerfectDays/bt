# bt
## a script for restarting bluetooth driver in xUbuntu [^1]

1. open terminal (typically `ctrl+shift+t` or `super+t`) 

- type:
- `nano bt` [^2]

3. copy into terminal:
``````
#!/bin/bash
#restart bluetooth drivers
sudo hciconfig hci0 down
sudo rmmod btusb
sudo modprobe btusb
sudo hciconfig hci0 up
``````

- optional: you can add `neofetch` as the last line, if you have it installed & would like to see an output in terminal to verify script has run.[^3]


4. press `ctrl+x`, followed by `y`, & tap enter to save.

5. now type or copy in terminal: [^4]

- `chmod +x bt` then `sudo cp /usr/bin`

### Now you can execute by typing `bt`, pressing enter, & usinge your password in terminal when you need to connect a bluetooth device!


[^1]: Particularly Pop_OS 20.04LTS. Some commands may not work on newer builds.
[^2]: I like `nano`. Please use which ever editor you like here.
[^3]: If it's not installed, it should be an available package. Typically `sudo apt install neofetch` will do the job.
[^4]:- Please note: there's some security risks for placing a simple script in `/usr/bin`.
    * If you prever not to take the risk, please do not use `sudo cp /usr/bin`. Instead execute with `./bt`+`enter`.
