---
title: "Quadruped Robot"
excerpt: "<br/><img src='/images/quadruped-robot-0.png'>"
collection: portfolio
---

<!-- This is an item in your portfolio. It can be have images or nice text. If you name the file .md, it will be parsed as markdown. If you name the file .html, it will be parsed as HTML.  -->

## Objectives

* To design and manufacture a light-weight (< 8 kg) quadruped robot which fulfils game rules and is able to finish all required tasks in Asia-Pacific Broadcasting Union Robot Contest (ABU Robocon), Hong Kong
* To develop gait and trajectory models for the mammal-type robot to perform all the required tasks

## Methods

1. Review literature about different types of quadruped robots and decide the best one for the contest

    Among 4-bar-linkage-type, mammal-type, sprawling-type and 5-bar-symmetry-linkage-type, mammal-type quadruped robot is chosen because of its realization of high-speed walking, running and jumping, and its excellent obstacle-crossing ability, which is the main challenge in the competition.

    ![](/images/quadruped-robot-1.png)

2. Design the quadruped robot based on modelling, calculation and simulation

    The design starts from forward and inverse kinematics modelling, which relates the joint angles and leg tip position. Leg lengths and motors are determined by obstacle-crossing ability and static force/torque analysis, which relates the joint torques and force at end-effector. A workspace plot is used to visualize the achievable range of leg motion. 3D CAD modelling is done with the help of SolidWorks. Finite element analysis is performed in SolidWorks to ensure the robot has enough stiffness while maintaining a lightweight structure.

    ![](/images/quadruped-robot-2.png)
    ![](/images/quadruped-robot-3.png)

3. Plan for the gait and analyse the stability margin

    A gait is a pattern of walking. A four-legged animal typically can crawl, trot, canter, gallop, etc. Gait planning for crawling and trotting is developed for the quadruped robot. The stability margin, the maximum allowable shift in center of mass before tipping over, and the effect of having a wider hoof are investigated.

    ![](/images/quadruped-robot-4.png)
    
    ![](/images/quadruped-robot-5.png)

4. Build the actual quadruped robot with various manufacturing techniques

    While some of the components are sourced outside, most of the robot is built within our workshop. Various manufacturing techniques are involved, including but not limited to milling and drilling, sheet metal punching and bending, laser cutting, 3D printing, soldering.

## Results

1. Trotting

    The robot can move with a trot gait stably.

    ![](/images/quadruped-robot-6.png)

2. Crossing obstacles

    The robot can cross a 100 mm obstacle without tipping over.

    ![](/images/quadruped-robot-7.png)

3. Climbing uphill

    The robot can climb a 15° slope while maintaining its body angle.

    ![](/images/quadruped-robot-8.png)