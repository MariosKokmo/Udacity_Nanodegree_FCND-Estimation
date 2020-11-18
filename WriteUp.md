# Estimation Project

### Step 1
For this step I ran the simulator and obtained the Graph txt files.
I ran a quick pandas analysis in Jupyter Notebook as seen below and I extracted
the mean and the standard deviation for the GPS and th eIMU.

<p align="center">
<img src="images/Step_1_1.PNG" width="500"/>
</p>

Running the simulation with those new updated values I obtained the
following performance:

<p align="center">
<img src="images/Step_1_2.PNG" width="500"/>
</p>

### Step 2

For this step I implemented the IMU update of the estimator.
The code appears below. We make use of the quaternion and the
method provided by the class. Then we extract the Roll, Pitch and Yaw.

<p align="center">
<img src="images/Step_2_1.PNG" width="500"/>
</p>

The performance obtained with the better integration scheme is shown below.

<p align="center">
<img src="images/Step_2_2.PNG" width="500"/>
</p>

### Step 3

For this step I implemented the state prediction step:

<p align="center">
<img src="images/Step_3_1.PNG" width="500"/>
</p>

And the estimator could accurately track the actual state, with a slow drift.

<p align="center">
<img src="images/Step_3_2.PNG" width="500"/>
</p>

After introducing the realistic IMU with noise as per the instructions,
I implemented the Rgb prime function

<p align="center">
<img src="images/Step_3_3.PNG" width="500"/>
</p>

and the Predict step:

<p align="center">
<img src="images/Step_3_4.PNG" width="500"/>
</p>

Modifying the  gains I could see that the covariance grows like the data:

<p align="center">
<img src="images/Step_3_5.PNG" width="500"/>
</p>

### Step 4

In this step I implemented the function that uses the magnetometer for the yaw updates

<p align="center">
<img src="images/Step_4_1.PNG" width="500"/>
</p>

and th eoutput was as follows, passing the criteria.

<p align="center">
<img src="images/Step_4_2.PNG" width="500"/>
</p>

### Step 5

In this step, I implemented the GPS update function (simple Implementation
of the document equations)

<p align="center">
<img src="images/Step_5_1.PNG" width="500"/>
</p>

After tuning, we get the following:

<p align="center">
<img src="images/Step_5_2.PNG" width="500"/>
</p>

### Step 6

Overall, after inserting the controller of the previous project and fine tuning (It was't necessary), the drone is able to fly and pass the criteria as required.

<p align="center">
<img src="images/Step_5_2.PNG" width="500"/>
</p>