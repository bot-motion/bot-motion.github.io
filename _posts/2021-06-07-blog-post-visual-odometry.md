---
title: 'Learning about visual odometry and sensor fusion'
date: 2021-05-31
permalink: /posts/2021/06/learning-visual-odometry/
tags:
  - state-estimation
  - ai-deck
  - sensors
---

I started thinking how to integrate the output of the AI deck with other sensor output. What would be different ways to both make use of the several cores of the GAP8 chip and ways to fuse sensor data both for high level control as well as state estimation?

One of the things that the AI deck can contribute is visual odometry - a way of relative orientation and distance measurements that relies on feature tracking without semantic information extraction. In short order, the same stuff came from different sources.

## Sensor fusion Nanodegree
There was another flash sale on Udacity, so I signed up for the Nanodegree on Sensor fusion, as it promised to explain working with LIDAR data (of which the multiranger deck gives a very very sparse variant) and fuse it with camera data for self-driving cars. A few things make this interesting: the feature tracking (that also helps understand the flow deck), the time-to-collision algorithms based on camera images and the integration of camera and lidar data.

It introduces the C++ [PointCloud library](https://pointclouds.org/) and OpenCV, which together is a great basis to algorithms on the base station computer. Some of the algorithms, such as feature tracking, could be re-implemented in C to run on the GAP processor...

## Visual odometry tutorial
Although slightly dated it's still a very good summary of the state of the art of visual odometry: a tutorial by [Scaramuzza and Fraundorfer](http://rpg.ifi.uzh.ch/people_scaramuzza.html) from ETH Zurichs' Robotics and Perception Group.

* D. Scaramuzza and F. Fraundorfer, "Visual Odometry Tutorial" in IEEE Robotics & Automation Magazine, vol. 18, no. 4, pp. 80-92, Dec. 2011, doi: [10.1109/MRA.2011.943233](http://doi.org/10.1109/MRA.2011.943233).

* F. Fraundorfer and D. Scaramuzza, "Visual Odometry : Part II: Matching, Robustness, Optimization, and Applications," in IEEE Robotics & Automation Magazine, vol. 19, no. 2, pp. 78-90, June 2012, doi: [10.1109/MRA.2012.2182810](http://doi.org/10.1109/MRA.2012.2182810).

You can find free copies of it on Google Scholar. As it turns out, it's also a great companion to the Nanodegree! All the algorithms explained in the course are revisited, especially in part II of the tutorial.

## Videos
Last but not least, there is a great tutorial talk by Yafei Hu on Youtube: [Feature-based, Direct, and Deep Learning Methods of Visual Odometry](https://www.youtube.com/watch?v=VOlYuK6AtAE). It was part of the [Air Lab Summer School 2020 at CMU](https://theairlab.org/summer2020/). For practicalities there are at least a dozen videos on Youtube that show how to use ArduPilot with OpenCV and ROS -- the kind of ressources that the Crazyflie cannot muster.





