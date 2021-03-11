# 查看该项目的最新版本请移至[https://github.com/teamssix/tig](https://github.com/teamssix/tig)

# 0x00 介绍

tig `Threat Intelligence Gathering` 威胁情报收集，旨在提高蓝队拿到攻击 IP 后对其进行威胁情报信息收集的效率，目前已集成微步、IP 域名反查、Fofa 信息收集三个模块，现已支持对 IP 进行微步标签、地理位置、开放端口、域名反查等信息的查询。

后续将集成更多模块，如有新的建议或 Bug 欢迎与我反馈，我的微信号：teamssix_com

# 0x01 安装

需要 python3 环境以及`requests`模块支持

```
pip3 install requests
python3 tig.py
```

# 0x02 使用

工具命令如下：

```
-h HELP			查看帮助信息
-i IP       目标 IP
-f FILE     IP 文本，一行一个
-c CONFIG   指定配置文件，默认 ./config.ini
```

在开始使用工具之前，需要对配置文件进行配置，默认配置文件如下：

```
[Threat Intelligence]

# 微步威胁情报查询，查看 api 地址：https://x.threatbook.cn/nodev4/vb4/myAPI（每天 50 次的免费额度）
ThreatBook_enable = true
ThreatBook_api = ''

[IP Information]

# IP 反查，调用 http://api.webscan.cc/ 的 api，如果目标 IP 没有反查到域名，该项即使开启也不会有输出
ip_reverse_enable = true

# Fofa ip 信息查询，查看 api 地址：https://fofa.so/user/users/detail（付费，普通会员每次100条，高级会员每次10000条）
Fofa_enable = true
Fofa_email = ''
Fofa_api = ''
```

需要在配置文件里添加自己的微步 API 和 Fofa API 才可使用，添加后，就可以正常使用了，例如这里获取某个 IP 的信息，直接使用 -i 命令即可。

![](https://teamssix.oss-cn-hangzhou.aliyuncs.com/Snipaste_2021-03-10_13-26-06.png)

# 0x03 最后

如果在工具使用的过程中发现存在 bug 等问题，欢迎与我反馈，我的微信号：teamssix_com，同时也欢迎关注我的个人微信公众号：TeamsSix

![](https://teamssix.oss-cn-hangzhou.aliyuncs.com/TeamsSix_Subscription_Logo2.png)