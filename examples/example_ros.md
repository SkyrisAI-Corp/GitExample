# 嵌入式机器人操作系统（ROS2）开发工程师自我介绍示例

## 基本信息

- **姓名**：林睿
- **职位**：ROS2嵌入式开发工程师
- **邮箱**：<linrui@robotics-example.com>
- **GitHub**：[github.com/ros2-linrui](https://github.com/ros2-linrui)
- **技术社区**：ROS Answers活跃用户（ID：ros_linrui）、知乎专栏《ROS2嵌入式实践》

## 技术栈

- **ROS2核心**：熟悉Foxy/Humble/Iron版本，掌握节点通信（Topics/Services/Actions）、参数服务器、生命周期节点
- **嵌入式平台**：
  - 主控：NVIDIA Jetson Nano/Xavier NX、STM32H743、Raspberry Pi 4/5
  - 实时系统：FreeRTOS+ROS2 Micro-ROS、RT-Thread+ROS2桥接
- **机器人硬件**：
  - 传感器：激光雷达（LiDAR）、IMU、摄像头、超声波、红外避障
  - 执行器：直流电机、舵机、步进电机（驱动控制与PID调速）
- **开发工具**：
  - 环境：Colcon、CMake、ament_cmake、vcs
  - 调试：rqt、ros2 bag、GDB、Valgrind（内存检测）
  - 仿真：Gazebo、RViz2、Webots
- **编程语言**：C++（主要开发语言）、Python（脚本与测试）、嵌入式C（底层驱动）
- **通信与算法**：CANopen、EtherCAT、SLAM（GMapping/RTAB-Map）、路径规划（A\*/Dijkstra）、PID控制

## 工作经历

### 某移动机器人公司 | ROS2开发工程师 | 2020.05 - 至今

- 负责自主移动机器人的ROS2系统架构设计与底层驱动开发，主导2款AGV产品的ROS2迁移（从ROS1）
- 开发基于Micro-ROS的嵌入式节点，实现传感器数据采集与执行器控制的低延迟通信（≤5ms）
- 优化机器人导航模块，将室内定位精度从±30cm提升至±5cm，路径规划效率提升40%
- 设计ROS2节点健康监控系统，实现节点故障自动重启与日志上报，系统稳定性提升95%

## 核心项目经验

### 仓储自主导航AGV（基于ROS2 Humble）

- **项目描述**：用于仓库货物转运的无人搬运机器人，支持自主避障、二维码定位与调度系统对接
- **技术实现**：
  - 系统架构：采用模块化节点设计（感知/决策/控制层分离），使用ROS2 Actions实现任务调度
  - 硬件集成：通过ROS2驱动适配激光雷达（SICK TiM561）、IMU（BNO055）、 mecanum轮驱动模块
  - 实时控制：基于Micro-ROS在STM32H743上实现电机闭环控制节点，支持1kHz控制频率
  - 仿真验证：在Gazebo中搭建仓库场景，通过ros2 bag回放真实数据验证算法可靠性
- **成果**：实现AGV最大行驶速度1.2m/s，连续运行72小时零故障，已部署至3个物流仓库

### 教育服务机器人（ROS2 + 语音交互）

- **项目描述**：面向中小学的教育机器人，支持编程教学、SLAM建图与语音控制
- **技术实现**：
  - 轻量化设计：在Raspberry Pi 4上部署ROS2 Foxy，优化节点启动时间（从8s降至3s）
  - 功能模块：开发自定义msg/srv接口，实现语音指令（基于百度AI）到ROS2话题的转换
  - 教学适配：封装简单API接口，支持学生通过Python调用ROS2服务控制机器人运动
- **成果**：入选30所学校的机器人实验室，编写的《ROS2教育机器人开发手册》被纳入校本教材

## 技术能力

- 精通ROS2节点通信机制与实时性优化，能解决多节点协同的资源竞争问题
- 具备嵌入式平台上ROS2（含Micro-ROS）的移植与裁剪经验，适配资源受限设备
- 熟悉机器人常用算法（SLAM、路径规划、运动控制）的ROS2实现与调优
- 能独立完成从硬件选型→驱动开发→ROS2节点封装→仿真测试的全流程开发

## 个人特点

- 注重代码规范性，严格遵循ROS2 Coding Standards，主导团队制定《ROS2节点开发规范》
- 擅长问题排查，通过ros2 trace与perf工具定位过多个系统延迟与内存泄漏问题
- 持续参与ROS2社区贡献，提交过2个关于Micro-ROS串口传输的bug修复PR
- 持有ROS Industrial认证工程师（Level 2）证书

## 开源与分享

- 开源项目：[ros2_agv_base](https://github.com/ros2-linrui/ros2_agv_base)（AGV底盘ROS2驱动包，GitHub星标400+）
- 技术分享：在ROSCon China 2023做《Micro-ROS在嵌入式设备中的实践》主题演讲
- 教程系列：在B站发布《ROS2从入门到实战》视频课程，累计播放量15万+
