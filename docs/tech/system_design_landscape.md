# System Design Landscape

## 静态资源加速

### 1，CDN（Content Delivery Network）

CDN 是分布式部署的，它将内容存储在多个地理位置的服务器上。当用户请求某个内容时，CDN 会根据用户的所在位置，将请求发送到距离用户最近的服务器。这样可以提高用户访问内容的速度和可靠性。

- CDN 服务商均由各云平台供应商提供。
- 应用于网站加速，流媒体加速等。
- 使用到路由，隧道，传输等网络技术，分布式存储等存储技术，以及各种调度算法，如基于距离的最短路径算法，基于负载的响应时间优先算法，以及基于成本或其它智能调度算法。

## 域名负载均衡

> 域名负载均衡是指通过域名解析技术，将域名解析到多个服务器上，从而实现用户请求的负载均衡。域名负载均衡可以提高网站或应用的访问速度、可用性和可扩展性。
>
> > 实现技术包括：
> >
> > - DNS 轮询：在 DNS 解析服务器上配置多个服务器的 IP 地址，按照一定的顺序将用户请求分发到这些服务器上。
> > - 权重轮询：在 DNS 解析服务器上配置多个服务器的 IP 地址和权重，按照权重的大小将用户请求分发到这些服务器上。
> > - 随机分发
> > - 哈希分发：在 DNS 解析服务器上配置多个服务器的 IP 地址，根据用户请求的某个属性（如 IP 地址或用户 ID）进行哈希计算，将用户请求分发到对应的服务器上。

### 1，硬件负载均衡

- F5 是一家提供负载均衡产品和服务的公司，其产品包括 BIG-IP 系列。BIG-IP 产品可以实现多种负载均衡功能，包括域名负载均衡。
- Citrix ADC，formerly known as Citrix NetScaler, is a line of products that are application delivery controllers (ADCs)
  > - Advanced Layer 4 (L4) load balancing
  > - Layer 7 (L7) traffic management

### 2，软件负载均衡

- Nginx
- [HAProxy](https://www.haproxy.org/){:target="\_blank"}：一个免费的、开源的、高性能的、可靠的、易于使用的代理和负载均衡器。
- LVS：Linux 虚拟服务器（LVS）是一个开源的、高性能的负载均衡软件，它可以用于将用户请求分发到多个后端服务器上。LVS 工作在网络层(L3)，可以实现高性能、高可用性的负载均衡。[中文文档](http://www.linuxvirtualserver.org/zh/index.html){:target="\_blank"}，[参考资料](https://superproxy.github.io/docs/lvs/index.html){:target="\_blank"}

### 3，云负载均衡器

- AWS Elastic Load Balancing
- Azure Load Balancing

---

**下述所有内容均需要罗列相应的技术选型方案**

---

## 后端系统架构

### 微服务架构

### 服务网格

### 容器化

- 云原生
- Docker
- K8S

## 前端系统架构

### SPA（Single Page Application）

### MPA（Multi-Page Application）

### 技术选型

## API 网关

### 负载均衡

### 限流和熔断

## 注册中心

## 配置中心

## 链路追踪

## 监控和告警

### 系统监控

### 日志系统

### 告警

## 鉴权

### Basic Auth

### OAuth

### JWT

### RBAC

## 服务间通信

### HTTP

### RPC

### MQ

### Websocket

## 数据存储

### DB 类型

### 存储架构

- 主从
- 集群

### 事物和分布式事物

### 大数据

#### 存储

#### 检索

- 事物特性
- 分布式事物

## 性能和调优

### 性能测试

### 系统调优

#### 缓存

### 高并发

### 批处理

## 锁和安全

### 分布式锁

### TSL/SSL

### 安全检测

## CI（Continuous Integration）

> CI 是指开发人员在每次提交代码后，自动化地将代码构建、测试和部署到一个预定的环境中。CI 的目的是尽早发现代码中的错误，并确保代码的质量。

### Package

#### 代码风格检测

#### 代码质量检测

### Test

#### 方法论

#### 自动化测试

#### 单元测试报告

### Repository

## CD（Continuous Delivery）

> CD 是指将持续集成的结果自动化地部署到生产环境中。CD 的目的是让软件能够更频繁地、更可靠地交付给用户。

### 方法论

- 蓝绿部署
- 灰度部署

### 工具链

- Jenkins
- Ansible

## 基建和 Cost 计算

### Cost 方法论和系统基建选型

### 系统基建安装和运维

## 软件开发模型

### 敏捷方法论

#### Scrum

#### Kanban

#### DevOps

### 管理方法论

#### Team 目标管理

#### 向上管理（领导预期管理）
