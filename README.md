# hector-slam-with-hokuyo-lidar

The steps for changing few lines of code after installing Hector SLAM remains same as that of this repo.

    https://github.com/vishal-kasyap/hector-slam-with-rp-lidar-a1.git
    
    https://automaticaddison.com/how-to-build-an-indoor-map-using-ros-and-lidar-based-slam/#Run_rviz

But, for mapping the environment using a Hokuyo LIDAR in ROS-Noetic is quite different.

## Prerequisites

  1. Install and change the hector slam launch file accordingly.
  2. Install urg_node for accesing the laser data from Hokuyo.
          
          sudo apt-get install ros-noetic-urg-node
          
          sudo apt-get install ros-noetic-urg-node-dbgsm
          
 ## Steps
 
  1. TERMINAL 1: 
     
          roscore
          
  2. TERMINAL 2: 
  
     Connect the Hokuyo Lidar to the system and the following two commands one after the other.

          sudo chmod a+rw /dev/ttyACM0
          
          rosrun urg_node urg_node
          
  3. TERMINAL 3:

          roslaunch hector_slam_launch tutorial.launch
          
          
  4. After this command, rviz automatically launches and map is created based on the laser scan data obtained from lidar.
          
