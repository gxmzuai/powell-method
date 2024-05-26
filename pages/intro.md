## Powell方法的简单介绍

<div grid="~ cols-2 gap-4">


<div class="mt-5 text-sm">

Powell 方法，又称 Powell 共轭方向法，是由 Michael J. D. Powell 提出的一种用于寻找函数局部最小值的算法。

该方法无需函数可导，也不依赖导数。要求目标函数是实值函数，且输入为固定维度的实值向量。Powell 方法通过沿每个搜索方向进行线性搜索来找到最优步长。

在每次迭代中，新的搜索方向会替换掉最成功的搜索方向。迭代过程会持续进行，直到函数值没有显著改进为止。Powell 方法特别适用于计算复杂连续函数的局部最小值，并且不依赖于函数的具体数学表达形式。

</div>

<div text-sm>

![](https://cdn.sa.net/2024/05/23/4g371PC6ZpXroei.webp)


<center> Michael Powell at the Chinese Academy of Sciences, 2011</center>

</div>

</div>