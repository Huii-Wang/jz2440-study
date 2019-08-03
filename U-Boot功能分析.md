# Uboot功能分析
## 1.以Windows系统为例，来说明电脑开机上电的流程
Window电脑|Linux电脑|说明/备注
---|:--:|---:
启动BIOS|Boot Loader|系统的启动引导程序
引导Windows系统启动|Linux内核|把操作系统从硬盘读取到内存
识别硬盘启动 C盘 D盘|挂载跟文件系统|开始识别文件存贮
运行应用程序 QQ MSN|Linux应用程序|基于操作系统的文件系统



## 2.Uboot分析编译步骤
    1.下载uboot
    2.下载并打入补丁
    3.配置Uboot信息
    4.编译烧写到开发板