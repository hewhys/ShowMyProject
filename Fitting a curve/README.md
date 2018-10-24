# 曲线拟合

## 功能介绍

代码中使用Bootstrap(页面布局与样式), EChart(图表展示效果)。


![main](D:\myWorkplace\GitHub\learnTfjs\Fitting a curve\pic\main.png)

<center>图1 主界面</center>

如图1所示，代码按照给定的曲线(y = a * x ^ 3 + b * x ^ 2 + c * x + d )生成散点，并绘制在平面坐标系上，当然图上也给出了实际的曲线。细心的读者可能发现散点并不在曲线上，而是分布在曲线的上下两侧。这是因为在代码中增加了随机偏移，目的是让数据更接近实际的测量数据。当然也可以手动输入曲线的参数来改变初设曲线。

![曲线拟合1](D:\myWorkplace\GitHub\learnTfjs\Fitting a curve\pic\曲线拟合1.png)

<center>图2 拟合曲线1</center>

预测曲线是在tf中生成随机参数a,b,c,d。可以看到现在的预测曲线并没有拟合散点。

![曲线拟合2](D:\myWorkplace\GitHub\learnTfjs\Fitting a curve\pic\曲线拟合2.png)

<center>图3 拟合曲线2</center>

接下来我们把散点数据输入到tf网络中，经过一次75轮迭代（每按一次迭代按钮就迭代75次）后，我们得到了图三中的曲线，可以看到现在的预测曲线以及初具雏形。![曲线拟合3](D:\myWorkplace\GitHub\learnTfjs\Fitting a curve\pic\曲线拟合3.png)



<center>图4 拟合曲线3</center>

经过多次迭代后，我们就能得到拟合的不错的曲线了。此时

$答案: y= -0.800 * x^3  -0.200 * x^2 + 0.900*x + 0.500$

$预测: y = -0.805*x^3  -0.226*x^2 + 0.902*x + 0.506$ 

## 参考资料

[官方教程 Training First Steps: Fitting a Curve to Synthetic Data](https://js.tensorflow.org/tutorials/fit-curve.html)

[官方 github 源码](https://github.com/tensorflow/tfjs-examples/tree/master/polynomial-regression-core)

[官方在线演示地址](https://storage.googleapis.com/tfjs-examples/polynomial-regression-core/dist/index.html)