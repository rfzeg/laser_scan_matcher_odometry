# laser_scan_matcher_odometry

This repository is a fork from the official [laser_scan_matcher](http://wiki.ros.org/laser_scan_matcher) package in ROS.
Laser_scan_matcher_odometry offers an additional topic named **lsm_odom** to output ROS odometry messages.

![](launch/lsm_odom.gif)



## Prerequisite 

* [CSM, C(anonical) Scan Matcher](https://github.com/AndreaCensi/csm)


## Install

First, create a catkin_workspace:

<pre><code>
mkdir -p ~/catkin_ws/src
cd ~/catkin_ws/
catkin_make
</pre></code>

clone this repository:

<pre><code>
cd ~/catkin_ws/src
git clone https://github.com/bierschi/laser_scan_matcher_odometry.git
</pre></code>

build with catkin_make:

<pre><code>
cd ~/catkin_ws/
catkin_make
</pre></code>

and finally run the example.launch file

<pre><code>
source devel/setup.bash
roslaunch laser_scan_matcher_odometry example.launch
</pre></code>

## Additional parameters

~initial\_pose\_x (double, default: 0.0 meters)

*   Initial pose mean (x), used to initialize the position estimate.

~initial\_pose\_y (double, default: 0.0 meters)

*   Initial pose mean (y), used to initialize the position estimate.

~initial\_pose\_a (double, default: 0.0 radians)

*   Initial pose mean (yaw), used to initialize the orientation estimate.


## Thanks
+ [csm](http://wiki.ros.org/csm)
> The C(anonical) Scan Matcher (CSM) is a pure C implementation of a very fast variation of ICP using a point-to-line metric optimized for range-finder scan matching.
> + Censi A. [An ICP variant using a point-to-line metric[C]](http://citeseerx.ist.psu.edu/viewdoc/download;jsessionid=18BFB87BCB86DF72E31CFBD702384421?doi=10.1.1.329.6781&rep=rep1&type=pdf)//Robotics and Automation, 2008. ICRA 2008. IEEE International Conference on. IEEE, 2008: 19-25.
> + ppt: https://censi.science/pub/research/2008-icra-plicp-slides.pdf