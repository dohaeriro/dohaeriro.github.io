---
created: 2020-09-14 14:00:00  
updated: 2020-09-18 17:38:00  
---

# Kubernetes 入门

## Kubernetes 架构

- [K8s基础概念和应用_01 K8s架构简介](_resources/K8s基础概念和应用_01.pdf)

## Kubernetes 概念

### Pods 

> Pod 是 K8S 中最重要也是最基本的概念，Pod 是最小的部署单元，是一组容器的集合。每个 Pod 都由一个特殊的根容器 Pause 容器，以及一个或多个紧密相关的用户业务容器组成。
>
> Pause 容器作为 Pod 的根容器，以它的状态代表整个容器组的状态。K8S 为每个 Pod 都分配了唯一的 IP 地址，称之为 Pod IP。Pod 里的多个业务容器共享 Pause 容器的IP，共享 Pause 容器挂载的 Volume。

- [K8s基础概念和应用_03 虚拟机抽象](_resources/K8s基础概念和应用_03.pdf)

### Workloads 工作负载

- 工作负载资源用于创建和管理 Pods，拥有控制器
- 使用 Pod 模板，是一种包含在工作负载对象中的规范

### Dashboard Web 界面

> K8S 提供了一个 Web 版 Dashboard，用户可以用 dashboard 部署容器化的应用、监控应用的状态，能够创建和修改各种 K8S 资源，比如 Deployment、Job、DaemonSet 等。用户可以 Scale Up/Down Deployment、执行 Rolling Update、重启某个 Pod 或者通过向导部署新的应用。Dashboard 能显示集群中各种资源的状态以及日志信息。Kubernetes Dashboard 提供了 kubectl 的绝大部分功能。

- web 界面是对 kubectl 的可视化
- Dashboard 是 Kubernetes 官方原生 web 界面
- GKE 的可视化操作也是一种第三方 web 界面
- GF 的 Eagle 平台也是一种第三方 web 界面

### Namespace 名字空间

物理集群下的虚拟集群
