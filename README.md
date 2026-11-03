# Awesome UAV Papers

> 📚 一个持续整理的无人机（UAV / Drone）研究论文库，覆盖自主导航、路径规划、集群协同、视觉感知、通信网络与反无人机等方向。

A curated list of influential research papers on Unmanned Aerial Vehicles (UAVs / Drones), spanning perception, navigation, planning, swarms, communications and counter-UAV systems.

## Contents

- [Surveys & Overviews](#surveys--overviews)
- [Autonomous Navigation & SLAM](#autonomous-navigation--slam)
- [Path Planning](#path-planning)
- [Swarm & Multi-UAV Coordination](#swarm--multi-uav-coordination)
- [Visual Perception & Object Detection](#visual-perception--object-detection)
- [Wireless Communications & Networking](#wireless-communications--networking)
- [Anti-UAV Detection & Classification](#anti-uav-detection--classification)

---

## Surveys & Overviews

- **[UAVs: practical aspects, applications, open challenges, security issues, and future trends](https://link.springer.com/content/pdf/10.1007/s11370-022-00452-4.pdf)** — *Mohsan et al., Intelligent Service Robotics, 2023.* Comprehensive review of UAV types, swarms, charging methods, regulations, application scenarios and security issues.
  > 中文：最全面的入门综述，把 UAV 分类、集群、充电、法规、应用场景与安全问题串成一张全景图。
- **[Recent Advances in Unmanned Aerial Vehicles: A Review](https://link.springer.com/content/pdf/10.1007/s13369-022-06738-0.pdf)** — *Ahmed et al., Arabian Journal for Science and Engineering, 2022.* Systematic review of 254 papers over the past decade, covering structure, sensing, path planning and AI behaviour.
  > 中文：筛了近 10 年 254 篇文献，梳理机体结构、飞行机制、感知、路径规划与 AI 行为的演进路线。
- **[Multiple UAV Systems: A Survey](https://pdfs.semanticscholar.org/bdb6/52a49782e5ca907d6cc729a473d77de763a3.pdf)** — *Skorobogatov, Barrado & Salami, Unmanned Systems.* A general review of multi-UAV applications with a nomenclature and architecture taxonomy.
  > 中文：专门讲多机系统的综述，给出命名法与架构分类体系，做集群方向的入门打底。
- **[Unmanned Aerial Vehicles: An Overview](http://insidegnss.com/auto/janfeb08-wp.pdf)** — *Bento, Inside GNSS.* Classic introduction to UAV classification, MEMS navigation, GPS/INS integration and Kalman-filter state estimation.
  > 中文：经典老文，讲 GPS/INS 组合导航与卡尔曼滤波在小型无人机上的应用，理解状态估计的历史脉络用。

## Autonomous Navigation & SLAM

- **[Large-scale Autonomous Flight with Real-time Semantic SLAM under Dense Forest Canopy](https://arxiv.org/pdf/2109.06479v5)** — *Liu, Nardari … Kumar, arXiv, 2021.* LiDAR-based semantic SLAM (tree trunks + ground planes) enabling large-scale autonomous flight under GPS-denied forest canopy.
  > 中文：Vijay Kumar 组的明星工作——密林冠层下用 LiDAR 识别树干和地面做语义建图，实现大范围无 GPS 自主飞行。
- **[A Simultaneous Control, Localization, and Mapping System for UAVs in GPS-Denied Environments](https://pdfs.semanticscholar.org/f595/ee5894ac4e376e8e61a1d321ab534a803943.pdf)** — *Munguia et al., Drones.* Visual monocular-SLAM integrated with high-level control for autonomous exploration and return-to-home.
  > 中文：单目视觉 SLAM 与控制一体化（SCLAM），支持无 GPS 环境下自主探索与返航。
- **[Visual–Inertial Autonomous UAV Navigation in Complex Illumination and Highly Cluttered Under-Canopy Environments](https://www.mdpi.com/2504-446X/9/1/27)** — *Zhao et al., Drones, 2025.* Image enhancement + ESIKF + boundary-sampling exploration for GNSS-denied, low-light forest under-canopy flight.
  > 中文：针对林下低光照、密集遮挡场景，融合图像增强、视觉特征与高维误差状态滤波，工程性很强。
- **[Autonomous UAV navigation in post-disaster environments using ORB-SLAM](https://ceur-ws.org/Vol-4204/ShortPaper5.pdf)** — *Riabchun et al., CEUR, 2023.* Feasibility study of ORB-SLAM as the sole onboard navigation module for disaster-response UAVs.
  > 中文：验证 ORB-SLAM 能否单独支撑灾后救援无人机导航，结论可行但对视觉退化环境敏感。
- **[Monocular Depth Estimation for Autonomous UAV Navigation Based on Deep Learning](https://ieeexplore.ieee.org/document/10279533)** — *Hensel et al., IEEE, 2023.* Deep monocular depth + visual SLAM for indoor drone mapping without an IMU.
  > 中文：低成本无 IMU 无人机，用深度估计网络补单目深度做室内建图。

## Path Planning

- **[Research on Unmanned Aerial Vehicle Path Planning](https://www.mdpi.com/2504-446X/8/2/51/pdf?version=1707050317)** — *Luo, Tian & Wang, Drones, 2024.* Taxonomy of UAV path-planning algorithms with a detailed comparison of strengths, weaknesses and open challenges.
  > 中文：Drones 上的算法分类综述，优缺点列得清楚，选方法之前先读这篇。
- **[Dynamic Scene Path Planning of UAVs Based on Deep Reinforcement Learning](https://www.mdpi.com/2504-446X/8/2/60/pdf?version=1707490422)** — *Tang, Liang & Li, Drones, 2024.* Improved D3QN with prioritized experience replay; outperforms A*, RRT and vanilla DQN in dynamic scenes.
  > 中文：改进 D3QN 带优先级经验回放，在动态场景下跑赢 A*、RRT 和原版 DQN。
- **[Three-Dimensional Path Planning of UAVs in a Complex Dynamic Environment Based on Environment Exploration TD3 (EE-TD3)](https://www.mdpi.com/2073-8994/15/7/1371/pdf?version=1688562644)** — *Zhang et al., Symmetry, 2023.* Symmetric 3D environment-exploration coding on top of TD3 for faster convergence in dynamic 3D environments.
  > 中文：在 TD3 基础上加对称 3D 环境探索编码（EE-TD3），加速动态 3D 环境下的收敛。
- **[Globally Guided Deep V-Network-Based Motion Planning Algorithm for Fixed-Wing UAVs](https://pdfs.semanticscholar.org/303b/f1aad17aaddaa17ff7c3595a1dfb89569281.pdf)** — *Du, You & Zhao, Sensors, 2024.* Hierarchical global planner + local RL planner for fixed-wing UAVs among static and dynamic obstacles.
  > 中文：固定翼专用分层规划——全局规划器给引导，局部 RL 规划器躲动态障碍。
- **[Spectrum Surveying: Active Radio Map Estimation with Autonomous UAVs](https://arxiv.org/pdf/2201.04125)** — *Shrestha, Romero & Chepuri, arXiv.* Bayesian + deep-learning active sensing: UAV actively chooses waypoints to build radio maps efficiently.
  > 中文：无人机主动选点采集无线电信号，用贝叶斯+深度学习快速建电磁地图，偏感知规划。

## Swarm & Multi-UAV Coordination

- **[UAV Swarm Intelligence: Recent Advances and Future Trends](http://xplorestaging.ieee.org/ielx7/6287639/8948470/09214446.pdf?arnumber=9214446)** — *Zhou, Rao & Wang, IEEE Access, 2020.* Five-layer survey (decision / planning / control / communication / application) of UAV swarm intelligence.
  > 中文：集群智能五层框架（决策/规划/控制/通信/应用），引用量很大的经典综述。
- **[UAV swarms: research, challenges, and future directions](https://jeas.springeropen.com/counter/pdf/10.1186/s44147-025-00582-3.pdf)** — *Alqadsi & Makaraci, Journal of Engineering and Applied Science, 2025.* Coordinated path planning, task assignment, formation control, security and AI/ML integration for swarms.
  > 中文：较新的集群综述，覆盖协同路径规划、任务分配、编队控制、安全与 AI/ML 集成。
- **[UAV Swarm Scheduling for Large-Scale Coordination: Applications, Challenges, Opportunities](https://engrxiv.org/preprint/download/6843/version/8894/11187/9502)** — *Zha et al. (Tsinghua SIGS), engrXiv.* Scheduling and planning algorithms for large-scale swarms under spatiotemporal constraints.
  > 中文：清华深研院工作，聚焦大规模集群在时空约束下的调度问题，偏运筹优化。
- **[Multi-Agent Deep Reinforcement Learning for Multi-Robot Applications: A Survey](https://www.mdpi.com/1424-8220/23/7/3625/pdf?version=1680188318)** — *Orr & Dutta, Sensors, 2023.* MADRL survey covering multi-robot coordination directly applicable to UAV fleets.
  > 中文：多智能体深度强化学习在多机器人上的综述，结论可直接迁移到无人机集群。
- **[An Overview of Q-Learning and Deep Q-Learning for an Autonomous Multi-UAV Wireless Network](https://onlinelibrary.wiley.com/doi/10.1111/exsy.70143)** — *Sharma & Roy, Expert Systems.* QL/DQL for route planning, relays, resource allocation and task scheduling in multi-UAV wireless networks.
  > 中文：Q-learning / 深度 Q-learning 在多无人机无线网络里做路径规划、中继与资源调度。
- **[A Study of Collaborative Trajectory Planning Based on Starling Swarm Bionic Algorithm for Multi-UAV](https://www.mdpi.com/2076-3417/13/11/6795/pdf?version=1685936996)** — *Chen et al., Applied Sciences, 2023.* Bionic starling-flock trajectory planning for lightweight fixed-wing swarms with limited onboard compute.
  > 中文：模仿欧椋鸟群飞行为的协同轨迹规划，适合算力有限的轻量固定翼集群。

## Visual Perception & Object Detection

- **[DCS-YOLOv8: A Lightweight Context-Aware Network for Small Object Detection in UAV Remote Sensing Imagery](https://mdpi-res.com/d_attachment/remotesensing/remotesensing-17-02989/article_deploy/remotesensing-17-02989.pdf?version=1756384554)** — *Zhao, Yang & Zhao, Remote Sensing, 2025.* DCAM attention + P2 detection head + SDBIoU loss; validated on VisDrone2019 and deployed on RK3588.
  > 中文：针对小目标难检问题，加动态卷积注意力+P2 检测头，VisDrone 上 mAP 从 40.6% 提到 44.5%，RK3588 嵌入式实测。
- **[UAV Object Detection Based on Information-Preserving and Fine-Grained Feature Aggregation (IF-YOLO)](https://www.mdpi.com/2072-4292/16/14/2590/pdf?version=1721054269)** — *Zhang et al. (NUDT), Remote Sensing, 2024.* IPFA + CSFM + FGAFPN to improve small/weak targets on VisDrone2019.
  > 中文：国防科大工作，解决特征聚合时小目标信息丢失与多层特征冲突，VisDrone mAP 47.3%。
- **[YOLOFIV: Around-the-Clock Aerial Object Detection by Fusing Infrared and Visible Features](https://ieeexplore.ieee.org/document/10643643)** — *Wang et al., IEEE J-STARS.* Dual-stream infrared+visible backbone with rotating detection head for 24/7 aerial detection.
  > 中文：红外+可见光双流融合，做昼夜全天候航拍目标检测，带旋转检测头。
- **[AERO: AI-Enabled Remote Sensing Observation with Onboard Edge Computing in UAVs](https://pdfs.semanticscholar.org/2925/f4caa6c7ff37b0b9bfe76266f205497361dc.pdf)** — *Koubaa et al., Remote Sensing.* Cloud-edge architecture with YOLOv4/v7 + DeepSORT + TensorRT on Jetson Xavier AGX (~15.5 FPS).
  > 中文：机载边缘系统，YOLOv4/v7+DeepSORT+TensorRT 在 Jetson Xavier 上跑 15.5 FPS，检测+跟踪+上云一条龙。
- **[Active Object Detection and Tracking Using Gimbal Mechanisms for Autonomous Drone Applications](https://www.mdpi.com/2504-446X/8/2/55/pdf?version=1707220068)** — *Hansen & Figueiredo, Drones, 2024.* Active gimbal tracking reduces motion blur and improves 6D pose estimation vs. passive cameras.
  > 中文：三轴云台主动追踪目标，减少运动模糊，6D 位姿估计比被动相机明显更准。

## Wireless Communications & Networking

- **[UAV-assisted wireless communications in the 6G-and-beyond era: An extensive survey](http://www.mosaic-lab.org/uploads/papers/6bdd8072-7716-4de6-a06a-ce96a05a49a7.pdf)** — *Mahbub et al., Vehicular Communications.* Channel modelling, energy, mobility, standardization, AI routing, sub-THz/THz, RIS and security for UAV-to-ground / UAV-to-UAV / UAV-to-satellite links.
  > 中文：这个方向最厚的一篇综述（约 7 万字），信道建模、能耗、移动性、标准化、太赫兹、RIS、安全全覆盖。
- **[What Will the Future of UAV Cellular Communications Be? A Flight from 5G to 6G](https://ieeexplore.ieee.org/ielaam/9739/9864286/9768113-aam.pdf)** — *Geraci et al., IEEE.* Tutorial covering 3GPP aerial-device features, massive MIMO, mmWave coverage, NTN, cell-free, RIS and THz enablers.
  > 中文：IEEE 教程式文章，从 3GPP 现状讲到 5G NR 支持无人机，再展望 NTN、无蜂窝、RIS、THz 这些 6G 使能技术。
- **[Green UAV communications for 6G: A survey](https://sci-hub.ru/download/2024/8646/0af6af33bc640ea8da6325a07cb128ad/jiang2022.pdf)** — *Jiang et al.* Energy-efficient UAV deployment as aerial base stations, relays and mobile users.
  > 中文：绿色通信专题——机载能量有限，怎么节能地把无人机当空中基站用。
- **[A Survey on UAV-Aided Maritime Communications](https://zenodo.org/api/files/71e18112-6cd2-4598-9003-b2c170b10159/A_Survey_on_UAV-Aided_Maritime_Communications_Deployment_Considerations_Applications_and_Future_Challenges.pdf)** — *Nomikos et al., IEEE OJ-COMS.* UAV-aided maritime coverage, resource management, edge caching and trajectory optimisation.
  > 中文：海上通信场景——无人机给船、浮标、海洋监测补覆盖，含资源管理与轨迹优化。
- **[Networked Unmanned Aerial Vehicles for Surveillance and Monitoring: A Survey](https://pdfs.semanticscholar.org/ab84/8f6c0ab61646e606b735d586464933e6d5bb.pdf)** — *Li & Savkin, Future Internet.* Control, navigation and deployment optimisation of networked UAVs as aerial sensor networks.
  > 中文：网络化无人机做空中传感器网络时的控制、导航与部署优化。
- **[A Survey of Path Loss Prediction and Channel Models for UAS System-Level Simulations](https://pubmed.ncbi.nlm.nih.gov/37430690/)** — *Moraitis, Psychogios & Panagopoulos, Sensors, 2023.* Air-to-ground / air-to-space / air-to-air channel models for 6G UAS simulations.
  > 中文：A2G/A2S/A2A 信道模型与路径损耗预测，做系统级仿真前必读。

## Anti-UAV Detection & Classification

- **[A Comprehensive Survey of UAV Detection and Classification Using Machine Learning: Challenges, Solutions, and Future Directions](https://www.mdpi.com/2072-4292/16/5/879/pdf?version=1709544744)** — *Rahman et al., Remote Sensing, 2024.* RF-based, vision-based, acoustic-based and radar-based UAV detection, plus hybrid-sensor and RL approaches, with dataset overview.
  > 中文：按无线电/视觉/声学/雷达四类梳理反无人机技术，外加混合传感与强化学习方法，并附公开数据集清单。

---

## Contributing

This list is community-curated. PRs adding high-quality UAV papers (with a working link and a one-line summary) are welcome.

## License

[CC0-1.0](https://creativecommons.org/publicdomain/zero/1.0/) — To the extent possible under law, the curator has waived all copyrights on this list.
