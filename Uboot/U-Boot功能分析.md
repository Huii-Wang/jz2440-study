# Uboot功能分析
    U-Boot，全称 Universal Boot Loader，是遵循GPL条款的开放源码项目。U-Boot的作用是系统引导.
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


## 3.Uboot要实现的功能
    UBoot是一个复杂的单片机程序
    ### 硬件相关初始化
        关看门口
        初始化时钟
        初始化SDRAM
    ### 软件相关初始化
    1.读Flash
        写Flash 写网卡 写USB
    2.初始化SDRAM
    3.启动内核


## 4.最简单的BootLoader的编写步骤
    1.初始化硬件
        关闭看门狗
        设置时钟
        设置SDRAM
        初始化NAND FLASH
    2.把内核从NAND FLASH 读到SDRAM
    3.设置要传给内核的参数
    4.跳转执行内核
