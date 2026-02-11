# Shadowsocks-Go 一键管理脚本

一个简洁而强大的 Shadowsocks-Go 版一键管理脚本。支持自动化安装、配置修改、状态监控及日志查看。

## 🚀 主要功能

* **一键操作**：自动化安装、卸载、更新 Shadowsocks-Go。
* **配置灵活**：支持在线修改端口、密码、加密方式（包括 AEAD 加密）。
* **服务管理**：一键启动、停止、重启服务，并自动配置 `init` 系统服务。
* **智能监控**：内置 Crontab 监控功能，进程意外退出时自动拉起。
* **连接详情**：支持查看当前连接 IP 数量及 IP 归属地。
* **防火墙自动化**：自动配置 `iptables` / `ip6tables` 规则，支持 IPv6。
* **快速分享**：安装完成后自动生成 SS 链接与二维码。

## 📋 系统要求

* **操作系统**：CentOS 6+ / Debian 8+ / Ubuntu 14.04+
* **架构**：目前脚本主要支持 `x86_64` 架构。
* **权限**：需要 `root` 用户执行。

## 🛠️ 安装与使用

### 1. 下载并运行

在终端输入以下命令：

```bash
wget -N --no-check-certificate "https://github.com/dow-ma/Shadowsocks-Go/releases/download/1.0.0/install.sh" && chmod +x install.sh && ./install.sh
```

### 2. 脚本菜单说明

运行脚本后，你将看到以下菜单：

| 编号 | 功能说明 | 描述 |
| --- | --- | --- |
| **1** | 安装 Shadowsocks | 自动下载、配置并启动 |
| **7** | 设置 账号配置 | 修改端口、密码、加密方式或日志模式 |
| **8** | 查看 账号信息 | 显示当前的 SS 链接、二维码及配置详情 |
| **10** | 查看 链接信息 | 查看当前连接的 IP 列表及归属地 |
| **0** | 升级脚本 | 从 GitHub 获取最新版本的管理脚本 |

## ⚙️ 加密方式支持

脚本集成了多种加密方式，推荐使用 **AEAD** 加密以获得更好的安全性：

* `aead_chacha20_poly1305` (默认)
* `aes-256-gcm` / `aes-128-gcm`
* `chacha20-ietf` / `xchacha20`
* 以及传统的 `aes-cfb` / `aes-ctr` 系列

## 📂 文件路径

* **安装目录**：`/usr/local/shadowsocks-go`
* **配置文件**：`/usr/local/shadowsocks-go/shadowsocks-go.conf`
* **日志文件**：`/usr/local/shadowsocks-go/shadowsocks-go.log`

---

## 📝 免责声明

本脚本仅供学习交流使用，请勿用于非法用途。在使用过程中请遵守当地法律法规。

## 🤝 鸣谢

* Shadowsocks-Go 核心项目：[shadowsocks/go-shadowsocks2](https://github.com/shadowsocks/go-shadowsocks2)
* 原始脚本思路：Toyo
