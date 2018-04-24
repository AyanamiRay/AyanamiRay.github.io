<script type="text/javascript" async src="//cdn.bootcss.com/mathjax/2.7.0/MathJax.js?config=TeX-AMS-MML_HTMLorMML"></script>
<script type="text/javascript" async src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.1/MathJax.js?config=TeX-MML-AM_CHTML"></script>

### numpy.random.random() 

生成随机浮点数

默认为生成一个随机浮点数，范围在$$0.0~1.0$$之间，可以通过设置size大小来设置返回数据的size

例子：

```python
import numpy as np 
n = np.random.random(size=(3,2))
```

### numpy.random.randint() 

生成随机整数

例子：

```python
import numpy as np
np.random.randint(8)
np.random.randint(5,size=3)
np.random.randint(low=5,high=10,size=3)#指定数的范围
```

### numpy.random.normal() 

高斯分布随机数

```python
normal(loc=0.0,scale=1.0,size=None)#loc均值 scale标准差 size 抽取样本的大小
```

### numpy.random.randn() 标准正态分布随机数

```python
import numpy as np
np.random.randn(4,2)
np.random.randn(4,2,3)
```

输出：

```
array([[-0.55800561,  0.50180528],
       [-0.2752747 , -0.1842792 ],
       [-1.38661732, -1.74695498],
       [ 1.34619662,  0.00197361]])
array([[[ 1.07024399,  1.15906395, -0.77406374],
        [-1.68423637, -0.20105249,  0.82418734]],

       [[-0.01086779, -0.39478289,  0.54466447],
        [-0.55131755,  0.80784033, -1.82454347]],

       [[ 0.15592497, -1.38745656, -0.40163218],
        [-0.41206824, -1.64512154, -0.53148108]],

       [[-0.26017423,  2.14275606, -0.23313072],
        [-0.753638  ,  0.50768485,  0.11476454]]])
```

### numpy.random.rand() 

生成$$[0,1)$$间随机数

```python
import numpy as np
np.random.rand(2,3)
```

### numpy.random.shuffle() 

随机打乱序列

```python
import numpy as np
x = np.arange(0,8,1)
np.random.shuffle(x)
```
```
array([0, 1, 2, 3, 4, 5, 6, 7])

array([7, 5, 1, 2, 0, 6, 3, 4])
```

### numpy.random.choice() 随机选取序列的一个元素

可以从序列（字符串，列表，元组等）中随机选取，返回一个列表，元组或字符串的随即项

```python
import numpy as np
np.random.choice(['a','b','c','d'])
np.random.choice(5,6)#输出六个小于5的元素
np.random.choice(5,3,p=[0.1,0,0.3,0.6,0])#p表示出现0，1，2，3，4的概率为0.1，0，0.3，0.6，0
```
### np.random.bytes(length)

返回随机字节

### np.random.seed()

seed()用于指定随机数生成时所用算法开始的整数值，如果使用相同的seed()值，则每次生成的随机数都相同，如果不设置这个值，则系统根据时间来自己选择这个值，此时每次生成的随机数因时间差异而不同。

```python
import numpy as np
num=0
while(num<5):
  random.seed(5)
  print(random.random())
  num+=1
```

输出：

```
0.22199317108973948
0.22199317108973948
0.22199317108973948
0.22199317108973948
0.22199317108973948
```

### 分布

| beta(a,b[,size]) | 贝塔分布样本，在[0,1]内 |
| binomial(n,p[,size]) | 二项分布样本|
| chisquare(df[,size]) | 卡方分布样本 |
| dirichlet(alpha[,size]) | 狄利克雷分布样本 |
| exponential([scale,size]) | 指数分布 |
| f(dfnum,dfden[,size]) | F分布样本 |
| gamma(shape[,scale,size]) | 伽马分布 |
| geometric(p[,size]) | 几何分布 |
| gumbel([loc,scale,size]) | 耿贝尔分布 |
| hypergeometric(ngood,nbad,nsample[],size) | 超几何分布样本 |
| laplace([loc,scale,size]) | 拉普拉斯分布样本 |
| logistic([loc,scale,size]) | Logistic分布样本 |
| lognormal([mean,sigma,size]) | 对数正态分布 |
| logseries(p[,size]) | 对数级数分布 |
| multinomial(n,pvals[,size]) | 多项分布 |
| multivariate_normal(mena,cov[,size]) | 多元正态分布 |
| negative_binomial(n,p[,size]) | 负二项分布 |
| noncentral_chisquare(df,nonc[,size]) | 非中心卡方分布 |
| noncentral_f(dfnum,dfden,nonc[,size]) | 非中心F分布 |
| normal([loc,scale,size]) | 正态（高斯）分布 |
| pareto(a[,size]) | 帕累托分布 |
| poisson([lam,size]) | 泊松分布 |
| power(a[,size]) | draws samples in [0,1] from a power distribution with positive exponent at -1 |
| rayleigh([scale,size]) | rayleigh分布 |
| standard_cauchy([size]) | 标准柯西分布 |
| standard_exponential([size]) | 标准指数分布 |
| standard_gamma(shape[,size]) | 标准伽马分布 |
| standard_normal([size]) | 标准正态分布 |
| standard_t(df[,size]) | Standard sthdent‘s distribution with df degrees of freedom |
| triangular(left,mode,right[,size]) | 三角形分布 |
| uniform([low,high,size]) | 均匀分布 |
| vonmises(mu,kappa[,size]) |von Mises分布 |
| wald(mean,scale[,size]) |瓦尔德（逆高斯）分布 |
| weibull(a[,size]) | Weibull分布 |
| zipf(a[,size]) | 齐普夫分布 |


[返回](./)