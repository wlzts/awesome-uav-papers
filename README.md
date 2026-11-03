# Awesome UAV Papers

> 📚 **无人机科研论文 + 中文导读 + 算法对比 + 代码复现 + 研究路线** 的一站式开源资源库。
>
> 覆盖自主导航、路径规划、集群协同、视觉感知、6G 通信与反无人机等方向，每篇论文附中英文摘要、年份、类型标签与可复现信息。

A curated list of UAV / Drone research papers with Chinese reading notes, organized by research direction, plus reading roadmaps, datasets and open-source tools.

---

## 📑 Contents

- [🚀 Start Here — Reading Roadmaps](#-start-here--reading-roadmaps)
- [📚 Surveys & Overviews (by direction)](#-surveys--overviews-by-direction)
- [🧭 Autonomous Navigation & SLAM](#-autonomous-navigation--slam)
- [🗺 Path Planning](#-path-planning)
- [🐝 Swarm & Multi-UAV Coordination](#-swarm--multi-uav-coordination)
- [👁 Visual Perception & Object Detection](#-visual-perception--object-detection)
- [📡 Wireless Communications & Networking](#-wireless-communications--networking)
- [🛡 Anti-UAV Detection](#-anti-uav-detection)
- [📊 Datasets & Benchmarks](#-datasets--benchmarks)
- [🛠 Open-source Projects & Simulation](#-open-source-projects--simulation)

---

## 🚀 Start Here — Reading Roadmaps

Don't know where to start? Pick your goal below.

### 🎓 如果你是刚入门的本科生 / 研一

1. **[UAVs: practical aspects, applications, open challenges](https://link.springer.com/content/pdf/10.1007/s11370-022-00452-4.pdf)** `2023` `Survey` — 建立全景认知：分类、应用、挑战、安全。
2. **[Recent Advances in UAVs: A Review](https://link.springer.com/content/pdf/10.1007/s13369-022-06738-0.pdf)** `2022` `Survey` — 近 10 年技术演进路线。
3. 然后再根据兴趣选下面的细分路线。

### 🧭 如果你做自主导航 / SLAM

1. 先读 **[A Simultaneous Control, Localization, and Mapping (SCLAM)](#)** 理解视觉 SLAM+控制闭环。
2. 再读 **[Large-scale Semantic SLAM under Forest Canopy (Kumar 组)](https://arxiv.org/pdf/2109.06479v5)** 看 LiDAR 语义建图 SOTA。
3. 工程落地看 **[Visual-Inertial Navigation Under Canopy](https://www.mdpi.com/2504-446X/9/1/27)** 和 **[ORB-SLAM for Post-disaster UAVs](https://ceur-ws.org/Vol-4204/ShortPaper5.pdf)**。

### 🐝 如果你做集群协同

1. **[UAV Swarm Intelligence: Recent Advances](http://xplorestaging.ieee.org/ielx7/6287639/8948470/09214446.pdf?arnumber=9214446)** `2020` `Survey` — 五层框架（决策/规划/控制/通信/应用）。
2. **[UAV swarms: research, challenges, future directions](https://jeas.springeropen.com/counter/pdf/10.1186/s44147-025-00582-3.pdf)** `2025` `Survey` — 最新进展。
3. 方法层看 **[MADRL for Multi-Robot: A Survey](https://www.mdpi.com/1424-8220/23/7/3625/pdf)** 和 **[Starling Bionic Trajectory Planning](https://www.mdpi.com/2076-3417/13/11/6795/pdf)**。

### 🧠 如果你做强化学习 / 路径规划

1. **[Research on UAV Path Planning (综述)](https://www.mdpi.com/2504-446X/8/2/51/pdf)** `2024` `Survey` — 先搞清楚传统算法版图。
2. **[Dynamic Scene Path Planning via DRL (D3QN)](https://www.mdpi.com/2504-446X/8/2/60/pdf)** — 看 DRL 怎么跑赢 A*/RRT。
3. **[EE-TD3 for 3D Dynamic Environments](https://www.mdpi.com/2073-8994/15/7/1371/pdf)** — 进阶连续控制。

> ⚠️ 以上路线是推荐顺序，不是唯一路径；实际研究中常常组合使用多种方法。

---

## 📚 Surveys & Overviews (by direction)

All survey papers are collected here. Cross-links point to the corresponding methods section.

### General UAV Surveys

- **[UAVs: practical aspects, applications, open challenges, security issues, and future trends](https://link.springer.com/content/pdf/10.1007/s11370-022-00452-4.pdf)** `2023` `Survey` `General`
  *Mohsan et al., Intelligent Service Robotics.*
  > 中文：最全面的入门综述，把 UAV 分类、集群、充电、法规、应用场景与安全问题串成一张全景图。
  > 适合：零基础建立全局图景 · 难度：低

- **[Recent Advances in Unmanned Aerial Vehicles: A Review](https://link.springer.com/content/pdf/10.1007/s13369-022-06738-0.pdf)** `2022` `Survey` `General`
  *Ahmed et al., Arabian J. for Science and Engineering.*
  > 中文：筛了近 10 年 254 篇文献，梳理机体、感知、路径规划与 AI 行为的演进路线。

- **[Multiple UAV Systems: A Survey](https://pdfs.semanticscholar.org/bdb6/52a49782e5ca907d6cc729a473d77de763a3.pdf)** `2018` `Survey` `Swarm`
  *Skorobogatov, Barrado & Salami, Unmanned Systems.*
  > 中文：多机系统综述，给出命名法与架构分类体系，做集群方向的入门打底。

- **[Unmanned Aerial Vehicles: An Overview](http://insidegnss.com/auto/janfeb08-wp.pdf)** `2008` `Survey` `Navigation`
  *Bento, Inside GNSS.*
  > 中文：经典老文，讲 GPS/INS 组合导航与卡尔曼滤波在小型无人机上的应用。

### Planning & Control Surveys

- **[Research on Unmanned Aerial Vehicle Path Planning](https://www.mdpi.com/2504-446X/8/2/51/pdf?version=1707050317)** `2024` `Survey` `Planning`
  *Luo, Tian & Wang, Drones.*
  > 中文：路径规划算法分类综述，优缺点列得清楚，选方法之前先读这篇。

- **[An Overview of Q-Learning and Deep Q-Learning for an Autonomous Multi-UAV Wireless Network](https://onlinelibrary.wiley.com/doi/10.1111/exsy.70143)** `2024` `Survey` `RL` `Network`
  *Sharma & Roy, Expert Systems.*
  > 中文：Q-learning / DQN 在多无人机无线网络里做路径规划、中继与资源调度。

### Swarm & Multi-UAV Surveys

- **[UAV Swarm Intelligence: Recent Advances and Future Trends](https://ieeexplore.ieee.org/document/9214446/)** `2020` `Survey` `Swarm`
  *Zhou, Rao & Wang, IEEE Access.*  ·  📜 DOI: `10.1109/ACCESS.2020.3028865`
  > 中文：集群智能五层框架（决策/规划/控制/通信/应用），引用量很大的经典综述。

- **[UAV swarms: research, challenges, and future directions](https://jeas.springeropen.com/counter/pdf/10.1186/s44147-025-00582-3.pdf)** `2025` `Survey` `Swarm`
  *Alqadsi & Makaraci, J. of Engineering and Applied Science.*
  > 中文：较新的集群综述，覆盖协同路径规划、任务分配、编队控制、安全与 AI/ML 集成。

- **[UAV Swarm Scheduling for Large-Scale Coordination](https://engrxiv.org/preprint/download/6843/version/8894/11187/9502)** `2025` `Survey` `Swarm`
  *Zha et al. (Tsinghua SIGS), engrXiv.*
  > 中文：清华深研院工作，聚焦大规模集群在时空约束下的调度问题，偏运筹优化。

- **[Multi-Agent Deep Reinforcement Learning for Multi-Robot Applications: A Survey](https://www.mdpi.com/1424-8220/23/7/3625/pdf?version=1680188318)** `2023` `Survey` `MADRL`
  *Orr & Dutta, Sensors.*
  > 中文：多智能体深度强化学习在多机器人上的综述，结论可直接迁移到无人机集群。

### Communications & Networking Surveys

- **[UAV-assisted wireless communications in the 6G-and-beyond era: An extensive survey](http://www.mosaic-lab.org/uploads/papers/6bdd8072-7716-4de6-a06a-ce96a05a49a7.pdf)** `2025` `Survey` `6G`
  *Mahbub et al., Vehicular Communications.*
  > 中文：这个方向最厚的一篇综述（约 7 万字），信道建模、能耗、移动性、标准化、太赫兹、RIS、安全全覆盖。

- **[What Will the Future of UAV Cellular Communications Be? A Flight from 5G to 6G](https://ieeexplore.ieee.org/ielaam/9739/9864286/9768113-aam.pdf)** `2022` `Survey` `6G`
  *Geraci et al., IEEE.*
  > 中文：IEEE 教程式文章，从 3GPP 现状讲到 5G NR，再展望 NTN、无蜂窝、RIS、THz。

- **[Green UAV communications for 6G: A survey](https://www.sciencedirect.com/science/article/pii/S1000936121001801)** `2022` `Survey` `GreenCom`
  *Jiang et al.*
  > 中文：绿色通信专题——机载能量有限，怎么节能地把无人机当空中基站。

- **[A Survey on UAV-Aided Maritime Communications](https://zenodo.org/api/files/71e18112-6cd2-4598-9003-b2c170b10159/A_Survey_on_UAV-Aided_Maritime_Communications_Deployment_Considerations_Applications_and_Future_Challenges.pdf)** `2023` `Survey` `Maritime`
  *Nomikos et al., IEEE OJ-COMS.*
  > 中文：海上通信场景——无人机给船、浮标、海洋监测补覆盖。

- **[Networked UAVs for Surveillance and Monitoring: A Survey](https://pdfs.semanticscholar.org/ab84/8f6c0ab61646e606b735d586464933e6d5bb.pdf)** `2017` `Survey` `Network`
  *Li & Savkin, Future Internet.*
  > 中文：网络化无人机做空中传感器网络时的控制、导航与部署优化。

- **[A Survey of Path Loss Prediction and Channel Models for UAS](https://pubmed.ncbi.nlm.nih.gov/37430690/)** `2023` `Survey` `Channel`
  *Moraitis, Psychogios & Panagopoulos, Sensors.*
  > 中文：A2G/A2S/A2A 信道模型与路径损耗预测，做系统级仿真前必读。

- **[Advancements in UAV-based Integrated Sensing and Communication: A Comprehensive Survey](https://arxiv.org/pdf/2501.06526)** `2025` `Survey` `ISAC` `6G`
  *Ahmed et al., arXiv / IEEE IoT J. (under review).*
  > 中文：无人机通感一体化（ISAC）最新综述，涵盖信道估计、波束跟踪、能效、感知-通信权衡与安全。

### Anti-UAV Surveys

- **[A Comprehensive Survey of UAV Detection and Classification Using ML](https://www.mdpi.com/2072-4292/16/5/879/pdf?version=1709544744)** `2024` `Survey` `Anti-UAV`
  *Rahman et al., Remote Sensing.*
  > 中文：按无线电/视觉/声学/雷达四类梳理反无人机技术，附公开数据集清单。

---

## 🧭 Autonomous Navigation & SLAM

具体算法与系统论文（综述见上方 [Navigation & SLAM Surveys](#general-uav-surveys)）。

- **[Large-scale Autonomous Flight with Real-time Semantic SLAM under Dense Forest Canopy](https://arxiv.org/pdf/2109.06479v5)** `2021` `System` `LiDAR-SLAM`
  *Liu, Nardari … Kumar, arXiv.*
  > 中文：Vijay Kumar 组明星工作——密林冠层下用 LiDAR 识别树干和地面做语义建图，实现大范围无 GPS 自主飞行。

- **[A Simultaneous Control, Localization, and Mapping (SCLAM) for UAVs in GPS-Denied Environments](https://pdfs.semanticscholar.org/f595/ee5894ac4e376e8e61a1d321ab534a803943.pdf)** `2024` `Method` `Visual-SLAM`
  *Munguia et al., Drones.*
  > 中文：单目视觉 SLAM 与控制一体化，支持无 GPS 环境下自主探索与返航。

- **[Visual–Inertial Autonomous UAV Navigation in Complex Illumination Under Canopy](https://www.mdpi.com/2504-446X/9/1/27)** `2025` `System` `VIO`
  *Zhao et al., Drones.*
  > 中文：针对林下低光照、密集遮挡，融合图像增强、视觉特征与高维误差状态滤波。

- **[Autonomous UAV navigation in post-disaster environments using ORB-SLAM](https://ceur-ws.org/Vol-4204/ShortPaper5.pdf)** `2023` `Case-Study` `Visual-SLAM`
  *Riabchun et al., CEUR.*
  > 中文：验证 ORB-SLAM 能否单独支撑灾后救援无人机导航。

- **[Monocular Depth Estimation for Autonomous UAV Navigation Based on Deep Learning](https://ieeexplore.ieee.org/document/10279533)** `2023` `Method` `Depth-Estimation`
  *Hensel et al., IEEE.*
  > 中文：低成本无 IMU 无人机，用深度估计网络补单目深度做室内建图。

---

## 🗺 Path Planning

- **[Dynamic Scene Path Planning of UAVs Based on Deep Reinforcement Learning](https://www.mdpi.com/2504-446X/8/2/60/pdf?version=1707490422)** `2024` `Method` `DRL`
  *Tang, Liang & Li, Drones.*
  > 中文：改进 D3QN 带优先级经验回放，动态场景下跑赢 A*、RRT 和原版 DQN。

- **[Three-Dimensional Path Planning Based on Environment Exploration TD3 (EE-TD3)](https://www.mdpi.com/2073-8994/15/7/1371/pdf?version=1688562644)** `2023` `Method` `DRL`
  *Zhang et al., Symmetry.*
  > 中文：在 TD3 基础上加对称 3D 环境探索编码，加速动态 3D 环境收敛。

- **[Globally Guided Deep V-Network Motion Planning for Fixed-Wing UAVs](https://pdfs.semanticscholar.org/303b/f1aad17aaddaa17ff7c3595a1dfb89569281.pdf)** `2024` `Method` `Fixed-Wing`
  *Du, You & Zhao, Sensors.*
  > 中文：固定翼专用分层规划——全局给引导，局部 RL 躲动态障碍。

- **[Spectrum Surveying: Active Radio Map Estimation with Autonomous UAVs](https://arxiv.org/pdf/2201.04125)** `2022` `Method` `Active-Perception`
  *Shrestha, Romero & Chepuri, arXiv.*
  > 中文：无人机主动选点采集无线电信号，用贝叶斯+深度学习快速建电磁地图。

---

## 🐝 Swarm & Multi-UAV Coordination

具体算法（综述见上方 [Swarm Surveys](#swarm--multi-uav-surveys)）。

- **[A Study of Collaborative Trajectory Planning Based on Starling Swarm Bionic Algorithm](https://www.mdpi.com/2076-3417/13/11/6795/pdf?version=1685936996)** `2023` `Method` `Bionic`
  *Chen et al., Applied Sciences.*
  > 中文：模仿欧椋鸟群飞行为的协同轨迹规划，适合算力有限的轻量固定翼集群。

---

## 👁 Visual Perception & Object Detection

- **[DCS-YOLOv8: Lightweight Context-Aware Network for Small Object Detection in UAV Imagery](https://mdpi-res.com/d_attachment/remotesensing/remotesensing-17-02989/article_deploy/remotesensing-17-02989.pdf?version=1756384554)** `2025` `Method` `YOLO`
  *Zhao, Yang & Zhao, Remote Sensing.*  ·  📊 Dataset: VisDrone2019
  > 中文：针对小目标难检，加动态卷积注意力+P2 检测头，VisDrone 上 mAP 40.6→44.5，RK3588 嵌入式实测。

- **[IF-YOLO: UAV Object Detection via Information-Preserving Feature Aggregation](https://www.mdpi.com/2072-4292/16/14/2590/pdf?version=1721054269)** `2024` `Method` `YOLO`
  *Zhang et al. (NUDT), Remote Sensing.*  ·  📊 Dataset: VisDrone2019
  > 中文：国防科大工作，解决特征聚合时小目标信息丢失与多层特征冲突，VisDrone mAP 47.3%。

- **[YOLOFIV: Around-the-Clock Aerial Detection via Infrared+Visible Fusion](https://ieeexplore.ieee.org/document/10643643)** `2024` `Method` `Multimodal`
  *Wang et al., IEEE J-STARS.*
  > 中文：红外+可见光双流融合，昼夜全天候航拍检测，带旋转检测头。

- **[AERO: Onboard Edge AI for UAV Remote Sensing](https://pdfs.semanticscholar.org/2925/f4caa6c7ff37b0b9bfe76266f205497361dc.pdf)** `2023` `System` `Edge-AI`
  *Koubaa et al., Remote Sensing.*
  > 中文：机载边缘系统，YOLOv4/v7+DeepSORT+TensorRT 在 Jetson Xavier 上跑 15.5 FPS。

- **[Active Object Detection and Tracking Using Gimbal Mechanisms](https://www.mdpi.com/2504-446X/8/2/55/pdf?version=1707220068)** `2024` `Method` `Tracking`
  *Hansen & Figueiredo, Drones.*
  > 中文：三轴云台主动追踪，减少运动模糊，6D 位姿估计比被动相机更准。

---

## 📡 Wireless Communications & Networking

具体方法（综述见上方 [Comms Surveys](#communications--networking-surveys)）。

---

## 🛡 Anti-UAV Detection

- **[A Comprehensive Survey of UAV Detection and Classification Using ML](https://www.mdpi.com/2072-4292/16/5/879/pdf?version=1709544744)** `2024` `Survey` `Anti-UAV`
  *Rahman et al., Remote Sensing.*
  > 中文：按 RF/视觉/声学/雷达四类梳理反无人机技术，附公开数据集。

---

## 📊 Datasets & Benchmarks

| Dataset | Task | Description | Link |
|---|---|---|---|
| **VisDrone2019** | Object Detection | 无人机视角目标检测 / 跟踪，密集小目标场景 | [github.com/VisDrone/VisDrone-Dataset](https://github.com/VisDrone/VisDrone-Dataset) |
| **UAVDT** | Detection / Tracking | 城市无人机视角车辆检测跟踪 | [paperswithcode](https://paperswithcode.com/dataset/uavdt) |
| **DroneVehicle** | Detection | 红外+可见光车辆检测 | [github.com/ VisDrone](https://github.com/VisDrone/VisDrone-Dataset) |
| **EUROC MAV** | VIO / SLAM | 无人机视觉-惯性里程计标准数据集 | [euroc-mav.github.io](https://projects.asl.ethz.ch/datasets/dataset/EuRoCMAV) |
| **KITTI-360 / Newer College** | LiDAR / Visual SLAM | 通用 SLAM 基准（可迁移到无人机场景） | — |

> 欢迎补充更多 UAV 专用数据集。

---

## 🛠 Open-source Projects & Simulation

- **[PX4 Autopilot](https://github.com/PX4/PX4-Autopilot)** — 开源飞控固件，支持多旋翼/固定翼/垂起，研究界最常用。
- **[ArduPilot](https://github.com/ArduPilot/ardupilot)** — 另一套成熟开源飞控，社区活跃。
- **[AirSim](https://github.com/microsoft/AirSim)** — 微软开源无人机/车辆仿真器，基于 Unreal Engine。
- **[Flightmare](https://github.com/uzh-rpg/flightmare)** — UZH RPG 组的高性能多旋翼仿真器，支持大规模并行。
- **[Gazebo](https://github.com/gazebosim/gazebo)** — 通用机器人仿真器，搭配 ROS 做无人机开发。
- **[ROS / ROS 2](https://docs.ros.org/)** — 机器人操作系统，无人机算法开发标准中间件。
- **[ORB-SLAM2](https://github.com/raulmur/ORB_SLAM2)** — 经典视觉 SLAM 开源实现。
- **[VINS-Fusion](https://github.com/HKUST-Aerial-Robotics/VINS-Fusion)** — 港科大黄宇捷组视觉-惯性融合开源方案。

---

## Contributing

PRs welcome! When adding a paper, please include:
- **Year** + **Type** (`Survey` / `Method` / `System` / `Dataset` / `Tool`) + key **tags**
- A working PDF / publisher link (avoid Sci-Hub / staging domains)
- One-line English summary **and** one-line Chinese summary
- Code / Dataset links **only if they actually exist**; otherwise mark `N/A` — do not fabricate.

## License

[CC0-1.0](https://creativecommons.org/publicdomain/zero/1.0/)