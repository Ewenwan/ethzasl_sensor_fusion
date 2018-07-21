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
    q for qwi: 在世界坐标下的 IMU姿态 IMU attitude in the world frame

    b_w for bw: 陀螺仪漂移 the gyro biases
    b_a for ba: 陀螺仪漂移 the accelerometer biases

    L for λ:    视觉尺度因子 the visual scale factor with pmetric*λ = psensor

    q_wv for q,,vw: 更新阶段参考帧(相机参考帧) 和 世界参考帧 之间的姿态变化
    q_ci for qic:   IMU and the update-sensor(相机) 姿态变化
    p_ci for pic:   IMU and the update-sensor(相机) 位置变换
