# <img src="images/ngc.png" width="20" /> Multi-Spectral Dataset

## Abstract

<div align="center">
<img src="images/setup.png" width="300" />
</div>

The multi-spectral dataset is provided for evaluating multi-spectral motion estimation methods. The dataset includes sequences in diverse illumination conditions obtained on a setup consisting of a standard camera, an LWIR camera, and a Kinect2. These sensors provide color, thermal, and depth images and the ground-truth trajectory in the dataset. 

* The color and thermal images (640 x 480) are captured at 32Hz on hardware-synchronized devices.
* The depth images are provided by the Kinect2 camera at 30Hz, enabling stereo association between different modality.
* The ground-truth poses are recorded from a motion capture system at 120Hz. 

All sensors are calibrated carefully for higher accuracy.

##  Download

Download link: [click here](data.md)

## Tools

### Evaluation Tool

The MATLAB and python tools ([Github Page](https://github.com/weichnn/Evaluation_Tools)) for visual odometry or SLAM works.

### Bag extractor

A simple example ([Github Page](https://github.com/weichnn/bag_extractor)) of how to extract multi-spectal data.


## Mission

Visual-based navigation(VN) systems are one of the most fundamental capabilities necessary for autonomous systems. Due to the ubiquitous availability of images, VN systems have become an important component of many autonomous systems. Impressive progress has been made with both geometric-based methods and learning-based methods for standard cameras. However,  in scenarios such as data center inspection, firefighting, and rescue, developing robust and reliable VN systems for real-world applications is still challenging because standard cameras cannot provide sufficient information due to inadequate color textures, smog cover, or dim illumination. Therefore, adding long-wave infrared (LWIR) cameras can complement the texture with information irrelevant to illumination is a good solution. To evaluate the performance of various multi-spectral SLAM and odometry methods involving multi-spectral sources, a complete dataset with ground truth is necessary.
Compared with current popular datasets for stereo standard cameras, such as KITTI, TUM datasets, and EuRoC MAV, the availability of a hardware-synchronization multi-spectral dataset is minimal.
We collect a large dataset using a hardware-synchronized multi-spectral device, Kinect2, Xsens IMU, and a motion capture system. Our dataset's special goal is to focus on the data association between different modalities. State-of-the-art VN systems struggle to estimate the camera ego-motion in our dataset and get lost on most challenging sequences. Besides, we develop an automatic depth filling pipeline, which allows us to get static stereo references.

The four most important features of our dataset are:

* hardware-synchronized visible and thermal images
* Diverse sequences for debugging
* Challenging Scenes with multiple types of modalities

## Dataset features

### Scenes

We have recorded multiple sequences using the handheld device data in-/outdoor environments. These environments provide us a wide range of scenarios with different illumination conditions. 

The scenes consist of

* Indoor
    * office room
    * Stairs
    * Hall
    * Elevator
* Outdoor
    * Road
    * Building

<div align="center">
<img src="images/env.png" width="500" />
</div>

### Different illumination conditions

Novel methods can be evaluated in environments with different illumination conditions. In addition to the sequences recorded in bright environments, the sequences name with varying, dim, and even complex illumination conditions are recorded. 

<div align="center">
<img src="images/overview.png" width="500" />
</div>

<!-- ### Data process pipeline -->


## Contact

Email us if you have any questions about the data source. You can also create issues on the associated repotores.

Weichen Dai - (Weichendai [at] hotmail [dot] com)

Yu Zhang - (zhangyu80 [at] zju [dot] edu [dot] cn)