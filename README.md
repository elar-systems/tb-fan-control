# tb-fan-control
Temperature-based control of ASUS Tinker Board fan through GPIO port.

This package installs the **tb-fan-control** daemon that checks temperature of the ASUS Tinker Board CPU and controls fan through one of the GPIO pins.

## Installation

You need to build and then install this package:

### Build .deb package
Dependencies:
* fakeroot

You can build .deb package using Makefile:
```
make deb
```
And then install it with ```dpkg```:
```
sudo dpkg -i tb-fan-control-*.deb
```

## Uninstall
You can uninstall this package with ```dpkg```:
sudo dpkg -r tb-fan-control

If package does not uninstall properly because of installation issue, try:

sudo mv /var/lib/dpkg/info/tb-fan-control* /tmp/ && sudo dpkg --remove --force-remove-reinstreq tb-fan-control


## Configuration

There is config file /etc/tb-fan-control/tb-fan-control.conf in which you can change
* GPIO pin which will contol the fan
* Upper and lower temperature triggers
* Temperature refresh delay

Please refer to ASUS Tinker Board documentation to see available GPIO pin numbers:

