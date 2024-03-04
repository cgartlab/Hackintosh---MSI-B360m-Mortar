# 微星 B360M 迫击炮 黑苹果OpenCore EFI

## Star History

[![Star History Chart](https://api.star-history.com/svg?repos=cgartlab/Hackintosh---MSI-B360m-Mortar&type=Date)](https://star-history.com/#cgartlab/Hackintosh---MSI-B360m-Mortar&Date)

## 写在前面

> 为什么选择 OpenCore

> * 从 2019 年 9 月以后, Acidanthera 开发的内核驱动 (Lilu, AppleALC 等等) 「不再会」 在 Clover 上做兼容性测试
> OpenCore 更加注重系统的安全性, 提供对 OpenCore 自身引导文件对加密, 同时对文件保险箱 (FileVault) 有更强大的支持, 在未来会支持 UEFI 安全启动
> * OpenCore 启动 FileVault (硬盘保险箱) 加密的分区速度远超 Clover
> * OpenCore 支持基于 boot.efi 的原生开机快捷键支持
> * OpenCore 使用更加先进的方法注入第三方内核扩展驱动 (Kext) 且与此同时不会破坏系统完整性保护
> * OpenCore 通过读取启动磁盘设置的 NVRAM 变量, 可以像白苹果一样支持在设置的启动磁盘切换默认引导项支持给其它 .efi 驱动或引导工具加入参数
> 大量 Acidanthera 维护的独立 UEFI 驱动 被合并入 OpenCore, 未来的开发直接与 OpenCore 绑定, 且不再支持 Clover
>
以上转载自<https://blog.daliansky.net/OpenCore-BootLoader.html>
ß
## 目录

- [微星 B360M 迫击炮 黑苹果OpenCore EFI](#微星-b360m-迫击炮-黑苹果opencore-efi)
  - [写在前面](#写在前面)
  - [目录](#目录)
  - [EFI 介绍](#efi-介绍)
  - [更新记录](#更新记录)
      - [2024-02-19](#2024-02-19)
      - [2023-10-29](#2023-10-29)
      - [2022-09-03](#2022-09-03)
      - [2022-06-30](#2022-06-30)
      - [2022-05-12](#2022-05-12)
      - [2021-11-09](#2021-11-09)
      - [2021-09-13](#2021-09-13)
      - [2021-07-28](#2021-07-28)
      - [2021-04-09](#2021-04-09)
  - [我的配置](#我的配置)
  - [兼容的配置](#兼容的配置)
  - [可正常工作](#可正常工作)
  - [硬件信息](#硬件信息)
  - [系统截图](#系统截图)
  - [性能测试](#性能测试)
  - [生产力工具测试](#生产力工具测试)
  - [鸣谢](#鸣谢)

## EFI 介绍

此 EFI 使用iMac19,1机型，微星 B360M 迫击炮 的绝大部分用户可通过修改使用，核显 + 独显共同硬解，默认启用全部 USB 端口，[OpenCore](https://github.com/acidanthera/OpenCorePkg) 版本：0.9.5

![](https://github.com/AskyStudio/Hackintosh---MSI-B360m-Mortar/blob/Hackintosh-OpenCore/Images/System-info.png?raw=true)

## 更新记录

#### 2024-02-19

* 系统跟进更新为 OpenCore 0.9.6引导
* 更新驱动 AppleALC - 1.8.9

#### 2023-10-29

* 系统跟进更新为 OpenCore 0.9.5引导
* 更新驱动 Lilu - 1.6.7
* 更新驱动 VirtualSMC - 1.3.2
* 更新驱动 AppleALC - 1.8.6
* 更新驱动 WhateverGreen - 1.6.6
* 更新驱动 IntelMausi - 1.0.7
* 更新驱动 NVMeFix - 1.1.1
* 更新驱动 HibernationFixup - 1.4.9
* 添加驱动 RadeonSensor - 0.3.3
* 添加驱动 SMCRadeonGPU - 0.3.3

#### 2022-09-03

* 系统跟进更新为 OpenCore 0.8.3引导
* 更新驱动 Lilu - 1.6.2
* 更新驱动 VirtualSMC - 1.3.0
* 更新驱动 AppleALC - 1.7.4
* 更新驱动 WhateverGreen - 1.6.1
* 更新驱动 IntelMausi - 1.0.7
* 更新驱动 NVMeFix - 1.1.0
* 添加驱动 RadeonSensor - 0.3.1
* 添加驱动 SMCRadeonGPU - 0.3.1

#### 2022-06-30

* 系统跟进更新为 OpenCore 0.8.1引导
* 更新驱动 AppleALC - 1.7.2
* 更新驱动 WhateverGreen - 1.5.9

#### 2022-05-12

* 系统跟进更新为 OpenCore 0.7.9引导
* 更新驱动 AppleALC - 1.7.1
* 更新驱动 Lilu - 1.6.0
* 更新驱动 WhateverGreen - 1.5.8
* 更新驱动 VirtualSMC - 1.2.9

#### 2021-11-09

* 系统跟进更新为 OpenCore 0.7.6引导
* 删除 SSDT-EC-USBX-DESKTOP.aml（影响睡眠唤醒）
* 新增驱动 HibernationFixup - 1.0（修复睡眠唤醒）
* 修正定制USB驱动 USBPorts.kext
* 更新驱动 AudioDxe.efi 为最新
* 更新驱动 HfsPlus.efi 为最新
* 更新驱动 AppleALC - 1.6.6
* 更新驱动 Lilu - 1.5.7
* 更新驱动 WhateverGreen - 1.5.5
* 默认开启启动声音

#### 2021-09-13

* 系统跟进更新为 OpenCore 0.7.3引导
* 更新驱动 Lilu - 1.5.6
* 更新驱动 AppleALC - 1.6.4
* 更新驱动 WhateverGreen - 1.5.3
* 更新驱动 VirtualSMC - 1.2.7

#### 2021-07-28

* 系统跟进更新为 OpenCore 0.7.1引导
* 更新驱动 AppleALC - 1.6.2
* 更新驱动 IntelMausi - 1.0.7
* 更新驱动 Lilu - 1.5.4
* 更新驱动 NVMeFix - 1.0.9
* 更新驱动 VirtualSMC - 1.2.5
* 更新驱动 WhateverGreen - 1.5.1

#### 2021-04-09

* 系统更换为OpenCore 0.6.8 引导
* 系统升级至macOS Catalina 10.15.7（理论已支持 macOS Big Sur）
* 所有驱动均针对OpenCore引导程序更新为目前的最新稳定版
* 优化了系统登陆界面进入桌面的切换动画
* 系统跨大版本更新仍然建议提前Time Machine备份

## 我的配置

|      硬件 | 型号                                         |
| ------: | :----------------------------------------- |
|      主板 | 微星 B360M 迫击炮                               |
|     处理器 | 英特尔酷睿 i7-9700                              |
|      显卡 | 公版 RX 5700XT 8GB                           |
|      硬盘 | Asgard AN2 500NVMe-M.2/80 500GB            |
|      内存 | 美商海盗船 16GB DDR4 2666MHz x 4                |
| 无线 + 蓝牙 | 奋威 BCM94360CD（双频 1750M + 蓝牙 4.0）PCI-E 无线网卡 |
| 电源 + 散热 | 航嘉 GX500 + 玄冰400                           |
|     显示器 | 冠捷 U2790B（27 英寸 4K 分辨率）                    |
|      键盘 | iKbc TypeMan C87                             |
|      鼠标 | 罗技 MX Master 2s（使用优联连接，以方便在 BIOS 中使用）       |

## 兼容的配置

| 硬件 | 型号     |
| :------------- | :------------- |
| 主板                | 微星 B360M 迫击炮      |
| 处理器              | 英特尔第 8 代、第 9 代酷睿处理器（推荐拥有核显的版本）  |
| 显卡                | RX 560 / RX 570 / RX 580 / RX 590 / RX VEGA⁵⁶ / RX VEGA⁶⁴ / Radeon VII / RX 5500 / RX 5500 XT / RX 5600 / RX 5600 XT / RX 5700 / RX 5700 XT  |
| 硬盘                | 除了几个特例（如三星 PM981），基本都可以  |
| 内存                | 除了非常差的，基本都可以  |
| Wi-Fi + 蓝牙        | 黑苹果免驱版无线 + 蓝牙 PCI-E 网卡都可以  |
| 机箱 + 电源 + 散热   | 根据个人喜好和 CPU、显卡的功率来决定  |
| 显示器              | 根据个人喜好选择（推荐 4K 分辨率）  |
| 摄像头 + 麦克风      | 根据个人喜好选择  |
| 其他外设            | 根据个人喜好选择  |

_显卡优先选择公版或蓝宝石，其次选择迪兰恒进、华硕和微星，尽量不选择盈通和讯景，一定避开 RX 580 2048SP 版本！_
_个人非常不推荐使用玄冰 400 散热器（不含扣具升级款），准备更换为利民 AS120，远离反人类设计保平安。_

## 可正常工作

* [x] 声卡（板载）/ 网卡（板载）
* [x] 显卡（核显 + 独显）/ 硬解 4K（HEVC + H.264）
* [x] WiFi（PCI-E 设备） / 蓝牙（PEI-E 载 USB 设备）
* [x] 隔空投送 / 接力 / 随航
* [x] FaceTime / iMessage
* [x] Apple Music / Apple TV Plus
* [x] 睿频 / HWP 变频 / 原生电源管理
* [x] 睡眠 / 键盘、鼠标唤醒
* [x] 其他白果功能（99%）

## 硬件信息

![硬件信息](https://github.com/AskyStudio/Hackintosh---MSI-B360m-Mortar/blob/Hackintosh-OpenCore/Images/Hardware-info-test.png?raw=true)

## 系统截图

![内存](https://github.com/AskyStudio/Hackintosh---MSI-B360m-Mortar/blob/Hackintosh-OpenCore/Images/Memory.png?raw=true)

![HiDPI](https://github.com/AskyStudio/Hackintosh---MSI-B360m-Mortar/blob/Hackintosh-OpenCore/Images/HiDPI.png?raw=true)

![4K 硬件解码](https://github.com/AskyStudio/Hackintosh---MSI-B360m-Mortar/blob/Hackintosh-OpenCore/Images/4k-video-decode.png?raw=true)

![音频输出](https://github.com/AskyStudio/Hackintosh---MSI-B360m-Mortar/blob/Hackintosh-OpenCore/Images/Audio-out.png?raw=true)

![音频输入](https://github.com/AskyStudio/Hackintosh---MSI-B360m-Mortar/blob/Hackintosh-OpenCore/Images/Audio-in.png?raw=true)

![无线网卡](https://github.com/AskyStudio/Hackintosh---MSI-B360m-Mortar/blob/Hackintosh-OpenCore/Images/Wi-Fi.png?raw=true)

![蓝牙](https://github.com/AskyStudio/Hackintosh---MSI-B360m-Mortar/blob/Hackintosh-OpenCore/Images/Bluetooth.png?raw=true)

![蓝牙](https://github.com/AskyStudio/Hackintosh---MSI-B360m-Mortar/blob/Hackintosh-OpenCore/Images/Bluetooth-2.png?raw=true)

![随航](https://github.com/AskyStudio/Hackintosh---MSI-B360m-Mortar/blob/Hackintosh-OpenCore/Images/Handoff.png?raw=true)

![系统备份](https://github.com/AskyStudio/Hackintosh---MSI-B360m-Mortar/blob/Hackintosh-OpenCore/Images/Time-Machine.png?raw=true)

![SSD硬盘](https://github.com/AskyStudio/Hackintosh---MSI-B360m-Mortar/blob/Hackintosh-OpenCore/Images/NVME%20ssd.png?raw=true)

![USB接口](https://github.com/AskyStudio/Hackintosh---MSI-B360m-Mortar/blob/Hackintosh-OpenCore/Images/USB.png?raw=true)

![GPU信息](https://github.com/AskyStudio/Hackintosh---MSI-B360m-Mortar/blob/Hackintosh-OpenCore/Images/Gpu.png?raw=true)

![电源管理](https://github.com/AskyStudio/Hackintosh---MSI-B360m-Mortar/blob/Hackintosh-OpenCore/Images/PM.png?raw=true)

## 性能测试

![](https://github.com/AskyStudio/Hackintosh---MSI-B360m-Mortar/blob/Hackintosh-OpenCore/Images/GeekBench-CPU.png?raw=true)

![](https://github.com/AskyStudio/Hackintosh---MSI-B360m-Mortar/blob/Hackintosh-OpenCore/Images/GeekBench-CPU-singlecore.png)

![](https://github.com/AskyStudio/Hackintosh---MSI-B360m-Mortar/blob/Hackintosh-OpenCore/Images/GeekBench-CPU-multicore.png)

![](https://github.com/AskyStudio/Hackintosh---MSI-B360m-Mortar/blob/Hackintosh-OpenCore/Images/GeekBench-GPU-Metal.png?raw=true)

![](https://github.com/AskyStudio/Hackintosh---MSI-B360m-Mortar/blob/Hackintosh-OpenCore/Images/GeekBench-GPU-OpenCL.png?raw=true)

## 生产力工具测试

* 个人测试过的一系列视觉设计相关的软件，功能均无明显异常

![](https://github.com/AskyStudio/Hackintosh---MSI-B360m-Mortar/blob/Hackintosh-OpenCore/Images/App-CGI.png?raw=true)

![](https://github.com/AskyStudio/Hackintosh---MSI-B360m-Mortar/blob/Hackintosh-OpenCore/Images/App-Design.png?raw=true)

![](https://github.com/AskyStudio/Hackintosh---MSI-B360m-Mortar/blob/Hackintosh-OpenCore/Images/App-Developer%20Tools.png?raw=true)

![](https://github.com/AskyStudio/Hackintosh---MSI-B360m-Mortar/blob/Hackintosh-OpenCore/Images/App-Normal%20Tools.png?raw=true)

## 鸣谢

[xjn](https://blog.xjn819.com/)<br>
[andot](https://github.com/andot/MSI-B360M-MORTAR-IMACPRO-EFI/)<br>
[daliansky](https://github.com/daliansky) ([黑果小兵](https://blog.daliansky.net/))<br>
[tonymoses](http://bbs.pcbeta.com/viewthread-1835637-1-1.html)<br>
[cattyhouse](https://github.com/cattyhouse/oc-guide/)<br>
[osx86zh](https://t.me/osx86zh/) ([Telegram](https://telegram.org/) 讨论组)
