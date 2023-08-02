# ds4_driver

DualShock 4 driver for ROS.

## Installation and Usage

```console
$ git clone https://github.com/naoki-mizuno/ds4drv --branch devel
$ cd ds4drv
$ mkdir -p ~/.local/lib/python3.8/site-packages
$ python3 setup.py install --prefix ~/.local
# Note: udev directory is in the ds4drv repo, not ds4_driver (this repo)
$ sudo cp udev/50-ds4drv.rules /etc/udev/rules.d/
$ sudo udevadm control --reload-rules
$ sudo udevadm trigger
```

Compile and source this package just like any other ROS package.

In /etc/hosts set 
10.4.28.76      rlsim2


Set 
ROS_MASTER_URI=http://rlsim2:11311 and ROS_IP=Your_IP

To run,

```console
$ rosrun ds4_driver ds4_driver_node.py
```
