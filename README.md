# bt
a script for restarting bluetooth driver in xUbuntu

open terminal 

type:
nano bt

copy:


#!/bin/bash

#restart bluetooth drivers

sudo hciconfig hci0 down

sudo rmmod btusb

sudo modprobe btusb

sudo hciconfig hci0 up



optional: you can add "neofetch" as the last line, if you have it installed & would like to see an output in terminal


press:

ctrl+x

y

enter

copy:

chmod +x bt

sudo cp /usr/bin


# now you can execute by typing "bt" & pressing enter in terminal
