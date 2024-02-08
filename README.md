# Task-Oriented Grasping with Point Cloud Representation of Objects
In Proceedings IROS 2023 [paper][video]

This is the Python Implementation of neural network-based task-oriented grasp synthesis on object point clouds described in our IROS 2023 paper.
If you find this work useful please cite our work: 

```
@inproceedings{patankar2023task,
  title={Task-Oriented Grasping with Point Cloud Representation of Objects},
  author={Patankar, Aditya and Phi, Khiem and Mahalingam, Dasharadhan and Chakraborty, Nilanjan and Ramakrishnan, IV},
  booktitle={2023 IEEE/RSJ International Conference on Intelligent Robots and Systems (IROS)},
  pages={6853--6860},
  year={2023},
  organization={IEEE}
}
```

# Installation 

1. Clone the repository

2. Create a conda environment using provided .yml file

The repository currently contains point clouds (PLY format) captured from multiple camera views using Intel Realsense D415 for a CheezIt box, Domino Sugar box and a Ritz cracker box in the folder ``` partial_point_cloud ```. 

# Usage

Current implementation is for computing an ideal grasping region on point clouds of cuboidal objects for the task of pivoting the cuboidal object about one of its edges. The pivoting motion is a constant screw motion (pure rotation) about one of the edges and is represented using a screw axis. The location of the screw axis is approximated using the edges of the bounding box. 

1. Open a terminal and activate the conda environment

2. Type the following command to run the file ```main.py``` and visualize the results on a CheezIt box:
  ``` python -u main.py --filename partial_point_cloud_multiple_views/cheezit_cracker_box.ply --visualize ```


