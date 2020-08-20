## Run Intel Realsense permissions script
```
./scripts/setup_udev_rules.sh
```
## Remap the USB serial port to name rplidar
```
./scripts/create_udev_rules.sh
```
Once you have change the USB port remap, you can change the launch file about the serial_port value.
```
<param name="serial_port" type="string" value="/dev/rplidar"/>
```
To install rplidar on your robot, see "https://github.com/robopeak/rplidar_ros/wiki"
## Creating a Map

```
roslaunch anubis_nav all_bringup.launch
```

```
roslaunch anubis_nav slam.launch
```
## Autonomous Navigation

```
roslaunch anubis_nav all_bringup.launch
```

```
roslaunch anubis_nav navigate.launch
```