# Unconventional tajectories datasets
Repository that contains 3D point and pose datasets and corresponding ground truth point clouds, using unconventional trajectories such as rolling, pendulum, and descending while rotating.

## Processing
We use [3DTK](https://slam6d.sourceforge.io/), which is a toolbox written in C++ for 3D point clouds that comes e.g. with a fast viewer and video creator.
To start, install the following dependencies on your system:
 - cmake
 - cmake-curses-gui
 - boost (libboost)
 - blas (libblas)
 - suitesparse (libsuitesparse)
 - opencv (libopencv)
 - zip (libzip)
 - cgal (libcgal)
 - eigen3 (libeigen3)
 - mesa (libglu1-mesa and mesa-common)
 - newmat (libnewmat)
 - ann (libann)
 - freeglut
 - wxgtk3.0 (optional, if you need wxShow viewer)
  
In Debian based systems such as Ubuntu, try the following to install them all:
```shell
sudo apt install cmake cmake-curses-gui build-essentials libboost-all-dev libblas-dev libsuitesparse-dev libopencv-dev libglu1-mesa-dev freeglut3-dev mesa-common-dev libwxgtk3.0-gtk3-dev libzip-dev qtbase5-dev libcgal-dev libeigen3-dev libann-dev libnewmat10-dev
```

Install 3DTK as follows:
```shell
svn checkout https://svn.code.sf.net/p/slam6d/code/trunk slam6d-code
cd slam6d-code
mkdir .build
make config 
```

Configure your build flags and generate buildfiles ("c" to configure, "g" to generate).
Then, install:
```shell
make -j<NUMBER_OF_CPUS>
```

To start, place datasets in the "dat" folder and show them with
```shell
bin/show dat/your/dataset -f <FILE_FORMAT> --advanced 
```

Refer to [3DTKs svn repository](https://sourceforge.net/p/slam6d/code/HEAD/tree/trunk/) for further guidance and wikipage. 

## Publication
Yet to be published.

Authors:
[Fabian Arzberger](fabian.arzberger@uni-weurzburg.de), [Jasper Zevering](jasper.zevering@uni-weurzburg.de), Dorit Borrmann, Anton Bredenbeck, and Andreas Nüchter

## Screenshots
![Bild](https://github.com/fallow24/unconventional_tajectories_datasets/blob/main/img/FireGroundTruth.png)
![Bild](https://github.com/fallow24/unconventional_tajectories_datasets/blob/main/img/fire_uncor.png)
![Bild](https://github.com/fallow24/unconventional_tajectories_datasets/blob/main/img/ground_truth.png)
![Bild](https://github.com/fallow24/unconventional_tajectories_datasets/blob/main/img/pendulum_uncor.png)
![Bild](https://github.com/fallow24/unconventional_tajectories_datasets/blob/main/img/radler_uncor.png)
![Bild](https://github.com/fallow24/unconventional_tajectories_datasets/blob/main/img/rolling_uncor.png)

