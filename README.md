# Multi-Motion Tracking #

 This code offers a multi-motion visual odometry system for dynamic environment.

## License

 This code is released under a [GPLv3 license](https://github.com/halajun/MultMotTracking/blob/master/License-gpl.txt). As the code is developed based on the framework of ORB-SLAM2, please check a list of all code/library dependencies (and associated licenses), see [Dependencies.md](https://github.com/halajun/MultMotTracking/blob/master/Dependencies.md).

## Prerequisites

 The prerequisites are the same as [ORB-SLAM2](https://github.com/raulmur/ORB_SLAM2).
 We have tested the library in **MacOS Mojave 10.14.6**, but it should be easy to compile in other platforms.

## Compiling

 Clone the repository:
 ```
 git clone https://github.com/halajun/MultMotTracking.git MultMotTracking
 ```

We provide a script `build.sh` to build the *Thirdparty* libraries and *MultMotTracking*. Please make sure you have installed all required dependencies. Execute:
```
cd MultMotTracking
chmod +x build.sh
./build.sh
```

This will create **libMultMotTrack.dylib**  at *lib* folder and the executables **rgbd_mmt** in *Examples* folder.

## Running Examples

We have included a small set of sample data in *kitti_sample* folder.

Execute the following command.
```
./Examples/RGB-D/rgbd_mmt Vocabulary/ORBvoc.txt kitti_sample/kitti03.yaml kitti_sample
```





