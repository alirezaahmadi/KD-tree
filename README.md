# CUDA Compatible KD-tree

<p align="center">
    <img src="data/3dtree.png?raw=true" width="250" title="3dtree">
</p>

A CUDA Compatible KD-tree implementation along with ANN. The k-d tree is a binary tree in which every node is a k-dimensional point. Every non-leaf node can be thought of as implicitly generating a splitting hyperplane that divides the space into two parts, known as half-spaces. Points to the left of this hyperplane are represented by the left subtree of that node and points to the right of the hyperplane are represented by the right subtree. The hyperplane direction is chosen in the following way: every node in the tree is associated with one of the k dimensions, with the hyperplane perpendicular to that dimension's axis. So, for example, if for a particular split the "x" axis is chosen, all points in the subtree with a smaller "x" value than the node will appear in the left subtree and all points with a larger "x" value will be in the right subtree. In such a case, the hyperplane would be set by the x value of the point, and its normal would be the unit x-axis.


Invented in 1970s by Jon Bentley
* Name originally meant “3d-trees, 4d-trees, etc” where k was the # of dimensions
* Now, people say “kd-tree of dimension d”
* Idea: Each level of the tree compares against 1 dimension.
* Let’s us have only two children at each node (instead of 2d)

<p align="center">
    <img src="data/simple.png?raw=true" width="200" title="3dtree">
</p>

Each level has a “cutting
dimension”
* Cycle through the dimensions as you walk down the tree.
* Each node contains a point P = (x,y) To find (x’,y’) you only compare coordinate from the cutting dimension 
    * e.g. if cutting dimension is x, then you ask: is x’ < x ?

<p align="center">
    <img src="data/details.png?raw=true" width="500" title="3dtree">
</p>
</p>



## Installation

for a compelte guide on using it in a project check [**DynaMap Project**](https://github.com/alirezaahmadi/dynamap)

```

sudo apt install nvidia-cuda-toolkit
nvcc -V

sudo apt install build-essential

sudo apt install gcc-6 g++-6
make sure gcc6 is selected
sudo update-alternatives --config gcc
or
sudo update-alternatives --install /usr/bin/g++ g++ /usr/bin/g++-6 60
sudo update-alternatives --install /usr/bin/gcc gcc /usr/bin/gcc-6 60
```


### Eigen
wget https://gitlab.com/libeigen/eigen/-/archive/3.3.7/eigen-3.3.7.zip 

## Deployment

## **Contribution**

Any contribution is highly appreciated 
dont hesitate to contact me! 
alireza.ahmadi@uni-bonn.de



---

<div align="center">
  
[![paypal](https://pics.paypal.com/00/s/NGRhNWNlODUtMzZlOS00MjJhLTg2NDEtMzNiNzczMTZkMDU4/file.PNG)](https://www.paypal.com/donate/?hosted_button_id=23TQAZ9MSLAUU)

</div>

---


## Citation
---

```bash

@article{ahmadi2021registration,
  title={Registration Techniques for Deformable Objects},
  author={Ahmadi, Alireza, Cyrill Stachniss},
  journal={arXiv preprint arXiv:2111.04053},
  year={2021}
}

```
