# pick-deploy-bench

面向桌面机械臂视觉抓取的具身策略部署与可靠性评测项目。

## Project Goal

构建一条可复现的最小闭环：

1. 相机获取目标位置与深度。
2. 坐标变换将目标位姿转换到机械臂基座坐标系。
3. 脚本基线或学习策略生成抓取动作。
4. ROS 2 部署推理与执行节点。
5. 对光照、物体位姿和相机误差进行可靠性评测。

## Current Status

- Ubuntu 22.04.5 LTS on WSL 2
- ROS 2 Humble installed
- `ros2 --help` verified
- `demo_nodes_cpp talker` and `demo_nodes_py listener` verified
- Repository initialization: in progress

## Planned Stack

- Ubuntu 22.04 + ROS 2 Humble
- Python
- MuJoCo/RoboSuite
- RGB-D or stereo camera
- ACT imitation-learning baseline
- One minimal C++ ROS 2 or inference benchmark module

## Repository Layout

```text
docs/       Environment, experiments, and learning records
src/        ROS 2 packages and deployment code
scripts/    Setup and benchmark entry points
data/       Small non-sensitive metadata only
```

## Reproduce the ROS 2 Smoke Test

```bash
source /opt/ros/humble/setup.bash
ros2 --help
```

Run these in two terminals:

```bash
ros2 run demo_nodes_cpp talker
ros2 run demo_nodes_py listener
```

