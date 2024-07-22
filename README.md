# 镜子联ban计划

## 主要目标

通过将不同mirror服务器的日志上传到中心服务器,经集中分析后,形成一个对于某些ip段有危险度标识的列表。该列表代表不同ip段对各镜像站机器攻击的可能性及威胁程度,此列表下发至各服务器后，各服务器可自行采取措施对指定ip段进行限速或封禁。

统一日志分析好能展望一下，分析各个 repo 的访问量、配额 mirrorz 的自动负载均衡 ，防止某些站累死某些站饿死


## 可能的日志分析算法

对于某个 IP 或 IP 段的请求来说，对于包的访问应该是集中的。类似于大模型中提到的向量距离，单独用户对于镜像站的访问应该是聚集成一个或某几个球状区域。如果有大量分散式的均匀访问即判定可能为分散式刷流

如果某个用户对不同镜像站请求了大量相同包，是否可以判定为刷流？



## 可能的刷流算法

比如用上千种ua刷几十万个文件 每个文件就访问几次



## 可能的问题

假如某高校 NAT 网很大，出口 IP 较少，可能会被误判

对于 IP 段的波动如何处理，按时间封禁可能的问题