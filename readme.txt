这是一篇论文的仿真，论文题目是Class-Dependent Sparse Representation Classifier for Robust Hyperspectral Image Classification
效果并不是很好，只是实现基本功能，参数设置还有待仔细调整。

一共10个.m文件，各自作用简单介绍如下（实际上只用到了下面第一部分的七块代码）：

cdSRC.m  主程序
normalize_data.m  用来对原始数据归一化
lda.m  用来对原始数据进行降维
select_train_data.m  用来按比例选择训练样本
select_train_data1.m  用来按个数选择训练样本
OMP.m  用来在cdOMP过程中得到关于每类的稀疏矩阵，进而求得残差作为相关度信息
cdKNN.m  用来进行cdKNN得到欧氏距离信息

cdOMP.m 和 gradient_descent.m 是用梯度下降法求解cdOMP中的优化公式，超慢超慢，几乎不能用，但其实能跑出来，没舍得删
LFDA.m 一开始降维用的这个，正确率一直上不了80，但是看了看代码找不到错误。梁云龙师兄给换了个lda，就好了。


放了几个数据集是因为正确率超低时，怀疑是数据的问题，就重找了数据，发现不是数据的影响，也没删，留这儿了。