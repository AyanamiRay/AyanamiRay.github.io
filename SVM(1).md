<script type="text/javascript" async src="//cdn.bootcss.com/mathjax/2.7.0/MathJax.js?config=TeX-AMS-MML_HTMLorMML"></script>
<script type="text/javascript" async src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.1/MathJax.js?config=TeX-MML-AM_CHTML"></script>

### 函数间隔

$$\hat{\gamma_{i}}=y_{i}(w\cdot x_{i}+b)$$.函数间隔用来判定类别，如：假设超平面为：$$w\cdot x+b=0,\mid w\cdot x+b\mid $$可以相对表示$$x$$距离超平面的远近。对于二分类问题，如果$$w\cdot x+b>0$$,那么$$x$$的类别被判定为1，否则为-1.

### 几何间隔

$$\gamma_{i}=y_{i}(\frac{w}{\mid\mid w \mid\mid} \cdot x_{i}+\frac{b}{\mid\mid w \mid\mid})$$,几何间隔就是点到超平面的距离.

### 函数间隔设置为1

函数间隔为：$$\hat{\gamma_{i}}=y_{i}(w^{T}\cdot x_{i}+b)$$,两边同时除以$$\hat{\gamma}$$(前提是线性可分情况下，所以一定存在一个可以完全分开所有点的超平面，即$$\hat{\gamma}\neq 0$$)

从上面可以得到：$$y_{i}((\frac{w}{\hat{\gamma}})^{T}x_{i}+\frac{b}{\hat{\gamma}})=1$$,令$$W=(\frac{w}{\hat{\gamma}}),B=\frac{b}{\hat{\gamma}}$$

从而得到：$$y_{i}(W^{T}x_{i}+B)=1$$

例子：

假设存在平面：$$2x_{1}+4x_{2}-8=0$$,如果存在一个正样本$$y_{k}=+1$$,且函数间隔为$$\hat{\gamma}_{k}=2$$,即$$+1(2x^{k}_{1}+4x^{k}_{2}-8)=2$$

两边同时除以2可以得到：$$x^{k}_{1}+2x^{k}_{2}-4=1$$,虽然$$w,b$$同时缩小了两倍，函数间隔变为了1，但是超平面并没有改变，我们可以理解为如果成比例的改变$$w,b$$,虽然函数间隔改变了，但是超平面并没有改变，每个点的分类也没有改变！！！

[返回](./)