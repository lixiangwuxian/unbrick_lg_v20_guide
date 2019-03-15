  # LG v20救砖教程

## **我不对因本教程的操作导致您的手机主板击穿或其他任何问题负责**
本教程对所有arb1机型 (目前无解) ，或gpt分区被清机型不适用 (这种情况必须根据gpt表写xml文件，我没有时间，也不会写)。

*写在前面：2019年3月8日，我的 vs995 因在 fastboot 执行命令：*

    fastboot erase devcfg

*重启后变成黑砖，按开机键、连电脑均无反应，本来打算再买个新主板凑活用，但是发现这手机板子没几个卖的，凑巧又发现9008短接点，于是打算自己修复。*
## 准备部分
 1. 9008驱动: https://www.mylgphones.com/lg-android-usb-device%20drivers
1. qfil(包含在QPST中):https://www.qpstflash.com/
2. firehouse文件:https://androidfilehost.com/?fid=11410963190603866856 或参考我以前发的贴子内的下载地址
   
    安装好驱动，QPST。
    
## 读取手机分区表

1. 安上电池，短接9008测试点，插上电脑安装驱动。

2. 