# Team13 第二阶段报告

## 项目优点介绍
- 通过类的定义，充分体现了封装的便利性
- 改进了第一阶段的规则实现，将规则重新在第二阶段实现，可以通过board_size不仅为6的情况
- 充分利用qt，包括使用qt自带的函数，或修改.ui文件来创建可视化界面

## 介绍本项目的代码文件：
- 规则代码的移植，我们在widget类下创建四个方向的函数up,down,left,right，通过判断四个方向移动的可行性，从而返回不同类型
- ui界面的实现，我们分别完成了initialpiece，surakarta position to qpoint，qpoint to id三个功能，并使用Qpainter绘制直线，弧线与棋子
- 超时功能，使用了QTimer设置计时器，在计时器为0时传输信号，返回失败的玩家
- 认输功能，接收button传输的信号，直接返回currentplayer为输即可
- 重开一局功能，设计了initpiece函数，将棋盘初始化

## 遇到的问题
- ***问题1***：如何设置倒计时
  使用Qt的定时器函数QTimer来实现倒计时功能，每隔一秒更新一次倒计时时间，并在界面上显示。
- ***问题2***：能否将第一阶段的规则直接搬运到第二阶段
  第一阶段的代码过于混乱），因此在保留必要的穷举类型和函数情况下，我们重新在widget.cpp中实现了规则

## 小组分工
- 主要代码框架与规则：武思豪 计时器：李佳俊 报告撰写：叶霁轩