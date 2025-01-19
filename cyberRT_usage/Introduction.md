
# cyberRT 介绍

Apollo Cyber​​ RT 是一个开源、高性能的运行时框架，专为自动驾驶场景而设计。针对自动驾驶的高并发、低延迟、高吞吐量进行了大幅优化。

## 优势

Apollo CyberRT具备以下优势：

#### 加速开发
- 具有数据融合功能的定义明确的任务接口
- 丰富的开发工具
- 大量传感器驱动程序

#### 简化部署
- 高效自适应的消息通信
- 具有资源意识的可配置用户级调度程序
- 可移植，依赖少

#### 赋能自动驾驶
- 默认的开源运行时框架
- 搭建自动驾驶专用模块

## 开发工具

#### 命令行工具

##### cyber_monitor

cyber_monitor 用法

``` bash
$ source setup.bash    
$ cyber_monitor
```

`cyber_monitor`会自动从拓扑中手机channel信息并分两列显示：`Channels（channel名称）`，`FrameRatio（数据频率）`