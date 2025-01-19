
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

### 命令行工具

#### cyber_monitor 用法

``` bash
$ source setup.bash    
$ cyber_monitor --help
```

    `cyber_monitor` 会自动从拓扑中收集channel信息并分两列显示：`Channels（channel名称）`，`FrameRatio（数据频率）`

#### cyber_recorder 用法

``` bash
$ source setup.bash    
$ cyber_recorder play -l [record]
# this will play the record in loop
```

    `cyber_recorder` 功能丰富

#### cyber_channel 用法



## 常用术语

#### Component
    在自动驾驶中，模块（感知、定位、控制、回传等）在 Cyber Rt 中以 Component 的形式存在。不同 Component 之间通过 Channel 通信。
    优势：
        解耦了模块，将模块拆分成多个字模块提升灵活性

#### Channel
    Channel 用于管理 Cyber​​ RT 中的数据通信。用户可以发布/订阅同一个 Channel，实现 P2P 通信。
    优势：
        消息定义主要使用 proto，高效

#### Task
    Cyber Rt 中异步计算任务的抽象描述

#### Node
    Node 是 Cyber​​ RT 的基本组成部分。每个模块都包含一个 Node 并通过 Node 进行通信。通过在节点中定义 Reader/Writer 或 Service/Client，模块可以具有不同类型的通信形式。

#### Dag
    Dag 文件是模块拓扑关系的配置文件。您可以在 dag 文件中定义使用的 Component 和上游/下游通道。

#### Parameter
    基于 Service/Client 模式构建的全局参数服务

#### Message
    Cyber RT 中用于模块间通信的数据单元

