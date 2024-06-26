#### 架构师的期望
- 接触过多种不同的技术、框架、平台、环境。
- 具有业务知识。
#### 软件架构法则
- 软件架构中的一切都是一种权衡。
#### 衡量模块化
- 内聚

#### 系统架构通用特征
- 可用性 Availability
系统需要提供多长时间的服务（如果是全天候服务，则需要制定措施，以便在出现任何故障时，系统能够迅速恢复运行）。
- 持续性 Continuity
灾后恢复能力。
- 性能 Performance
包括压力测试、峰值分析、功能使用频率分析、所需容量和响应时间。性能验收有时需要自己进行演练，耗时数月才能完成。
- 可恢复性 Recoverability
业务连续性要求（例如，发生灾难时，要求系统多快恢复运行？） 这将影响备份策略和对复制硬件的要求。
- 可靠性/安全性 Reliability/safety
评估该系统是否需要故障安全保护，或者它是否是影响生命的关键任务。如果出现故障，是否会给公司带来巨额损失？
- 鲁棒性 Robustness
在互联网连接中断、断电或硬件故障的情况下，能够在运行过程中处理错误和边界条件。
- 可扩展性 Scalability
当用户或请求数量增加时，系统执行和运行的能力。
#### 架构权衡
- 永远不要追求最好的架构，而是追求最不糟糕的架构。
#### 架构特性识别
- 外部服务意味着集成点，可能会影响系统的可靠性，避免在服务中加入不必要的脆性/弱性。
- 可移植性，多终端的兼容。
- 性能通常不是那么高优先级的特性。

#### 架构特性测量
- 代码复杂度，圈复杂度CC，一般行业阈值是10
- 敏捷性可以细化为模块化、可测试性、可部署性。
- 度量、监控、单元测试库、混沌工程。
#### 架构特征范围
- 如果一个组件的修改需要修改另外一个组件以保持系统的正确性，那么这两个组件就是关联的。

#### 架构师角色
- 康威定律：组织结构会影响所设计的系统结构。
- 按技术分区，还是按业务领域分区。
- 业务领域分区围绕工作流。
- 技术分区可以让开发迅速找到相应的代码。

#### 架构风格
- 敏捷性（快速响应变更的能力）、可测试性（测试的简易型以及完整性）、可扩展性、性能、可部署性（部署简易性、频率以及风险）。
#### 分布式架构的谬误
- 网络是可靠的。
- 没有延迟。
- 带宽是无限的。
- 网络是安全的。
- 网络拓扑结构是固定的。
- 只有一位管理员，不需要找谁协调沟通。
- 传输成本为0.
- 网络是同构。（例如都是一个运营商，都是同一份网络硬件。）
#### 分布式架构的考虑

- 分布式日志记录
- 分布式ACID事务
- 合约维护和版本控制
#### 分层架构风格

#### 异步处理

- 数据丢失是一个首要问题。
#### 请求-回复，同步通信

- 一个请求队列，一个回复队列。
- 第一种可以采用消息头中，包含相关ID.
- 第二种可以采用创建特定的临时队列，用完就销毁。

#### 微服务架构

- 服务粒度的把握，因为服务间需要通信完成协同工作，比函数调用更耗时。
- 数据的隔离，有别于其他架构风格都使用单一数据库进行持久化。
- 坚定的领域分区。
- 避免跨服务边界构建事务。
#### 服务间的通信

- 尽可能使用同步通信。
#### 架构决策

- 证明架构决策合理性四个常见的业务理由：成本、上市时间、用户满意度、战略定位。
- 提供沟通架构决策的效率：邮件只提及决策的性质和上下文，提供一个链接指向架构决定和细节的文档；并且只通知那些真正关心架构决策的人，也就是利益相关者（受影响的人）。
#### 决策记录工具ADR

- 标题，简明概要描述架构决策。例如：服务之间采用异步通信。
- 决策的状态，例如：待讨论、已接受、已替代。
- 背景，说明为什么做这个决策。
- 决策，采用命令式语气表达决策。
- 该决策带来的影响，正面以及负面的影响或者问题，权衡的结果。
- 合规性
- 备注说明
#### 分析架构风险

- 风险评估矩阵，【出现风险的可能性, 该风险出现带来的影响】。

| 可能性\影响 | 影响高 | 影响低 |
| ------- | ------- | ------- |
| 高 | - | - |

- 风险风暴。
#### 架构师对开发团队控制力度的考量因素

- 开发团队内部的熟悉度，反相关。
- 团队成员的数量，正相关。
- 团队成员的经验系数，反相关。
- 项目的复杂程序，反相关。
- 项目周期长度，正相关。
#### 团队的一些注意事项

- 多元化的无知，当众多人都同意某一项决定时，极少数人可能由于怕被嘲笑而不敢说出自己的想法，从而明面上也赞同该决定实际私底下反对这个决定。架构师需要觉察，并鼓励发言。
- 太大的团队可能会导致责任分散。
- 利用好checklist，就像航空公司飞行员在每次飞行中都会使用checklist.不要担心在checklist列出显而易见的事项。显而易见的东西往往是最容易被忽略的。
- 需要意识到使用某项新技术的商业理由。
#### 谈判技能

- 要从毫无意义的语句中，提炼出有价值的信息。例如：“我昨天就需要这个功能了”，言外之意就是上市时间对于利益相关者非常重要。
- 如果其他方法都不奏效，就从成本和时间的角度说明问题。这个谈判策略一般都是留到最后。
- 分而治之，将有难度的事情缩小作用范围，例如高可用性，缩减到某个细节领域。
- 如果开发人员不同意某项决策时，可以让他们自行解决。
#### 领导技能

- 避免使用“你必须”、“你需要做的是”，而是尽量使用“你是否考虑”、“这样怎么样”，创建协作式对话。
- 交谈或者谈判中尽量使用对方的名字。
- 把请求转换为帮助。
- 要成为得力助手，发现团队成员的烦恼，主动沟通解决。
#### 与开发团队一起

- 提前询问会议议程，可以帮助确定是否真的需要参加。
- 召开会议应该尽量安排在早上的第一件事，或者一天的末尾，而不是在开发人员处于状态中的白天。
- 与开发团队坐在一起，与利益相关者多走动，顺便打招呼，保持开放沟通。
#### 架构师职业管理
- 架构师的广度比深度更重要。
- 20分钟法则：每天花至少20分钟学习新知识或者深入研究某个特定主题，谷歌一下一些你不知道的流行语。
#### 技术雷达
- 工具
- 语言和框架
- 技术，包括开发流程、工程实践、建议
- 平台，包括数据库、云商、操作系统
#### 扩散环
- 搁置，技术太新了，无法评估
- 评估，技术可以值得投入时间探索
- 试用
- 采纳