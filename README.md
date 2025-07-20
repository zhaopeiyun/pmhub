[//]: # (<p align="center"><img src= "https://cdn.tobebetterjavaer.com/stutymore/pmhub_%E7%AE%80%E4%BB%8B%E7%89%88.png" alt="MaxKB" width="300" /></p>)
<h3 align="center">PmHub，一个基于 SpringCloud & LLM 的智能项目管理系统</h3>

[//]: # (<p align="center">)

[//]: # (  <a href="https://opensource.org/license/MIT"><img src="https://img.shields.io/github/license/laigeoffer/pmhub?color=rgb&#40;25%2C%20121%2C%20255&#41;" alt="The MIT License"></a>)

[//]: # (  <a href=""><img src="https://img.shields.io/github/forks/laigeoffer/pmhub?color=green" alt="Forks"></a>)

[//]: # (  <a href="https://laigeoffer.cn/"><img src="https://img.shields.io/badge/PmHub-%E5%AE%98%E7%BD%91-green" alt="Official"></a>)

[//]: # (  <a href="https://github.com/laigeoffer/pmhub"><img src="https://img.shields.io/github/stars/laigeoffer/pmhub?style=flat-square&color=rgb&#40;25%2C%20121%2C%20255&#41;" alt="Stars"></a>    )

[//]: # (  <a href="https://pmhub.laigeoffer.cn/"><img src="https://img.shields.io/badge/PmHub-%E4%BD%93%E9%AA%8C%E5%9C%B0%E5%9D%80-blue" alt="Experience"></a>  )

[//]: # (</p>)

<hr/>
PmHub 是一套基于 SpringCloud & LLM 的微服务智能项目管理系统。

[//]: # ()
[//]: # (## 项目亮点)

[//]: # ()
[//]: # (- **热门技术**：采用时下企业最热门的技术框架，如 SpringCloud-Gateway、Nacos、Sentinel 等，主打一个硬核，与真实的企业项目接轨。)

[//]: # (- **单体与微服务**：提供单体和微服务两个版本，完美照顾零基础和需要进阶的同学，带大家体验从单体到微服务架构的改造全过程，并深入理解两种架构的优缺点。)

[//]: # (- **硬核面试题**：我们将结合付费球友的实际面试体验，为大家提供可以真正吊打面试官的真是面试场景和题目，并提供 1v1 的简历修改服务，主打一个投了就有、面了就拿 offer 的快乐体感。)

[//]: # (- **代码质量**：由蚂蚁金服工作过的技术专家苍何亲自下场，严格遵循代码规范和最佳实践，帮大家养成优雅的代码编写习惯。)

[//]: # (- **持续集成**：提供持续集成和持续部署的完整配置，带你从 0-1 用 Docker 上线 生产环境级别的真实项目。)

[//]: # (- **产品设计**：[提供完整的产品设计文档]&#40;https://lanhuapp.com/link/#/invite?sid=qxZji4oa&#41;，包括产品需求、产品架构、产品原型等，这是别的项目不曾给你的，但工作后又不可或缺的能力。)

[//]: # (- **企业工作流**：提供企业级的工作流系统，代码完全开源，你可以在此基础上进行二开，为公司节省巨额的研发成本，从而升职加薪。)

[//]: # ()

## 一、项目简介

PmHub 包括认证、流程、项目管理、用户、网关等服务。包含了 Redis 缓存、RocketMQ 消息队列、Docker 容器化、Jenkins 自动化部署、Spring Security 安全框架、Nacos 服务注册和发现、Sentinel 熔断限流、Seata 分布式事务、Spring Boot Actuator 服务监控、SkyWalking 链路追踪、OpenFeign 服务调用，Vue3 前端框架等互联网开发中需要用到的主流技术栈，可以帮助同学们快速掌握微服务/分布式项目的核心知识点。

并且同时 PmHub 也是一套企业工作流的开发框架，您可以根据自身需求，快速定制出适合自己公司的企业工作流系统。


我已经推出两个版本：
- 单体架构版本：适合初学者，直接运行 pmhub-boot 模块下的 pmhub-admin 中的 PmhubApplication 类即可。
- 微服务架构版本：适合有一定基础，想进阶学习微服务/分布式的同学，可以分别启动网关、认证、流程、项目管理、代码生成等多个服务。

![pmhub-业务架构图](https://cdn.tobebetterjavaer.com/stutymore/laigeoffer-pmhub-%E4%B8%9A%E5%8A%A1%E5%A4%A7%E5%9B%BE.png)

## 二、项目详情
### 2.1、技术架构

下面这张系统架构图可以帮助大家快速了解 PmHub 项目的系统架构，从前端到网关、从服务应用到基础服务组件、从存储技术到运维部署，可以说是一目了然。

![pmhub-系统架构图](https://cdn.tobebetterjavaer.com/stutymore/01.什么是PmHub-20240708113736.png)

下面这张架构选型图可以帮助大家快速了解 PmHub 项目的技术选型

![pmhub-架构选型](https://cdn.tobebetterjavaer.com/stutymore/PmHub%E6%9E%B6%E6%9E%84%E9%80%89%E5%9E%8B.png)

下面这张技术架构图可以帮助大家快速了解 PmHub 项目的技术架构，以及各个模块之间的交互关系。

![pmhub-技术架构图](https://cdn.tobebetterjavaer.com/stutymore/01.什么是PmHub-20240702103552.png)

优质的项目，离不开一张清晰的鸟瞰图（😄）。

### 2.2、代码展示
![pmhub代码展示](https://cdn.tobebetterjavaer.com/stutymore/20240529152747.png)

### 2.3、代码结构

```
com.laigeoffer.pmhub     
├── pmhub-ui              // 前端框架 [1024]
├── pmhub-gateway         // 网关模块 [6880]
├── pmhub-auth            // 认证中心 [6800]
├── pmhub-api             // 接口模块
│       └── pmhub-api-system                          // 系统接口
│       └── pmhub-api-workflow                        // 流程接口
├── pmhub-base          // 通用模块
│       └── pmhub-base-core                           // 核心模块组件
│       └── pmhub-base-datasource                     // 多数据源组件
│       └── pmhub-base-seata                          // 分布式事务组件
│       └── pmhub-base-security                       // 安全模块组件
│       └── pmhub-base-swagger                        // 系统接口组件
│       └── pmhub-base-notice                         // 消息组件组件
├── pmhub-modules         // 业务模块
│       └── pmhub-system                              // 系统模块 [6801]
│       └── pmhub-gen                                 // 代码生成 [6802]
│       └── pmhub-job                                 // 定时任务 [6803]
│       └── pmhub-project                             // 项目服务 [6806]
│       └── pmhub-workflow                            // 流程服务 [6808]
├── pmhub-monitor             						  // 监控中心 [6888]                 
├──pom.xml                                            // 公共依赖
```

## 三、项目部署
> 单体版本请参考：[单体版本部署手册](https://github.com/laigeoffer/pmhub/blob/master/docs/%E6%9C%8D%E5%8A%A1%E5%99%A8%E5%90%AF%E5%8A%A8%E6%95%99%E7%A8%8B.md)
### 3.1、环境准备
|    | 技术                  | 名称        | 版本         | 官网                                                                                                 |
|----|---------------------|-----------|------------|----------------------------------------------------------------------------------------------------|
| 1  | Spring Boot         | 基础框架      | 2.7.18     | [https://spring.io/projects/spring-boot](https://spring.io/projects/spring-boot)                   |
| 2  | SpringCloud         | 微服务框架     | 2021.0.8   | [https://spring.io/projects/spring-cloud](https://spring.io/projects/spring-cloud)                 |
| 3  | SpringCloud Alibaba | 阿里微服务框架   | 2021.0.5.0 | [https://github.com/alibaba/spring-cloud-alibaba](https://github.com/alibaba/spring-cloud-alibaba) |
| 4  | SpringCloud Gateway | 服务网关      | 3.1.8      | [https://spring.io/projects/spring-cloud-gateway](https://spring.io/projects/spring-cloud-gateway) |
| 5  | MyBatis-Plus        | 持久层框架     | 3.5.1      | [https://baomidou.com](https://baomidou.com)                                                       |
| 6  | Redis               | 分布式缓存数据库  | Latest     | [https://redis.io](https://redis.io)                                                               |
| 7  | RocketMQ            | 消息队列      | 2.2.3      | [https://rocketmq.apache.org](https://rocketmq.apache.org)                                         |
| 8  | HuTool              | 小而全的工具集项目 | 5.8.11     | [https://hutool.cn](https://hutool.cn)                                                             |
| 9  | Maven               | 项目构建管理    | 3.9.1      | [http://maven.apache.org](http://maven.apache.org)                                                 |
| 10 | Sentinel            | 流控防护框架    | 1.8.6      | [https://github.com/alibaba/Sentinel](https://github.com/alibaba/Sentinel)                         |
| 11 | Java                | 开发版本      | 1.8        | [https://www.oracle.com/java/technologies](https://www.oracle.com/java/technologies)               |



### 3.2、后端项目启动

#### 第一步，下载项目源码

[//]: # ()
[//]: # (![]&#40;https://cdn.tobebetterjavaer.com/images/20240324/27136b6558d84edb861461ca5452021d.png&#41;)

#### 第二步，使用 Intellij IDEA 导入项目

![](https://cdn.tobebetterjavaer.com/stutymore/20240601234905.png)
#### 第三步，导入数据库

推荐大家使用 [Navicat](https://javabetter.cn/nice-article/itmind/navicatmacyjpx.html) 这款图形化数据库管理工具。


数据库文件路径在 pmhub/sql/,在Navicat中导入所有数据库文件（每一个微服务对应一个数据库）

![](https://cdn.tobebetterjavaer.com/stutymore/20240629223138.png)

可以直接右键在 terminal 终端中打开，然后通过 pwd 和 ls 命令查看文件的绝对路径。

![](https://cdn.tobebetterjavaer.com/images/20240324/24f0cbafe1fb4995827015c294196eb2.png)

拿到绝对路径后，就可以在 Navicat 中导入数据库文件了。

![](https://cdn.tobebetterjavaer.com/images/20240324/aa4cb8f705aa4f46a7d4835c9d26a596.png)

导入完成后，刷新一下就可以看到最新的数据库表了。
（当然你也可以直接复制sql，然后在Navicat执行）

#### 第四步，基础环境准备
* 1、启动 MySQL（必须）

可以选择本机直接安装 MySQL，也可以通过 Docker 的方式，但需要做好磁盘挂载，推荐本机安装！


* 2、启动 Redis（必须）

①、如果你是 macOS 用户，可以直接在终端输入`redis-server`启动 Redis。

![](https://cdn.tobebetterjavaer.com/images/README/1711692102829.png)

②、如果你是 Windows 用户，可以直接双击 redis-server.exe 启动 Redis。

③、当然也可以直接通过 Docker 启动 Redis。
```shell
# 拉取 Redis 镜像:
docker pull redis
# 启动 Redis 容器:
docker run --name my-redis -d redis
```

* 3、启动 Nacos（必须）

[官网](https://nacos.io/download/nacos-server/)下载 Nacos，找到 /conf/application.properties 文件，修改数据库连接信息。可以直接复制 pmhub/docker/nacos/conf/application.properties 内容。

修改下数据库配置信息为你自己的数据库，本地启动可以把鉴权关了。

```
1. 如果数据库名也是 pmhub-nacos，那么只需要修改用户名和密码即可。
2. 如果用户名也是 root，那么只需要修改密码即可。
3. 如果密码也一样，那么就不需要修改了（不可能，绝对不可能这么巧😂）。
```

![修改nacos配置文件](https://cdn.tobebetterjavaer.com/stutymore/20240529173446.png)

①、如果你是 macOS 用户，可以直接在终端输入`sh startup.sh -m standalone`启动 Nacos。

②、如果你是 Windows 用户，可以直接双击 startup.cmd 启动 Nacos。

启动成功后访问 http://localhost:8848/nacos 即可看到 Nacos 控制台。默认用户名密码都是 nacos。

![nacos启动成功界面](https://cdn.tobebetterjavaer.com/stutymore/20240529173621.png)

* 4、启动 SkyWalking 分布式链路追踪（非必须）

参考手册：[SkyWalking 启动手册](https://laigeoffer.cn/pmhub/interview/skywalking/)

* 5、启动 Sentinel 分布式熔断和降级（非必须）

参考手册：[Sentinel 启动手册](https://laigeoffer.cn/pmhub/interview/feign-sentinel/)


* 6、启动 Seata 分布式事务（非必须）

参考手册：[Seata 启动手册](https://laigeoffer.cn/pmhub/interview/seata/)

* 7、启动 Rocketmq 消息队列（非必须）

参考手册：[Rocketmq 启动手册](https://laigeoffer.cn/pmhub/interview/rocketmq/)



#### 第五步，启动各个微服务

> 注意：如果遇到服务启动失败，可自行查看 nacos 配置是否做了修改，如数据库连接信息等。

①、启动 pmhub-gateway 网关服务

找到 pmhub-gateway 项目，右键 Run PmHubGatewayApplication.main()。

![pmhub-gateway启动成功](https://cdn.tobebetterjavaer.com/stutymore/20240529174025.png)

②、启动 pmhub-auth 认证服务

找到 pmhub-auth 项目，右键 Run PmHubAuthApplication.main()。

③、启动 pmhub-system 系统服务

找到 pmhub-system 项目（在pmhub-modules 下），右键 Run PmHubSystemApplication.main()。
pmhub-system 启动前需要修改 nacos 中的 pmhub-system-dev.yml 配置文件，修改数据库连接信息为你自己的数据库。


![修改pmhub-system配置](https://cdn.tobebetterjavaer.com/stutymore/img.png)

④、启动 pmhub-project 项目管理服务

找到 pmhub-project 项目（在pmhub-modules 下），右键 Run PmHubProjectApplication.main()。

启动前需要修改 nacos 中的 pmhub-project-dev.yml 配置文件，修改数据库连接信息为你自己的数据库。

⑤、启动 pmhub-workflow 流程管理服务

找到 pmhub-workflow 项目（在pmhub-modules 下），右键 Run PmHubWorkflowApplication.main()。

启动前需要修改 nacos 中的 pmhub-workflow-dev.yml 配置文件，修改数据库连接信息为你自己的数据库。

⑥、启动 pmhub-gen 代码生成服务

找到 pmhub-gen 项目（在pmhub-modules 下），右键 Run PmHubGenApplication.main()。

启动前需要修改 nacos 中的 pmhub-gen-dev.yml 配置文件，修改数据库连接信息为你自己的数据库。

⑦、启动 pmhub-job 定时任务调度服务

找到 pmhub-job 项目（在pmhub-modules 下），右键 Run PmHubJobApplication.main()。

启动前需要修改 nacos 中的 pmhub-job-dev.yml 配置文件，修改数据库连接信息为你自己的数据库。

⑧、启动 pmhub-monitor 监控服务

找到 pmhub-monitor 项目，右键 Run PmHubMonitorApplication.main()。

启动前需要修改 nacos 中的 pmhub-monitor-dev.yml 配置文件，修改监控后台的用户名和密码，以及首页展示标题。

启动成功后可访问：http://localhost:6888/wallboard

可以在线实时查案各个服务的状态以及日志：

![主界面](https://cdn.tobebetterjavaer.com/stutymore/image.webp)




### 3.3、前端项目启动

请参考 pmhub-ui 项目的 README.md 文档，[前端工程结构说明](pmhub-ui/README.md)

> 注意：微服务版本直接启动 pmhub-ui 即可，如果是单体版本的前端需要到 pmhub-boot下的 pmhub-ui 启动。

### 3.4、在线接口文档

[https://laigeoffer.cn/pmhub/api-doc.html](https://laigeoffer.cn/pmhub/api-doc.html)

### 3.5、服务器部署（Docker 方式）

请参考 [云容器部署系统](https://laigeoffer.cn/pmhub/quickstart/docker/)

## 四、技术选型

后端技术栈

|         技术          | 说明                   | 官网                                                                                                                         |
|:-------------------:|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Spring & SpringMVC  | Java全栈应用程序框架和WEB容器实现 | [https://spring.io/](https://spring.io/)                                                                                   |
|     SpringBoot      | Spring应用简化集成开发框架     | [https://spring.io/projects/spring-boot](https://spring.io/projects/spring-boot)                                           |
|     SpringCloud     | 微服务框架                | [https://spring.io/projects/spring-cloud](https://spring.io/projects/spring-cloud)                                         |
|    mybatis-plus     | 数据库orm框架             | [https://baomidou.com/](https://baomidou.com/)                                                                             |
| mybatis PageHelper  | 数据库翻页插件              | [https://github.com/pagehelper/Mybatis-PageHelper](https://github.com/pagehelper/Mybatis-PageHelper)                       |
|    elasticsearch    | 近实时文本搜索              | [https://www.elastic.co/cn/elasticsearch/service](https://www.elastic.co/cn/elasticsearch/service)                         |
|        redis        | 内存数据存储               | [https://redis.io](https://redis.io)                                                                                       |
|      rocketmq       | 消息队列                 | [https://rocketmq.apache.org/](https://rocketmq.apache.org/)                                                               |
|       mongodb       | NoSql数据库             | [https://www.mongodb.com/](https://www.mongodb.com/)                                                                       |
|        nginx        | 服务器                  | [https://nginx.org](https://nginx.org)                                                                                     |
|       docker        | 应用容器引擎               | [https://www.docker.com](https://www.docker.com)                                                                           |
|      hikariCP       | 数据库连接                | [https://github.com/brettwooldridge/HikariCP](https://github.com/brettwooldridge/HikariCP)                                 |
|         oss         | 对象存储                 | [https://help.aliyun.com/document_detail/31883.html](https://help.aliyun.com/document_detail/31883.html)                   |
|        https        | 证书                   | [https://letsencrypt.org/](https://letsencrypt.org/)                                                                       |
|         jwt         | jwt登录                | [https://jwt.io](https://jwt.io)                                                                                           |
|       lombok        | Java语言增强库            | [https://projectlombok.org](https://projectlombok.org)                                                                     |
|        guava        | google开源的java工具集     | [https://github.com/google/guava](https://github.com/google/guava)                                                         |
|      thymeleaf      | html5模板引擎            | [https://www.thymeleaf.org](https://www.thymeleaf.org)                                                                     |
|       swagger       | API文档生成工具            | [https://swagger.io](https://swagger.io)                                                                                   |
| hibernate-validator | 验证框架                 | [hibernate.org/validator/](hibernate.org/validator/)                                                                       |
|     quick-media     | 多媒体处理                | [https://github.com/liuyueyi/quick-media](https://github.com/liuyueyi/quick-media)                                         |
|      liquibase      | 数据库版本管理              | [https://www.liquibase.com](https://www.liquibase.com)                                                                     |
|       jackson       | json/xml处理           | [https://www.jackson.com](https://www.jackson.com)                                                                         |
|      ip2region      | ip地址                 | [https://github.com/zoujingli/ip2region](https://github.com/zoujingli/ip2region)                                           |
|      websocket      | 长连接                  | [https://docs.spring.io/spring/reference/web/websocket.html](https://docs.spring.io/spring/reference/web/websocket.html)   |
|   sensitive-word    | 敏感词                  | [https://github.com/houbb/sensitive-word](https://github.com/houbb/sensitive-word)                                         |
|       chatgpt       | chatgpt              | [https://openai.com/blog/chatgpt](https://openai.com/blog/chatgpt)                                                         |
|        讯飞星火         | 讯飞星火大模型              | [https://www.xfyun.cn/doc/spark/Web.html](https://www.xfyun.cn/doc/spark/Web.html#_1-%E6%8E%A5%E5%8F%A3%E8%AF%B4%E6%98%8E) |


