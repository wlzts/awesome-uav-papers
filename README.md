# Awesome UAV Papers

> 📚 **无人机科研论文 + 中文导读 + 算法对比 + 代码复现 + 研究路线** 的一站式开源资源库。
>
> 覆盖自主导航、路径规划、集群协同、视觉感知、6G 通信、反无人机与行业应用等方向，收录 2022–2026 年精选论文，每篇附中英文摘要、年份、类型标签与 Code / DOI 信息。

A curated list of UAV / Drone research papers with Chinese reading notes, organized by research direction, plus reading roadmaps, datasets and open-source tools.

🔍 **[在线检索界面 →](https://wlzts.github.io/awesome-uav-papers/)** 支持按标题、作者、方向、年份、类型实时过滤。

---

## 📑 Contents

- [🚀 Start Here — Reading Roadmaps](#-start-here--reading-roadmaps)
- [📚 Surveys & Overviews](#-surveys--overviews)
- [🧭 Autonomous Navigation & SLAM](#-autonomous-navigation--slam)
- [🗺 Path Planning](#-path-planning)
- [🐝 Swarm & Multi-UAV Coordination](#-swarm--multi-uav-coordination)
- [👁 Visual Perception & Object Detection](#-visual-perception--object-detection)
- [📡 Wireless Communications & Networking](#-wireless-communications--networking)
- [🛡 Anti-UAV Detection](#-anti-uav-detection)
- [🚜 Applications: Agriculture, Inspection & Delivery](#-applications-agriculture-inspection--delivery)
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

1. 先读 **[VINS-Fusion](https://github.com/HKUST-Aerial-Robotics/VINS-Fusion)** 理解视觉-惯性融合开源方案。
2. 再读 **[Faster-LIO](https://github.com/gaoxiang12/faster-lio)** 看轻量紧耦合 LiDAR-惯性里程计。
3. 工程落地看 **[Visual-Inertial Navigation Under Canopy](https://www.mdpi.com/2504-446X/9/1/27)** 和 **[Large-scale Semantic SLAM under Forest Canopy](https://arxiv.org/pdf/2109.06479v5)**。

### 🐝 如果你做集群协同

1. **[UAV Swarm Intelligence: Recent Advances](https://ieeexplore.ieee.org/document/9214446/)** `2020` `Survey` — 五层框架（决策/规划/控制/通信/应用）。
2. **[UAV swarms: research, challenges, future directions](https://jeas.springeropen.com/counter/pdf/10.1186/s44147-025-00582-3.pdf)** `2025` `Survey` — 最新进展。
3. 方法层看 **[MADRL for Multi-Robot: A Survey](https://www.mdpi.com/1424-8220/23/7/3625/pdf)**。

### 🧠 如果你做强化学习 / 路径规划

1. **[Research on UAV Path Planning (综述)](https://www.mdpi.com/2504-446X/8/2/51/pdf)** `2024` `Survey` — 先搞清楚传统算法版图。
2. **[Dynamic Scene Path Planning via DRL (D3QN)](https://www.mdpi.com/2504-446X/8/2/60/pdf)** — 看 DRL 怎么跑赢 A*/RRT。
3. **[TOGT: Time-Optimal Gate-Traversing Planner](https://github.com/FSC-Lab/TOGT-Planner)** — ICRA 2024 最佳 UAV 论文，无人机竞速轨迹规划。

> ⚠️ 以上路线是推荐顺序，不是唯一路径；实际研究中常常组合使用多种方法。

---

## 📚 Surveys & Overviews

### General UAV Surveys

- **[UAVs: practical aspects, applications, open challenges, security issues, and future trends](https://link.springer.com/content/pdf/10.1007/s11370-022-00452-4.pdf)** `2023` `Survey` `General`
  *Mohsan et al., Intelligent Service Robotics.*
  > 中文：最全面的入门综述，把 UAV 分类、集群、充电、法规、应用场景与安全问题串成一张全景图。
  > 📜 DOI: `10.1007/s11370-022-00452-4` · 💻 Code: N/A · 📊 Data: N/A

- **[Recent Advances in Unmanned Aerial Vehicles: A Review](https://link.springer.com/content/pdf/10.1007/s13369-022-06738-0.pdf)** `2022` `Survey` `General`
  *Ahmed et al., Arabian J. for Science and Engineering.*
  > 中文：筛了近 10 年 254 篇文献，梳理机体、感知、路径规划与 AI 行为的演进路线。
  > 📜 DOI: `10.1007/s13369-022-06738-0` · 💻 Code: N/A · 📊 Data: N/A

- **[Multiple UAV Systems: A Survey](https://pdfs.semanticscholar.org/bdb6/52a49782e5ca907d6cc729a473d77de763a3.pdf)** `2018` `Survey` `Swarm`
  *Skorobogatov, Barrado & Salami, Unmanned Systems.*
  > 中文：多机系统综述，给出命名法与架构分类体系，做集群方向的入门打底。
  > 📜 DOI: N/A · 💻 Code: N/A · 📊 Data: N/A

- **[A Review of UAV Autonomous Navigation in GPS-Denied Environments](https://www.sciencedirect.com/science/article/abs/pii/S0921889023001347)** `2023` `Survey` `Navigation`
  *Zhao et al., Robotics and Autonomous Systems.*
  > 中文：GPS 拒止环境下 UAV 自主导航综述，覆盖视觉、LiDAR、惯性融合与多传感器方案对比。
  > 📜 DOI: `10.1016/j.robot.2023.104350` · 💻 Code: N/A · 📊 Data: N/A

### Planning & Control Surveys

- **[Research on Unmanned Aerial Vehicle Path Planning](https://www.mdpi.com/2504-446X/8/2/51/pdf)** `2024` `Survey` `Planning`
  *Luo, Tian & Wang, Drones.*
  > 中文：路径规划算法分类综述，优缺点列得清楚，选方法之前先读这篇。
  > 📜 DOI: `10.3390/drones8020051` · 💻 Code: N/A · 📊 Data: N/A

- **[An Overview of Q-Learning and Deep Q-Learning for an Autonomous Multi-UAV Wireless Network](https://onlinelibrary.wiley.com/doi/10.1111/exsy.70143)** `2024` `Survey` `RL` `Network`
  *Sharma & Roy, Expert Systems.*
  > 中文：Q-learning / DQN 在多无人机无线网络里做路径规划、中继与资源调度。
  > 📜 DOI: `10.1111/exsy.70143` · 💻 Code: N/A · 📊 Data: N/A

- **[Autonomous Drone Racing: A Survey](https://arxiv.org/abs/2306.09218)** `2023` `Survey` `Racing`
  *Kaufmann et al., arXiv.*
  > 中文：无人机竞速综述，涵盖感知、规划、控制全栈，ICRA 最佳论文团队出品。
  > 📜 DOI: N/A · 💻 Code: N/A · 📊 Data: N/A

- **[UAVs Meet LLMs: Overviews and Perspectives Toward Agentic Low-Altitude Mobility](https://arxiv.org/abs/2501.02341)** `2025` `Survey` `LLM`
  *Tian et al., arXiv.*
  > 中文：大模型驱动低空机动 agent 的最新综述，VLM 导航、任务规划与人机协作。
  > 📜 DOI: N/A · 💻 Code: https://github.com/Hub-Tian/UAVs_Meet_LLMs · 📊 Data: N/A

### Swarm & Multi-UAV Surveys

- **[UAV Swarm Intelligence: Recent Advances and Future Trends](https://ieeexplore.ieee.org/document/9214446/)** `2020` `Survey` `Swarm`
  *Zhou, Rao & Wang, IEEE Access.*
  > 中文：集群智能五层框架（决策/规划/控制/通信/应用），引用量很大的经典综述。
  > 📜 DOI: `10.1109/ACCESS.2020.3028865` · 💻 Code: N/A · 📊 Data: N/A

- **[UAV swarms: research, challenges, and future directions](https://jeas.springeropen.com/counter/pdf/10.1186/s44147-025-00582-3.pdf)** `2025` `Survey` `Swarm`
  *Alqadsi & Makaraci, J. of Engineering and Applied Science.*
  > 中文：较新的集群综述，覆盖协同路径规划、任务分配、编队控制、安全与 AI/ML 集成。
  > 📜 DOI: `10.1186/s44147-025-00582-3` · 💻 Code: N/A · 📊 Data: N/A

- **[UAV Swarm Scheduling for Large-Scale Coordination](https://engrxiv.org/preprint/download/6843/version/8894/11187/9502)** `2025` `Survey` `Swarm`
  *Zha et al. (Tsinghua SIGS), engrXiv.*
  > 中文：清华深研院工作，聚焦大规模集群在时空约束下的调度问题，偏运筹优化。
  > 📜 DOI: N/A · 💻 Code: N/A · 📊 Data: N/A

- **[Multi-Agent Deep Reinforcement Learning for Multi-Robot Applications: A Survey](https://www.mdpi.com/1424-8220/23/7/3625/pdf)** `2023` `Survey` `MADRL`
  *Orr & Dutta, Sensors.*
  > 中文：多智能体深度强化学习在多机器人上的综述，结论可直接迁移到无人机集群。
  > 📜 DOI: `10.3390/s23073625` · 💻 Code: N/A · 📊 Data: N/A

- **[Advancement Challenges in UAV Swarm Formation Control: A Comprehensive Review](https://www.mdpi.com/1424-8220/24/2/1893/pdf)** `2024` `Survey` `Formation`
  *Bu et al., Sensors.*
  > 中文：无人机编队控制最新综述，集中式 vs 分布式、通信约束、抗扰与避障。
  > 📜 DOI: `10.3390/s24021893` · 💻 Code: N/A · 📊 Data: N/A

### Communications & Networking Surveys

- **[UAV-assisted wireless communications in the 6G-and-beyond era: An extensive survey](http://www.mosaic-lab.org/uploads/papers/6bdd8072-7716-4de6-a06a-ce96a05a49a7.pdf)** `2025` `Survey` `6G`
  *Mahbub et al., Vehicular Communications.*
  > 中文：这个方向最厚的一篇综述（约 7 万字），信道建模、能耗、移动性、标准化、太赫兹、RIS、安全全覆盖。
  > 📜 DOI: N/A · 💻 Code: N/A · 📊 Data: N/A

- **[What Will the Future of UAV Cellular Communications Be? A Flight from 5G to 6G](https://ieeexplore.ieee.org/document/9768113/)** `2022` `Survey` `6G`
  *Geraci et al., IEEE Communications Surveys & Tutorials.*
  > 中文：IEEE 教程式文章，从 3GPP 现状讲到 5G NR，再展望 NTN、无蜂窝、RIS、THz。
  > 📜 DOI: `10.1109/COMST.2022.3182826` · 💻 Code: N/A · 📊 Data: N/A

- **[Green UAV communications for 6G: A survey](https://www.sciencedirect.com/science/article/pii/S1000936121001801)** `2022` `Survey` `GreenCom`
  *Jiang et al., China Communications.*
  > 中文：绿色通信专题——机载能量有限，怎么节能地把无人机当空中基站。
  > 📜 DOI: `10.23919/JCC.ja.2022.01.03` · 💻 Code: N/A · 📊 Data: N/A

- **[A Survey on UAV-Aided Maritime Communications](https://zenodo.org/api/files/71e18112-6cd2-4598-9003-b2c170b10159/A_Survey_on_UAV-Aided_Maritime_Communications_Deployment_Considerations_Applications_and_Future_Challenges.pdf)** `2023` `Survey` `Maritime`
  *Nomikos et al., IEEE OJ-COMS.*
  > 中文：海上通信场景——无人机给船、浮标、海洋监测补覆盖。
  > 📜 DOI: N/A · 💻 Code: N/A · 📊 Data: N/A

- **[A Survey of Path Loss Prediction and Channel Models for UAS](https://www.mdpi.com/1424-8220/23/13/5986)** `2023` `Survey` `Channel`
  *Moraitis, Psychogios & Panagopoulos, Sensors.*
  > 中文：A2G/A2S/A2A 信道模型与路径损耗预测，做系统级仿真前必读。
  > 📜 DOI: `10.3390/s23135986` · 💻 Code: N/A · 📊 Data: N/A

- **[Advancements in UAV-based Integrated Sensing and Communication: A Comprehensive Survey](https://arxiv.org/pdf/2501.06526)** `2025` `Survey` `ISAC` `6G`
  *Ahmed et al., arXiv.*
  > 中文：无人机通感一体化（ISAC）最新综述，涵盖信道估计、波束跟踪、能效、感知-通信权衡与安全。
  > 📜 DOI: N/A · 💻 Code: N/A · 📊 Data: N/A

### Anti-UAV Surveys

- **[A Comprehensive Survey of UAV Detection and Classification Using ML](https://www.mdpi.com/2072-4292/16/5/879/pdf)** `2024` `Survey` `Anti-UAV`
  *Rahman et al., Remote Sensing.*
  > 中文：按无线电/视觉/声学/雷达四类梳理反无人机技术，附公开数据集清单。
  > 📜 DOI: `10.3390/rs16050879` · 💻 Code: N/A · 📊 Data: N/A

- **[UAV Detection and Tracking in Urban Environments Using Passive Sensors: A Survey](https://www.mdpi.com/1424-8220/23/3/2397)** `2023` `Survey` `Anti-UAV`
  *Bentamou et al., Sensors.*
  > 中文：城市环境中被动传感器（RF/声学/视觉）反无人机检测与跟踪综述。
  > 📜 DOI: `10.3390/s23032397` · 💻 Code: N/A · 📊 Data: N/A

---

## 🧭 Autonomous Navigation & SLAM

- **[Visual–Inertial Autonomous UAV Navigation in Complex Illumination Under Canopy](https://www.mdpi.com/2504-446X/9/1/27)** `2025` `System` `VIO`
  *Zhao et al., Drones.*
  > 中文：林下低光照下融合图像增强与高维误差状态滤波。
  > 📜 DOI: `10.3390/drones9010027` · 💻 Code: N/A · 📊 Data: N/A

- **[Autonomous Flights inside Narrow Tunnels](https://arxiv.org/abs/2505.19657)** `2025` `System` `autonomous exploration` `narrow tunnel` `ego-disturbance`
  *Luqi Wang, Yan Ning, Hongming Chen, Peize Liu, Yang Xu, Hao Xu, Ximin Lyu, Shaojie Shen, IEEE Transactions on Robotics (TRO).*
  > 中文：直径0.5m窄隧道自主飞行系统，虚拟全向感知+CFD建模的自气流扰动感知重规划，开源部署包。
  > 📜 DOI: `10.1109/TRO.2025.3548525` · 💻 Code: N/A · 📊 Data: N/A

- **[A Simultaneous Control, Localization, and Mapping (SCLAM) for UAVs in GPS-Denied Environments](https://pdfs.semanticscholar.org/f595/ee5894ac4e376e8e61a1d321ab534a803943.pdf)** `2024` `Method` `Visual-SLAM`
  *Munguia et al., Drones.*
  > 中文：单目视觉SLAM与控制一体化，无GPS自主探索返航。
  > 📜 DOI: `10.3390/drones8030126` · 💻 Code: N/A · 📊 Data: N/A

- **[Low Latency Visual Inertial Odometry with On-Sensor Accelerated Optical Flow for Resource-Constrained UAVs](https://arxiv.org/abs/2406.13345)** `2024` `Method` `VIO` `on-sensor acceleration` `nano drone`
  *Jonas Kühne, Michele Magno, Luca Benini, IEEE Sensors Journal.*
  > 中文：用片上ASIC光流传感器替换VINS-Mono特征跟踪，延迟降49%、算力降54%，在树莓派CM4上跑到50FPS。
  > 📜 DOI: N/A · 💻 Code: N/A · 📊 Data: N/A

- **[Swarm-LIO2: Decentralized Efficient LiDAR-Inertial Odometry for Aerial Swarm Systems](https://arxiv.org/abs/2409.17798)** `2024` `System` `LiDAR-inertial` `swarm` `decentralized`
  *Fangcheng Zhu, Yunfan Ren, Li Yan, Fanze Kong, Qianhao Liu, Rui Xue, Wei Liu, Yixi Cai, Guanya Lu, Hengli Li, Fu Zhang, IEEE Transactions on Robotics (TRO).*
  > 中文：完全去中心化即插即用的无人机群LIO，仅交换低维互观量测，实现厘米级自定位与相对定位。
  > 📜 DOI: N/A · 💻 Code: https://github.com/hku-mars/Swarm-LIO2 · 📊 Data: N/A

- **[A Tree-based Next-best-trajectory Method for 3D UAV Exploration (ERRT)](https://arxiv.org/abs/2407.04386)** `2024` `Method` `autonomous exploration` `RRT` `next-best-view`
  *Björn Lindqvist, Akash Patel, Kalle Löfgren, George Nikolakopoulos, IEEE Transactions on Robotics (TRO).*
  > 中文：树状NBV探索规划算法，联合优化信息增益、行驶距离与执行代价，ROS开源，已在地下GPS拒止环境实测。
  > 📜 DOI: N/A · 💻 Code: https://github.com/LTU-RAI/ExplorationRRT · 📊 Data: N/A

- **[LAEA: A 2D LiDAR-Assisted UAV Exploration Algorithm for Unknown Environments](https://www.mdpi.com/2504-446X/8/4/128)** `2024` `Method` `autonomous exploration` `frontier` `LiDAR`
  *Xiaolei Hou, Zheng Pan, Li Lu, Yuhang Wu, Jinwen Hu, Yang Lyu, Chunhui Zhao, Drones (MDPI), 8(4):128.*
  > 中文：2D LiDAR辅助的边界探索算法，重估近距小边界簇权重，避免往返已探索区域，提升探索效率。
  > 📜 DOI: `10.3390/drones8040128` · 💻 Code: N/A · 📊 Data: N/A

- **[MPCC++: Model Predictive Contouring Control for Time-Optimal Flight with Safety Constraints](https://arxiv.org/abs/2403.17551)** `2024` `Method` `MPC` `drone racing` `safety constraints`
  *Maria Krinner, Angel Romero, Leonard Bauersfeld, Melanie Zeilinger, Andrea Carron, Davide Scaramuzza, Robotics: Science and Systems (RSS) 2024.*
  > 中文：在MPCC中加入赛道空间约束与终端集保证安全，学习气动残差，TuRBO调参，80km/h穿越机零撞门。
  > 📜 DOI: N/A · 💻 Code: N/A · 📊 Data: N/A

- **[Autonomous UAV navigation in post-disaster environments using ORB-SLAM](https://ceur-ws.org/Vol-4204/ShortPaper5.pdf)** `2023` `Method` `Visual-SLAM`
  *Riabchun et al., CEUR.*
  > 中文：验证ORB-SLAM能否单独支撑灾后救援导航。
  > 📜 DOI: N/A · 💻 Code: N/A · 📊 Data: N/A

- **[Monocular Depth Estimation for Autonomous UAV Navigation Based on Deep Learning](https://ieeexplore.ieee.org/document/10279533)** `2023` `Method` `Depth-Estimation`
  *Hensel et al., IEEE.*
  > 中文：低成本无IMU无人机用深度估计网络补单目深度。
  > 📜 DOI: `10.1109/ICUAS57470.2023.10279533` · 💻 Code: N/A · 📊 Data: N/A

- **[Visual-Inertial Odometry Using High Flying Altitude Drone Datasets](https://www.mdpi.com/2504-446X/7/1/36)** `2023` `Dataset` `VIO` `outdoor` `dataset`
  *Anand George, Niko Koivumäki, Teemu Hakala, Juha Suomalainen, Eija Honkavaara, Drones (MDPI), 7(1):36.*
  > 中文：在40-100m飞行高度评测VINS-Fusion，立体VIO最优，800m轨迹定位误差2.19m，并公开数据集。
  > 📜 DOI: `10.3390/drones7010036` · 💻 Code: https://github.com/HKUST-Aerial-Robotics/VINS-Fusion · 📊 Data: https://www.mdpi.com/2504-446X/7/1/36

- **[Range-Visual-Inertial Odometry with Coarse-to-Fine Image Registration Fusion for UAV Localization](https://www.mdpi.com/2504-446X/7/8/540)** `2023` `Method` `VIO` `geo-localization` `GNSS-denied`
  *Yun Hao, Mengfan He, Yuzhen Liu, Jiacheng Liu, Ziyang Meng, Drones (MDPI), 7(8):540.*
  > 中文：用1D激光测距抑制VIO尺度漂移，结合CNN由粗到精图像配准实现GNSS拒止下全局无漂移定位。
  > 📜 DOI: `10.3390/drones7080540` · 💻 Code: N/A · 📊 Data: N/A

- **[A Robust Disturbance-Rejection Controller Using Model Predictive Control for Quadrotor UAV in Tracking Aggressive Trajectory](https://www.mdpi.com/2504-446X/7/9/557)** `2023` `Method` `MPC` `disturbance rejection` `aggressive flight`
  *Zhixiong Xu, Li Fan, Wei Qiu, Guangwei Wen, Yunhan He, Drones (MDPI), 7(9):557.*
  > 中文：位置环MPC加电机约束、姿态环SO(3)鲁棒控制，解耦设计，在剧烈轨迹与强扰动下保持高精度跟踪。
  > 📜 DOI: `10.3390/drones7090557` · 💻 Code: N/A · 📊 Data: N/A

- **[Wind Preview-Based Model Predictive Control of Multi-Rotor UAVs Using LiDAR](https://www.mdpi.com/1424-8220/23/7/3711)** `2023` `Method` `MPC` `wind disturbance` `LiDAR sensing`
  *Arthur P. Mendez, James F. Whidborne, Lejun Chen, Sensors (MDPI), 23(7):3711.*
  > 中文：用地基LiDAR提前感知来风，MPC在预测时域内前馈补偿阵风，位置保持性能提升80%。
  > 📜 DOI: `10.3390/s23073711` · 💻 Code: N/A · 📊 Data: N/A

- **[End-to-end neural network based optimal quadcopter control (G&CNets)](https://pure.tudelft.nl/ws/portalfiles/portal/170870840/1_s2.0_S0921889023002270_main.pdf)** `2023` `Method` `learning-based control` `end-to-end` `energy optimal`
  *Robin Ferede, Guido De Croon, Christophe De Wagter, Dario Izzo, Robotics and Autonomous Systems (Elsevier).*
  > 中文：G&CNets直接从最优轨迹学习状态到电调RPM的端到端策略，在线估计未建模力矩补偿sim-to-real差距。
  > 📜 DOI: `10.1016/j.robot.2023.104396` · 💻 Code: N/A · 📊 Data: N/A

- **[A review of UAV autonomous navigation in GPS-denied environments](https://www.sciencedirect.com/science/article/pii/S0921889023001720)** `2023` `Survey` `survey` `GPS-denied` `navigation taxonomy`
  *Yingxiu Chang, Yongqiang Cheng, Umar Manzoor, John Murray, Robotics and Autonomous Systems (Elsevier).*
  > 中文：对GPS拒止下无人机导航做无地图/有地图分类法综述，用120次飞行实验对比CNN监督、边界导航等策略。
  > 📜 DOI: `10.1016/j.robot.2023.104395` · 💻 Code: N/A · 📊 Data: N/A

- **[Semantic Real-Time Mapping with UAVs](https://link.springer.com/article/10.1007/s41064-023-00242-2)** `2023` `System` `semantic mapping` `real-time` `disaster response`
  *Phillipp Fantasia-Jende, Daniel Steininger, Alexander Kern, Verena Widhalm, Javier G. Apud Baca, Markus Hofstätter, Julia Simon, Felix Brücklmüller, Christoph Sulzbachner, PFG – Journal of Photogrammetry, Remote Sensing and Geoinformation Science (Springer).*
  > 中文：在实时三维建图管线中加入土地覆盖语义分割与目标检测，面向灾害响应快速地理数据处理。
  > 📜 DOI: `10.1007/s41064-023-00242-2` · 💻 Code: N/A · 📊 Data: N/A

- **[LOCUS 2.0: Robust and Computationally Efficient Lidar Odometry for Real-Time 3D Mapping](https://arxiv.org/abs/2205.11784)** `2022` `System` `LiDAR odometry` `underground` `DARPA SubT`
  *Andrzej Reinke, Matteo Palieri, Benjamin Morrell, Yun Chang, Kameron Ebadi, Luca Carlone, Aliakbar Agha-mohammadi, IEEE Robotics and Automation Letters (RA-L).*
  > 中文：DARPA地下挑战赛CoSTAR队的轻量LIO，法向GICP+自适应体素+滑窗地图，公开11小时地下数据集。
  > 📜 DOI: `10.1109/LRA.2022.3190110` · 💻 Code: N/A · 📊 Data: https://arxiv.org/abs/2205.11784

- **[Faster-LIO: Lightweight Tightly Coupled Lidar-Inertial Odometry Using Parallel Sparse Incremental Voxels](https://arxiv.org/abs/2202.11281)** `2022` `Method` `LiDAR-inertial` `lightweight` `iVox`
  *Chunge Bai, Tao Xiao, Yajie Chen, Haoqian Wang, Fang Zhang, Xiang Gao, IEEE Robotics and Automation Letters (RA-L).*
  > 中文：用增量稀疏体素iVox替代ikd-Tree，固态LiDAR跟踪达1000-2000Hz，精度与FAST-LIO相当。
  > 📜 DOI: `10.1109/LRA.2022.3161951` · 💻 Code: https://github.com/gaoxiang12/faster-lio · 📊 Data: N/A

- **[Large-scale Autonomous Flight with Real-time Semantic SLAM under Dense Forest Canopy](https://arxiv.org/pdf/2109.06479v5)** `2021` `System` `LiDAR-SLAM` `Semantic`
  *Liu, Nardari … Kumar, arXiv.*
  > 中文：Kumar组密林冠层下LiDAR语义建图，大范围无GPS飞行。
  > 📜 DOI: N/A · 💻 Code: N/A · 📊 Data: N/A
| 方法/代表论文 | 年份 | 核心思路 | 优点 | 局限 | 适用场景 |
|---|---|---|---|---|---|
| VINS-Fusion (stereo-VIO, George 2023) | 2023 | 立体相机+IMU紧耦合VIO，在40-100m高度做GNSS冗余定位 | 成熟开源、立体对抑制尺度漂移、公开高海拔数据集 | 基线/高度比随高度下降而退化，长距离仍有漂移 | 室外中高空巡检、GNSS拒止冗余定位 |
| On-sensor Optical-Flow VIO (Kühne 2024) | 2024 | ASIC片上光流替代CPU特征跟踪，硬件加速VIO前端 | 延迟降49%、算力降54%，适合nano drone资源受限平台 | 依赖专用光流传感器硬件，通用性受限 | 纳米无人机、低功耗嵌入式平台 |
| Faster-LIO (Bai 2022) | 2022 | 用增量稀疏体素iVox替代ikd-Tree做点云配准 | 固态LiDAR跟踪1000-2000Hz，精度与FAST-LIO相当，开源 | 近似k-NN在极端退化场景鲁棒性略逊 | 机载实时LIO、算力受限无人机 |
| Swarm-LIO2 (Zhu 2024) | 2024 | 去中心化群飞LIO，仅交换低维互观量测，ESIKF联合估计自/他机状态 | 即插即用、带宽高效、厘米级精度、开源硬件+算法 | 依赖LiDAR反射率检测队友，密集遮挡下检测率下降 | 无人机群协同探索、GPS拒止集群任务 |
| LOCUS 2.0 (Reinke 2022) | 2022 | 法向GICP+自适应体素+滑窗地图，面向地下大尺度建图 | DARPA SubT验证、公开11小时地下数据集、异构平台适配 | 主要面向腿/轮式平台，无人机轻量部署需裁剪 | 地下/隧道/废墟大尺度LiDAR建图 |
| ERRT Exploration-RRT (Lindqvist 2024) | 2024 | 树状NBV联合优化信息增益、距离与执行代价，Rust NMPC跟踪 | 实时、ROS集成、开源、地下实测 | 局部探索为主，大规模全局重定位能力有限 | 未知3D环境自主探索、地下侦察 |
| MPC + SO(3) Disturbance Rejection (Xu 2023) | 2023 | 位置环MPC加电机约束，姿态环SO(3)非线性鲁棒控制 | 解耦设计、显式电机约束、抗剧烈轨迹与外扰 | 仅仿真验证，未公开实物与代码 | Aggressive轨迹跟踪、抗风扰航线飞行 |
| MPCC++ (Krinner 2024) | 2024 | MPCC加赛道空间约束与终端集，学习气动残差，TuRBO自动调参 | 80km/h零撞门、安全可证、性能追平最优RL策略 | 面向穿越机赛道场景，需预先给定门型中心线 | 无人机竞速、极限飞行安全约束控制 |

---

## 🗺 Path Planning

- **[UAVs Meet LLMs: Overviews and Perspectives Toward Agentic Low-Altitude Mobility](https://arxiv.org/abs/2501.02341)** `2025` `Survey` `LLM` `foundation model` `aerial agent` `multimodal` `agentic navigation` `knowledge reasoning`
  *Yonglin Tian, Fei Li, Yiduo Li, Tengchao Zhang, Qiyao Zhang, Xuan Fu, Jun Huang, Xingyuan Dai, Yutong Wang, Chunwei Tian, Bai Li, Yisheng Li, Levente Kovacs, Fei-Yue Wang, arXiv preprint (CASIA).*
  > 中文：综述LLM与无人机低空智驾融合，提出感知-记忆-推理-工具调用的Agent路线图。
  > 📜 DOI: `10.48550/arXiv.2501.02341` · 💻 Code: https://github.com/Hub-Tian/UAVs_Meet_LLMs · 📊 Data: N/A

- **[See, Point, Fly: A Learning-Free VLM Framework for Universal Unmanned Aerial Navigation (SPF)](https://arxiv.org/abs/2509.22653)** `2025` `Method` `VLM` `vision-language navigation` `training-free` `2D grounding` `3D waypoint` `closed-loop` `zero-shot`
  *Chih-Yao Hu, Yang-Sen Lin, Yuna Lee, Chih-Hai Su, Jie-Ying Lee, Shu-Ruei Tsai, Chin-Yang Lin, Kuan-Wen Chen, Tsung-Wei Ke, Yu-Lun Liu, arXiv preprint (NYCU/NTU).*
  > 中文：免训练VLM把模糊指令分解为图像上的2D航点，转3D位移闭环飞控，DRL基准SOTA提升63%。
  > 📜 DOI: `10.48550/arXiv.2509.22653` · 💻 Code: N/A · 📊 Data: N/A

- **[Dynamic Scene Path Planning of UAVs Based on Deep Reinforcement Learning](https://www.mdpi.com/2504-446X/8/2/60/pdf)** `2024` `Method` `DRL`
  *Tang, Liang & Li, Drones.*
  > 中文：改进D3QN带优先级经验回放，动态场景跑赢A*/RRT/DQN。
  > 📜 DOI: `10.3390/drones8020060` · 💻 Code: N/A · 📊 Data: N/A

- **[Globally Guided Deep V-Network Motion Planning for Fixed-Wing UAVs](https://pdfs.semanticscholar.org/303b/f1aad17aaddaa17ff7c3595a1dfb89569281.pdf)** `2024` `Method` `Fixed-Wing`
  *Du, You & Zhao, Sensors.*
  > 中文：固定翼分层规划，全局引导+局部RL躲动态障碍。
  > 📜 DOI: `10.3390/s24072130` · 💻 Code: N/A · 📊 Data: N/A

- **[UAV Multi-Dynamic Target Interception: A Hybrid Intelligent Method Using Deep Reinforcement Learning and Fuzzy Logic](https://www.mdpi.com/2504-446X/8/6/226)** `2024` `Method` `SAC` `fuzzy logic` `hybrid` `multi-target` `dynamic environment` `interception` `model-free`
  *Bingze Xia, Iraj Mantegh, Wenfang Xie, Drones (MDPI), 8(6):226.*
  > 中文：将SAC与模糊推理融合，注入专家经验加速学习，实现多动态目标实时拦截规划。
  > 📜 DOI: `10.3390/drones8060226` · 💻 Code: N/A · 📊 Data: N/A

- **[Reducing Oscillations for Obstacle Avoidance in a Dense Environment Using Deep Reinforcement Learning and Time-Derivative of an Artificial Potential Field](https://www.mdpi.com/2504-446X/8/3/85)** `2024` `Method` `APF` `DRL` `hybrid` `hierarchical` `oscillation reduction` `quadrotor` `dense obstacle`
  *Zhilong Xi, Haoran Han, Jian Cheng, Maolong Lv, Drones (MDPI), 8(3):85.*
  > 中文：APF输出伪目标喂给下层DRL控制器，引入斥力时间导数抑制密集障碍避障振荡。
  > 📜 DOI: `10.3390/drones8030085` · 💻 Code: N/A · 📊 Data: N/A

- **[Quad-Rotor UAV Path Planning Based on the Target Bias Extension and Dynamic Step Size RRT* Algorithm (TD-RRT*)](https://www.mdpi.com/2032-6653/15/1/29)** `2024` `Method` `RRT*` `target bias` `dynamic step size` `B-spline` `3D planning` `quadrotor` `sampling-based`
  *Haitao Gao, Xiaozhu Hou, Jiangpeng Xu, Banggui Guan, World Electric Vehicle Journal (MDPI), 15(1):29.*
  > 中文：目标偏置采样+动态步长改进RRT*，配合三次B样条平滑，3D四旋翼规划更快更短。
  > 📜 DOI: `10.3390/wevj15010029` · 💻 Code: N/A · 📊 Data: N/A

- **[DWA-3D: A Reactive Planner for Robust and Efficient Autonomous UAV Navigation in Confined Environments](https://arxiv.org/abs/2409.05421)** `2024` `System` `DWA` `RRT*` `reactive planning` `LiDAR` `OctoMap` `online navigation` `cluttered environment` `ROS`
  *Jorge Bes, Juan Dendarieta, Luis Riazuelo, Luis Montano, Robotics and Autonomous Systems (Elsevier), vol.195, 2026 (arXiv:2409.05421).*
  > 中文：RRT*全局+3D动态窗口反应式局部规划，无先验图在线建图，真实实验约40ms/步。
  > 📜 DOI: `10.1016/j.robot.2025.105196` · 💻 Code: N/A · 📊 Data: N/A

- **[Path Planning for Fixed-Wing UAVs: An Integrated Approach with Theta* and Clothoids](https://www.mdpi.com/2504-446X/8/2/62)** `2024` `Method` `fixed-wing` `Theta*` `clothoid` `Euler spiral` `curvature constraint` `smooth path` `vision cone`
  *Salvatore R. Bassolillo, Gennaro Raspaolo, Luciano Blasi, Egidio Damato, Immacolata Notaro, Drones (MDPI), 8(2):62.*
  > 中文：Theta*节点间用回旋曲线连接，绑定曲率约束，自适应探索距离+视觉锥降低计算量。
  > 📜 DOI: `10.3390/drones8020062` · 💻 Code: N/A · 📊 Data: N/A

- **[Safe Low-Altitude Navigation in Steep Terrain with Fixed-Wing Aerial Vehicles](https://arxiv.org/abs/2401.04831)** `2024` `Method` `fixed-wing` `steep terrain` `inevitable collision state` `sampling-based` `Dubins Airplane` `circular periodic path` `flight test` `alpine`
  *Jaeyoung Lim, Florian Achermann, Rik Girod, Nicholas R. J. Lawrance, Roland Siegwart, IEEE Robotics and Automation Letters (RA-L), arXiv:2401.04831.*
  > 中文：用周期圆路径分类不可避撞状态，Dubins Airplane空间采样规划，阿尔卑斯地形实飞验证。
  > 📜 DOI: `10.48550/arXiv.2401.04831` · 💻 Code: https://github.com/ethz-asl/terrain-navigation · 📊 Data: N/A

- **[Integrated the Artificial Potential Field with the Leader-Follower Approach for UAV Cooperative Obstacle Avoidance](https://www.mdpi.com/2227-7390/12/7/954)** `2024` `Method` `APF` `leader-follower` `formation` `local minimum` `rotational force` `Lyapunov` `cooperative`
  *Yingxue Zhang, Jinbao Chen, Meng Chen, Chuanzhi Chen, Zeyu Zhang, Xiaokang Deng, Mathematics (MDPI), 12(7):954.*
  > 中文：图论拓扑+Leader-Follower替代APF引力场，加旋转力跳出局部极小，Lyapunov证稳。
  > 📜 DOI: `10.3390/math12070954` · 💻 Code: N/A · 📊 Data: N/A

- **[Time-Optimal Gate-Traversing Planner for Autonomous Drone Racing (TOGT)](https://arxiv.org/abs/2309.06837)** `2024` `Method` `time-optimal` `drone racing` `gate constraint` `numerical optimization` `single-rotor thrust limit` `aggressive flight` `ICRA 2024 Best Paper UAV`
  *Chao Qin, Maxime S. J. Michet, Jingxiang Chen, Hugh H.-T. Liu, IEEE ICRA 2024 (Best Paper Award on UAVs).*
  > 中文：显式建模门框位形与单旋翼推力极限，秒级求解穿过数十门的时间最优轨迹。
  > 📜 DOI: `10.1109/ICRA57147.2024.10610148` · 💻 Code: https://github.com/FSC-Lab/TOGT-Planner · 📊 Data: N/A

- **[Online Trajectory Replanning for Avoiding Moving Obstacles Using Fusion Prediction and Gradient-Based Optimization](https://www.mdpi.com/2076-3417/14/18/8339)** `2024` `Method` `online replanning` `fixed-wing` `moving obstacle` `fusion prediction` `gradient-based optimization` `smoothness` `kinodynamic feasibility`
  *Qianyi Fu, Wenjie Zhao, Shiyu Fang, Yiwen Zhu, Jun Li, Qili Chen, Applied Sciences (MDPI), 14(18):8339.*
  > 中文：物理+模式预测融合估计动态障碍，梯度优化离散航点实现固定翼在线重规划。
  > 📜 DOI: `10.3390/app14188339` · 💻 Code: N/A · 📊 Data: N/A

- **[Three-Dimensional Path Planning Based on Environment Exploration TD3 (EE-TD3)](https://www.mdpi.com/2073-8994/15/7/1371/pdf)** `2023` `Method` `DRL`
  *Zhang et al., Symmetry.*
  > 中文：TD3加对称3D环境探索编码，加速动态3D收敛。
  > 📜 DOI: `10.3390/sym15071371` · 💻 Code: N/A · 📊 Data: N/A

- **[Autonomous Drone Racing: A Survey](https://arxiv.org/abs/2301.01755)** `2023` `Survey` `drone racing` `trajectory optimization` `aggressive flight` `planning` `learning-based` `model-based`
  *Drew Hanover, Antonio Loquercio, Leonard Bauersfeld, Angel Romero, Robert Penicka, Yunlong Song, Giovanni Cioffi, Elia Kaufmann, Davide Scaramuzza, arXiv preprint (TRO survey).*
  > 中文：系统综述自主无人机竞速的规划/控制方法，覆盖基于模型与学习两类路线，速度超80kph。
  > 📜 DOI: `10.48550/arXiv.2301.01755` · 💻 Code: N/A · 📊 Data: N/A

- **[Deep Reinforcement Learning for Vision-Based Navigation of UAVs in Avoiding Stationary and Mobile Obstacles](https://www.mdpi.com/2504-446X/7/4/245)** `2023` `Method` `DRL` `DQN` `PPO` `SAC` `vision-based` `AirSim` `dynamic obstacle avoidance` `image input`
  *Amudhini P. Kalidas, Christy Jackson Joshua, Abdul Quadir Md, Shakila Basheer, Senthilkumar Mohan, Sapiah Sakri, Drones (MDPI), 7(4):245.*
  > 中文：在AirSim上对比DQN/PPO/SAC仅靠图像避障，发现离策略SAC在3D动态场景最优。
  > 📜 DOI: `10.3390/drones7040245` · 💻 Code: N/A · 📊 Data: N/A

- **[Multiple UAVs Path Planning Based on Deep Reinforcement Learning in Communication Denial Environment](https://www.mdpi.com/2227-7390/11/2/405)** `2023` `Method` `multi-UAV` `C51 Dueling DQN` `independent policy` `communication denial` `collision avoidance` `N-step TD` `HITL`
  *Yahao Xu, Yiran Wei, Keyang Jiang, Di Wang, Hongbin Deng, Mathematics (MDPI), 11(2):405.*
  > 中文：C51-Dueling-DQN独立策略，在无通信条件下实现多无人机协同避障与动态目标规划。
  > 📜 DOI: `10.3390/math11020405` · 💻 Code: N/A · 📊 Data: N/A

- **[Spectrum Surveying: Active Radio Map Estimation with Autonomous UAVs](https://arxiv.org/pdf/2201.04125)** `2022` `Method` `Active-Perception`
  *Shrestha, Romero & Chepuri, arXiv.*
  > 中文：无人机主动选点采集无线电，贝叶斯+DL建电磁地图。
  > 📜 DOI: `10.1109/TSP.2022.3163067` · 💻 Code: N/A · 📊 Data: N/A

- **[Fixed-Wing UAV Energy Efficient 3D Path Planning in Cluttered Environments (EEA*)](https://link.springer.com/article/10.1007/s10846-022-01608-1)** `2022` `Method` `fixed-wing` `A*` `energy efficiency` `3D mountainous` `local planner` `dynamic threat` `multi-UAV`
  *Giuseppe Aiello, Kimon P. Valavanis, Alessandro Rizzo, Journal of Intelligent & Robotic Systems (Springer), 105:54.*
  > 中文：节点式EEA*在3D山地兼顾能耗与几何约束，配套局部规划器应对未知动态威胁。
  > 📜 DOI: `10.1007/s10846-022-01608-1` · 💻 Code: N/A · 📊 Data: N/A
| 方法/代表论文 | 年份 | 核心思路 | 优点 | 局限 | 适用场景 |
|---|---|---|---|---|---|
| EEA* (Energy-Efficient A*) | 2022 | 在A*节点代价中融合能耗与威胁项，3D栅格搜索+局部规划器兜底 | 最优性可证、计算可控、能耗显式建模、对山地静态障碍可靠 | 维数灾难、对动态障碍反应慢、需先验3D地图、非连续曲率不可直飞 | 固定翼长航时巡航、山地巡检全局路径 |
| TD-RRT* | 2024 | 目标偏置采样+随障碍距离自适应步长，B样条后处理平滑 | 概率完备+渐近最优、3D高维可扩展、路径短且迭代少 | 重规划延迟仍较大、最优性保证依赖采样数、动态障碍需额外层 | 四旋翼3D结构化环境全局规划 |
| APF + Leader-Follower | 2024 | 用长机对僚机的引力替代目标引力场，加旋转力逃逸局部极小 | 反应快、计算轻、天然适合编队、Lyapunov稳定 | 仍易受窄通道/对称障碍困局影响、不保证全局最优、势场调参经验性强 | 多机编队实时避障、协同穿越 |
| SAC + Fuzzy (Xia 2024) | 2024 | SAC策略网络+模糊推理注入专家规则，加速多动态目标拦截学习 | 样本效率高、连续动作空间、无需精确动力学、模糊规则可解释 | 训练成本高、sim-to-real gap、模糊规则设计依赖经验、安全边界需外部兜底 | 不确定空域多目标拦截、动态规避 |
| C51-Duel-IP (Xu 2023) | 2023 | C51分布Q值+Dueling结构+独立策略，无通信下多机协同避障 | 通信拒止下可用、分布Q提升拟合、N-step TD加速收敛 | 离散动作空间、扩展性受独立策略一致性约束、城市HITL外泛化未验证 | GPS/通信拒止环境的多UAV协同导航 |
| DWA-3D + RRT* (Bes 2024) | 2024 | RRT*全局规划+扩展到3D的动态窗口法局部反应，OctoMap在线更新 | 无先验图即可飞行、~40ms实时、真实世界鲁棒、垂直/横向权重可调 | 两层耦合调参复杂、全局规划器不感知无人机尺寸时仍有失败、LiDAR依赖 | 室内/城市狭窄空间自主导航 |
| TOGT (Qin 2024) | 2024 | 数值优化同时求解时间分配与轨迹，显式建模门框位形与单旋翼推力极限 | 逼近真时间最优、秒级求解、实飞击败人类冠军、ICRA最佳UAV论文 | 需精确模型与门位地图、对感知误差敏感、不直接处理未知动态障碍 | 无人机竞速、极致穿越检查 |

---

## 🐝 Swarm & Multi-UAV Coordination

- **[Learned Controllers for Agile Quadrotors in Pursuit-Evasion Games (AMSPBH / PSRO)](https://arxiv.org/abs/2506.02849)** `2025` `Method` `MADRL` `pursuit-evasion` `population-based-training` `sim2real` `Crazyflie`
  *Alejandro Sánchez Roncero, Yixi Cai, Olov Andersson, Petter Ögren, IEEE Robotics and Automation Letters (RA-L).*
  > 中文：基于PSRO与Hedge采样的种群式对抗训练,解决非平稳与策略循环,Crazyflie零样本迁移。
  > 📜 DOI: N/A · 💻 Code: N/A · 📊 Data: N/A

- **[Is Intermediate Fusion All You Need for UAV-based Collaborative Perception? (LIF)](https://arxiv.org/abs/2504.21774)** `2025` `Method` `cooperative-perception` `communication-efficient` `BEV` `uncertainty` `3D-detection`
  *Jiuwu Hao, Liguo Sun, Yuting Wan, Yueyang Wu, Ti Xiang, Haolin Song, Pin Lv, arXiv preprint (IEEE/ACM submission).*
  > 中文：晚期-中间层融合LIF,仅交换紧凑检测结果并经VPE+BoBEV融合,不确定性驱动通信,极低带宽。
  > 📜 DOI: N/A · 💻 Code: https://github.com/weslchw/LiF · 📊 Data: N/A

- **[Decentralized Multi-UAV Trajectory Task Allocation in Search and Rescue Applications (CBBA extension)](https://findresearcher.sdu.dk/ws/files/268650626/Decentralized_Multi_Robot_Trajectory_Task_Allocation_in_Search_and_Rescue_Applications_11_.pdf)** `2024` `Method` `task-allocation` `CBBA` `auction` `search-and-rescue` `coverage`
  *Kasper A. R. Grøntved, Ulrik P. S. Lundquist, Anders Lyhne Christensen, ICUAS / SDU working paper.*
  > 中文：扩展CBBA把任务建模为有向轨迹,SAR覆盖路径规划去中心化,仅比集中式多1.9%开销。
  > 📜 DOI: N/A · 💻 Code: N/A · 📊 Data: N/A

- **[Advancement Challenges in UAV Swarm Formation Control: A Comprehensive Review](https://www.mdpi.com/2504-446X/8/7/320)** `2024` `Survey` `formation-control` `survey` `consensus` `potential-field` `DRL`
  *Yajun Bu, Ye Yan, Yueneng Yang, Drones, 8(7):320.*
  > 中文：系统综述编队控制:leader-follower/共识/势函数与DRL/ANN对比,指出融合趋势。
  > 📜 DOI: `10.3390/drones8070320` · 💻 Code: N/A · 📊 Data: N/A

- **[Fast Swarming of UAVs in GNSS-denied Feature-poor Environments without Explicit Communication](https://arxiv.org/abs/2404.18729)** `2024` `Method` `bionic` `flocking` `collision-avoidance` `GNSS-denied` `communication-free`
  *Jiri Horyna, Vit Kratky, Vaclav Pritzl, Tomas Baca, Eliseo Ferrante, Martin Saska, IEEE Robotics and Automation Letters, 9(6):5284-5291.*
  > 中文：CVUT/Saska组提出无通信、无GNSS的快速集群邻域模型与MRSE状态估计,实物高速拦截验证。
  > 📜 DOI: `10.1109/LRA.2024.3393356` · 💻 Code: N/A · 📊 Data: N/A

- **[High-Speed Motion Planning for Aerial Swarms in Unknown and Cluttered Environments (HDSM)](https://arxiv.org/abs/2402.19033)** `2024` `Method` `collision-avoidance` `decentralized` `motion-planning` `cluttered` `real-hardware`
  *Charbel Toumieh, Dario Floreano, IEEE Transactions on Robotics, vol.40.*
  > 中文：EPFL首个高 decentralized 同步高速运动规划框架,显式处理未知环境,多机穿越杂乱场景。
  > 📜 DOI: `10.1109/TRO.2024.3429193` · 💻 Code: https://github.com/lis-epfl/multi_agent_mpc · 📊 Data: N/A

- **[U2UData: A Large-scale Cooperative Perception Dataset for Swarm UAVs Autonomous Flight](https://arxiv.org/abs/2408.00606)** `2024` `Method` `cooperative-perception` `dataset` `benchmark` `LiDAR` `3D-detection` `BEV`
  *Tongtong Feng, Xin Wang, Feilin Han, Leping Zhang, Wenwu Zhu, ACM MM 2024.*
  > 中文：首个大规模集群UAV协同感知数据集:3机315K LiDAR帧+2.41M 3D框,8种SOTA算法基准。
  > 📜 DOI: `10.1145/3664647.3681394` · 💻 Code: https://fengtt42.github.io/U2UData-2/ · 📊 Data: https://fengtt42.github.io/U2UData-2/

- **[A Study of Collaborative Trajectory Planning Based on Starling Swarm Bionic Algorithm](https://www.mdpi.com/2076-3417/13/11/6795/pdf)** `2023` `Method` `Bionic`
  *Chen et al., Applied Sciences.*
  > 中文：模仿欧椋鸟群飞行为的协同轨迹规划。
  > 📜 DOI: `10.3390/app13116795` · 💻 Code: N/A · 📊 Data: N/A

- **[Multi-Target Pursuit by a Decentralized Heterogeneous UAV Swarm using Deep Multi-Agent Reinforcement Learning](https://arxiv.org/abs/2303.01799)** `2023` `Method` `MADRL` `pursuit-evasion` `heterogeneous` `sim2real` `Crazyflie`
  *Maryam Kouzeghar, Youngbin Song, Malika Meghjani, Roland Bouffanais, IEEE ICRA 2023.*
  > 中文：基于角色化MADDPG与Voronoi奖励的去中心化多目标围捕,真实Crazyflie集群验证。
  > 📜 DOI: `10.1109/ICRA48891.2023.10160919` · 💻 Code: N/A · 📊 Data: N/A

- **[Task Assignment of UAV Swarms Based on Deep Reinforcement Learning (Ex-MADDPG)](https://www.mdpi.com/2504-446X/7/5/297)** `2023` `Method` `MADRL` `task-allocation` `scalability` `MADDPG`
  *Bo Liu, Shulei Wang, Qinghua Li, Xinyang Zhao, Yunqing Pan, Changhong Wang, Drones, 7(5):297.*
  > 中文：Ex-MADDPG引入局部通信、均值观测与同步参数训练,任务分配可随集群规模扩展。
  > 📜 DOI: `10.3390/drones7050297` · 💻 Code: N/A · 📊 Data: N/A

- **[A Distributed Collaborative Allocation Method of Reconnaissance and Strike Tasks for Heterogeneous UAVs](https://www.mdpi.com/2504-446X/7/2/138)** `2023` `Method` `task-allocation` `distributed` `heterogeneous` `auction` `combat`
  *Hanqiang Deng, Jian Huang, Quan Liu, Tuo Zhao, Cong Zhou, Jialong Gao, Drones, 7(2):138.*
  > 中文：分布式协商+时间协同与威慑机动,降低侦察-打击任务在未知目标下的风险,可扩展大规模。
  > 📜 DOI: `10.3390/drones7020138` · 💻 Code: N/A · 📊 Data: N/A

- **[Starling-Behavior-Inspired Flocking Control of Fixed-Wing UAV Swarm in Complex Environments with Dynamic Obstacles](https://www.mdpi.com/2308-0851/8/4/28)** `2023` `Method` `bionic` `flocking` `starling` `fixed-wing` `collision-avoidance`
  *Weihuan Wu, Xiangyin Zhang, Yang Miao, Biomimetics, 8(4):328.*
  > 中文：模仿椋鸟集体/规避/局部跟随三模式,提升固定翼集群在动态障碍下的避障速度与安全性。
  > 📜 DOI: `10.3390/biomimetics8040328` · 💻 Code: N/A · 📊 Data: N/A

- **[Unmanned Aerial Vehicle Swarm Cooperative Decision-Making for SEAD Mission: A Hierarchical Multiagent Reinforcement Learning Approach](https://ieeexplore.ieee.org/document/9869884)** `2022` `Method` `MADRL` `task-allocation` `hierarchical` `SEAD` `defense`
  *Longfei Yue, Rennong Yang, Jialiang Zuo, Ying Zhang, Qiuni Li, Yijie Zhang, IEEE Access, vol.10.*
  > 中文：分层MARL:高层MADQN分配目标,低层IAPPO协同攻击,解决异构集群SEAD决策。
  > 📜 DOI: `10.1109/ACCESS.2022.3202938` · 💻 Code: N/A · 📊 Data: N/A

- **[Bearing-Based Distributed Formation Control of UAV Swarm by Quaternion-Based Attitude Synchronization in 3D](https://www.mdpi.com/2504-446X/6/9/227)** `2022` `Method` `formation-control` `distributed` `bearing` `quaternion` `3D`
  *Muhammad Baber Sial, Yuwei Zhang, Shaoping Wang, Sara Ali, Xinjiang Wang, Xinyu Yang, Zirui Liao, Zunheng Yang, Drones, 6(9):227.*
  > 中文：仅依靠方位(bearing)与四元数姿态同步实现3D编队,无需全局位置与定向知识。
  > 📜 DOI: `10.3390/drones6090227` · 💻 Code: N/A · 📊 Data: N/A

- **[Enhanced Decentralized Autonomous Aerial Robot Teams with Group Planning](https://arxiv.org/abs/2203.01069)** `2022` `Method` `large-scale` `decentralized` `MAPF` `group-planning` `real-hardware`
  *Jialiang Hou, Xin Zhou, Zhongxue Gan, Fei Gao, Science China Information Sciences.*
  > 中文：浙大高飞组:按空间动态分组,组内MAPF+轨迹联合优化,兼顾大规模可扩展性与规划质量。
  > 📜 DOI: `10.1007/s11432-022-3612-x` · 💻 Code: N/A · 📊 Data: N/A
| 方法/代表论文 | 年份 | 核心思路 | 优点 | 局限 | 适用场景 |
|---|---|---|---|---|---|
| CBBA (auction-based, Grøntved 2024) | 2024 | 市场拍卖+共识冲突消解,任务被建模为有向轨迹分配 | 收敛有保证、对通信拓扑鲁棒、无中心节点;仅比集中式多1.9%开销 | 依赖预定义任务集,动态环境需重协商;处理连续运动耦合能力有限 | 搜索救援覆盖、侦察-打击分布式分配 |
| Ex-MADDPG (Liu 2023) | 2023 | CTDE MADDPG+局部通信+均值观测+可扩展多决策机制 | 可随集群规模扩展,适应动态任务;仿真+实物验证 | 训练样本大、奖励工程依赖;泛化到新任务分布仍需微调 | 动态不确定环境下的UAV任务分配 |
| HMARL / MADQN+IAPPO (Yue 2022) | 2022 | 分层:上层MADQN做目标分配,下层独立异步PPO做协同攻击 | 解耦决策复杂度,下层独立学习易扩展,适合大规模异构 | 分层接口需手工设计;异质角色间信用分配仍不清晰 | SEAD压制防空、异构集群对空作战 |
| PSRO/AMSPBH population-based RL (Sánchez Roncero 2025) | 2025 | 种群化策略响应Oracle+Hedge采样,缓解自博弈非平稳与策略循环 | 学到多样化鲁棒策略,真实Crazyflie零样本迁移达4.87 m/s | 训练成本高(多代种群);仅验证1v1对抗,多智能体协作未覆盖 | 敏捷追逃、对抗式攻防控制器 |
| Bearing/Quaternion formation (Sial 2022) | 2022 | 仅依赖方位测量与无向图,四元数姿态同步避免奇异 | 无需全局定位,通信需求低,理论稳定性清晰 | 需已知方位-运动学映射;动态避障需额外模块 | GPS受限/弱通信下的3D几何编队保持 |
| Starling-inspired flocking (Wu 2023 / Horyna 2024) | 2023 | 模仿椋鸟群体/规避/局部跟随三模式或最小信息邻域模型 | 通信与传感需求极低,天然去中心化,可在GNSS拒止环境运行 | 队形柔性、无显式任务目标;参数多依赖经验/进化优化 | 大规模快速穿越、特征贫乏地区集群飞行 |
| HDSM decentralized MPC (Toumieh 2024) | 2024 | 去中心化同步运动规划,显式建模未知/未探索环境与机间碰撞 | 高速、杂乱环境下实物验证,规划质量接近集中式,代码开源 | 依赖机载感知与同步时钟;重计算,对单机算力要求高 | 未知杂乱环境中的高速集群穿越 |
| LIF / U2UData cooperative perception (Hao 2025; Feng 2024) | 2024 | 交换紧凑检测结果而非原始特征,BEV中间层融合,不确定性驱动通信 | 带宽极小、SOTA精度;提供大规模基准数据集与8种算法对照 | 目前主要仿真验证;3D检测对定位/标定误差敏感 | 低空经济、城市交通监控、协同3D检测/跟踪 |

---

## 👁 Visual Perception & Object Detection

- **[DCS-YOLOv8: Lightweight Context-Aware Network for Small Object Detection in UAV Imagery](https://mdpi-res.com/d_attachment/remotesensing/remotesensing-17-02989/article_deploy/remotesensing-17-02989.pdf)** `2025` `Method` `YOLO`
  *Zhao, Yang & Zhao, Remote Sensing.*
  > 中文：动态卷积注意力+P2检测头，VisDrone mAP提升，RK3588实测。
  > 📜 DOI: `10.3390/rs17082989` · 💻 Code: N/A · 📊 Data: https://github.com/VisDrone/VisDrone-Dataset

- **[HSF-DETR: Hyper Scale Fusion Detection Transformer for Multi-Perspective UAV Object Detection](https://www.mdpi.com/2072-4292/17/12/1997)** `2025` `Method` `DETR` `transformer` `small-object-detection` `VisDrone` `multi-scale`
  *Yi Mao, Haowei Zhang, Rui Li, Feng Zhu, Rui Sun, Pingping Ji, Remote Sensing (MDPI).*
  > 中文：混合渐进融合主干HPFNet+多尺度优化+位置感知对齐模块，VisDrone mAP50达42.8%，69FPS仅15M参数。
  > 📜 DOI: `10.3390/rs17121997` · 💻 Code: N/A · 📊 Data: https://github.com/VisDrone/VisDrone-Dataset

- **[AeroReformer: Aerial Referring Transformer for UAV-based Referring Image Segmentation](https://arxiv.org/abs/2502.16680)** `2025` `Method` `referring-segmentation` `vision-language` `UAV` `instance-segmentation`
  *Rui Li, et al., arXiv preprint.*
  > 中文：首个UAV指代表达图像分割框架，视觉-语言交叉注意力+旋转感知多尺度融合解码器，自动标注管线构建新基准。
  > 📜 DOI: N/A · 💻 Code: https://github.com/lironui/AeroReformer · 📊 Data: N/A

- **[Multi-Scale Attention and Boundary-Aware Network for Military Camouflaged Object Detection using Unmanned Aerial Vehicles](https://link.springer.com/article/10.1007/s11760-025-03602-3)** `2025` `Method` `camouflaged-object-detection` `military` `boundary-aware` `ViT`
  *Keshun Liu, Aihua Li, Sen Yang, Changlong Wang, Yuhua Zhang, Signal, Image and Video Processing (Springer).*
  > 中文：金字塔ViT主干+边界提取/引导/上下文融合三模块，新建MCOD-UAV数据集，伪装目标检测mAP达48.92%。
  > 📜 DOI: `10.1007/s11760-025-03602-3` · 💻 Code: N/A · 📊 Data: N/A

- **[IF-YOLO: UAV Object Detection via Information-Preserving Feature Aggregation](https://www.mdpi.com/2072-4292/16/14/2590/pdf)** `2024` `Method` `YOLO`
  *Zhang et al., Remote Sensing.*
  > 中文：解决小目标信息丢失与多层特征冲突，VisDrone mAP 47.3%。
  > 📜 DOI: `10.3390/rs16142590` · 💻 Code: N/A · 📊 Data: https://github.com/VisDrone/VisDrone-Dataset

- **[YOLOFIV: Around-the-Clock Aerial Detection via Infrared+Visible Fusion](https://ieeexplore.ieee.org/document/10643643)** `2024` `Method` `Multimodal`
  *Wang et al., IEEE J-STARS.*
  > 中文：红外+可见光双流融合，昼夜全天候航拍检测。
  > 📜 DOI: `10.1109/JSTARS.2024.3436620` · 💻 Code: N/A · 📊 Data: N/A

- **[Active Object Detection and Tracking Using Gimbal Mechanisms](https://www.mdpi.com/2504-446X/8/2/55/pdf)** `2024` `Method` `Tracking`
  *Hansen & Figueiredo, Drones.*
  > 中文：三轴云台主动追踪，6D位姿估计比被动相机更准。
  > 📜 DOI: `10.3390/drones8020055` · 💻 Code: N/A · 📊 Data: N/A

- **[SOD-YOLO: Small-Object-Detection Algorithm Based on Improved YOLOv8 for UAV Images](https://www.mdpi.com/2072-4292/16/12/2230)** `2024` `Method` `small-object-detection` `YOLO` `VisDrone` `aerial`
  *Yangang Li, Qi Li, Jie Pan, Ying Zhou, Hongliang Zhu, Hongwei Wei, Chong Liu, Remote Sensing (MDPI).*
  > 中文：在YOLOv8中引入RFCBAM注意力与BSSI-FPN多尺度融合金字塔，VisDrone2019上mAP50提升3%且参数量大降。
  > 📜 DOI: `10.3390/rs16122230` · 💻 Code: https://github.com/iamwangxiaobai/SOD-YOLO · 📊 Data: https://github.com/VisDrone/VisDrone-Dataset

- **[HSP-YOLOv8: UAV Aerial Photography Small Target Detection Algorithm](https://www.mdpi.com/2504-446X/8/4/144)** `2024` `Method` `small-object-detection` `YOLO` `VisDrone` `dense-occlusion`
  *Heng Zhang, Wei Sun, Changhao Sun, Ruofei He, Yumeng Zhang, Drones (MDPI).*
  > 中文：新增微小目标预测头与SPD-Conv空间转深度卷积，配合Soft-NMS缓解密集遮挡漏检，VisDrone mAP50提升11%。
  > 📜 DOI: `10.3390/drones8040144` · 💻 Code: N/A · 📊 Data: https://github.com/VisDrone/VisDrone-Dataset

- **[DCEF²-YOLO: Aerial Detection YOLO with Deformable Convolution-Efficient Feature Fusion for Small Target Detection](https://www.mdpi.com/2072-4292/16/6/1071)** `2024` `Method` `small-object-detection` `YOLO` `DOTA` `real-time`
  *Yeonha Shin, Heesub Shin, Jaewoo Ok, Minyoung Back, Jaehyuk Youn, Sungho Kim, Remote Sensing (MDPI).*
  > 中文：可变形卷积DFConv保留小目标信息，高效特征融合结构在DOTA上mAP提升6.1%，RTX3090达120FPS。
  > 📜 DOI: `10.3390/rs16061071` · 💻 Code: N/A · 📊 Data: https://captain-whu.github.io/DOTA/dataset.html

- **[DV-DETR: Improved UAV Aerial Small Target Detection Algorithm Based on RT-DETR](https://www.mdpi.com/1424-8220/24/23/7603)** `2024` `Method` `DETR` `RT-DETR` `small-object-detection` `VisDrone`
  *Xiaolong Wei, Ling Yin, Liangliang Zhang, Fei Wu, Sensors (MDPI).*
  > 中文：基于RT-DETR换ResNet18主干，引入重标定注意力与可变形注意力融合，Focaler-IoU损失，VisDrone mAP50达50.1%、90FPS。
  > 📜 DOI: `10.3390/s24237603` · 💻 Code: N/A · 📊 Data: https://github.com/VisDrone/VisDrone-Dataset

- **[TFITrack: Transformer Feature Integration Network for Object Tracking](https://link.springer.com/article/10.1007/s44196-024-00500-0)** `2024` `Method` `tracking` `transformer` `UAV123` `aerial`
  *Xiuhua Hu, Huan Liu, Shuang Li, Jing Zhao, Yan Hui, International Journal of Computational Intelligence Systems (Springer).*
  > 中文：Transformer编解码融合时空与全局上下文，相似度计算层+双注意力，UAV123等航拍基准上抗快速运动。
  > 📜 DOI: `10.1007/s44196-024-00500-0` · 💻 Code: N/A · 📊 Data: N/A

- **[MFMG-Net: Multispectral Feature Mutual Guidance Network for Visible-Infrared Object Detection](https://www.mdpi.com/2504-446X/8/3/112)** `2024` `Method` `multimodal` `infrared-visible` `fusion` `drone`
  *Fei Zhao, Wenzhong Lou, Hengzhen Feng, Nanxi Ding, Chenglong Li, Drones (MDPI).*
  > 中文：双主干间多光谱特征互引导模块，注意力双分支深度融合，VEDAI/M3FD/LLVIP上跨模态检测领先。
  > 📜 DOI: `10.3390/drones8030112` · 💻 Code: N/A · 📊 Data: https://sites.google.com/view/vedai

- **[Drone-Based Visible-Thermal Object Detection with Transformers and Prompt Tuning (VIP-Det)](https://www.mdpi.com/2504-446X/8/5/194)** `2024` `Method` `multimodal` `infrared-visible` `transformer` `DroneVehicle` `prompt-tuning`
  *Rui Chen, Dongdong Li, Zhinan Gao, Yangliu Kuai, Chengyuan Wang, Drones (MDPI).*
  > 中文：以Transformer为主干做全局长程建模，视觉提示融合双模态特征，DroneVehicle上超越同类Transformer方法。
  > 📜 DOI: `10.3390/drones8050194` · 💻 Code: N/A · 📊 Data: https://github.com/VisDrone/DroneVehicle

- **[IV-YOLO: A Lightweight Dual-Branch Object Detection Network for Infrared-Visible Fusion](https://www.mdpi.com/1424-8220/24/19/6181)** `2024` `Method` `multimodal` `infrared-visible` `lightweight` `YOLO`
  *Dan Tian, Xin Yan, Dong Zhou, Chen Wang, Wenshuai Zhang, Sensors (MDPI).*
  > 中文：YOLOv8双分支融合Bi-Fusion金字塔与Shuffle-SPP，仅4.31M参数达203FPS，DroneVehicle/FLIR/KAIST全面提升。
  > 📜 DOI: `10.3390/s24196181` · 💻 Code: N/A · 📊 Data: https://github.com/VisDrone/DroneVehicle

- **[AerialFormer: Multi-Resolution Transformer for Aerial Image Segmentation](https://www.mdpi.com/2072-4292/16/16/2930)** `2024` `Method` `semantic-segmentation` `transformer` `aerial` `iSAID` `LoveDA`
  *Taisei Hanyu, Kashu Yamazaki, Minh Tran, Roy A. McCann, Haitao Liao, Chase Rainwater, Meredith Adkins, Jackson Cothren, Ngan Le, Remote Sensing (MDPI).*
  > 中文：CNN Stem保高分辨率细节，Transformer编码多尺度特征，多膨胀CNN解码器聚合，iSAID/LoveDA/Potsdam SOTA。
  > 📜 DOI: `10.3390/rs16162930` · 💻 Code: https://github.com/UARK-AICV/AerialFormer · 📊 Data: https://github.com/CAPTAIN-WHU/iSAID_Devkit

- **[AERO: Onboard Edge AI for UAV Remote Sensing](https://pdfs.semanticscholar.org/2925/f4caa6c7ff37b0b9bfe76266f205497361dc.pdf)** `2023` `System` `Edge-AI`
  *Koubaa et al., Remote Sensing.*
  > 中文：YOLOv4/v7+DeepSORT+TensorRT在Jetson Xavier跑15.5FPS。
  > 📜 DOI: `10.3390/rs15051297` · 💻 Code: N/A · 📊 Data: N/A

- **[Efficient YOLOv7-Drone: An Enhanced Object Detection Approach for Drone Aerial Imagery](https://www.mdpi.com/2504-446X/7/10/616)** `2023` `Method` `YOLO` `VisDrone` `UAVDT` `lightweight`
  *Xiaofeng Fu, Guoting Wei, Xia Yuan, Yongshun Liang, Yuming Bo, Drones (MDPI).*
  > 中文：去掉P5检测头加入P2微小目标头，TGM-CESC稀疏卷积掩码聚焦前景，VisDrone/UAVDT上实时SOTA。
  > 📜 DOI: `10.3390/drones7100616` · 💻 Code: N/A · 📊 Data: https://github.com/VisDrone/VisDrone-Dataset

- **[Slight Aware Enhancement Transformer and Multiple Matching Network for Real-Time UAV Tracking](https://www.mdpi.com/2072-4292/15/11/2857)** `2023` `Method` `tracking` `Siamese` `transformer` `edge-deployment` `Jetson`
  *Anping Deng, Guangliang Han, Dianbin Chen, Tianjiao Ma, Zhichao Liu, Remote Sensing (MDPI).*
  > 中文：轻量Transformer编码目标外观，多重匹配网络感知响应图，Jetson AGX Xavier上实时35FPS。
  > 📜 DOI: `10.3390/rs15112857` · 💻 Code: N/A · 📊 Data: N/A

- **[Enhancing UAV Visual Landing Recognition with YOLO's Object Detection by Onboard Edge Computing](https://www.mdpi.com/1424-8220/23/20/8999)** `2023` `Method` `edge-deployment` `Jetson` `TensorRT` `real-time` `landing`
  *Mingyou Ma, Shangen Shen, Yicheng Huang, Sensors (MDPI).*
  > 中文：Jetson Xavier NX部署YOLOv4-tiny+TensorRT加速，自动云台跟踪，35FPS以上实时识别应急降落点。
  > 📜 DOI: `10.3390/s23208999` · 💻 Code: N/A · 📊 Data: N/A
| 方法/代表论文 | 年份 | 核心思路 | 优点 | 局限 | 适用场景 |
|---|---|---|---|---|---|
| SOD-YOLO | 2024 | YOLOv8+RFCBAM注意力+BSSI-FPN平衡空间与语义融合 | 参数量降84%仍mAP50提升3%，工程易复现 | 仍是CNN架构，全局建模能力有限 | 无人机城市交通监控小目标检测 |
| HSF-DETR | 2025 | RT-DETR改进，HPFNet混合渐进融合+位置感知对齐 | 纯Transformer端到端无NMS后处理，15M参数69FPS | 训练收敛慢于YOLO，工程门槛较高 | 多视角无人机实时目标检测 |
| DV-DETR | 2024 | RT-DETR+ResNet18主干+重标定注意力+Focaler-IoU | VisDrone mAP50达50.1%，90FPS实时 | 依赖RT-DETR生态，垂直领域泛化未验证 | 高密度城市场景无人机监控 |
| SiamSTM | 2023 | Siamese+轻量Transformer外观编码+多重匹配响应 | Jetson AGX Xavier 35FPS真正机载实时 | 长时遮挡漂移仍需模板更新策略 | 无人机自主导航目标跟踪 |
| MFMG-Net | 2024 | 双主干间多光谱特征互引导+注意力深度融合 | 昼夜全天候，跨模态互补信息利用充分 | 双主干计算量大于单模态 | 无人机城市道路巡检可见光+红外融合 |
| IV-YOLO | 2024 | YOLOv8双分支Bi-Fusion轻量融合，4.31M参数 | 203FPS超高速，参数仅4.31M适合机载 | 模态融合较浅，极端工况鲁棒性待验证 | 无人机昼夜全天候安防 surveillance |
| Ma 2023 (Jetson Edge) | 2023 | YOLOv4-tiny+TensorRT+自动云台多线程 | 完整机载闭环系统，跨100km迁移验证 | 模型较老，精度低于新YOLOv8 | 无人机应急降落点识别与侦察 |
| AerialFormer | 2024 | Transformer编码器+多膨胀CNN解码器混合架构 | iSAID/LoveDA/Potsdam三基准SOTA，开源代码 | 语义分割非实时，适合离线后处理 | 无人机航拍地物分类与地图更新 |

---

## 📡 Wireless Communications & Networking

- **[Deep Reinforcement Learning-Based Energy-Efficient Resource Allocation and Scheduling in 6G-Enabled UAV-Assisted IoT Wireless Networks](https://swon.yu.ac.kr/pdf/2020/202608-sensors.pdf)** `2026` `Method` `DRL` `resource-allocation` `UAV-relay` `6G` `IoT`
  *Ali Nauman, Sung Won Kim, Sensors (MDPI).*
  > 中文：DQN联合调度IoT设备功率/带宽/UAV位置，奖励函数平衡能效/队列稳定/公平/电池寿命。
  > 📜 DOI: N/A · 💻 Code: N/A · 📊 Data: N/A

- **[Integrated Communication and Control for Energy-Efficient UAV Swarms: A Multi-Agent Reinforcement Learning Approach](https://arxiv.org/abs/2509.23905)** `2025` `Method` `multi-uav` `MARL` `communication-control-co-design` `energy-efficiency`
  *Tianjiao Sun, Ningyan Guo, Haozhe Gu, Yanyan Peng, Zhiyong Feng, arXiv preprint.*
  > 中文：提出MAHPPO-AM算法处理混合动作空间，UAV群通信与控制联合设计，节能25%、公平指数0.99。
  > 📜 DOI: N/A · 💻 Code: N/A · 📊 Data: N/A

- **[Joint Optimization of Trajectory, Offloading, Caching, and Migration for UAV-Assisted MEC](https://www.cs.newpaltz.edu/~lik/publications/Mingxiong-Zhao-IEEE-TMC-2025)** `2025` `Method` `MEC` `trajectory` `caching` `Lyapunov-optimization`
  *Mingxiong Zhao, Rongqian Zhang, Zhenli He, Keqin Li, IEEE Transactions on Mobile Computing.*
  > 中文：用Lyapunov将轨迹+卸载+缓存+迁移多目标问题分解，BCD求解，吞吐时延显著优于传统方法。
  > 📜 DOI: N/A · 💻 Code: N/A · 📊 Data: N/A

- **[HAPS-ISAC for 6G: Architecture, Design Trade-offs, and a Practical Roadmap](https://arxiv.org/abs/2510.23147)** `2025` `Method` `NTN` `HAPS` `ISAC` `6G` `multi-layer`
  *Parisa Kanani, Mohammad Javad Omidi, Mahmoud Modarres-Hashemi, Halim Yanikomeroglu, arXiv preprint.*
  > 中文：平流层HAPS与UAV群构成3D ISAC网络，仿真验证较纯UAV方案显著提升感知精度与用户公平。
  > 📜 DOI: N/A · 💻 Code: N/A · 📊 Data: N/A

- **[UAV-Mounted RIS-Aided Mobile Edge Computing System: A DDQN-Based Optimization Approach](https://www.mdpi.com/2504-446X/8/5/184)** `2024` `Method` `RIS` `MEC` `DDQN` `resource-allocation`
  *Min Wu, Shibing Zhu, Changqing Li, Jiao Zhu, Yudi Chen, Xiangyu Liu, Rui Liu, Drones (MDPI).*
  > 中文：UAV搭载RIS辅助车联网MEC，用DDQN联合控制UAV轨迹、RIS被动波束与卸载资源。
  > 📜 DOI: `10.3390/drones8050184` · 💻 Code: N/A · 📊 Data: N/A

- **[Cost-Efficient Task Offloading in Mobile Edge Computing With Layered Unmanned Aerial Vehicles](http://clouds.cis.unimelb.edu.au/papers/TaskOffloadMEC-UAV2024.pdf)** `2024` `Method` `MEC` `task-offloading` `layered-UAV` `metaheuristic`
  *Haitao Yuan, Meijia Wang, Jing Bi, Shuyuan Shi, Jinhong Yang, Jia Zhang, Mengchu Zhou, Rajkumar Buyya, IEEE Internet of Things Journal.*
  > 中文：分层UAV云边协同MEC，提出AGSP混合元启发式算法，时延能耗较SOTA降7-8%。
  > 📜 DOI: `10.1109/JIOT.2024.3363968` · 💻 Code: N/A · 📊 Data: N/A

- **[UAV Assisted Integrated Sensing and Communications for Internet of Things: 3D Trajectory Optimization And Resource Allocation](https://strathprints.strath.ac.uk/89226/1/Liu-etal-IEEE-TWC-2024-UAV-assisted-integrated-sensing-and-communications-for-internet.pdf)** `2024` `Method` `ISAC` `3D-trajectory` `radar-estimation-rate` `resource-allocation`
  *Zechen Liu, Xin Liu, Yuemin Liu, Victor C. M. Leung, Tariq S. Durrani, IEEE Transactions on Wireless Communications.*
  > 中文：UAV作为ISAC空中平台，以雷达估计率为指标，三层迭代优化任务调度/功率/3D飞行参数。
  > 📜 DOI: `10.1109/TWC.2024.3367589` · 💻 Code: N/A · 📊 Data: N/A

- **[Enhancing User Localization with an Integrated Sensing and Communication (ISAC) System: An Experimental UAV Search-and-Rescue Use Case](https://www.mdpi.com/2072-4292/16/16/3031)** `2024` `Method` `ISAC` `experimental` `search-and-rescue` `localization`
  *Stefano Moro, Francesco Linsalata, Marco Manzoni, Maurizio Magarini, Stefano Tebaldini, Remote Sensing (MDPI).*
  > 中文：SDR载荷UAV实测ISAC搜救，融合SAR成像与上行三角定位，雪崩掩埋目标定位误差厘米至10米。
  > 📜 DOI: `10.3390/rs16163031` · 💻 Code: N/A · 📊 Data: N/A

- **[Miniature UAV-Aided Cooperative THz Networks with Reconfigurable Energy Harvesting Holographic Surfaces](https://arxiv.org/abs/2411.18791)** `2024` `Method` `terahertz` `holographic-surface` `wireless-power-transfer` `NOMA`
  *Yifei Song, Jalal Jalali, Yanyu Qin, Mostafa Darabi, Filip Lemic, Natasha Devroye, arXiv preprint.*
  > 中文：微型UAV搭载可重构全息表面(RHS)，THz频段同时信息+能量 harvesting，SCA优化轨迹与NOMA功率。
  > 📜 DOI: N/A · 💻 Code: N/A · 📊 Data: N/A

- **[Energy-Efficient Multi-UAVs Cooperative Trajectory Optimization for Communication Coverage: An MADRL Approach](https://www.mdpi.com/2072-4292/15/2/429)** `2023` `Method` `trajectory-optimization` `multi-uav` `MADRL` `coverage`
  *Tianyong Ao, Kaixin Zhang, Huaguang Shi, Zhanqi Jin, Yi Zhou, Fuqiang Liu, Remote Sensing (MDPI).*
  > 中文：提出DSAAC多智能体注意力Actor-Critic算法，协同优化多UAV应急覆盖轨迹，吞吐提升71%。
  > 📜 DOI: `10.3390/rs15020429` · 💻 Code: N/A · 📊 Data: N/A

- **[UAV-aided Aerial Reconfigurable Intelligent Surface Communications with Massive MIMO System](https://discovery.researcher.life/download/article/535748bc905f39f99b58691d8bb6ac8a/full-text)** `2023` `Method` `RIS` `massive-mimo` `aerial-RIS` `beamforming`
  *Minhhien T. Nguyen, Emiliano Garcia-Palacios, Tan Do-Duy, Octavia A. Dobre, Trung Q. Duong, IEEE Transactions on Cognitive Communications and Networking.*
  > 中文：多个搭载RIS面板的UAV辅助大规模MIMO，联合零陷预编码与相位优化最大化吞吐。
  > 📜 DOI: `10.1109/TCCN.2023.3263487` · 💻 Code: N/A · 📊 Data: N/A

- **[Energy Efficiency of Unmanned Aerial Vehicle with Reconfigurable Intelligent Surfaces: A Comparative Study](https://www.mdpi.com/2504-446X/7/2/98)** `2023` `Method` `RIS` `active-RIS` `hybrid-RIS` `energy-efficiency`
  *Chi Yen Goh, Chee Yen Leow, Rosdiadee Nordin, Drones (MDPI).*
  > 中文：首次对比被动/主动/混合RIS-UAV，混合方案较被动RIS能效提升14倍，主动达26倍。
  > 📜 DOI: `10.3390/drones7020098` · 💻 Code: N/A · 📊 Data: N/A

- **[UAV Trajectory and Beamforming Optimization for Integrated Periodic Sensing and Communication](https://wnt.sjtu.edu.cn/papers/ieee-wcl-uavsens.pdf)** `2023` `Method` `ISAC` `trajectory` `beamforming` `periodic-sensing`
  *Kaitao Meng, Qingqing Wu, Shaodan Ma, Wen Chen, Tony Q. S. Quek, IEEE Wireless Communications Letters.*
  > 中文：提出周期式ISAC机制，闭式最优预编码+UAV轨迹设计，揭示不同帧间解的结构对称性。
  > 📜 DOI: `10.1109/LWC.2023.3256167` · 💻 Code: N/A · 📊 Data: N/A

- **[UAV Trajectory Design and Power Optimization for Terahertz Band-Integrated Sensing and Communications](https://www.mdpi.com/1424-8220/23/6/3005)** `2023` `Method` `terahertz` `ISAC` `PPO` `trajectory`
  *Ying Gao, Hongmei Xue, Long Zhang, Enchang Sun, Sensors (MDPI).*
  > 中文：THz-UAV空中基站做ISAC，Lagrange+PPO交替优化轨迹/频段关联/收发功率，最小化端到端时延。
  > 📜 DOI: `10.3390/s23063005` · 💻 Code: N/A · 📊 Data: N/A

- **[An Energy-Efficient UAV Deployment Scheme for Emergency Communications in Air-Ground Networks with Joint Trajectory and Power Optimization](https://ieeexplore.ieee.org/document/9837849)** `2022` `Method` `trajectory-optimization` `emergency-communication` `power-allocation` `energy-efficiency`
  *Shuo Zhang, Shuo Shi, Weizhi Wang, Zhenyu Xu, Xuemai Gu, China Communications (IEEE).*
  > 中文：面向应急通信，联合UAV轨迹与功率分配，用TSP分组+Dinkelbach法最大化能效。
  > 📜 DOI: `10.23919/JCC.2022.07.007` · 💻 Code: N/A · 📊 Data: N/A
| 方法/代表论文 | 年份 | 核心思路 | 优点 | 局限 | 适用场景 |
|---|---|---|---|---|---|
| DSAAC MADRL multi-UAV coverage (Ao 2023) | 2023 | 双流注意力Actor-Critic，分层多头注意力Critic处理多UAV/多用户状态耦合 | 分布式训练，吞吐+71%，能耗-19.8%，可扩展到多UAV规模 | 需大量仿真训练，泛化到新场景需重训；未考虑非视距遮挡 | 应急通信、临时空中基站覆盖 |
| Hybrid/active RIS-UAV comparative (Goh 2023) | 2023 | 首次系统对比被动/主动/混合RIS-UAV能效，给出各方案适用功率预算 | 理论清晰，量化混合RIS较被动提升14倍，为硬件选型提供依据 | 仅静态部署分析，未联合UAV轨迹优化；主动RIS功耗高 | 城市盲区补盲、IoT中继 |
| Lyapunov joint trajectory/offload/cache/migration (Zhao 2025) | 2025 | 用Lyapunov将长期多目标队列问题转为逐时隙子问题，BCD联合求解 | 理论保证队列稳定，兼顾吞吐与时延，适合动态任务到达 | 算法复杂度较高；未考虑UAV间干扰 | 偏远地区MEC、智慧城市边缘服务 |
| 3D ISAC UAV radar estimation rate (Liu 2024) | 2024 | 以雷达估计率为ISAC性能指标，三层迭代优化任务调度/功率/3D飞行参数 | 首次用信息论度量感知性能，3D飞行参数优化显式提升感知率 | 假设理想信道；计算量大，三层迭代收敛慢 | 应急IoT感知+回传、基础设施less场景 |
| SCA+PPO THz-ISAC UAV (Gao 2023) | 2023 | Lagrange解功率子问题，PPO解UAV位置/频段关联，交替优化最小化时延 | THz特有的分子吸收/波束偏斜建模，PPO处理离散-连续混合变量 | PPO训练样本效率低；THz链路对遮挡敏感 | 6G近距超高速回传、应急高带宽感知 |
| DQN energy-efficient UAV-relay IoT (Nauman 2026) | 2026 | DQN基于队列/信道/位置/电池状态联合决策调度、功率、带宽、UAV移动 | 奖励函数显式平衡能效/公平/电池寿命，对比6种基线稳定胜出 | 单一UAV中继；DQN离散动作空间限制细粒度功率控制 | 6G低空IoT接入、偏远传感网络回传 |

---

## 🛡 Anti-UAV Detection

- **[The Sound of Surveillance: Enhancing Machine Learning-Driven Drone Detection with Advanced Acoustic Augmentation](https://www.mdpi.com/2504-446X/8/3/105)** `2025` `Method` `acoustic` `data-augmentation` `EU-classes`
  *Sebastian Kmmritz, Drones (MDPI), 8(3):105.*
  > 中文：系统研究音高偏移、时延、谐波失真、环境噪声等声学增强对C0-C3类无人机分类性能的影响。
  > 📜 DOI: `10.3390/drones8030105` · 💻 Code: N/A · 📊 Data: N/A

- **[Detecting infrared UAVs on edge devices through lightweight instance segmentation (YOLO11-AU-IR)](https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0330074)** `2025` `Method` `infrared` `instance-segmentation` `Jetson`
  *YuZhi Chen, HaoYue Sun, Liang Tian, Ye Yang, ShenYang Wang, TianYou Wang, PLOS ONE, 2025.*
  > 中文：轻量化实例分割框架YOLO11-AU-IR，AUVD-Seg300上mAP@0.5=97.7%，Jetson TX2可实时部署。
  > 📜 DOI: `10.1371/journal.pone.0330074` · 💻 Code: https://github.com/chen-yuzhi/YOLO11-AU-IR · 📊 Data: AUVD-Seg300

- **[A Comprehensive Survey of UAV Detection and Classification Using ML](https://www.mdpi.com/2072-4292/16/5/879/pdf)** `2024` `Survey` `Anti-UAV`
  *Rahman et al., Remote Sensing.*
  > 中文：按RF/视觉/声学/雷达四类梳理反无人机技术。
  > 📜 DOI: `10.3390/rs16050879` · 💻 Code: N/A · 📊 Data: N/A

- **[Drones Detection Using a Fusion of RF and Acoustic Features and Deep Neural Networks](https://www.mdpi.com/1424-8220/24/8/2427)** `2024` `Method` `RF` `acoustic` `sensor-fusion`
  *Alan Frid, Yehuda Benshimol, Erez Manor, Shlomo Greenberg, Sensors (MDPI), 24(8):2427.*
  > 中文：融合RF通信信号与旋翼声学特征，用LSTM在-10dB低信噪比下取得91%分类精度。
  > 📜 DOI: `10.3390/s24082427` · 💻 Code: N/A · 📊 Data: N/A

- **[Intelligent Identification and Classification of Small UAV Remote Control Signals Based on Improved Yolov5-7.0](https://ieeexplore.ieee.org/document/10471392)** `2024` `Method` `RF` `SDR` `YOLO`
  *Minjing Li, Donglai Hao, Jiaming Wang, Shuozhe Wang, Zijian Zhong, Zhiwen Zhao, IEEE Access, vol. 12.*
  > 中文：用SDR采集无人机遥控RF信号，STFT/小波时频图后送入改进YOLOv5-7.0，F1=0.93，mAP=0.967。
  > 📜 DOI: `10.1109/ACCESS.2024.3376235` · 💻 Code: N/A · 📊 Data: N/A

- **[AIMED-Net: An Enhancing Infrared Small Target Detection Net in UAVs with Multi-Layer Feature Enhancement for Edge Computing](https://www.mdpi.com/2072-4292/16/10/1776)** `2024` `Method` `infrared` `small-target` `edge-AI`
  *Lehao Pan, Tong Liu, Jianghua Cheng, Bang Cheng, Yahui Cai, Remote Sensing (MDPI), 16(10):1776.*
  > 中文：基于YOLOv7的多层特征增强红外小目标检测网，HIT-UAV数据集上mAP提升2.6%，边缘推理时间降15.2%。
  > 📜 DOI: `10.3390/rs16101776` · 💻 Code: N/A · 📊 Data: HIT-UAV

- **[The Drone-vs-Bird Detection Grand Challenge at ICASSP 2023: A Review of Methods and Results](https://ieeexplore.ieee.org/document/10475518)** `2024` `Dataset` `benchmark` `drone-vs-bird` `video`
  *Angelo Coluccia, Alessio Fascista, Lars Sommer, Arne Schumann, Anastasios Dimou, Dimitrios Zarpalas, IEEE Open Journal of Signal Processing, vol. 5.*
  > 中文：第6届Drone-vs-Bird视频检测挑战赛综述，公开视频数据集对比各团队深度学习方案优劣势。
  > 📜 DOI: `10.1109/OJSP.2024.3374761` · 💻 Code: N/A · 📊 Data: Drone-vs-Bird dataset

- **[Multi-Sensor Fusion for UAV Classification Based on Feature Maps of Image and Radar Data](https://arxiv.org/abs/2410.16089)** `2024` `Method` `multi-sensor-fusion` `thermal` `radar`
  *Nikos Sakellariou, Konstantinos Votis, Antonios Lalas, Dimitrios Tzovaras, arXiv:2410.16089.*
  > 中文：在特征级融合热成像、光电与雷达三路CNN特征，三模态F1=0.95，显著优于单传感器。
  > 📜 DOI: N/A · 💻 Code: N/A · 📊 Data: N/A

- **[UAV Detection and Tracking in Urban Environments Using Passive Sensors: A Survey](https://www.mdpi.com/2076-3417/13/20/11320)** `2023` `Survey` `anti-UAV` `passive-sensors` `urban-surveillance`
  *Xiaochen Yan, Tingting Fu, Huaming Lin, Feng Xuan, Yi Huang, Yuchen Cao, Haoji Hu, Peng Liu, Applied Sciences (MDPI), 13(20):11320.*
  > 中文：综述城市IoT场景下RF/声学/视觉三类被动反无人机探测、定位与跟踪技术，并盘点公开数据集。
  > 📜 DOI: `10.3390/app132011320` · 💻 Code: N/A · 📊 Data: N/A

- **[RF-Enabled Deep-Learning-Assisted Drone Detection and Identification: An End-to-End Approach](https://www.mdpi.com/1424-8220/23/8/4202)** `2023` `Method` `RF` `end-to-end` `deep-learning`
  *Syed Samiul Alam, Arbil Chakma, Md Habibur Rahman, Raihan Bin Mofidul, Md Morshed Alam, Ida Bagus Krishna Yoga Utama, Yeong Min Jang, Sensors (MDPI), 23(8):4202.*
  > 中文：端到端多尺度特征+残差块的RF信号检测识别模型，CardRF数据集上97.5%精度，推理0.37ms。
  > 📜 DOI: `10.3390/s23084202` · 💻 Code: N/A · 📊 Data: CardRF dataset

- **[Micro-Doppler Signature Detection and Recognition of UAVs Based on OMP Algorithm](https://www.mdpi.com/1424-8220/23/18/7922)** `2023` `Method` `radar` `micro-Doppler` `clutter-suppression`
  *Shiqi Fan, Ziyan Wu, Wenqiang Xu, Jiabao Zhu, Gangyi Tu, Sensors (MDPI), 23(18):7922.*
  > 中文：基于OMP稀疏字典的LFMCW雷达杂波抑制方法，-10dB SNR下提取旋翼微多普勒特征识别不同无人机。
  > 📜 DOI: `10.3390/s23187922` · 💻 Code: N/A · 📊 Data: N/A

- **[mmHawkeye: Detection and Identification of Non-Cooperative UAV using a COTS mmWave Radar](https://yimiao-sun.github.io/files/PDF/2023mmHawkeye_TOSN.pdf)** `2023` `System` `mmWave-radar` `micro-motion` `LSTM`
  *Yuan He, Jia Zhang, Rui Xi, Xin Na, Yimian Sun, Beibei Li, ACM Transactions on Sensor Networks (TOSN), 1(1).*
  > 中文：商用毫米波雷达利用UAV周期性微动特征+粒子滤波跟踪+LSTM分类，探测精度95.8%，距离达80m。
  > 📜 DOI: N/A · 💻 Code: N/A · 📊 Data: N/A

- **[Real-time drone detection and tracking in distorted infrared images](https://hal-emse.ccsd.cnrs.fr/emse-04341911)** `2023` `Method` `infrared` `YOLOv7` `SORT-tracking`
  *Abdelouahid Bentamou, Abbass Zeineddine, Oussama Messai, Yann Gavet, IEEE ICIP 2023.*
  > 中文：YOLOv7检测+SORT跟踪并行ViT畸变检测，红外无人机mAP=92.6%，应对噪声与畸变。
  > 📜 DOI: `10.1109/ICIP49359.2023.10522789` · 💻 Code: https://github.com/a-bentamou/Drone-detection-and-tracking · 📊 Data: N/A
| 方法/代表论文 | 年份 | 核心思路 | 优点 | 局限 | 适用场景 |
|---|---|---|---|---|---|
| RF信号检测 (Alam et al. 2023) | 2023 | 端到端深度网络从遥控RF签名直接分类无人机型号 | 探测距离远(可达数百米)、可识别厂商/型号、被动隐蔽、推理快0.37ms | 对静默/预编程无人机无效；与同频段蓝牙/WiFi干扰需分离 | 机场、要地周界实时无人机识别 |
| 毫米波雷达+微多普勒 (mmHawkeye, He et al. 2023) | 2023 | COTS mmWave雷达提取旋翼周期性微动特征+LSTM分类 | 全天候、可测距方位角、不依赖无人机配合、80m实测 | 小RCS目标弱、鸟与无人机易混、成本高于声学 | 低空静默无人机主动探测、要地跟踪 |
| LFMCW雷达+OMP杂波抑制 (Fan et al. 2023) | 2023 | 稀疏字典OMP抑制地杂波后提取旋翼微多普勒闪烁特征 | -10dB低信噪比仍可提取特征、杂波抑制-15dB | 需雷达硬件部署、对悬停外运动状态依赖参数估计 | 城市/低空复杂背景雷达反无人机 |
| 声学检测+数据增强 (Kmmritz 2025) | 2025 | ML分类器+多种声学增强(音高/时延/谐波/噪声)识别C0-C3类 | 成本极低、被动、可与其它模态互补 | 探测距离短(数十米)、城市环境噪声干扰大、远距离衰减严重 | 机场/围栏近距离辅助告警 |
| RF+声学特征融合 (Frid et al. 2024) | 2024 | LSTM融合RF频谱特征与音频特征联合分类 | -10dB低SNR仍91%，单模态失效时互为冗余 | 需双传感器部署、特征对齐与同步成本 | 城市多传感器互补反无人机 |
| 红外视觉小目标检测 (AIMED-Net, Pan et al. 2024) | 2024 | YOLOv7+GAN浅层增强+深层检测增强，边缘端优化 | 夜间/低光照可用、可成像取证、边缘部署快 | 雾/雨/强光受限、无人机像素占比小、与鸟群混淆 | 夜间要地监视、机载边缘反制 |
| 热成像+光电+雷达三模态特征级融合 (Sakellariou et al. 2024) | 2024 | CNN特征级堆叠融合热像、光电、雷达三路特征 | F1=0.95，互补模态显著优于单模(0.91) | 系统复杂、需严格时空对齐、算力与成本高 | 高安全等级要地综合反无人机 |
| Drone-vs-Bird视频挑战赛 (Coluccia et al. 2024) | 2024 | 公开视频基准对比运动相机+鸟群干扰下的深度学习检测 | 标准化评测、推动方法对比、数据持续扩展 | 仅限视频模态、依赖数据集分布 | 视觉反无人机算法公平评测 |

---

## 🚜 Applications: Agriculture, Inspection & Delivery

- **[A Deep-Learning-Based Method for Extracting an Arbitrary Number of Individual Power Lines from UAV-Mounted Laser Scanning Point Clouds](https://www.mdpi.com/2072-4292/16/2/393)** `2024` `Method` `power-line` `point-cloud` `LiDAR`
  *Sha Zhu, Qiang Li, Jianwei Zhao, Chunguang Zhang, Guang Zhao, Lu Li, Zhenghua Chen, Yiping Chen, Remote Sensing (MDPI), 16(2):393.*
  > 中文：多分支深度网络从机载LiDAR点云中自动提取任意数量电力线，加权CE+Mean Shift聚类区分线路。
  > 📜 DOI: `10.3390/rs16020393` · 💻 Code: N/A · 📊 Data: N/A

- **[Aerial Inspection of High-Voltage Power Lines Using YOLOv8 Real-Time Object Detector](https://www.mdpi.com/1996-1073/17/11/2535)** `2024` `Method` `power-line` `YOLOv8` `insulator-defect`
  *Elisavet Bellou, Ioana Pisica, Konstantinos Banitsas, Energies (MDPI), 17(11):2535.*
  > 中文：微调YOLOv8实时检测杆塔/绝缘子/导线，mAP@0.5=83.8%，GPU上243fps，缺陷绝缘子分类99.5%。
  > 📜 DOI: `10.3390/en17112535` · 💻 Code: N/A · 📊 Data: N/A

- **[Optimization of Drone Delivery Routes for E-commerce in Urban Areas](https://pdfs.semanticscholar.org/86cd/6df0baacc48cdfd0a6f90db534bd3e000551.pdf)** `2024` `Method` `delivery` `VRP` `stochastic-optimization`
  *Feifei Huang, Xinyang Zhang, Xiaoli Su, Journal of Engineering Science and Technology Review.*
  > 中文：考虑续航与载荷约束的机会约束模型求解城市无人机配送路径，历史需求数据线性化分布未知约束。
  > 📜 DOI: `10.25103/jestr.172.11` · 💻 Code: N/A · 📊 Data: N/A

- **[A Lightweight Man-Overboard Detection and Tracking Model Using Aerial Images for Maritime Search and Rescue (YOLOv7-FSB)](https://www.mdpi.com/2072-4292/16/1/165)** `2024` `Method` `search-and-rescue` `maritime` `ByteTrack`
  *Yijian Zhang, Qianyi Tao, Yong Yin, Remote Sensing (MDPI), 16(1):165.*
  > 中文：FSNet主干+SP-ELAN轻量化检测网融合ByteTrack，海上落水人员检测89.2%，跟踪82.7FPS。
  > 📜 DOI: `10.3390/rs16010165` · 💻 Code: N/A · 📊 Data: N/A

- **[An modified intelligent real-time crack detection method for bridge based on improved target detection algorithm and transfer learning (YOLOv7-CD)](https://www.frontiersin.org/articles/10.3389/fmats.2024.1351938)** `2024` `Method` `infrastructure` `bridge-crack` `YOLOv7`
  *Yang Yang, Long Li, Gang Yao, Hongbo Du, Yuxiao Chen, Linjun Wu, Frontiers in Materials, 11:1351938.*
  > 中文：YOLOv7嵌入SE注意力+Focal-EIoU损失+两阶段迁移学习，长江大桥实测AP=98.01%。
  > 📜 DOI: `10.3389/fmats.2024.1351938` · 💻 Code: N/A · 📊 Data: N/A

- **[Design and validation of a multi-objective waypoint planning algorithm for UAV spraying in orchards based on improved ant colony algorithm (MS-ACO)](https://www.frontiersin.org/articles/10.3389/fpls.2023.1101828)** `2023` `Method` `agriculture` `path-planning` `ant-colony`
  *Haoxin Tian, Zhenjie Mo, Chenyang Ma, Junqi Xiao, Ruichang Jia, Yubin Lan, Yali Zhang, Frontiers in Plant Science, 14:1101828.*
  > 中文：改进多源蚁群算法MS-ACO，结合转角与距离成本优化果园航点，能耗降低30%+，航次时间缩短50%。
  > 📜 DOI: `10.3389/fpls.2023.1101828` · 💻 Code: N/A · 📊 Data: N/A

- **[Generalized data-driven optimal path planning framework for uniform coverage missions using crop spraying UAVs](https://link.springer.com/article/10.1007/s11119-023-09999-3)** `2023` `Method` `agriculture` `coverage-path` `neural-network`
  *Rohit V. Vanavati, Yanhua Meng, Matthew Coombes, Cunjia Liu, Precision Agriculture, 25.*
  > 中文：高斯核神经元建模喷洒分布，自动优化航速与喷幅以最小化覆盖率不均，DJI AGRAS-T10实测验证。
  > 📜 DOI: `10.1007/s11119-023-09999-3` · 💻 Code: N/A · 📊 Data: N/A

- **[Aerial-ground collaborative routing with time constraints (VRPD-T)](https://www.sciencedirect.com/science/article/pii/S1000936122002175)** `2022` `Method` `delivery` `truck-drone` `time-window`
  *Jiahao Xing, Lichen Su, Wenjing Hong, Lu Tong, Renli Lyu, Wenbo Du, Chinese Journal of Aeronautics, 36(3).*
  > 中文：建模VRPD-T混合整数规划，考虑客户时间窗与时变行程时间，时空混合启发式求解大规模卡车-无人机协同配送。
  > 📜 DOI: `10.1016/j.cja.2022.06.012` · 💻 Code: N/A · 📊 Data: N/A

---

## 📊 Datasets & Benchmarks

| Dataset | Task | Description | Link |
|---|---|---|---|
| **VisDrone2019** | Object Detection / Tracking | 无人机视角目标检测 / 跟踪，密集小目标场景 | [github.com/VisDrone/VisDrone-Dataset](https://github.com/VisDrone/VisDrone-Dataset) |
| **UAVDT** | Detection / Tracking | 城市无人机视角车辆检测跟踪 | [paperswithcode](https://paperswithcode.com/dataset/uavdt) |
| **DroneVehicle** | Detection | 红外+可见光车辆检测 | [github.com/VisDrone](https://github.com/VisDrone/VisDrone-Dataset) |
| **EUROC MAV** | VIO / SLAM | 无人机视觉-惯性里程计标准数据集 | [projects.asl.ethz.ch](https://projects.asl.ethz.ch/datasets/dataset/EuRoCMAV) |
| **Drone-vs-Bird** | Anti-UAV Detection | 无人机 vs 鸟类声学/视觉检测基准 | [doi.org/10.1109/ICASSP49357.2023.10096123](https://doi.org/10.1109/ICASSP49357.2023.10096123) |
| **U2UData** | Cooperative Perception | 大规模无人机间协同感知数据集 | [fengtt42.github.io/U2UData-2](https://fengtt42.github.io/U2UData-2/) |
| **UAV123** | Tracking | 无人机视角目标跟踪基准 | [cvrl.stonybrook.edu/uav123](https://cvrl.stonybrook.edu/uav123/) |
| **iSAID / LoveDA** | Segmentation | 航拍图像实例/语义分割数据集 | [github.com/sizhewe/iSAID](https://github.com/sizhewe/iSAID) |
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
- **[Faster-LIO](https://github.com/gaoxiang12/faster-lio)** — 轻量紧耦合 LiDAR-惯性里程计。
- **[Swarm-LIO2](https://github.com/hku-mars/Swarm-LIO2)** — HKU MARS 去中心化多机 LiDAR 惯性里程计。

---

## Contributing

PRs welcome! When adding a paper, please include:
- **Year** + **Type** (`Survey` / `Method` / `System` / `Dataset` / `Tool`) + key **tags**
- A working PDF / publisher link (avoid Sci-Hub / staging domains)
- One-line English summary **and** one-line Chinese summary
- Code / Dataset links **only if they actually exist**; otherwise mark `N/A` — do not fabricate.

## License

[CC0-1.0](https://creativecommons.org/publicdomain/zero/1.0/)
