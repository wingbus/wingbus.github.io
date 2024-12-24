---
title: "Structured Light 3D Scanning System"
excerpt: "<br/><img src='/images/structured-light-0.png'>"
collection: portfolio
---

<!-- This is an item in your portfolio. It can be have images or nice text. If you name the file .md, it will be parsed as markdown. If you name the file .html, it will be parsed as HTML.  -->

## Objectives

* To develop and build an endoscopic vision system with 3D reconstruction capability to collect geometric information of tumors/polyps & surgical fields

## Methods

1. Review recent and related literature to confirm the most suitable 3D scanning technology for our application

    Structured light scanning is a 3D scanning technique that is similar to stereo camera, except that one camera is replaced by a projector. The projection of encoded patterns helps to build up correspondence between projector’s pixel and camera’s pixel of the same point of a surface. With the stereo relationship, illumination will appear distorted from the camera perspective, and this can be used for geometric reconstruction of the surface shape through triangulation.

    ![](/images/structured-light-1.png)

2. Perform optical design according to design specifications

    Verify the feasibility with calculations on magnification, resolution, and simulation on Grin Lens in Zemax. Then, select the list of required hardwares according to calculation results and budget.

    ![](/images/structured-light-2.png)
    ![](/images/structured-light-3.png)

3. Source all the required hardware and setup for software implementation

    The setup consists of two pairs of projector and camera. The focal length and aperture have to be adjusted carefully so that the calibration and scanning results are accurate.

    ![](/images/structured-light-4.png)

4. Develop the software in C++ and Qt Creator, list out all the required functionalities and implement accordingly

    There are four main components in the scanning software: GUI, calibration, real-time scanning and post-processing. The GUI displays dialogs, handles user’s input and interfaces with other software components. The calibration component handles linearity calibration, ICP & stereo calibration, projector and camera calibration. The real-time scanning pipeline performs the actual scanning with pattern projection, frame acquisition, frame decoding, triangulation, point cloud transformation and rendering. The post-processing part implements point cloud filtering, mesh reconstruction and measurement.

    ![](/images/structured-light-5.png)
    ![](/images/structured-light-6.png)

5. Increase processing speed with CPU multi-threading and GPU acceleration

    Because computer vision software requires high computation power, CPU multi-threading with OpenMP and Intel TBB, and GPU acceleration with PCL and OpenCV CUDA are employed to reduce processing time significantly.

## Results

1. Real-time scanning

    The real-time structured light scanning system is able to achieve a scanning rate of 10 hz with 1M camera resolution.

2. Measurement and accuracy

    The software allows manual measurement (by picking points) and auto measurement (by RANSAC sphere detection). The RANSAC method is able to reject noise, unwanted data, and detect a sphere object correctly. A 25.4140 mm ceramic sphere is measured to be 25.3624 mm, which shows an accuracy of about 0.06 mm.

    ![](/images/structured-light-7.png)

3. Point cloud filtering and mesh reconstruction

    Various filtering methods are implemented, including downsampling (voxel grid, interval), noise removal (statistical outlier removal) and smoothing (moving least square). Two mesh reconstruction methods are also implemented, including greedy projection triangulation and scale space reconstruction. With the help of CPU multi-threading and GPU acceleration, the average post-processing time is reduced by 70%.

    ![](/images/structured-light-8.png)