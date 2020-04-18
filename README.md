# control_project
控制系统综合实践，持续龟速更新中...
## 01basic_work  
1. 《Simulink基础入门教程》；  
2. 课堂小作业1 ---**task1_1.slx**  
好像就是把老师给的几个公式用simulink搭一下，有两个阶跃响应函数，一个稍微简单，一个有点复杂，二者动态品质差不多的。简单的对应的控制器传递函数不是真有理函数，复杂的对应控制器的传递函数不仅稳定真有理，而且简单，工程易实现。但是实际设计过程中，设计人可能想不到复杂的，从而说明控制系统设计的难点所在。
3. 课堂小作业2 ---**task1_2.slx**  
利用simulink搭建表示阶跃响应、阶跃响应的变化速度、阶跃响应的变化加速度，分析为什么不可以人为主观设置响应时间。
## 02signals_generator
在simulink中设计离线信号发生器（正弦波、方波、三角波）；
```
signals_generator 
├── signals1.slx
├── /signals2/
│  ├── /signals2.slx
│  ├── /Test.fig
│  ├── /Test.m
└── README.md

```
1. 模型signals1.slx是完全离线的，拖动Gain_slider模块后需要重新运行仿真，我觉得和直接修改每个参数的Constant值并没有太大的区别；  

2. 模型signals2.slx的调参通过MATLAB GUI实现，基于回调函数的事件触发可以让仿真模型的参数实时变化，从而实时观察信号生成的结果。同时使用Simulation Pace模块自适应步长，不需手动设置步长。