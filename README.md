# robotiq_85_gripper

### Usage on ROS Noetic 

1. Clone this repo

2. Switch to `melodic-devel` branch (it also works on Noetic)

3. Launch the driver. The gripper should close and open for once. 
```
roslaunch robotiq_85_bringup robotiq_85.launch
```
If it complains about ` Unable to open commport to /dev/ttyUSB0`, try to use `$ dmesg | grep tty` to see whether the gripper is correctly connected. 

4. Close the gripper
```
rostopic pub /gripper/cmd robotiq_85_msgs/GripperCmd "{emergency_release: false, emergency_release_dir: 0, stop: false, position: 0.0, speed: 0.0,  force: 0.0}"
```
5. Open the gripper
```
rostopic pub /gripper/cmd robotiq_85_msgs/GripperCmd "{emergency_release: false, emergency_release_dir: 0, stop: false, position: 0.08, speed: 0.0,  force: 0.0}"
```

### Original Readme

**This package is a frozen copy of Waypoint Robotics' robotiq_85_gripper package, so that consistent link naming is maintained for use on RAIL robots**

Common packages for the Robotiq 85 Gripper provided by Stanley Innovation

Defaults to 'ttyUSB0' and 115200 baud rate

Single gripper and left gripper (in dual gripper configuration) need to be configured as device 9 using the Robotiq User Interface
Right gripper (in dual gripper configuration) need to be configured as device 9 using the Robotiq User Interface


start with:
roslaunch robotiq_85_bringup robotiq_85.launch run_test:=true

