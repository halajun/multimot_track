# Multi-Motion Tracking

This code offers a multi-motion visual odometry system for dynamic environments. If you use it in an academic work, please cite:

    @article{zhang2020iros,
      title={{Robust Ego and Object 6-DoF Motion Estimation and Tracking}},
      author={Zhang, Jun and Henein, Mina and Mahony, Robert and Ila, Viorela},
      booktitle={IEEE/RSJ International Conference on Intelligent Robots and Systems (IROS). To appear},
      year={2020},
      organization={IEEE}
     }

An ArXiv version of this paper is available [<b>HERE</b>](https://arxiv.org/abs/2007.13993).

<td> <img src="https://github.com/halajun/halajun.github.io/blob/master/images/iros20zhang.jpg" alt="iros20zhang" width="960" height="480" border="10" /></a> </td>

<ins><b>!!! IMPORTANT NOTES</b>: This work has been extended to a Visual Object-aware Dynamic SLAM system (VDO-SLAM), acting as the front end with many improvements. Please refer to [<b>VDO-SLAM</b>](https://github.com/halajun/VDO_SLAM) for detailed information. The author recommends potential users try the full VDO-SLAM system with latest updates (this repository is not guaranteed to be updated as frequently as the VDO-SLAM repository).</ins>


## License

 This code is released under a [GPLv3 license](https://github.com/halajun/MultMotTracking/blob/master/License-gpl.txt). As the code is developed based on the framework of ORB-SLAM2, please check a list of all code/library dependencies (and associated licenses), see [Dependencies.md](https://github.com/halajun/MultMotTracking/blob/master/Dependencies.md).

## Prerequisites

 The prerequisites are the same as ORB-SLAM2. If compiling problems met, please refer to [ORB-SLAM2](https://github.com/raulmur/ORB_SLAM2).
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

Execute the following command to get the code run on the sample data.
```
./Examples/RGB-D/rgbd_mmt Vocabulary/ORBvoc.txt kitti_sample/kitti03.yaml kitti_sample
```





