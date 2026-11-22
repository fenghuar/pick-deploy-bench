# Development Environment

## Host

| Item | Value |
|---|---|
| Operating system | Windows 10 22H2, build 19045.6466 |
| CPU | To be completed |
| RAM | To be completed |
| Disk | To be completed |
| GPU | NVIDIA GeForce RTX 4060, 8 GB |
| NVIDIA driver | 596.49 |

## Linux and ROS

| Item | Value |
|---|---|
| WSL distribution | Ubuntu-22.04 |
| WSL version | 2 |
| Ubuntu version | 22.04.5 LTS (Jammy Jellyfish) |
| Linux kernel | 6.18.40.1-microsoft-standard-WSL2 |
| ROS distribution | Humble |

## Verification

Completed on 2026-11-20:

- Ubuntu reports `VERSION_ID="22.04"`.
- `ros2 --help` displays the ROS 2 command list.
- `demo_nodes_cpp talker` and `demo_nodes_py listener` exchange messages.
- Listener received continuous `Hello World` messages from sequence 43 to 53.

## Notes

- The imported Ubuntu distribution currently uses the `root` user.
- A dedicated non-root development user should be added before routine development.
- Docker, CUDA in WSL, camera access, and robot hardware remain to be verified.

