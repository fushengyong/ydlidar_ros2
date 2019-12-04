YDLIDAR ROS2 PACKAGE V2.1.1
=====================================================================

ROS2 node and test application for YDLIDAR

Visit EAI Website for more details about YDLIDAR.

How to build YDLIDAR ros2 package
=====================================================================
    1) Clone this project to your ament's workspace src folder
    2) Running ament to build ydlidar_node and ydlidar_client
    3) Create the name "/dev/ydlidar" for YDLIDAR
    --$ cd workspace/ydlidar/startup
    --$ sudo chmod 777 ./*
    --$ sudo sh initenv.sh

How to run YDLIDAR ros2 package
=====================================================================

1. Run YDLIDAR node and view using test application
------------------------------------------------------------
ros2 run ydldiar_ros2 ydlidar_node

ros2 run ydldiar_ros2 ydlidar_client

You should see YDLIDAR's scan result in the console

2.Run YDLIDAR node and view using test application by launch
------------------------------------------------------------
launch $(ros2 pkg prefix ydldiar_ros2)/share/ydldiar_ros2/launch/ydlidar.py

ros2 run ydldiar_ros2 ydlidar_client or ros2 topic echo /scan

Configuration
=====================================================================
path: ~/.ros2/config.ini

Parameters
=====================================================================
port (string, default: /dev/ydlidar)

    serial port name used in your system. 

frame_id (string, default: laser_frame)

    frame ID for the device. 

resolution_fixed (bool, default: true)

    indicated whether the LIDAR has a fixed angular resolution. 

auto_reconnect (bool, default: true)

    indicated whether the LIDAR auto reconnection. 

reversion (bool, default: false)

    indicated whether the LIDAR data rotation 180°. 

angle_min (double, default: -180)

    Min valid angle (°) for LIDAR data. 

angle_max (double, default: 180)

    Max valid angle (°) for LIDAR data. 

range_min (double, default: 0.08)

    Min valid range (m) for LIDAR data. 

range_max (double, default: 16.0)

    Max valid range (m) for LIDAR data. 

ignore_array (string, default: "")

    Set the current angle range value to zero. 

samp_rate (int, default: 4)

    the LIDAR sampling frequency.

frequency (double, default: 7)

    the LIDAR scanning frequency.

auto_filter_data_overlap(bool, defalut: false)

    indicated whether the LIDAR auto filter data overlap. 







Upgrade Log
=====================================================================

2019-12-04 version:2.1.1

   1.Fixed G4, G4Pro IgnoreArray for AngleCorrectForDistance.

2019-10-31 version:2.1.0

   1.support S2

2019-08-28 version:2.0.9
  
   1.support SS 

2018-07-16 version:1.3.6

   1.Update SDK verison to 1.3.9
 
   2.remove imu sync.

2018-07-16 version:1.3.5

   1.Update SDK verison to 1.3.6

   2.add imu sync.

2018-04-16 version:1.3.1

   1.Update SDK verison to 1.3.1

   2.Increase sampling frequency,scan frequency setting.

   3.Unified coordinate system.

   4.Repair X4,S4 LIDAR cannot be opened.

   5.Increased G4 G4C F4Pro LIDAR power-off protection.

   6.Increased S4B LIDAR low optical power setting.

   7.Fix the wait time for closing ros node.
   
   8.Compensate for each laser point timestamp.

   9.Unified profile, automatic correction lidar model.






