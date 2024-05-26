## PPT1

大家好，今天由我来给大家讲解powell方法。

## PPT2

今天我讲解的内容包括9个部分，

1～3部分讲解powell基本算法，包括该算法的基本思想、具体的计算步骤，以及一道典型例题；

4～6部分讲解powell方法的二次终止性。包含3个定理的讲解，以及一道演示当搜索方向线性相关时，powell方法的弊端。

7～8部分讲解基于powell方法的弊端，改进的powell方法的定义，计算步骤，以及一道用改进的powell方法解决的例题。

第9部分，检测一下我的讲解效果以及大家对于powell方法的理解程度。

## PPT3

首先来对powell方法进行一个简单的介绍。

Powell 方法，又称 Powell 共轭方向法，是由 Michael J. D. Powell 提出的一种用于寻找函数局部最小值的算法。

该方法无需函数可导，也不依赖导数。要求目标函数是实值函数，且输入为固定维度的实值向量。Powell 方法通过沿每个搜索方向进行线性搜索来找到最优步长。

在每次迭代中，新的搜索方向会替换掉最成功的搜索方向。迭代过程会持续进行，直到函数值没有显著改进为止。Powell 方法特别适用于计算复杂连续函数的局部最小值，并且不依赖于函数的具体数学表达形式。

共轭方向的含义：

共轭方向（Conjugate Directions）是指在优化算法中，用于搜索函数极值的特殊方向。这些方向之间具有一种特殊的数学关系，使得在一个方向上搜索不会破坏在之前方向上已经取得的优化效果。在数值优化中，共轭方向可以加速收敛，特别是对于二次函数的最小化问题。

简单来说，共轭方向确保每次搜索都能有效地减少目标函数的值，而不会干扰前几步的成果。

右侧是powell方法的发明者—剑桥大学的Michael J.D. Powell教授，于2011年在中科院做报告的图片。

## PPT4

接下来介绍powell方法的基本思想和基本计算步骤。

基本思想为：......

基本计算步骤，我们可以边做例题边体会该基本计算步骤。

## PPT5

对照右侧的基本计算步骤，来解一下该例题。

在做该例题的同时，请大家带着这3个思考来进行例题的解答。

......

![](https://cdn.sa.net/2024/05/26/JgGeRImTutX1cYf.webp)

![](https://cdn.sa.net/2024/05/26/cCA2od618tkiamV.webp)

附：

思考题：

1、为啥在优化问题中使用列向量/转置矩阵？

a.位置明确

向量表示为列向量，有助于明确表示向量在多维空间中的位置

b.矩阵运算规范

矩阵加法或点积计算时，列向量的形式更直观和一致。
避免维度不匹配的问题.确保运算的正确性。

2、选择新方向为$d^{(n+1)} = x^{(n+1)} - x^{(1)}$的理由？

选择这个新方向的理由如下：
1. 综合搜索效果
新的方向d^3是从初始点x^1到当前点x^3的向量，它综合了前面两个方向上的搜索效果。通过沿这个方向搜索，我们能够进一步优化目标函数，并可能找到更好的点。
2. 保证线性无关性
更新后的方向d^3保证了搜索方向之间的线性无关性，从而避免了重复搜索已经探索过的路径，增加了搜索的效率。
3. 加快收敛速度
通过引入新的方向，可以更快地逼近目标函数的最小值，提升算法的收敛速度。

3、为啥计算梯度为0，也是停止迭代的依据？

![](https://cdn.sa.net/2024/05/23/yQJTjuWMH9EChdD.webp)

第一轮迭代结束后，没有停止迭代的原因：

原因小结：

![](https://cdn.sa.net/2024/05/26/3OTvj9aqKclRdu4.webp)

![](https://cdn.sa.net/2024/05/26/jyZQTelKoJLvz61.webp)

![](https://cdn.sa.net/2024/05/26/KLkMCaNzOib9vXe.webp)

## PPT6

例题8.2.1的完整解析见图示。

## PPT7

接下来，我们来看一下powell方法的二次终止性中的定理8.2.1，这个定理主要在讲：

![](https://cdn.sa.net/2024/05/26/ykMg7dtYfFSmXQz.webp)

我们来证明一下该定理。

![](https://cdn.sa.net/2024/05/26/bt4vABhNaIjH7rZ.webp)

梯度的推导过程和极小点条件：

![](https://cdn.sa.net/2024/05/26/8UfIevWzqliZwM5.webp)

![](https://cdn.sa.net/2024/05/26/nD7jNo3fhLHPXIk.webp)

![](https://cdn.sa.net/2024/05/26/wJOvkQglhcZBxYA.webp)

定理8.2.1有啥用呢？

![](https://cdn.sa.net/2024/05/26/RdhTVg4oDvNaAHe.webp)

## PPT8

接下来，我们来学习一下powell方法的二次终止性中的定理8.2.2，我们来证明一下该定理：

![](https://cdn.sa.net/2024/05/26/LqxP7AEQnv4Megl.webp)

![](https://cdn.sa.net/2024/05/26/PFHOEmCN4aiK9bk.webp)

![](https://cdn.sa.net/2024/05/26/pntMGWjNgcD7PXv.webp)

定理8.2.2有啥用呢？如果一个定理证明完，却发现该定理无处可用，那也挺没意思的。

![](https://cdn.sa.net/2024/05/26/NcTzBhDSnHt5Es1.webp)

![](https://cdn.sa.net/2024/05/26/AmcVT63iMgjZ1UD.webp)

定理8.2.1和定理8.2.2都提及到一个词—共轭，我们来讲解一下共轭是啥意思？

![](https://cdn.sa.net/2024/05/26/85eJ6hg17oqsUEX.webp)

## PPT9

接着，我们再学习一下powell方法的二次终止性中的定理8.2.3，

证明过程：

![](https://cdn.sa.net/2024/05/26/VRDPU4FdwTEJAjM.webp)

![](https://cdn.sa.net/2024/05/26/ctCz6vKTuQL4nbe.webp)

![](https://cdn.sa.net/2024/05/26/mhfFGiOQWD3Jk6K.webp)

有关powell方法二次终止性的结论：

![](https://cdn.sa.net/2024/05/26/8SHvmsBPCJN7f5y.webp)

我们来试着解答一下例题8.2.2

![](https://cdn.sa.net/2024/05/26/zqYbocFs2GHjU7T.webp)

![](https://cdn.sa.net/2024/05/26/IrzQ6jwOmA4JVuM.webp)

![](https://cdn.sa.net/2024/05/26/7AeoJRhztaYZ8cF.webp)

经过这道例题，相信大家对于“在powell方法中，保持n个搜索方向线性无关”的重要性有了进一步的理解。

## PPT10

例题8.2.2的完整解析见图示。

## PPT11

正是powell方法存在的这个缺陷，剑桥大学的Michael J.D. Powell教授本人及其他人对这个方法进行了修正，给出了改进的powell方法。

首先，介绍一下改进的powell方法与原本的powell方法的区别。

......

基本计算步骤，我们可以边做例题边体会该基本计算步骤。

## PPT11

我们来对照右侧的基本计算步骤来解一下该例题。

一开始求解梯度和hessian矩阵

![](https://cdn.sa.net/2024/05/26/TWlVHqu9MJn8mck.webp)

一维搜索步长的定义

![](https://cdn.sa.net/2024/05/26/awp47sYMBEHVhoU.webp)

![](https://cdn.sa.net/2024/05/26/raxO6PMjGcd5Byw.webp)

第一轮迭代

![](https://cdn.sa.net/2024/05/26/MTU78DpdoCyBRAO.webp)

![](https://cdn.sa.net/2024/05/26/GSgxIlAn94YFR2h.webp)

![](https://cdn.sa.net/2024/05/26/o9ZJdA8h4LQ7HgD.webp)

![](https://cdn.sa.net/2024/05/26/XPgTQrmMZR4jilh.webp)

第一轮迭代剩余部分解析：

![](https://cdn.sa.net/2024/05/26/QNuKSHmvhWXi1PG.webp)

![](https://cdn.sa.net/2024/05/26/H2yLSAMXbUpqzYe.webp)

第二轮迭代：

![](https://cdn.sa.net/2024/05/26/8oOfREe3gY56jhc.webp)

![](https://cdn.sa.net/2024/05/26/BtUCdHNYqg9flQx.webp)

![](https://cdn.sa.net/2024/05/26/jTweEkB6anUIpyM.webp)

## PPT12、13

例题8.2.3的完整解析见图示。

## PPT14

最后来检测一下我的讲解效果和大家对于powell方法的理解程度。