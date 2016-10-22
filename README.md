[The Baidu File System](http://github.com/baidu/bfs)
======

 [![Build Status](https://travis-ci.org/baidu/bfs.svg?branch=master)](https://travis-ci.org/baidu/bfs)  [![Build Status](https://scan.coverity.com/projects/8135/badge.svg)](https://scan.coverity.com/projects/myawan-bfs-1/) 

The Baidu File System (BFS) is a distributed file system designed to support real-time applications. Like many other distributed file systems, BFS is highly fault-tolerant. But different from others, BFS provides low read/write latency while maintains high throughout rates. Together with [Galaxy](https://github.com/baidu/galaxy) and [Tera](http://github.com/baidu/tera), BFS supports many real-time products in Baidu, including Baidu webpage database, Baidu incremental indexing system, Baidu user behavior analysis system, etc.

百度的核心业务和数据库系统都依赖分布式文件系统作为底层存储，文件系统的可用性和性能对上层搜索业务的稳定性与效果有着至关重要的影响。现有的分布式文件系统（如HDFS等）是为离线批处理设计的，无法在保证高吞吐的情况下做到低延迟和持续可用，所以我们从搜索的业务特点出发，设计了百度文件系统。

## Features
1. Continuous availability  
数据多机房、多地域冗余，元数据通过Raft维护一致性，单个机房宕机，不影响整体可用性。  
2. High throughput  
通过高性能的单机引擎，最大化存储介质IO吞吐；  
3. Low latency  
全局负载均衡、慢节点自动规避  
4. Linear scalability  
设计支持两地三机房，1万+台机器管理。  

## Architecture
![架构图](resources/images/bfs-arch2-mini.png)

## Quick Start
#### Build  
./build.sh
#### Standalone BFS
cd sandbox; ./deploy.sh; ./start.sh

## How to Contribute
Please see the [RoadMap](docs/roadmap.md) file or source code for how to help out, select features which you are interested in, coding and and then send pull request to us. After the codereview, your code will run in thousands of servers~

阅读[RoadMap](docs/roadmap.md)文件或者源代码，了解我们当前的开发方向，找到自己感兴趣的功能或模块进行开发，并进行自测，然后发起pull request。CodeReview通过后，您的代码便有机会运行在百度数以万计的服务器上~

## Contact us
opensearch@baidu.com

