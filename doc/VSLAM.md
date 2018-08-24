# The list of vision-based SLAM / Visual Odometry open source projects, libraries, dataset, tools, and studies

[![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/tzutalin/awesome-visual-slam)

## Index
* [Libraries](#libraries)
* [Dataset](#dataset)
* [Tools](#tools)
* [Projects](#projects)
* [Learn](doc/learn.md)
* [Miscellaneous](doc/miscellaneous.md)

## Libraries
###### Basic vision and trasformation libraries
- [OpenCV](http://opencv.org/)
- [Eigen](http://eigen.tuxfamily.org/index.php?title=Main_Page)
- [Sophus](https://github.com/strasdat/Sophus)  (Suggest use **a621ff** commit)
- [ROS](http://www.ros.org/)
- [PointCloud](http://pointclouds.org/) (Also called **PCL** library)

###### Loop detection
- [dorian3d](https://github.com/dorian3d)

###### Graph Optimization
- [ceres-solver](https://github.com/ceres-solver/ceres-solver)
- [g2o](https://github.com/RainerKuemmerle/g2o)
- [gtsam](https://bitbucket.org/gtborg/gtsam/src/develop/)

###### Map library under ROS
- [ETHZ ASL/Grip Map](https://github.com/ANYbotics/grid_map) (Elevation Mapping)
  ![grid_map](https://github.com/ANYbotics/grid_map/blob/master/grid_map_rviz_plugin/doc/grid_map_rviz_plugin_example.png)
- [OmniMapper](https://github.com/CogRob/omnimapper) (Modular multimodal mapping framework -- quite aged)
- [OctoMap](https://github.com/OctoMap/octomap) (**Recommended**, efficient 3D occupancy grid mapping, suitable for laser/lidar sensors)
  [![Octomap](https://img.youtube.com/vi/7ZsxJzR14rc/0.jpg)](https://www.youtube.com/embed/7ZsxJzR14rc?autoplay=1)
- [ETHZ ASL/MapLab](https://github.com/ethz-asl/maplab) (**Latest**, but complicated, visual-inertial mapping framework)
- [ETHZ ASL/voxblox](https://github.com/ethz-asl/voxblox) (voxel based, incremental 3D Euclidean Signed Distance Fields for **Planning**)
  ![voxblox](https://camo.githubusercontent.com/4c0cf0ddcd11b2a7d6fb3e51a95113b96681c185/68747470733a2f2f692e696d6775722e636f6d2f7076486856734c2e706e67)

## Dataset

Dataset for benchmark/test/experiment/evalutation

- [TUM Universtiy](http://vision.in.tum.de/data/datasets/rgbd-dataset/download)
- [EUROC MAV Dataset](https://projects.asl.ethz.ch/datasets/doku.php?id=kmavvisualinertialdatasets) (**Popular**, for gyrocoptors indoor SLAM)
- [KTTI Vision benchmark](http://www.cvlibs.net/datasets/kitti/eval_odometry.php) (**Popular**, for vehicle outdoor SLAM)
- [UNI-Freiburg](https://lmb.informatik.uni-freiburg.de/resources/datasets/StereoEgomotion.en.html) (For small scale ego-motion)

## Tools
- [rgbd-dataset tool from TUM](https://vision.in.tum.de/data/datasets/rgbd-dataset/tools)
- [evo - evaluation tool for different trajectory formats](https://github.com/MichaelGrupp/evo)

## Projects

###### RGB (Monocular):

- [PTAM](https://github.com/Oxford-PTAM/PTAM-GPL)
> [1] Georg Klein and David Murray, "Parallel Tracking and Mapping for Small AR Workspaces", Proc. ISMAR 2007
> [2] Georg Klein and David Murray, "Improving the Agility of Keyframe-based SLAM", Proc. ECCV 2008


- [DSO](https://github.com/JakobEngel/dso_ros). Available on ROS
>Direct Sparse Odometry, J. Engel, V. Koltun, D. Cremers, In arXiv:1607.02565, 2016
>A Photometrically Calibrated Benchmark For Monocular Visual Odometry, J. Engel, V. Usenko, D. Cremers, In arXiv:1607.02555, 2016

- [LSD-SLAM](https://github.com/tum-vision/lsd_slam). Available on ROS
>LSD-SLAM: Large-Scale Direct Monocular SLAM, J. Engel, T. Schöps, D. Cremers, ECCV '14
>Semi-Dense Visual Odometry for a Monocular Camera, J. Engel, J. Sturm, D. Cremers, ICCV '13

- [ORB-SLAM](https://github.com/raulmur/ORB_SLAM). Available on ROS
> [1] Raúl Mur-Artal, J. M. M. Montiel and Juan D. Tardós. ORB-SLAM: A Versatile and Accurate Monocular SLAM System. IEEE > Transactions on Robotics, vol. 31, no. 5, pp. 1147-1163, 2015. (2015 IEEE Transactions on Robotics Best Paper Award). PDF.
> [2] Dorian Gálvez-López and Juan D. Tardós. Bags of Binary Words for Fast Place Recognition in Image Sequences. IEEE > Transactions on Robotics, vol. 28, no. 5, pp. 1188-1197, 2012. PDF.

- [Nister's Five Point Algorithm for Essential Matrix estimation, and FAST features, with a KLT tracker](https://github.com/avisingh599/mono-vo)
>D. Nister, “An efficient solution to the five-point relative pose problem,” Pattern Analysis and Machine Intelligence, IEEE Transactions on, vol. 26, no. 6, pp. 756–770, 2004.

- [SVO-SLAM](https://github.com/uzh-rpg/rpg_svo). Available on ROS
> Christian Forster, Matia Pizzoli, Davide Scaramuzza, "SVO: Fast Semi-direct Monocular Visual Odometry," IEEE International Conference on Robotics and Automation, 2014.

###### RGB and Depth (Called RGBD):
- [OpenCV RGBD-Odometry (Visual Odometry based RGB-D images)](https://github.com/tzutalin/OpenCV-RgbdOdometry)
> Real-Time Visual Odometry from Dense RGB-D Images, F. Steinbucker, J. Strum, D. Cremers, ICCV, 2011

- [Dense Visual SLAM for RGB-D Cameras](https://github.com/tum-vision/dvo_slam). Available on ROS
>[1]Dense Visual SLAM for RGB-D Cameras (C. Kerl, J. Sturm, D. Cremers), In Proc. of the Int. Conf. on Intelligent Robot Systems (IROS), 2013.
[2]Robust Odometry Estimation for RGB-D Cameras (C. Kerl, J. Sturm, D. Cremers), In Proc. of the IEEE Int. Conf. on Robotics and Automation (ICRA), 2013
[3]Real-Time Visual Odometry from Dense RGB-D Images (F. Steinbruecker, J. Sturm, D. Cremers), In Workshop on Live Dense Reconstruction with Moving Cameras at the Intl. Conf. on Computer Vision (ICCV), 2011.


- [RTAB MAP - Real-Time Appearance-Based Mapping](https://github.com/introlab/rtabmap). Available on ROS
> Online Global Loop Closure Detection for Large-Scale Multi-Session Graph-Based SLAM, 2014
> Appearance-Based Loop Closure Detection for Online Large-Scale and Long-Term Operation, 2013

- [ORB2-SLAM](https://github.com/raulmur/ORB_SLAM2). Available on ROS (ALso supports **Stereo** and **Monocular** sensors)
> [1] Raúl Mur-Artal, J. M. M. Montiel and Juan D. Tardós. ORB-SLAM: A Versatile and Accurate Monocular SLAM System. IEEE > Transactions on Robotics, vol. 31, no. 5, pp. 1147-1163, 2015. (2015 IEEE Transactions on Robotics Best Paper Award).
> [2] Dorian Gálvez-López and Juan D. Tardós. Bags of Binary Words for Fast Place Recognition in Image Sequences. IEEE Transactions on Robotics, vol. 28, no. 5, pp. 1188-1197, 2012.

- [InfiniTAM∞ v2](http://www.robots.ox.ac.uk/~victor/infinitam/index.html)
> Kahler, O. and Prisacariu, V.~A. and Ren, C.~Y. and Sun, X. and Torr, P.~H.~S and Murray, D.~W. Very High Frame Rate Volumetric Integration of Depth Images on Mobile Device. IEEE Transactions on Visualization and Computer Graphics (Proceedings International Symposium on Mixed and Augmented Reality 2015

- [Kintinuous](https://github.com/mp3guy/Kintinuous)
> Real-time Large Scale Dense RGB-D SLAM with Volumetric Fusion, T. Whelan, M. Kaess, H. Johannsson, M.F. Fallon, J. J. Leonard and J.B. McDonald, IJRR '14

- [ElasticFusion](https://github.com/mp3guy/ElasticFusion)
> [1] ElasticFusion: Real-Time Dense SLAM and Light Source Estimation, T. Whelan, R. F. Salas-Moreno, B. Glocker, A. J. Davison and S. Leutenegger, IJRR '16
> [2] ElasticFusion: Dense SLAM Without A Pose Graph, T. Whelan, S. Leutenegger, R. F. Salas-Moreno, B. Glocker and A. J. Davison, RSS '15

- [Co-Fusion](http://visual.cs.ucl.ac.uk/pubs/cofusion/index.html)
> Martin Rünz and Lourdes Agapito. Co-Fusion: Real-time Segmentation, Tracking and Fusion of Multiple Objects. 2017 IEEE International Conference on Robotics and Automation (ICRA)

###### RGBD and LIDAR:
- [Google's cartographer](https://github.com/googlecartographer/cartographer). Available on ROS