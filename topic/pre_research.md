# Pre-Research
## Distributed-OS

### 定义

将若干节点的资源统筹调配，对用户透明。这些计算机在物理上是分开的，在体系结构上可能是异构的，但是通过网络相互连接，形成一个统一的计算系统。分布式系统的各个计算机通过相互发送消息实现交流和协调。
主要分为两部分：
* minimal kernel, 用于直接控制该节点的硬件
* system management component, 用于引导节点的单独或协作活动

### 实例
* 传统意义上的操作系统：基于底层硬件开发，提供了一套完整的系统，用户可以直接使用：
  * 还活着的： Barrelfish, HarmonyOS, Inferno, Plan 9 from Bell Labs, QNX
* 亚操作系统：
  * Ray(Python, 主要用于分布式计算), Ceph(C++, 分布式存储系统)

### 过往项目
#### OSH-2022 x-DelayNoMore
* 利用了去中心化的 ROS 信息传递机制， 使用 Ray 来实现分布式计算
* 使用Ray将多个节点的算力结合起来。将部署的ROS节点（分布式计算集群节点）发出的任务通过Ray中的分布式计算框架进行计算调度后返回到各个节点中去

### 可能的开发方向
* 专一功能：如分布式存储系统 -> (分布式OS)、分布式计算系统
* 通用：
  * 从零写起的分布式OS（轻量化，最基本功能，可选用某一种架构单独开发）
  * 改写某种已有OS的内核使其支持分布式（如Linux），保持上层内容不变
  

## Distributed-File-System

### 定义
若干存储节点被封装在统一的接口之后，对用户透明，用户只能看到一个整体的文件系统。

### 过往项目：

#### OSH-2022 x-WowKiddy
* 数据一致性问题 - Paxos算法
* 高性能问题 - 缓存

## Mobile Operating System

几乎没人做过， Android OS 和 IOS 从操作系统层面讲学习较难。

### IOS

IOS 一般需要 Mac 作为开发平台，skip。

## Android

Android OS 有开发空间，并且开源。

然而众多手机厂商已经对其进行深度开发，创新空间不大。有想法的话可以:)

## Reference

2022年之前项目：

参见 [pre_research_2022.pdf](../reference/pre_research_2022.pdf)