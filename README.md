# xingchen-lab-assets

星辰 App「实验室」运行环境包仓库（公开）。

`env/` 目录下是 11 种 Android arm64 运行环境包（zip），由星辰 App 内「实验室」页下载安装：

| 环境 | 包 | 版本 | 大小 |
|---|---|---|---|
| Python 环境 | env-python.zip | 3.14.8 | ~14 MB |
| Node 环境 | env-node.zip | 26.4.0 | ~52 MB |
| PHP 环境 | env-php.zip | 8.5.1 | ~49 MB |
| mihomo | env-mihomo.zip | 1.19.30 | ~18 MB |
| alist | env-alist.zip | 3.63.0 | ~44 MB |
| frp | env-frp.zip | 0.71.0 | ~13 MB |
| aria2 | env-aria2.zip | 1.37.0 | ~2.5 MB |
| Ubuntu 环境 | env-ubuntu.zip | 24.04.4 | ~42 MB |
| Java 环境 | env-java.zip | 17.0.20 | ~66 MB |
| Bun 环境 | env-bun.zip | 1.4.3 | ~39 MB |
| ffmpeg | env-ffmpeg.zip | 5.1 | ~8.7 MB |

包格式：zip 解压后根目录带 `bin/`（可执行文件与 .so），与 App 内 `LabRuntimeManager` 的安装校验对齐。

来源：mihomo/alist/frp/aria2/bun 取各官方 Release；python/node/php/java 取 Termux 官方包重打包（arm64）；ubuntu 取 Ubuntu 官方 `ubuntu-base-24.04.4-base-arm64`；ffmpeg 取第三方预编译（NotAHero04）。

注意：Ubuntu 包目前仅为 rootfs 备包，App 侧 proot 接入未完成，暂不可安装。
