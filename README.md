# Papers

个人论文收藏：计算机系统、大数据、分布式、数据库、编译原理等领域的技术论文 PDF。

> 目录结构即分类，文件链接均为仓库内相对路径。

## 目录

- [Algorithms](#algorithms) — 分布式算法与一致性哈希
- [Architecture](#architecture) — 系统架构
- [BigData](#bigdata) — 大数据与分布式计算
- [Computer](#computer) — 计算机体系结构
- [Database](#database) — 数据库
- [MicroService](#microservice) — 微服务与可观测性
- [MiddleWare](#middleware) — 中间件与分布式存储
- [Parser](#parser) — 解析器与组合子
- [Programme](#programme) — 编程与工程实践
- [Slides](#slides) — 行业分享
- [Tools](#tools) — 基础工具与参考资料

## Algorithms

分布式算法、一致性协议与哈希算法。

- [SWIM: Scalable Weakly-consistent Infection-style Process Group Membership Protocol](algorithms/SWIM.pdf) — 基于 gossip 的可扩展成员关系协议
- [Lightweight Asynchronous Snapshots for Distributed Dataflows](algorithms/Lightweight_Asynchronous_Snapshots_for_Distributed_Dataflows.pdf) — Flink Checkpoint 背后的异步快照算法

### ConsistentHash

- [Consistent Hashing and Random Trees: Distributed Caching Protocols for Relieving Hot Spots on the World Wide Web](algorithms/ConsistentHash/chash.pdf) — 一致性哈希的奠基性论文
- [A Fast, Minimal Memory, Consistent Hash Algorithm](algorithms/ConsistentHash/JumpConsistentHash.pdf) — Google Jump Hash，O(1) 内存的一致性哈希
- [A Fast, Minimal Memory, Consistent Hash Algorithm with Super-Fast Hash Table Search](algorithms/ConsistentHash/Multi-probe-consistent-hashing.pdf) — Multi-Probe 一致性哈希，减少虚拟节点内存开销

## Architecture

- [SEDA: An Architecture for Well-Conditioned, Scalable Internet Services](architecture/seda-sosp01.pdf) — 分阶段事件驱动架构，用队列隔离与负载控制

## BigData

大数据处理引擎与查询优化。

- [MapReduce: Simplified Data Processing on Large Clusters](bigData/mapreduce.pdf) — Google 大规模集群数据处理模型
- [Apache Flink™: Stream and Batch Processing in a Single Engine](bigData/flink-deb.pdf) — Flink 流批一体引擎
- [Presto: SQL on Everything](bigData/Presto-SQL-on-Everything.pdf) — Facebook 分布式 SQL 查询引擎
- [The Dataflow Model: A Practical Approach to Balancing Correctness, Latency, and Cost in Massive-Scale, Unbounded, Out-of-Order Data Processing](bigData/DataFlow-Model.pdf) — Google Dataflow，流式语义模型
- [Morsel-Driven Parallelism: A NUMA-Aware Query Evaluation Framework for the Many-Core Age](bigData/p743-leis.pdf) — 现代 OLAP 引擎的 morsel 并行执行框架
- [Optimizing Queries Using Materialized Views: A Practical, Scalable Solution](bigData/opt_views.pdf) — 基于物化视图的查询改写优化
- [Bubble Execution: Resource-aware Reliable Analytics at Cloud Scale](bigData/Bubble-Execution.pdf) — 资源感知的多租户分析隔离
- [HoTTSQL: Proving Query Rewrites with Univalent SQL Semantics](bigData/hottsql.pdf) — 用同伦类型论证明 SQL 查询改写等价性
- [Nitro: A Fast, Scalable In-Memory Storage Engine for NoSQL Global Secondary Index](bigData/Nitro.pdf) — 面向全局二级索引的内存存储引擎
- [Spanner: Google's Globally-Distributed Database](bigData/spanner-osdi2012.pdf) — 全球分布式数据库与 TrueTime

### WareHouse

- [The Snowflake Elastic Data Warehouse](bigData/wareHouse/The-Snowflake-Elastic-Data-Warehouse.pdf) — 云原生数仓的多集群共享架构
- [Real-time Data Infrastructure at Uber](bigData/wareHouse/Real-time-Data-Infrastructure-at-Uber.pdf) — Uber 实时数据基础设施

## Computer

- [Computer Organization and Architecture Lecture Notes](computer/computer-architecture.pdf) — 计算机组成原理课程讲义汇编
- [Latency Numbers Every Programmer Should Know](computer/rule-of-thumb-latency-numbers-letter.pdf) — 各层级延迟数量级速查表

## Database

- [Architecture of a Database System](database/fntdb07-architecture.pdf) — 数据库系统五大组件架构综述
- [The Design and Implementation of a Log-Structured File System](database/LFS.pdf) — LFS，写优化与日志结构设计
- [Apache Calcite: A Foundational Framework for the Next Generation of Data Management](database/Apache-Calcite.pdf) — 动态可扩展的数据管理框架
- [DBLog: A Watermark Based Change-Data-Capture Framework](database/DBLog-A-Watermark-Based-Change-Data-Capture-Framework.pdf) — Netflix 基于水位线的 CDC 框架
- [Data Chunk Compaction in Vectorized Execution](database/3709676.pdf) — 向量化执行引擎中的数据块压缩

## MicroService

- [Dapper, a Large-Scale Distributed Systems Tracing Infrastructure](microservice/Dapper-a-Large-Scale-Distributed-Systems-Tracing-Infrastructure.pdf) — Google 分布式链路追踪
- [Falling Off the Cliff: When Systems Go Nonlinear](microservice/green.pdf) — 系统在输入超界时的非线性行为分析

## MiddleWare

- [Dynamo: Amazon's Highly Available Key-value Store](middleWare/amazon-dynamo-sosp2007.pdf) — 高可用 KV 存储的经典设计
- [F1: A Distributed SQL Database That Scales](middleWare/CSE550.F1.pdf) — Google 基于 Spanner 的分布式 SQL 数据库
- [LogStore: A Cloud-Native and Multi-Tenant Log Database](middleWare/LogStore.pdf) — 云原生多租户日志数据库
- [Alluxio: A Virtual Distributed File System](middleWare/Alluxio.pdf) — 内存速度的虚拟分布式文件系统

## Parser

- [Parsec: Direct Style Monadic Parser Combinators For The Real World](parser/parsec-paper-letter.pdf) — Parsec 单子组合子解析器的正式论文
- [Parsec, a Fast Combinator Parser](parser/parsec.pdf) — Parsec 的早期技术报告
- [Monadic Parser Combinators](parser/monparsing.pdf) — Hutton & Meijer 的单子解析组合子教程

## Programme

- [Scalable IO in Java](programme/Scalable-IO-in-Java.pdf) — Doug Lea 讲 Reactor 模式与 Java NIO
- [Parsing Gigabytes of JSON per Second](programme/Parsing-Gigabytes-of-JSON-per-Second.pdf) — simdjson 的高性能 JSON 解析
- [AOP Alliance](programme/aopalliance.pdf) — AOP 联盟的面向切面编程接口规范

## Slides

- [Offloading xPU Storage Compute Tasks to SSD](slides/20250807_DCTR-301-1_Saluja_fnl.pdf) — KIOXIA：将存储计算任务下推到 SSD

## Tools

- [Join Processing in Relational Databases](tools/Join%20processing%20in%20relational%20databases.pdf) — 关系数据库连接算法综述（ACM Computing Surveys）
- [Plumbr Handbook: Java Garbage Collection](tools/Plumbr%20Handbook%20Java%20Garbage%20Collection.pdf) — Java 垃圾回收原理与实践手册
- [Implementing Lexer Generators](tools/DFANFA.pdf) — Cornell CS4120 课程：用 DFA/NFA 实现词法分析器生成器
- [ANTLR 解析原理](tools/allstar.pdf) — 中国科学技术大学《编译原理和技术》ANTLR 解析器讲义
