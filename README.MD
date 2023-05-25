此教程已转移至本人博客[lxwx 的备忘录](https://www.lxtend.com/lgv20-unbrick/)

# LG v20救砖教程 @lxwx in gfan

## 本教程根据CC-BY协议发布，继续阅读即代表您同意协议内容。
## **我不对因本教程导致您的手机主板被击穿或出现的其他任何问题负责**
本教程对arb1机型 (如果你能搞到arb1的firehouse文件，当我没说) ，及分区表被清机型不适用 (这种情况必须根据分区表生成xml文件，我不会弄)。

*2019年3月8日，我的 vs995 因在 fastboot 执行命令：*

    fastboot erase devcfg

*重启后变成黑砖，按开机键、连电脑均无反应，本来打算再买个新主板凑活用，但是发现这手机板子没几个卖的，凑巧又发现9008短接点，于是打算自己修复。*
### 适应情况：误擦写分区导致不开机，刷错kdz不开机
## 一  准备
* 一份对应你手机型号的kdz文件
* kdz解包工具
* 9008驱动: <a href>https://www.mylgphones.com/lg-android-usb-device%20drivers</a>
* qfil(包含在QPST中): <a href>https://www.qpstflash.com/</a>
* firehouse文件: <a href>https://androidfilehost.com/?fid=11410963190603866856</a>  或参考我以前发的贴子内的下载地址
* 安装好驱动，QPST工具包，将kdz用解包工具解包
    
## 二  读取分区表
* 如果你的电脑没有连接过9008模式的手机(否则跳过)
    1. 安上电池，短接9008测试点，不要松手，手机用数据线连接电脑安装驱动，电脑出现提示音后松手。
    2. 断开连接，拔下电池3秒以上。
* 打开QFIL，在"Configuration"中将“Device type”改为UFS，勾选“Reset After Download”后点击“OK”。
* 在“Select Programmer”中打开v20的firehouse文件。
* 在“Tools”中找到“Partition Manager”选项，鼠标移到选项上。
* 插上电池，短接测试点，连接电脑后松手，迅速按下“Partition Manager”按钮，并点击确定，电脑会将firehouse文件下载到手机。
## 三  刷写镜像 
* 在弹出的分区刷写框中，选择你要重新刷写的分区，右键，选择“Manage Partition Data”，在弹出的“Raw Data Manager”中选择“Load Image”,选择从kdz解压出来的img文件中对应分区的镜像文件刷入。如果你是误擦写分区，只需重新擦写误擦掉的分区。如果你刷错了kdz，建议将kdz解包出来的img挨个刷一遍。
## 四  收尾
* 刷写完成后，断开手机与电脑的连接，插拔一下电池，按下开机键，不出意外，你的手机现在应该能能正常开机了。如不放心，可以在Download模式下重新刷写一遍手机对应的kdz。
#### Tips
1. 为了防止主板短路损坏，我用纸质胶带将短接点周围粘了起来。
1. 短接所使用的线材我使用了杜邦线，同样两头用胶带粘了起来。
1. 我电脑使用的Win10系统在QFIL下载firehouse文件时QFIL会卡住，换用Win7后解决。
1. 没有配图是因为我没截图。
