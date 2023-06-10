+++
title = "Linux Install Party"
outputs = ["Reveal"]

[reveal_hugo]
theme = "white"

[logo]
src = "/shuosc.webp"
width = "7%" # Overrides diag.
+++

# <span style="text-transform: none;">Linux Install Party</span>

by [SHUOSC](https://shuosc.org)

---

{{% section %}}

## 声明

事实上，Linux 指的是一个操作系统的内核，而Linux 一般和 GNU 操作系统一起使用：整个系统基本上就是 GNU 加上 Linux，或叫 GNU/Linux。

所有被叫做“Linux”的发行版实际上是 GNU/Linux 发行版。

{{% /section %}}

---

{{% section %}}

## <span style="text-transform: none;">为什么选择 Linux</span>

---

### 开源自由

Linux 是开源的，你可以自由地使用、复制、分发、学习、修改 Linux

---

### 安全稳定

由于 Linux 的开源性质，任何人都可以查看源代码，发现并修复漏洞

> Given enough eyeballs, all bugs are shallow. 
>   —— Linus' Law

---

### 轻量高效

- 遵循 [UNIX 哲学](https://zh.wikipedia.org/wiki/Unix%E5%93%B2%E5%AD%A6)“小即是美”
- 系统占用资源少，这使得 Linux 硬件下限极低
- 让你的老电脑焕发第二春

---

### 适合程序员

- 强大的命令行
- 方便的包管理器（apt, pacman...）
- 详细的报错提示和日志信息
- 接近实际服务器环境

---

### 自定义程度高

- 自定义内核(zen, lts, xanmod...)
- 自定义桌面环境(GNOME, KDE, XFCE, i3wm...)
- 自定义一切，理论上你可以自由修改 Linux 的任何开源代码并编译安装，~~让她彻底变成你的形状~~

---

### <span style="text-transform: none;">Linux 应用实例</span>

- 服务器、超算
- 路由器
- Android
- ...

---

### 日常使用

- 办公学习
- 娱乐
- 开发
- ...

{{% /section %}}

---

{{% section %}}

## <span style="text-transform: none;">Linux 常见发行版介绍</span>

适合自己的才是最好的

---

![Linux Rank](img/LinuxRank.webp)

---
### ![Ubuntu](https://upload.wikimedia.org/wikipedia/commons/thumb/7/76/Ubuntu-logo-2022.svg/640px-Ubuntu-logo-2022.svg.png)

- 简单易上手，适合新手
- 基于 Debian，有着丰富软件源
- Canonical 公司运营，商业推广出色
- 群众基础广泛，有大量的教程和问答

---

### ![Debian](https://cdn.icon-icons.com/icons2/2699/PNG/512/debian_logo_icon_168290.png)

- 固若金汤，稳定性极强
- 坚守 UNIX 和自由软件的精神
- 支持众多计算机架构
- 众多发行版的直接上游或源头

---
### ![Arch Linux](https://upload.wikimedia.org/wikipedia/commons/thumb/e/e8/Archlinux-logo-standard-version.png/640px-Archlinux-logo-standard-version.png)

- 遵循 [KISS 原则](https://zh.wikipedia.org/wiki/KISS%E5%8E%9F%E5%88%99)，简单而高效，
- 滚动更新，永不过时
- 极其丰富的软件源和积极的社区支持
- [Arch Wiki](http://wiki.archlinux.org/) 是 Linux 社区最好的 Wiki
- 适合有 DIY 需求的用户，~~除了难装，其他都很简单~~
---

[![LinuxChoose](img/LinuxChoose.webp)](https://distrochooser.de/zh-hans)

---
### ![Manjaro](https://upload.wikimedia.org/wikipedia/commons/thumb/8/85/Manjaro_logo_text.svg/640px-Manjaro_logo_text.svg.png)

- 基于 Arch Linux，但安装更友好，适合新手
- 能使用大部分 Arch Linux 的软件源）
- 界面美观，自带驱动，可更换内核

---
### ![Fedora](https://upload.wikimedia.org/wikipedia/commons/thumb/8/8f/Fedora_logo_%282021%29.svg/640px-Fedora_logo_%282021%29.svg.png)

- 由 Red Hat 公司赞助，可看作 CentOS/RHEL 的上游
- 有着丰富的软件源
- Linus Torvalds 使用的发行版
- 适合有一定 Linux 基础的用户
---
### ![openSUSE](https://upload.wikimedia.org/wikipedia/commons/thumb/d/d0/OpenSUSE_Logo.svg/640px-OpenSUSE_Logo.svg.png)

- 新手友好，易于上手，有着优秀的桌面环境体验
- 特性丰富，YaST 以简便直接的形式控制系统的一切
- 坚如磐石，比较稳定，有社区和商业支持
---
### ![Deepin](https://wiki.deepin.org/deepin_logo_1.png)

- 国产 Linux 发行版，以美观易用著称
- 对国产应用以及中文支持友好
---
### ![Kali Linux](https://upload.wikimedia.org/wikipedia/commons/thumb/4/4b/Kali_Linux_2.0_wordmark.svg/640px-Kali_Linux_2.0_wordmark.svg.png)

- 专注于渗透测试，内置大量渗透工具
- ~~KALI 学得好，牢饭吃到饱~~

---
### ![Gentoo](https://www.gentoo.org/assets/img/logo/gentoo-horizontal.svg)

- 勤快一时，懒惰一世
- 适合对性能有极高要求的用户

---
### ![NixOS](https://upload.wikimedia.org/wikipedia/commons/thumb/c/c4/NixOS_logo.svg/640px-NixOS_logo.svg.png)

- 声明式配置，纯函数式包管理
- 原子化升级和回滚
- 易于复现系统环境，安全稳定
- 适合进阶用户

{{% /section %}}

---

{{% section %}}

## Linux 桌面环境速览

桌面环境=Desktop Environment(DE)

---

### Linux 桌面环境的特点

- 桌面环境可单独安装，独立于发行版
- 不同桌面环境风格各异，提供丰富的软件选择
- 稳定性在逐渐提升，完全满足日用需求

---

## GNOME

外观简洁，功能稍差

![GNOME](https://www.gnome.org/wp-content/uploads/2023/02/wgo-splash-40.webp)

---
## KDE

强大高效，设置丰富

![KDE](https://kde.org/announcements/plasma/5/5.27.0/fullscreen_with_apps.png)

---

## Xfce

朴实无华，资源消耗低

![Xfce](https://spins.fedoraproject.org/static/images/screenshots/screenshot-xfce.jpg)

{{% /section %}}

---

{{% section %}}

## <span style="text-transform: none;">Linux 安装的 N 种方式</span>

---

### 实体机安装

- 性能最好，体验最真实
- 需要对磁盘分区和系统启动方式有一定了解

---

### 虚拟机安装

- 无需重启
- 管理方便
- 隔离性好，安全稳定

---

### WSL 安装

- 性能损耗低
- 无需重启
- 与 Windows 无缝集成

---

### 容器安装

- 使用 Podman/Docker 等容器方案可以便捷创建轻量的 Linux 环境
- 借助 [Termux](https://f-droid.org/zh_Hans/packages/com.termux/) 和 proot/chroot 容器可以实现在 Android 等设备上运行 Linux 系统

```shell
. <(curl -L gitee.com/mo2/linux/raw/2/2)
```

{{% /section %}}

---

{{% section %}}

## Linux 用户遇到问题该怎么办？

---

### 自力更生

- RTFM: Read The Manual
- STFW: Search The Web

---

### 社区支持

[提问的智慧](https://lug.ustc.edu.cn/wiki/doc/smart-questions/)

- Linux User Group
  - USTCLUG
  - SJTUG
  - SHLUG
- Forum/BBS
- Telegram/QQ Group

{{% /section %}}

---

{{% section %}}

## <span style="text-transform: none;">Talk is cheap, Let's install Linux</span>

{{% /section %}}
