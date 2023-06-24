+++
title = "Linux 101"
outputs = ["Reveal"]

[reveal_hugo]
theme = "simple"

[logo]
src = "/shuosc.webp"
width = "7%" # Overrides diag.
+++

# Linux 101

by [SHUOSC](https://shuosc.org)

---

{{% section %}}

## 宗旨目标

- 以爆款 C++ 开源项目为抓手
- 快速上手 Linux 下编程开发
  - 编译构建 C/C++ 项目
  - 现代集成开发环境 VS Code
  - Git 的基本操作流程
- 任务驱动、即时反馈和场景化设计

---

## 配置准备

- 安装方式：虚拟机，实体机，WSL，服务器 均可
- 硬件要求: 2 Core, 2GB RAM, 5GB Disk
- 准备好搜索引擎、发行版 wiki 或 AI问答助手

{{% /section %}}

---

{{% section %}}

## Linux 日用软件速览

本节所介绍软件均可在常见发行版上用包管理器安装

---

### 命令行终端 [Konsole](https://konsole.kde.org/) 和 [Yakuake](https://apps.kde.org/zh-cn/yakuake/)

![konsole](https://konsole.kde.org/assets/img/konsolefancy.png)

---

### 文件管理器 [Dolphin](https://apps.kde.org/zh-cn/dolphin/)

![dolphin-terminal](https://cdn.kde.org/screenshots/dolphin/dolphin-terminal.png)

---

### 终端文件管理器 [ranger](https://github.com/ranger/ranger)

![ranger](https://raw.githubusercontent.com/ranger/ranger-assets/master/screenshots/multipane.png)

---

### 文档查看器 [Okular](https://apps.kde.org/zh-cn/okular/)

![okular](https://cdn.kde.org/screenshots/okular/okular-annotation.png)

---

### 跨平台设备互连软件[KDE Connect](https://apps.kde.org/zh-cn/kdeconnect/)

![kde-connect](https://cdn.kde.org/screenshots/kdeconnect/kcm.png)

{{% /section %}}

---

{{% section %}}

## 小目标：从源码编译[Bitcoin Core](https://bitcoincore.org/)

---

### 拉取源码（5min）

- 用包管理器安装 Git
- `git clone https://github.com/bitcoin/bitcoin`
- 网络不好可用[Gitee镜像](https://gitee.com/mirrors/bitcoin)

思考：
- `git clone` 跟下载 zip 文件有什么区别？
- 为什么我 `git clone` 走 https 这么慢？

---

### 安装依赖（5min）

- 编译工具链：
  - Deb系: `apt install build-essential`
  - Arch Linux: `pacman -S base-devel`
- 查看 [`doc/build-unix.md`](https://github.com/bitcoin/bitcoin/blob/master/doc/build-unix.md) 中 [Linux Distribution Specific Instructions](https://github.com/bitcoin/bitcoin/blob/master/doc/build-unix.md#linux-distribution-specific-instructions)

思考：
- Linux发行版的包管理器将软件安装到哪了？
- 为什么要 `sudo`？

---

### 传统功夫，三步编译（15min）

1. `./autogen.sh`
2. `./configure`
3. `make`
    - `-j <任务数量>` 多核并行编译
    - `bear -- make` 生成 `compile_commands.json` 后面有用

思考：
- 这三步分别做了什么？
- 有更现代的方案吗？

---

### 安装到位（5min）

- `make install` 报错？使用 `sudo`
- 尝试运行 `bitcoin-cli`，`bitcoind` 并退出

思考：
- 安装了哪些可执行程序到哪里？
- 程序安装路径是什么时候指定的？

{{% /section %}}

---

{{% section %}}

## 小目标：使用[VS Code](https://code.visualstudio.com/)搭建C++开发环境

---

### 安装并体验[VS Code](https://code.visualstudio.com/)（15min）

- 官网可以下载 deb/rpm/tarball 手动安装
- 推荐添加软件源并通过包管理器安装
- [Arch Linux 安装方式](https://wiki.archlinux.org/title/Visual_Studio_Code)
  - `pacman -S code` 纯开源版，不含微软专有组件
  - AUR: [visual-studio-code-bin](https://aur.archlinux.org/packages/visual-studio-code-bin/)
  - 添加 [arch4edu](https://mirrors.tuna.tsinghua.edu.cn/help/arch4edu/) 源，`pacman -S visual-studio-code-bin`

思考：
- 使用包管理器相比网上下载安装包有那些优势？
- 为什么官方软件源不自带 VS Code？

---

### 安装并体验VS Code扩展（10min）

- `clangd`: C/C++ 静态检查、代码补全、跳转定义等
- `Remote Development`：使用 SSH，WSL，Docker 进行开发
- `CodeLLDB`: 方便调试C++程序
- `GitLens`: 方便进行Git版本控制操作

{{% /section %}}

---

{{% section %}}

## 小目标：使用Git为Bitcoin创建分叉

---

### 修改 Bitcoin 的参数创建新币种


在 [PR#26177](https://github.com/bitcoin/bitcoin/pull/26177) 之后，比特币的区块链参数从 [src/chainparams.cpp](https://github.com/bitcoin/bitcoin/blob/master/src/chainparams.cpp) 移到了 [src/kernel/chainparams.cpp](https://github.com/bitcoin/bitcoin/blob/master/src/kernel/chainparams.cpp)，修改 `CMainParams` 类中的变量即可创建新的加密货币


参考（注意时效性）：
- [Complete Guide on How to Create a New Alt Coin](https://bitcointalk.org/index.php?topic=3345808.msg35016844)
- [How to fork Bitcoin](https://medium.com/@jordan.baczuk/how-to-fork-bitcoin-c39139506443)
- [How to fork Bitcoin and create your own Blockchain?](https://motion-software.com/blog/how-to-create-your-own-blockchain-network-from-bitcoin)

---

### Git 本地操作

- `git checkout -b <名称>` 创建并切换到新分支
- 修改代码后 `git add <对应文件>` 添加其到暂存区
- `git commit` 提交更改记录

提示：可使用 VS Code 自带的图形界面进行版本控制

---

### GitHub 远程操作

- 创建全新仓库或 `Fork` [bitcoin/bitcoin](https://github.com/bitcoin/bitcoin)
- `git remote add <名称> <地址>` 添加远程仓库
- `git push <远程> <分支名>` 推送到远程仓库
- 如 Fork 原仓库则可在网页端创建 Pull Request 请求贡献代码到上游

思考：Git Branch，仓库的 Fork 和比特币的分叉，三者之间有何关系？

{{% /section %}}

---

{{% section %}}

## 扩展阅读
- [USTCLUG Linux 101讲义](https://101.lug.ustc.edu.cn/)
- [计算机教育中缺失的一课](https://missing-semester-cn.github.io/)

{{% /section %}}
