# Conveyor Belt and parcels 

Welcome to the Conveyor Belt and Parcels repository! This repository for simulating conveyor belt systems and parcel handling within ROS (Robot Operating System) and Gazebo. It comprises two main packages:


## belt_n_parcel_description

This package contains the necessary `URDF` (Unified Robot Description Format) files for creating conveyor belt and parcel models. These `URDF` files enable the creation and visualization of various conveyor belt configurations and diverse parcel types of different sizes within simulation environments.

## belt_n_parcel_gazebo

The package is equipped with essential functionalities to simulate conveyor belt operations and dynamic parcel handling in Gazebo. It includes a Python script designed to dynamically spawn parcels onto the conveyor belt. Additionally, there's a launch file provided for a seamless initiation of Gazebo with pre-configured conveyor and parcels, facilitating easy simulation setup and execution.

## Setup

```bash
git clone https://github.com/khaledgabr77/belt_n_parcel_sim.git
```

## RUN 

* Make sure this package is inside the ROS workspace
* Make sure that you build the ROS workspace, and source `devel/setup.bash`
* To run the Conveyor Belt and Parcel, run the following launch file,

```bash
roslaunch belt_n_parcel_gazebo belt_n_parcel.launch
```

## Power the conveyor 

```bash
rosservice call /conveyor/control "power: 10.0"
```
> note The power `0` means `stop` the convyor, and you can `move` the convoyer with certin speed `1-100`. 