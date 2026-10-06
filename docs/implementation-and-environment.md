# 软件与运行环境

我在 Linux/ROS 下集成 VINS-Fusion、EGO-Planner 和飞控通信模块，参与相机与 IMU 标定，并用 Gazebo 做飞行仿真联调。

## 开源组件

| 组件 | 项目中的用途 |
| --- | --- |
| [VINS-Fusion](https://github.com/HKUST-Aerial-Robotics/VINS-Fusion) | 视觉惯性位姿估计 |
| [EGO-Planner](https://github.com/ZJU-FAST-Lab/ego-planner) | 局部轨迹规划 |
| [MAVROS](https://github.com/mavlink/mavros) | 连接 ROS 与 MAVLink，传递状态和指令 |
| [XTDrone](https://github.com/robin-shaun/XTDrone) | PX4、ROS 与 Gazebo 仿真平台 |
| [OpenCV](https://docs.opencv.org/4.x/) | 颜色分割、轮廓和标靶中心提取 |

我的工作主要是组件集成、接口联调、视觉处理和仿真测试，定位、规划和飞控的基础算法来自相应开源项目。

## 运行环境

| 部分 | 使用的环境或组件 |
| --- | --- |
| 操作系统 | Linux |
| 中间件与通信 | ROS、MAVROS、MAVLink |
| 飞控 | PX4 |
| 仿真与可视化 | Gazebo、XTDrone、RViz |
| 感知与规划 | OpenCV、VINS-Fusion、EGO-Planner |

项目资料中同时出现 ROS 与 ROS2 写法。重新部署时，需要结合原工程确认操作系统、ROS 分支、PX4 固件和各组件版本。

## 工程文件

目前保存下来的代码主要是 OpenCV 桌面实验、ROS 红色检测节点和 OpenMV 实验脚本，完整的定位、规划及任务控制工程没有一并归档。

这些脚本包含不同实验版本，不能单独启动整机系统。因此仓库以项目图文和演示视频为主，没有上传零散源码或提供整机启动命令。视觉算法和节点接口见 [视觉处理](vision.md)。

重新运行还需要对应版本的依赖、launch 文件、相机与 IMU 标定、轨迹到飞控的转换接口、任务控制包和仿真场景。
