

# NUC8i5BEK Catalina Guide

## 前言
在这份EFI内

## 机型配置
* 机型：Intel NUC KIT NUC8I5BEK
* CPU：Intel(R) Core(TM) i5-8259U CPU @ 2.30GHz
* 内存：十铨（Team） DDR4 2666 16G X 2
* 硬盘：海康威视 C2000 PRO 1T
* 显卡：Intel Iris Plus Graphics 655
* 显示器：Dell U2718Q（3840 x 2160）
* 声卡：Realtek ALC235
* 无线网卡：BCM94360CS2（1300Mbps + Bluetooth 4.0）
* BIOS: BECFL357.86A.0078.2020.0309.1538（Version 0078）

## 开始前需要准备的工具
* OpenCore Configurator
* Clover Configurator
* Hackintool

没有选择一些进阶性的配置工具是为了方便用户使用最少的时间消耗以及最低的学习成本进行启动文件的配置。

## BIOS配置
一些资料指出我们需要调整一些BIOS的设置以获得更好的macOS体验
这里以0078版本的BIOS为基准 分享一些我对BIOS设置的调整

Devices - Video
- IGD Minimum Memory 64MB
- IGD Aperture Size 256MB

Devices - Onboard Devices 
如果是经过硬改的版本 需要关掉板载的蓝牙和WLAN来避免冲突 同时需要打开SD Card的读写功能保证拆机卡的正常运行

- WLAN 关闭
- Bluetooth 关闭
- SD Card Read/Write

Security - Security Features
- Inter® Virtualization Technology 打开
- Inter® VT for Directed I/O (VT-d) 关闭
- Inter® Software Guard Extension(SGX) Disabled

Power - Secondary Power Settings
- PCIe ASPM Support 打开

Boot - Boot Configuration - UEFI Boot
- Fast Boot 关闭

Boot - Secure Boot - Secure Boot Config
- Secure Boot 关闭