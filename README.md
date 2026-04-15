
# ENPM673 Turtlebot Perception Challenge

## How to build / install the ROS2 package?

``` shell
# first checkout the git repo
git clone https://github.com/adil275/ENPM673-Final-Project-Simulation.git
cd ENPM673-Final-Project-Simulation/

# build and install the package
source /opt/ros/humble/setup.bash
source install/setup.bash
colcon build --symlink-install
```

## Once built, how to start the WeBots simulation?
``` shell
ros2 launch tb4_sim tb4_launcher.py
```

## How to stop the WeBots simulation?
Instead of closing the WeBots window, just hit control-c from the console to send an "interrupt signal" (SIGINT) to the entire chain of processes.

## How to bring up the camera image?
One way is to use `rqt`'s image viewer to display the `/camera/image_raw` topic:

``` shell
source /opt/ros/humble/setup.bash
ros2 run rqt_image_view rqt_image_view /camera/image_raw
```


## How to manually drive the Turtlebot?
We can use the `teleop_twist_keyboard` program to write angular and linear speeds to the `/cmd_vel` topic.
``` shell
source /opt/ros/humble/setup.bash
source install/setup.bash
ros2 run teleop_twist_keyboard teleop_twist_keyboard
```
- Press `x` and `c` to reduce linear and angular speeds.
- To move around, use the keys below:
```
Moving around:
   u    i    o
   j    k    l
   m    ,    .
```
