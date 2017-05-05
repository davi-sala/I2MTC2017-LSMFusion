# Experiments used for the paper submitted to I2MTC 2017

---------------------
## Sensor Fusion Approach Using Liquid StateMachines for Positioning Control

---------------------
### Abstract
>A sensor fusion controller based on Spiking Neural Networks suitable to run on a neuromorphic computer. The proposed framework uses the paradigm of reservoir computing to control the collaborative robot BAXTER. The system was designed to work in parallel with an already working Liquid State Machine(LSM) that performs trajectories in 2D closed shapes. In order to keep a felt pen touching the drawing surface, information of force and range are fed to our controller. The controller was trained using data from a Proportional Integral Derivative controller (PID), merging force and range sensors’ information. Our results show that the LSM can copy the behavior of the PID controller on different situations.


---------------------------

(this work is intended to work with the LSM control loop presented in github.com/ricardodeazambuja/IJCNN2016)

#### 1) The trajectories are generated using a simulated BAXTER robot inside V-REP.
    generate_square_joint_angles_vrep.ipynb
    /VREP_scenes/Baxter_IK_felt_pen_TallerTable(2xIK).ttt

#### 2) Training data set created with the PID controlled using the notebook:
    create_training_set(PID_CONTROL).ipynb

#### 3) After the generation of the training data, it is necessary create the LSMs and generate the input spikes. This is done by:
    generate_LSM_training_data.ipynb

#### 4) Readout weights are generated using linear regression:
    generate_LINEAR_REG.ipynb
    
#### 5) With all the readout weights defined, it's possible to verify the system using BAXTER:
    BAXTER_LSM_Z_CONTROLLER_INDIVIDUALS.ipynb
------------------------------------

#### OBS:
* BEE SNN simulator:
    * https://github.com/ricardodeazambuja/BEE

* V-REP simulator:
    * http://www.coppeliarobotics.com/downloads.html
    

* Related works:  
    * https://github.com/ricardodeazambuja/ICONIP2016  
    * https://github.com/ricardodeazambuja/IJCNN2017  
    * https://github.com/ricardodeazambuja/IJCNN2017-2  
