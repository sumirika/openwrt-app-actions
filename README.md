# 中文 | [English](https://github.com/Siriling/openwrt-app-actions/blob/main/EngLish.md)

# 移动通信模组自动构建

[![Modem使用文档](https://img.shields.io/badge/使用文档-Modem-brightgreen?style=flat-square)](https://blog.siriling.com:1212/2023/03/18/openwrt-5g-modem) [![最新软件包下载](https://img.shields.io/github/v/release/Siriling/istoreos-actions?style=flat-square&label=最新软件包下载)](../../releases/latest)

![支持架构](https://img.shields.io/badge/支持架构:-blueviolet.svg?style=flat-square) ![X86](https://img.shields.io/badge/X86-blue.svg?style=flat-square) ![ARM](https://img.shields.io/badge/ARM-blue.svg?style=flat-square)

# 目录

[一、简介](#一简介)

[二、源代码地址 ](#二源代码地址)

[三、资源](#三资源)

[四、使用说明](#四使用说明)

# 一、简介

Modem插件自动构建

# 二、源代码地址

- luci-app-modem：https://github.com/Siriling/5G-Modem-Support/tree/main/luci-app-modem

- sms-tool：https://github.com/obsy/sms_tool
- quectel_cm_5G：https://github.com/Siriling/5G-Modem-Support/tree/main/quectel_cm_5G
- quectel_MHI：https://github.com/Siriling/5G-Modem-Support/tree/main/quectel_MHI

# 三、资源



# 四、使用说明

## 在线构建

使用步骤

1. 选择actions标签，选择Build IPKs![image](https://user-images.githubusercontent.com/1214708/153843131-615197e2-4ff4-4c0b-b30a-372e1c513158.png)

2. 点击run workflow，输入要编译的插件名称，空格隔开，或者填“all”用来编译所有插件，然后开始编译![image](https://user-images.githubusercontent.com/1214708/153843217-0591a7e6-4758-461e-8b2b-9bb830b87fb2.png)

3. 等待编译完成，点击任务进入详情页
4. 在详情页下载插件压缩包![image](https://user-images.githubusercontent.com/1214708/153843272-81843b45-6dc8-4945-871f-a9a467f63c33.png)

## 离线构建

ForkApp使用步骤

```shell
./forkapp forkapp -from ../applications/luci-app-modem -to ../applications/luci-app-demo
```

```shell
./forkapp upload -ip 192.168.100.1 -pwd "password" -from ../applications/luci-app-modem -to /root/
```

```shell
./forkapp upload -ip 192.168.100.1 -pwd "password" -from ../applications/luci-app-modem -to /root/ -script ../tools/simple-install.sh -install
```
