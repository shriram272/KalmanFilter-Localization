# KalmanFilter-Localization
# UKF
Unscented Kalman Filter using IMU and GNSS data for vehicle or mobile robot localization.

Requirements: Eigen3, ROS

Input: sensor_msgs/NavSatFix, sensor_msgs/Imu

Output: nav_msgs/Odometry

Key Features:

1. Assumes 2D motion.
2. Initializes the state{position x, position y, heading angle, velocity x, velocity y} to (0.0, 0.0, yaw, 0.0, 0.0) with the yaw from IMU at the start of the program if no initial state is provided.
3. Uses acceleration and yaw rate data from IMU in the prediction step.
4. GNSS data is used for correction.
5. Yaw from the IMU is only used to initialize and not in correction step.
