# 微星 B360M 迫击炮 黑苹果Clover EFI

## EFI 介绍

此 EFI 使用iMac19,1机型，微星 B360M 迫击炮 的绝大部分用户可通过修改使用，核显 + 独显共同硬解，默认启用全部 USB 端口，[Clover](https://github.com/CloverHackyColor/CloverBootloader)版本：5120

![](![](https://github.com/AskyStudio/Hackintosh---MSI-B360m-Mortar/blob/master/Images/系统信息.png
)

### 可正常工作

- [x] 声卡（板载）/ 网卡（板载）
- [x] 显卡（核显 + 独显）/ 硬解 4K（HEVC + H.264）
- [x] WiFi（PCI-E 设备） / 蓝牙（PEI-E 载 USB 设备）
- [x] 隔空投送 / 接力 / 随航
- [x] FaceTime / iMessage
- [x] Apple Music / Apple TV Plus
- [x] 睿频 / HWP 变频 / 原生电源管理
- [x] 睡眠 / 键盘、鼠标唤醒
- [x] 其他白果功能（99%）

### 系统截图

![](https://github.com/AskyStudio/Hackintosh---MSI-B360m-Mortar/blob/master/Images/内存.png)

![](https://github.com/AskyStudio/Hackintosh---MSI-B360m-Mortar/blob/master/Images/HiDPI.png)

![](https://github.com/AskyStudio/Hackintosh---MSI-B360m-Mortar/blob/master/Images/4k%20核心显卡加速解码.png)

![](https://github.com/AskyStudio/Hackintosh---MSI-B360m-Mortar/blob/master/Images/音频输出.png)

![](https://github.com/AskyStudio/Hackintosh---MSI-B360m-Mortar/blob/master/Images/音频输入.png)

![](https://github.com/AskyStudio/Hackintosh---MSI-B360m-Mortar/blob/master/Images/Wi-Fi.png)

![](https://github.com/AskyStudio/Hackintosh---MSI-B360m-Mortar/blob/master/Images/蓝牙.png)

![](https://github.com/AskyStudio/Hackintosh---MSI-B360m-Mortar/blob/master/Images/随航.png)

![](https://github.com/AskyStudio/Hackintosh---MSI-B360m-Mortar/blob/master/Images/Time%20Machine%20备份.png)

![](https://github.com/AskyStudio/Hackintosh---MSI-B360m-Mortar/blob/master/Images/NVME%20ssd.png)

![](https://github.com/AskyStudio/Hackintosh---MSI-B360m-Mortar/blob/master/Images/USB.png)

![](https://github.com/AskyStudio/Hackintosh---MSI-B360m-Mortar/blob/master/Images/显卡.png)

![](https://github.com/AskyStudio/Hackintosh---MSI-B360m-Mortar/blob/master/Images/电源管理.png)

![](https://github.com/AskyStudio/Hackintosh---MSI-B360m-Mortar/blob/master/Images/蓝牙2.png)

### 我的配置

|         硬件       |                   型号                     |
|-------------------:|:------------------------------------------|
|               主板 | 微星 B360M 迫击炮                               |
|             处理器 | 英特尔酷睿 i7-9700                            |
|               显卡 | 公版 RX 5700XT 8GB                           |
|               硬盘 | Asgard AN2 500NVMe-M.2/80 500GB                          |
|               内存 | 美商海盗船 16GB DDR4 2666MHz x 4                 |
|        无线 + 蓝牙 | 奋威 BCM94360CD（双频 1750M + 蓝牙 4.0）PCI-E 无线网卡  |
|        电源 + 散热 | 航嘉 GX500 + 玄冰400 |
|             显示器 | 冠捷 U2790B（27 英寸 4K 分辨率）                 |
|               键盘 | iKbc TypeMan C87）                 |
|               鼠标 | 罗技 MX Mster 2s（使用优联连接，以方便在 BIOS 中使用） |

### 兼容的配置

|         硬件       |                              型号                           |
|-------------------:|:------------------------------------------------------------|
|               主板 | 微星 B360M 迫击炮（钛金版）                                    |
|             处理器 | 英特尔第 8 代、第 9 代酷睿处理器（推荐拥有核显的版本）                |
|               显卡 | RX 560 / RX 570 / RX 580 / RX 590 / RX VEGA⁵⁶ / RX VEGA⁶⁴ / Radeon VII / RX 5500 / RX 5500 XT / RX 5600 / RX 5600 XT / RX 5700 / RX 5700 XT |
|               硬盘 | 除了几个特例（如三星 PM981），基本都可以                            |
|               内存 | 除了非常差的，基本都可以                                        |
|        无线 + 蓝牙 | 黑苹果免驱版无线 + 蓝牙 PCI-E 网卡都可以                          |
|     摄像头 + 麦克风 | macOS 免驱版都可以                                             |
|  机箱 + 电源 + 风扇 | 根据个人喜好和 CPU、显卡的功率来决定                               |
|             显示器 | 根据个人喜好选择（推荐 4K 分辨率）                                |
|  键盘 + 鼠标 + 音箱 | 根据个人喜好选择                                                |
|           其它外设 | 根据个人喜好选配                                              |

*显卡优先选择公版或蓝宝石，其次选择迪兰恒进、华硕和微星，尽量不选择盈通和讯景，一定避开 RX 580 2048SP 版本！*
*个人非常不推荐使用玄冰 400 散热器（不含扣具升级款），准备更换为利民 AS120，远离反人类设计保平安。*

## 更新记录
#### 2020.07.31
* 升级 macOS Catalina 10.15.6
* 升级 Clover v5120
* 升级 WhateverGreen v1.4.1 (7月15日编译，根治安装/更新中的黑屏现象)，原生支持UHD620/UHD630等八代核显，不需要注入platform-id， 同时它也支持NVIDIA和AMD的显卡，以及整合了Shiki和CoreDisplayFixup的驱动，现在是All In One了
* 升级 Lilu v1.4.6
* 内存修正驱动采用 OcQuirks，原则上支持 Big Sur

## 鸣谢
[xjn](https://blog.xjn819.com/)<br>
[andot](https://github.com/andot/MSI-B360M-MORTAR-IMACPRO-EFI/)<br>
[daliansky](https://github.com/daliansky) ([黑果小兵](https://blog.daliansky.net/))<br>
[tonymoses](http://bbs.pcbeta.com/viewthread-1835637-1-1.html)<br>
[cattyhouse](https://github.com/cattyhouse/oc-guide/)<br>
[osx86zh](https://t.me/osx86zh/) ([Telegram](https://telegram.org/) 讨论组)
