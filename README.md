ethzasl_sensor_fusion
=====================

time delay compensated single and multi sensor fusion framework based on an EKF

![](http://wiki.ros.org/ethzasl_sensor_fusion/Tutorials/Introductory%20Tutorial%20for%20Multi-Sensor%20Fusion%20Framework?action=AttachFile&do=get&target=structure.png)

    红色字体部分是从传感器获取的数据，用于输入到预测(prediction)和更新阶段(update).
    蓝色字体是更新阶段会变化的部分。
    黑色部分为约束部分，是不变的。

    变量：
    p for pwi: 在世界坐标下的 IMU位置 IMU position in the world frame

    v for vwi: 在世界坐标下的 IMU速度 IMU velocity in the world frame

    q for qwi: the imu attitude in the world frame

    b_w for bw: the gyro biases

    b_a for ba: the accelerometer biases

    L for λ: the visual scale factor with pmetric*λ = psensor

    q_wv for q,,vw: the attitude between the update-sensor reference frame and the world reference frame

    q_ci for qic: the attitude between IMU and the update-sensor

    p_ci for pic: the distance between IMU and the update-sensor 
