 <center>
     <h1>个人简历 - 张小军</h1>
 </center>

## 个人信息 

* 姓 名：**张小军**&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;性 别：男
* 年 龄：27&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;开发经验：**4.5年**
* 手 机：见boss直聘  &emsp;&emsp;&emsp; &emsp;&emsp;&emsp;&ensp;  邮 箱：见boss直聘    
* 专 业：计算机信息管理（专科） &emsp;&emsp; 应聘岗位：**Java开发/架构**
---
## 专业技能

* 熟练使用 Java/C# 进行Web/桌面开发，了解 Scala/Python
* 了解JVM，字节码/内存结构/垃圾回收
* 掌握常见网络协议TCP/IP/HTTP
* 熟练使用相关网络嗅探/抓包工具，Wireshark/Tcpdump/Fiddler，多次通过相关网络流量分析发现和解决网络故障问题
* 掌握Spring boot/Spring Cloud体系开发
* 掌握kubernetes使用，熟悉Deployment/Service/Ingress/ConfigMap/健康检查，对k8s网络有一定的了解，2年多的使用以及维护经验
* 掌握Docker使用，了解Docker网络模型/常用网络驱动，多年Docker使用经验，解决过跨主机网络互通问题
* 了解Kafka基本原理，分区/副本/负载均衡
* 熟练使用Nginx
* 熟练使用Redis，了解Redis常用的数据结构
* 掌握基本的外语阅读能力，能利用Google快速检索以及定位问题
---
## 工作经历

1. 广州 **龙腾出行** 股份有限公司 &emsp;&emsp;&emsp; 2016-06-20 到 2020-07-15 （**四年**）
    * 公司介绍
      * “龙腾出行”是一个全球化的**智能出行服务平台**
      * 主营业务包括 候机休息室、接送机、餐饮、快速安检、机场管家、交通、购物、休闲等
      * 目前，在出行领域，龙腾出行在全球服务网络上，已位于**亚太第一，全球第二**的位置。
    * 岗位
      *  **Java开发**工程师
      *  **.NET/C#开发**工程师
      *  **数据开发**工程师
    * 成就
      * 连续两年被评为"**优秀员工**"以及"**科技标兵**"
      * 公司"**技术委员会**"核心成员
      * "**数据部**"技术负责人
      * 多个项目的核心开发人员

3. 广州 **星唯科技** 有限公司 &emsp;&emsp;&emsp;&emsp;&emsp; 2015-12-08 到 2016-06-16  （**半年**）
    * 公司介绍
      * 广州星唯信息科技有限公司是以**GPS产品的研发、生产和销售**为主营业务的有限公司。
    * 岗位
       * .NET/C#开发工程师 
---

## 项目经历 - 龙腾出行

7. 中台项目组 - 【**项目服务化**】 &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; 2017.09 ~ 2019.06 
    * 职责 ：**核心开发人员之一**，参与整体架构设计/微服务拆分/开发实现 
    * 技术栈
      * Spring Boot/Feign/Appolo/Eureka/Mybaits
    * 技术要点
      * 业务梳理，进行服务划分
      * 使用Eureka/K8S解决服务发现问题
      * 使用Ribbon/K8S进行客户端负载均衡
      * 使用Filebeat做日志采集，发到ELK
      * 使用Skywalking进行链路跟踪
      * 使用K8S对应用进行监控检查
1. 中台项目组 - 【**业务中台管理系统（后端）**】 &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; 2019.06 ~ 至今 
    * 职责 ：**核心开发人员**，负责架构搭建/需求评审/部分核心功能开发/表设计 
    * 项目说明
      * 该项目是公司“中台战略”的最重要的系统。在此之前，公司内部系统繁多，功能分散，运营/销售人员要同时熟悉多个系统，一个产品上下线，需要在各个系统进行复杂的配置，效率低下。内部系统多，开发复杂，开发成本提高。该系统整合了所有系统的功能
    * 技术栈
      * Spring Boot/Feign/Appolo/Common-dao/Mybaits
    * 技术要点
      * 基于角色的权限系统
      * 使用Mybaits + Common-dao进行数据访问
      * 利用触发器保证新旧表的数据同步
2. 架构组 - 【**自研ORM Common-dao**】 &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; 2020.04 ~ 2020.05  
    * 职责：**技术负责人**，负责设计/开发实现
    * 项目背景
      * 原来的Mybaits加代码生成器方式，**效率低**，对于新增修改字段不友好
      * 使用**Xml方式**进行配置，**易出错**，无法保证Sql的正确性
    * 技术要点
      * 使用**JdbcTemplate**作为Sql的执行层
      * 对Lamda表达式友好，**可读性好**，使用**强类型**方式去操作数据库
      * 使用**Cglib动态拦截**，记录Lamda表达式内部的调用方法，比如 w->$(w.getName(),eq,"x") 
      * 在Java代码里面**构建**一个与Sql数据库无关的**AST语法树**，再通过对应数据库驱动将AST语法树**翻译成合法Sql**
      * 编写实体代码生成器，集成到IDEA
      * 适配多种数据库，Oracle/Mysql/ANSI Sql
      * 适配多种**实体注解**，JPA注解/Mybaits Plus注解
    * 成就
      * 大幅度改善后端开发人员**开发效率**问题，改善**开发体验**
      * 涉及到数据库切换，开发人员几乎不需要做任何代码层面的调整
    * GitHub
      * https://github.com/zhxjdwh/common-dao
3. 数据部 - 【**龙腾BI可视化自助分析系统**】    &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; 2019.10 ~ 至今  
    * 职责：**技术负责人**，负责机器采购/技术调研/基础设施搭建/开发实现/培训使用
    * 项目说明
      * 该系统是一个可视化的BI系统，整合公司所有业务数据，通过可视化的UI界面，为运营人员提供一个定制化数据展示的功能。拥有丰富的图表，包括表格/透视表/折线图/柱状图/饼图/词汇云等
    * 项目背景
      * 内部**系统繁多**，**数据分散**在多个系统/多个数据库里面，运营人员/管理层无法直观看到公司的经营情况
      * 原有报表系统仅仅是作为一个“导数据”的平台，**性能差**，无法完成**复杂的统计分析**
      * 原有报表系统展现形式单一，报表**开发周期长**
    * 技术栈
      * Hadoop/Hive/Impala/Nifi/Superset
      * Java/Scala/Python
    * 技术要点
      * 使用Nifi设计ETL流程，实现Oracle/Mysql/SqlServer数据**增量导入**Hive
      * 使用**分层**思想搭建Hive数仓，ods层/ods层/ads层
      * 使用Java编写Hive/Impala常用的**UDF**
      * 使用**Superset可视化**
      * 使用Impala对数仓进行查询
      * 分析需求，设计常用维度，时间维度/产品维度/客户维度/供应商维度
      * 该项目使用Esxi/Vsphere进行虚拟化，CDH 6.0集群，总共6个节点
    * 成就
      * 解决了公司BI系统**从无到有**
      * 运营人员通过“**拖拉拽**”方式生成想要的报表，**不需要**开发人员进行**开发**跟进
      * 上线半年250+张各式图表，满足运营人员大多数分析需求
      * 相比原来的报表系统，部分复杂的统计报表查询时间从**分钟级变成毫秒级**（单表3000万数据）
4. 架构组 - 【**Kubernetes-服务容器化调研以及落地**】 &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; 2018.06 ~ 2018.09 
    * 职责：**技术负责人之一**，负责技术调研/基础设施搭建/痛点难点解决/使用培训 
    * 项目背景
      * 公司服务化**项目繁多**，部署方式**混乱**
      * 部分应用多个实例的负载均衡通过Nginx进行配置，**配置繁琐**
      * 服务发现依赖Eureka，依赖客户端实现，**可靠性差**
    * 技术要点
      * **高可用**集群搭建
      * 使用nginx-ingress解决**外网访问**问题
      * 通过coredns的host插件，解决**内部域名解析**问题
      * 调整内部DNS解析服务器，**针对k8s的服务域名，交由coredns解析**，解决了内部Vm**通过Service Name访问k8s应用**问题
      * 为网关交换机添加多条**静态路由**，解决了k8s集群外的**vm虚拟机访问问题**
      * 使用hostPath将所有应用的**日志挂着到宿主机**的文件目录
      * 部署filebeat**采集**集群容器**日志**，推送到公司**ELK**
      * 使用**健康检查**来监控应用健康情况
      * 开发**dns切换工具**，允许在办公室切换访问生产环境和测试环境的k8s内部服务，方便开发人员排查故障
    * 成就
      * 将公司大部分项目**从VM迁移到K8S**
      * 提高了**可靠性**，去掉Eureka，利用K8S的**负载均衡与服务发现**机制
      * 提高了开发人员部署/故障排查的**效率**
5. 架构组 - 【**GitLab CI/CD Devops流水线设计**】  &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; 2018.09 ~ 2018.11 
    * 职责：**技术负责人**，负责技术调研/基础设施搭建/痛点难点解决 
    * 项目背景
      * 公司服务化**项目繁多**，部署方式**混乱**
      * 传统手工部署，**繁琐低效，容易出错，增加开发人员负担**
    * 项目说明
      * **后端流程**：Maven编译 -> 单元测试/集成测试 -> Docker打包 -> 上传Maven/Docker仓库 -> 部署
      * **前端流程**：npm编译 -> Docker打包 -> 部署
    * 技术要点
      * 利用**Docker镜像缓存机制**，加速npm install过程，部署时间**从10分钟缩短成2分钟以内**
      * 针对团队以及技术栈，**制作多个基础Docker镜像**，前端React应用/前端H5应用/后端Spring boot应用/Tomcat应用
      * 制定多个yaml**部署模板**，部署到VM或者K8S
    * 成就
      * 提高**部署效率**，减轻开发人员负担
      * 简化部署流程，加快项目交付时间
      * 两年内**1万多次**编译和部署
6. 中台项目组 - 【事件通知以及API回调】&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;2019.08 ~ 2019.09 
    * 职责：**技术负责人**，负责架构搭建/开发实现
    * 项目背景
      * 历史遗留的项目较多，功能分布在各个系统里面，**没法提供一个统一的事件通知机制**
      * 很多核心的业务事件，需要**通知APP端以及合作伙伴**
    * 技术栈
      * Spring Scheduling/Kafka/Redis
    * 技术要点
      1. 使用Oracle触发器，将数据的**变更记录保存到一张单独的表**
      2. 使用Spring定时任务定时**拉取表数据**
      3. 将变更的数据解析出来，处理后**发送到Kafka**
      4. 处理程序订阅Kafka消息，根据数据的修改记录，**还原成实际的业务操作**，比如订单下单/修改/取消
      5. 将业务操作的相关信息，**发送到对应的Kafka Topic**，供应用订阅
      6. 将业务操作的相关消息，通过Http**推送到第三方**合作伙伴的系统（利用Redis List保存Http消息，异步推送，实现失败重试机制）

8. 架构组 - 【**公共项目**】 
    * 职责：**参与开发**
    * 项目说明
      * 公共项目作为公司的基础设施，提供大量工具类，基础服务功能，通过jar方式发布到maven仓库，供内部开发人员使用
    * 技术要点
      * 改进版雪花ID算法，其中 10bit 表名hash + 35 bit 时间戳 + 5 bit的递增标识 + 40bit的随机数，并且使用改进的32进制表示法，id串长度仅为18，单线程每秒生成50w Id
      * 基于Redis的分布式独占锁，使用SETNX+超时时间
9.  其他项目
    |项目名|介绍|技术栈|职责|
    |---|---|---|---|
    |企业门户（后端）|无|Java/Feign/Eureka/Appolo/|核心开发人员，开发设计/任务安排|
    |短信服务（API）|无|Java/Feign/Eureka/Appolo/|技术负责人，设计开发实现|
    |白云机场数据大屏项目(后端)|无|Java/Mysql/Spring/腾讯云图|技术负责人，设计开发实现|
    |Kong网关落地|无|Kong|技术负责人，调研搭建/培训使用|
    |堡垒机调用以及落地|无|JumpServer|技术负责人之一，基础设施搭建|
    |龙腾运营系统(前后端)|无|C#/WebForm/Dwz/Dapper|参与人员，实现功能模块|
    |航班中心接口服务(后端)|无|C#/WebApi/Oracle/Dapper|技术负责人，设计开发实现|
    |票点系统(前后端)|无|C#/WebForm/Oracle|参与人员，实现功能模块|
    |基于Dapper（ORM）的ExpressionTree扩展|无|C#|技术负责人，实现功能模块|

---

## 项目经历 - 星唯科技（实习）
1. 其他项目
    |项目名|介绍|技术栈|职责|
    |---|---|---|---|
    |如约拼车后台系统（前后端）|无|C#/Mysql/Redis/Ext.Js|参与人员，实现功能模块|
    |广州如约巴士管理后台|无|C#/Mysql/Redis/Ext.Js|参与人员，实现功能模块|
    |湖北机动车性能检测与监管后台系统|无|C#/WebApi/Oracle/Bootstrap|参与人员，实现功能模块|
---
## 获奖经历
* “优秀员工”/“科技标兵”  &emsp;&emsp;&emsp;&emsp; 龙腾出行 &emsp;&emsp;&emsp;&emsp; 2020年
* “优秀员工”/“科技标兵”  &emsp;&emsp;&emsp;&emsp; 龙腾出行 &emsp;&emsp;&emsp;&emsp; 2019年
---
## 相关证书

* 软件设计师（软考中级）&emsp;&emsp;&emsp;&emsp;2019年
* 信息管理员（软考初级）&emsp;&emsp;&emsp;&emsp;2016年
* 英语四级&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;2015年  
---
## 教育经历

* 计算机信息管理（全日制专科）&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&ensp;2013.9~2016.6&emsp;&emsp;&emsp;&emsp;&emsp; 广东轻工职业技术学院     
---
## 自我评价 
* 工作主动积极，善于发现问题，提出改进意见。期间，改善了公司很多问题，包括开发人员的开发效率，部署效率，运维效率。
* 热爱学习，敢于挑战未知的事情。负责公司内部的BI系统建设时，翻阅大量书籍/教程进行学习，几乎仅靠一人之力将这项目高效交付给运营人员
* 多门开发语言经验，有同时参与以及维护多个开发语言/技术栈的经验，能对老旧系统的技术升级提出改进建议
* 责任心强，不推卸，多次第一时间参与公司技术事故的排查与系统恢复
* 性格开朗，不爱争吵，与同事关系融洽
---

## 个人常用的工具 
  
* 操作系统 ： Window10/Manjaro
* Api调试 ：Postman/Yapi
* 搜索引擎 ： Google/百度/Bing
* 网络抓包 ：Tcpdump/Wireshark/Fiddler
* 开发工具：IDEA/Visual Stutio/Vs Code
* 数据库管理：PLSQL Developer/Mysql Workbench/DBeaver/DataGrip
* Redis管理：Redis Desktop Manager
* Vpn: OpenVpn/Shadowsocks
* Host文件 ： Switch Host
* 浏览器 ： Chrome/360
* 远程桌面 ： Window远程/TeamViewer/AnyDesk
* 版本管理 ： Git/SVN/TFS
* Linux终端 ： XShell/MobaXterm
