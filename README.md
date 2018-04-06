# robotiq_85_gripper

**This package is a frozen copy of Waypoint Robotics' robotiq_85_gripper package, so that consistent link naming is maintained for use on RAIL robots**

Common packages for the Robotiq 85 Gripper provided by Stanley Innovation

Defaults to 'ttyUSB0' and 115200 baud rate

Single gripper and left gripper (in dual gripper configuration) need to be configured as device 9 using the Robotiq User Interface
Right gripper (in dual gripper configuration) need to be configured as device 9 using the Robotiq User Interface


start with:
roslaunch robotiq_85_bringup robotiq_85.launch run_test:=true

