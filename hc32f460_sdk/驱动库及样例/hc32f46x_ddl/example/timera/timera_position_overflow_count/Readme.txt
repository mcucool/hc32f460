﻿================================================================================
                                样例使用说明
================================================================================
版本历史
日期        版本    负责人         IAR     MDK     GCC     描述
2018-11-14  1.0     Yangjp         7.70    5.16    8.3.1   first version
================================================================================
平台说明
================================================================================
GCC工程，由Eclipse IDE外挂GNU-ARM Toolchain，再结合pyOCD GDB Server实现工程的编译、
链接和调试。在用Eclipse导入工程后，请将xxxx_PyOCDDebug中pyocd-gdbserver和SVD文件
设置为正确的路径；请将xxxx_PyOCDDownload中pyocd设置为正确的路径。注意，这些路径不
能包含非英文字符。


功能描述
================================================================================
本样例展示Timera模块3相正交编码相位差计数和公转位置溢出计数功能。

说明：
本样例设置Timera时钟源为外部端口正交编码输入，设置单元1的PE9为端口A、PE11为端口B，
配置通道B为高电平时，通道A采样到上升沿触发递加计数，配置单元2当单元1上溢触发递加
计数，单元1递加计数溢出则LED0切换状态，单元2递加计数溢出则LED1切换状态。

================================================================================
测试环境
================================================================================
测试用板:
---------------------
EV-HC32F460-LQFP100-050-V1.1

辅助工具:
---------------------
函数发生器（编码器）

辅助软件:
---------------------
无

================================================================================
使用步骤
================================================================================
1）打开工程并重新编译；
2）启动IDE的下载程序功能，关闭IDE下载界面；
3）配置函数发生器，通道A、B输出频率（1000HZ）、占空比相同，将函数发生器输出通道连
接到PE9和PE11引脚；
4）修改函数发生器相位配置，B通道的相位超前A通道1/4周期，观察LED0闪烁；
5）LED0状态切换6次则触发LED1状态切换。

================================================================================
注意
================================================================================
无

================================================================================
