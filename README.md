# HDMI转MIPI屏幕驱动

>基于稚晖的HDMI-PI项目的东芝方案，他本人做出了龙迅的方案，但基于龙讯的调性，代码是没有开源的。而东芝方案有一版硬件，软件没有进行相关调试。开源连接：https://github.com/peng-zhihui/HDMI-PI

# 关于硬件和软件

>这个项目的硬件部分参考了稚晖的原理图，PCB部分由于原版的板厂做出来价格太高，所以进行了重画，是一块核心板加一块转接板的方式。这里两块板之间的连接是用的排针，虽然对这种高速信号来说不太好，但是实际测试是可以使用的。屏幕使用的是稚晖POCKET-LCD开源项目中的那块屏幕，开源链接：https://github.com/peng-zhihui/PocketLCD。
>由于龙迅方案的资料等都不太好弄到，所以这个项目做的是东芝方案，目前已经点亮了这块屏幕，之后也会尽量找时间点亮其他屏幕。由于MIPI屏幕的特性，必须针对每一块屏幕定制驱动。这个项目会开源点亮屏幕的源码，目前还没有写状态切换方面的代码，只能先插上HDMI之后再插上电源才能显示，如果拔下HDMI就需要重新上电。由于原版的原理图中iic接口没加上拉电阻，我这里也没有注意到，所以在调试的时候需要外接iic的上拉。另外1.8v电源需要改为3.3v电源，有源48M晶振供电也选择3.3v。

>2021.01.24 更新了夏普屏的转接板PCB与驱动代码，型号LQ055T3SX02Z，分辨率1080x1920。底板有一点小问题，需要给PA2的排针接口，飞一个1.8v的上拉电阻。

# 交流
感兴趣的可以加QQ群：879256453交流。PS:不是我的群。

# 一些注意事项
> 本仓库的项目是**GPL协议**，不支持任何形式的私自产品化，当然自己DIY是没有任何问题的。
