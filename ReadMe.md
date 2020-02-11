# Hackintosh Of Qftm

**黑苹果爱好者**

**定制：macOS Catalina 10.15.1**

![3B1BE9FA-5BF4-4CC5-A0BE-C35C4CD0CF73](img/3B1BE9FA-5BF4-4CC5-A0BE-C35C4CD0CF73.png)

## 电脑配置

一键查看电脑配置（鲁大师、360驱动管理、Lenovo管家等）

| 规格     | 详细信息                                                     |
| -------- | ------------------------------------------------------------ |
| 电脑型号 | Lenovo R720 15IKBN                                           |
| 操作系统 | macOS Catalina 10.15 / macOS Mojave 10.14 / macOS High Sierra 10.13 |
| 处理器   | Intel Core i5-7300HQ ( Kaby Lake )                           |
| 内存     | 16 GB ( Kingston DDR4 2666MHz )                              |
| 硬盘     | NVMe HS-SSD-C2000Pro ( 512 GB )                              |
| 显卡     | Intel HD Graphics 630 / GTX1050Ti                            |
| 显示器   | 友达 AUO61ED ( 1920×1080  )                                  |
| 声卡     | Realtek @ Intel High Definition Audio                        |
| 网卡     | Realtek 8821AE Wireless LAN 802.11ac PCI-E NIC / Realtek RTL8111 |
## 核心显卡

根据CPU型号确定核心显卡型号，笔记本一般都是双显卡，安装黑果主要使用核心显卡。

| CPU代数 | 核心架构名称 | 核心显卡      |
| ------- | ------------ | ------------- |
| 第2代   | Sandy Bridge | HD2000/HD3000 |
| 第3代   | Ivy Bridge   | HD4000/HD2500 |
| 第4代   | Haswell      | HD4200-5200   |
| 第5代   | Broadwell    | HD5300-6300   |
| 第6代   | Skylake      | HD510-580     |
| 第7代   | Kaby Lake    | HD610-650     |
| 第8代   | COFFE LAKE   | UHD630        |
| 第9代   | Ice Lake     | UHD630        |

或者也可以使用GPU_Z软件和CPU_Z软件来检测出来。

![image-20200211172628882](img/image-20200211172628882.png)

## 安装教程

网上太多的教程，不必重复造轮子

### CLOVER 基础

![image-20200211175441337](img/image-20200211175441337.png)

`Clover` 由一位创建者kabyl命名。要安装黑果首先必须知道CLOVER是什么，否则一切飘渺！！！

简单来说CLOVER就是一个操作系统启动加载器(boot loader)。

详细描述见：[[**黑果小兵的部落阁**] : CLOVER使用教程](https://blog.daliansky.net/clover-user-manual.html)

PS：不想使用CLOVER的可以使用OpenCore（简称OC）

### OpenCore 基础

![image-20200211175838949](img/image-20200211175838949.png)

OpenCore(简称 OC)是一个着眼于未来开源引导工具, 最初诞生于 HermitCrabs 实验室, 现在接手于 Acidanthera, 其目的是创造一个更加严谨的模组化的轻量引导系统。尽管 OpenCore 的主要用途是黑苹果, 它也支持其它操作系统的引导。

详细描述见：[OpenCore 官方文档 ](https://github.com/acidanthera/OpenCorePkg/blob/master/Docs/Configuration.pdf)、[[**黑果小兵的部落阁**] : 精解OpenCore](https://blog.daliansky.net/OpenCore-BootLoader.html)

### MacOS 镜像

根据自己的EFI引导，下载合适的镜像（注意：CLOVER本身可以引导低版本的镜像，但不可以引导比自己高的版本）

各版本镜像下载：[daliansky_macos](https://mirrors.dtops.cc/iso/MacOS/daliansky_macos/)、[黑果小兵](https://blog.daliansky.net/categories/下载/镜像/)

### KITS

黑果常用的工具（必不可少）

云盘下载

```
链接：https://pan.baidu.com/s/1Xa_bLjv95Nb1PGdxOACWew 
提取码：8e1e 
```

#### Tools For Windows

![截屏2020-02-11下午11.47.27](img/截屏2020-02-11下午11.47.27.png)

#### Tools For MAC

![截屏2020-02-11下午11.47.07](img/截屏2020-02-11下午11.47.07.png)

### 具体安装步骤

启动盘制作、安装MacOS等

具体参考：[**[微信公众号-macos101]**：精品学习教程集合贴](https://mp.weixin.qq.com/s/qcvEuPDB3bwXtr2li8CPgQ)

![image-20200211160221929](img/image-20200211160221929.png)

## macOS Catalina 10.15.1

项目**EFI**支持MacOS 10.15.2以下版本，macOS Catalina 10.15.1与macOS Catalina 10.15.2皆测试成功。

![0E837B02-FD8D-4786-B913-5A4A5294EC11](img/0E837B02-FD8D-4786-B913-5A4A5294EC11.png)

### 已驱动硬件

已经驱动的硬件皆测试成功

![ED6D068A-E660-4A16-BFDD-89DFF74FEB94](img/ED6D068A-E660-4A16-BFDD-89DFF74FEB94.png)

#### 声卡

声卡注入ID是28，采用AppleALC.kext驱动。

![70857380-155D-410F-9C2E-3C5FEE0CD58B](img/70857380-155D-410F-9C2E-3C5FEE0CD58B.png)

扬声器/耳机输出可自行切换

![C5CB2E37-FBFF-403B-A2FA-A78487D307DA](img/C5CB2E37-FBFF-403B-A2FA-A78487D307DA.png)

麦克风正常 - 可以是使用Siri

![BB12C2A4-8446-48B1-A19E-C656E4BACDE7](img/BB12C2A4-8446-48B1-A19E-C656E4BACDE7.png)

#### 网卡

**有线网卡已驱动**：可正常连接网线接入网络

**USB共享网络已驱动**：可连接USB共享网络接入网络

![50327FC9-1109-419D-AE8B-0D25D4C9A1D5](img/50327FC9-1109-419D-AE8B-0D25D4C9A1D5.png)

![EB744A07-95FF-43D4-AFFA-452DEDBD590B](img/EB744A07-95FF-43D4-AFFA-452DEDBD590B.png)

正常接入网络

![FF2714FA-8102-4F5D-B223-A0C7BC50A752](img/FF2714FA-8102-4F5D-B223-A0C7BC50A752.png)

#### 显卡

**核心显卡已驱动**：Intel HD 630核显正常，可缩放

**支持一键HIDPI**：提升系统 UI 质量、增强视觉效果

```
sh -c "$(curl -fsSL https://raw.githubusercontent.com/xzhih/one-key-hidpi/master/hidpi.sh)"
```

![D68162B1-933E-4428-8EE0-78EBEA354064](img/D68162B1-933E-4428-8EE0-78EBEA354064.png)

![0C9901A4-A6F2-4AE9-9B16-277AD37E2A46](img/0C9901A4-A6F2-4AE9-9B16-277AD37E2A46.png)

![89775F5D-DC1A-45D9-AC1B-F3FE443856E1](img/89775F5D-DC1A-45D9-AC1B-F3FE443856E1.png)

#### 摄像头

**摄像头已驱动**：摄像头可正常使用

#### 电池

**电池已驱动**：可正常显示电量、睡眠正常可唤醒

![030DB0EF-1D36-40CF-AC42-22C2B785D199](img/030DB0EF-1D36-40CF-AC42-22C2B785D199.png)

![55220657-1323-4937-A750-00F0A03523ED](img/55220657-1323-4937-A750-00F0A03523ED.png)

![E67D91F8-D9F0-4F15-BC3E-57DA4F546378](img/E67D91F8-D9F0-4F15-BC3E-57DA4F546378.png)

#### USB

**USB已驱动**：USB定制、解除端口限制

机械硬盘&固态硬盘、鼠标、键盘等皆可识别

![C66F6CEE-B825-44AC-B41E-50A2CE55BEDA](img/C66F6CEE-B825-44AC-B41E-50A2CE55BEDA.png)

#### 键盘

**键盘已驱动**：键盘所有键均可使用、背光灯可调节、快捷键可定制

#### 触摸板

**触摸板已驱动**：触摸板可支持多指操作

![1C8F8D2F-233A-407D-BD9C-C50E50DC85D2](img/1C8F8D2F-233A-407D-BD9C-C50E50DC85D2.png)

![C79ABB29-14B1-4B3D-8B87-0C05C4EC54B6](img/C79ABB29-14B1-4B3D-8B87-0C05C4EC54B6.png)

例如：3指操作等

![19792312-486C-454D-94F3-C231F3D3E21A](img/19792312-486C-454D-94F3-C231F3D3E21A.png)

#### CPU

**CPU变频正常**：支持多档位

![166130B6-1642-4752-9812-1A0389963220](img/166130B6-1642-4752-9812-1A0389963220.png)

![7670DDF3-C710-4A4D-9948-C424045D09FB](img/7670DDF3-C710-4A4D-9948-C424045D09FB.png)

![C09F7D85-03A3-465D-96CF-E2101C5709BC](img/C09F7D85-03A3-465D-96CF-E2101C5709BC.png)

#### AppStore

**AppStore正常**：可登录、可下载软件

![28470452-1601-4519-ACF7-A4A19C5868FB](img/28470452-1601-4519-ACF7-A4A19C5868FB.png)

![089D3D78-4465-4749-9C82-58D52E152085](img/089D3D78-4465-4749-9C82-58D52E152085.png)

#### Icloud

**Icloud正常**：可登录、备份文件正常

PS：不过就5G，有需求的，自己可另外购买增加容量

#### 终端

**终端正常**

![CBFB7FC7-DD62-4A17-B18A-C200AACA3D4C](img/CBFB7FC7-DD62-4A17-B18A-C200AACA3D4C.png)

#### 其它功能

几乎大部分功能均能正常使用

![92032A0D-A319-4BE0-9DC7-F63E80E3D335](img/92032A0D-A319-4BE0-9DC7-F63E80E3D335.png)

### 未驱动硬件

#### 无线网卡

**无线网卡未驱动**：Hackintosh无线网开无解，不过最近有大佬好像已经破解了Intel的无线网卡

PS：关于无线网卡可以更换博通的，免驱黑苹果支持无线+蓝牙（体验极佳）

等闲时就更换网卡：BCM94360CS2（支持R720），黑苹果免驱，支持无线网+蓝牙

![image-20200211170803933](img/image-20200211170803933.png)

#### 蓝牙

**蓝牙未驱动**：其实蓝牙驱动很简单，注入ID就行，本身没做是因为没必要，内置蓝牙一点都不好用，不如直接更换网卡！！！

#### 独显

**独显**：针对笔记本双显卡，独显都无法驱动，不过核显已经够用了

### 小问题

- 休眠一段时间后唤醒，左键变成右键       解决办法：【Ctrl+右键】即可解决

### 黑苹果论坛

- **国内**：[远景论坛](http://bbs.pcbeta.com/)、[威锋论坛](http://bbs.feng.com/)
- **国外**：[insanelymac 论坛](https://www.insanelymac.com/forum/)、[tonymacx86论坛](https://www.tonymacx86.com/)、[德国黑苹果论坛](https://www.hackintosh-forum.de/)、[俄罗斯黑苹果论坛](https://www.applelife.ru/)、[法国黑苹果论坛](https://www.hackintosh-montreal.com/)、 [osxlatitude论坛](https://osxlatitude.com/forums/)

- **博客**：[黑果小兵的部落阁](https://blog.daliansky.net/)、[醉渔小站](https://zuiyu1818.cn/)、[唐少游的黑苹果从入门到精通](https://post.smzdm.com/xilie/40890/)、 [云屋小站](https://www.misonsky.cn/)

PS：平时没事多逛逛论坛，许多问题就解决了

### 感慨

- **建议经不起折腾人不要碰，浪费时间 ！！！**

- **一时黑苹果，一时爽，一直黑苹果，一直爽 ！！！**

### 贡献

**Author**：[**【Qftm】**](https://qftm.github.io/)

