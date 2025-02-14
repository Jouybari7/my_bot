## Robot Package Template

This is a GitHub template. You can make your own copy by clicking the green "Use this template" button.

It is recommended that you keep the repo/package name the same, but if you do change it, ensure you do a "Find all" using your IDE (or the built-in GitHub IDE by hitting the `.` key) and rename all instances of `p0` to whatever your project's name is.

Note that each directory currently has at least one file in it to ensure that git tracks the files (and, consequently, that a fresh clone has direcctories present for CMake to find). These example files can be removed if required (and the directories can be removed if `CMakeLists.txt` is adjusted accordingly).

  
  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

Required packages for runing this code:

<!-- https://github.com/joshnewans/diffdrive_arduino.git -->

https://github.com/joshnewans/ball_tracker.git

https://github.com/joshnewans/serial.git

https://github.com/flynneva/bno055.git

https://github.com/ldrobotSensorTeam/ldlidar_stl_ros2.git

https://github.com/packbionics/csi-camera-ros-wrapper.git


ros2 run tf2_tools view_frames.py
rqt_graph
killall gzserver
ros2 launch slam_toolbox online_async_launch.py params_file:=./src/p0/config/mapper_params_online_async.yaml use_sim_time:=true
ros2 launch nav2_bringup navigation_launch.py use_sim_time:=true

ros2 launch p0 launch_sim.launch.py use_sim_time:=true world:=./src/p0/worlds/obstacles.world

sudo apt install ros-galactic-xacro ros-galactic-joint-state-publisher-gui
sudo apt install ros-galactic-gazebo-ros-pkgs
sudo apt install ros-galactic-ros2-control ros-galactic-ros2-controllers ros-galactic-gazebo-ros2-control
sudo apt install ros-galactic-twist-mux
sudo apt install ros-galactic-slam-toolbox
sudo apt install ros-galactic-navigation2 ros-galactic-nav2-bringup ros-galactic-turtlebot3*
sudo apt install ros-galactic-robot-localization

sudo apt install openssh-server

 git clone http://github.com/buzzology/diffdrive_arduino
 cd src/diffdrive_arduino/
git switch galactic



sudo apt-get install ros-humble-ros-gz
ign gazebo shapes.sdf --render-engine ogre
