# 树莓派 ROS2 自动定位与导航小车

「树莓派 4B（ROS2 上位机）+ STM32 底盘 + 激光雷达」的 SLAM 建图定位与导航小车工程集合。

## 组成

| 目录 | 说明 |
|---|---|
| `ros2工作空间/RaspberryPi4/ros2_ws` | 车载 ROS2 工作空间（car_pkg：节点 + launch） |
| `ros2工作空间/VMWare/ros2_ws` | PC 虚拟机端 ROS2 工作空间（可视化 / 联调） |
| `stm32底盘/ros2_car` | STM32 底盘控制固件（串口对接 ROS2 上位机） |
| `cspc_lidar_sdk_ros2_D4_20250731.tar.gz` | 激光雷达 ROS2 SDK |

## 构建（车载端）

```bash
cd ros2工作空间/RaspberryPi4/ros2_ws
colcon build
source install/setup.bash
```

---

**EN**: ROS2 SLAM / navigation car project: Raspberry Pi 4B ROS2 workspace (`car_pkg`), STM32 chassis firmware, and lidar ROS2 SDK. Build with `colcon build`.

## 声明

学习实践项目，用于个人技术归档与求职展示。
