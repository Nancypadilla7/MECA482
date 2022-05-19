# Furuta Pendulum
## MECA 482-01 Group 2
Aaron Fawcett, Alexander Hernandez, Nancy Padilla, Dylan Sanders, Marius Van Zyl 
## Table of Contents
1. Introduction
2. System Requirements
3. Model
4. Controller and Design Simulations
5. Results
6. References
## Background

The "Furuta Pendulum" is a sytem of two arms linked together controlled by one motor. The first arm rotates in a horizontal plane and the second arm rotates in a vertical plane at the end of the first arm. A motor is attached to one end of the first arm while the second arm is attached to the other end. The second arm rotates freely about its rotation plane. A Furuta Pendulm can be seen in the figure below.

<p align="center">
  <img width="165" height="300" src="https://github.com/Nancypadilla7/MECA482/blob/main/images/RotaryInvertedPendulum.png?raw= true" title="Furuta Pendulum Example">
</p>



The goal is to balance the second arm in an upwards vertical position. To acheive this, control methods must be developed, tested and implemented. A mathematical model is devloped in MATLAB using the methods developed by Hernández-Guzmán (870). The model is simulated in CoppeliaSim to verify its success.


## System Requirements

* Must keep pendulum within 90 degrees from vertical
* Must be able to be disturbed and self-correct

<p align="center">
  <img width="1000" height="473" src="https://github.com/Nancypadilla7/MECA482/blob/main/images/OperationViewpoint.png?raw= true" title="operational ViewPoint for the Pendulum">
</p>

<h3 align="center">Operational Viewpoint for the Furuta Pendulum</h3>

## Model
<p align="center">
<img width="500" height="320" src="https://github.com/Nancypadilla7/MECA482/blob/main/images/symbolicschematic.PNG?raw= true" title="Symbolic Schematic">

1. Schematic
In order to model the Furuta Pendulum, a schematic was use to derive the mathematical model.The reference axes and the system variable is define by the figure below. The mathematical model for the this system is obtained by using the Euler Lagrangian equations. 
<p align="center">
<img width="493" height="316" src="https://github.com/Nancypadilla7/MECA482/blob/main/images/symbolicschematic.PNG?raw= true" title="Furuta Pendulum Example">
</p>

The following parameters are obtained based on the schematic above and the parametersare used in the derivation of the mathematical model. 

* g is the acceleration due to gravity 
* m1 is the pendulum mass
* θo is the angular position of the arm in radians
* θ1 is the angular position of the pendulum with respect to the pendulum in the downward position, in radians.
*  τ is the torque generated by the electric motor that is applied to the arm.
*  I0 is the arm inertia when it rotates around one of its ends plus the motor inertia.
*  L0 is the arm length.
*  l1 is the location of the center mass of the pendulum.
*  J1 is the moment of inertia

2. Equation of Motion 
  <p align="center">
<img width="262" height="53" src=https://github.com/Nancypadilla7/MECA482/blob/main/images/newequation1.PNG?raw= true" title="Furuta Pendulum Example">
</p>
 
 For the system total kinetic energy is the summation of the kintic energy of the pendulum arm rotating, as well as the kintic enegy rotating.The equation shown above are the general definition for the given system. 
                                                                                                                                  
Next, the Kinetic energy for the body is the translational movement of the body's center of mass and the rotative movement of a beam around an axis passing through the pendulum center. The equation below define the systems total kinetic energy.
                                                                                                                                     <p align="center">
<img width="305" height="41" src="https://github.com/Nancypadilla7/MECA482/blob/main/images/eq2.PNG?raw= true" title="Furuta Pendulum Example">
</p>
                                                                                                                                  To comute the pendulum poential energy, θ1 is equal to zero, and its the reference point. The equation below is the potential energy equation. 
               <p align="center">
<img width="291" height="30" src="https://github.com/Nancypadilla7/MECA482/blob/main/images/poten.PNG?raw= true" title="Furuta Pendulum Example">
</p>                                                                                                       
                                                                                                            The equation below is the representation of of the system mathematical model, which is nonlinear. 
   <p align="center">
<img width="418" height="172" src="https://github.com/Nancypadilla7/MECA482/blob/main/images/fmm.PNG?raw= true" title="Furuta Pendulum Example">
</p>                                                                                                        
                                                                                                           The next step is to write the Mathematical model in terms of state space representation. State space representation is found by definding the state x components as an unknown variable. Below shows the system variables in state space representation.
 <p align="center">
<img width="173" height="97" src="https://github.com/Nancypadilla7/MECA482/blob/main/images/15.3.PNG?raw= true" title="Furuta Pendulum Example">
</p>
                                                                                                            Applying  the prevoius equations, the relationship of the equations, it expression is define as a vector matrix state space eqation. the result is seen below. 
   <p align="center">
<img width="466" height="150" src="https://github.com/Nancypadilla7/MECA482/blob/main/images/15.18.PNG?raw= true" title="Furuta Pendulum Example">
</p>                                                                                                                                            
                                                                                                                                   
## Controller and Design Simulations
## Results
## References
Hernández-Guzmán, Victor Manuel, and Ramón Silva-Ortigoza. Automatic control with experiments. Cham, Switzerland: Springer, 2019.

Nise, N. S. (2011). Control Systems Engineering. John Wiley & Sons.

