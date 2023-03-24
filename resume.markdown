---
   layout: page
   title: "Resume"
   permalink: /resume/
---

上海交通大学并行与分布式系统研究所（IPADS）博五学生。导师为臧斌宇教授与陈海波教授。主要研究兴趣包括多核同步、线程调度、微内核。

## 工作经验

### ARM弱内存下内存屏障的性能刻画及优化 — 2019

**关键词：** 弱内存模型，内存屏障，互斥锁，同步

**简介：**由于ARM采用了弱内存模型，现有软件，特别是那些从x86移植过来的软件，需要插入内存屏障，其将严重影响应用程序的性能。本工作首先通过一系列系统性实验，完整刻画了不同内存屏障的性能差异，执导开发者在合适的地方插入合适的内存屏障；且提出了一个新的同步机制，Pilot，其可以用于消除造成严重性能开销的内存屏障，从而提升弱内存系统性能可扩展性。本工作被CCF-A类会议PPoPP ‘20接收，本人为第一作者。


### 微内核开发 — 2019-Now

**关键词：**微内核，内核开发，进程间通讯，故障恢复

**简介：**我们从头构建了一个新型的微内核ChCore（C语言书写）。ChCore与现有的内核的主要差别为采用了很多系统领域最新的技术，包括用户态系统服务，高性能IPC等。ChCore同时作为我们研究实验平台，且已经可以允许一系列真实应用（包括ROS2，数据库等）。我的主要贡献包括构建内核线程管理/调度器/同步（如同步原语/通知机制），并协助完善ChCore软件生态（如移植LibC、POSIX兼容，网络栈乃至ROS2等大型应用）。基于ChCore，我们使用Intel MPK硬件优化了进程间通讯的性能 [ATC ’20]，提供了一套基于事务性进程间通讯的故障恢复机制 [ICDCS ’21]，并且为其提供了一套操作系统教材 [MOSPI]。

### 同构ISA非对称多核可扩展互斥锁 — 2020-2021

**关键词：**可扩展互斥锁，非对称多核

**简介：**非对称多核（俗称大小核）以其灵活性在移动端乃至桌面端收到了极大的关注。然而所有现有互斥锁均无法扩展到大小核上。其主要原因是这些互斥锁都隐式地假设了对称核心。本工作提出了首个大小核可扩展的互斥锁LibASL，其使用了一个新型时延执导的可乱序锁传递顺序。该顺序能够在保证小核时延满足应用粗粒度时延需求的同时，尽可能多的允许大核获取互斥锁以达到更好的吞吐率。现实世界测试集显示，LibASL最多能提升现有互斥锁5倍的性能。本工作被CCF-A类会议PPoPP ‘22接收，本人为第一作者。


### 异构众核可扩展互斥锁 — 2022-2023

**关键词：**可扩展互斥锁，异构众核

**简介：**异构众核在众核服务器中包含了多种异构特征，如非对称多核与非一致性内存访问。由于其异构特征，传统单一静态优先同步策略（如单一优先大核/单一优先本地核心）无法扩展到异构众核系统中。本工作通过根据异构众核的异构特征提供动态、多层优先级同步策略，提升同步原语在异构众核系统中的可扩展性。

## 教育背景

上海交通大学, Ph.D. in Computer Science, 2018-Now (GPA：3.79/4.0)
湖南大学, B.S. in Computer Science, 2014-2018 (GPA：3.91/4.5, 排名 1/128)

## 发表论文

- [PPoPP ’20] Nian Liu, Binyu Zang, Haibo Chen. No Barrier in the Road: A Comprehensive Study and Optimization of ARM Barriers. (CCF-A 第一作者)
- [ATC ’20] Jinyu Gu, Xinyue Wu, Wentai Li, Nian Liu, Zeyu Mi, Yubin Xia and Haibo Chen. Harmonizing Performance and Isolation in Microkernels with Efficient Intra-kernel Isolation and Communication. (CCF-A)
- [ICDCS ’21] Wentai Li, Jinyu Gu, Nian Liu, Binyu Zang. Efficiently Recovering Stateful System Components of Multi-server Microkernels. (CCF-B)
- [PPoPP ’22] Nian Liu, Jinyu Gu, Dahai Tang, Kenli Li, Binyu Zang, Haibo Chen. Asymmetry-aware Scalable Locking. (CCF-A 第一作者)
- [MOSPI] 现代操作系统：原理与实现。 其中第8章及第12章为本人书写。

##  获得奖项

2022年 	英特尔奖学金
2020年 	卓越助教奖
2017年	国家奖学金
