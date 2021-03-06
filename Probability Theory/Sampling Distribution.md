# 抽样分布    

## 总体      

总体必须是由两个或两个以上的个体构成的，根据包含个体的数目可以将总体分为有限总体和无限总体。     

统计问题所研究的对象的全体称为总体，总体可以由一个随机变量及其分布来描述。(统计学中视总体、总体的分布为同义词)       

## 样本    

从总体中抽取一部分出来个体构成样本(不同的抽样方法构成不同的样本)     

样本具有两重性：   

* 在抽样前，样本看作是随机变量    

* 完成抽样后，样本看作是具体的数      

若已知总体和其分布函数，同时知道样本，则样本的联合分布律为各个样本分布函数的连乘。     

若总体的分布为连续型的，可求出概率密度函数，则样本的联合密度函数为各个样本密度函数的连乘。     


### 简单随机样本    

* 代表性：    

总体中的每个样本由同等的机会被抽入样本，每个个体与总体具有相同的分布。    

* 独立性：   

样本中每个个体的取值不影响其他样本的取值，样本中的各个个体之间都是相互独立的。     

我们常说的有放回的抽取就属于简单随机样本，对无放回抽样来说，当总体的数目相当大或为无限总体，则抽样也可看作是简单随机样本。       


## 抽样分布    

有了总体和样本的概念后，就可以提出统计量的概念，统计量就是抽样分布中我们具体研究的对象。     

统计量是样本的实值函数，它完全取决于样本，且函数中不能存在未知参数，样本均值、样本方差、样本矩都是统计量。     

我们根据实际问题的不同，对样本进行适当的统计量函数设计，研究设计出来的统计量的分布，来估计总体的情况。      

因为样本本身就是随机变量，统计量是样本的函数，所以统计量也是随机变量，也具有确定的概率分布，统计量的概率分布称为抽样分布。           

## 自由度      

在统计学中，在计算一个统计量时，取值不受限制的变量个数。当以样本的统计量来估计总体的参数时，样本中独立或者能自由变化的自变量的个数，称为自由度。通常`df=n-k`。其中`n`为样本数量，`k`为被限制的条件数或变量个数，或计算某一统计量时用到其它独立统计量的个数。自由度通常用于抽样分布中。      

* 估计均值时     

使用样本估计总体均值时，由于样本中的n个数据都是独立的，所以从中拿走任意一个都不会影响其他数据，所以这时的自由度是n。     

* 估计方差时     

使用样本估计总体的方差时，采用样本与均值差的平方和来确定，因为我们首先要明确样本的均值，这时如果我们清楚了`n-1`个数据，那根据均值我们也能确定最后一个数据，所以，这里均值就是一个限制条件，这时的自由度也就是`n-1`         


## 分位点(数)     

抽样分布主要研究的是一些连续性随机变量的函数的分布，常见的有正态分布、chi2分布、t分布和f分布等，这几大分布的概率密度函数是非常复杂的，如果我们需要计算它们的概率的话，不是一件简单的事情，所以数学家已经把一些常见的概率计算好了制成了表，我们只需要查表寻找概率就可以了。      

分位数在区间估计中也有相当大的作用。

在查表的时候就需要使用分位点的概念，我们可以先将随机变量统计量的分布函数画出来，然后横轴就是各个样本点，纵轴就是对应的概率。      

* 定义     

设F(x)为一概率分布函数，0<α<1,且有λ，使得：    

`P{X <= λ} = F(λ) = α`        

则称α是F(x)的分位数(下侧分位数)，可以理解为在x=λ点处，随机变量的概率取到α。      

* 例子     

X~N(0,1)，那么标准正态分布的α分位数μα(μα专门表示标准正态分布的α分位数)满足：    

`Φ(μα) = ∫ 1/√￣2Π e^-x^2/2 dx = α`      
哦里，
又根据正态分布的对称性，有:`-μα = u1-α`           

* 上侧分位数    

默认的定义中，分位数根据概率式的不等于号的方向确定为下侧分位数，表示位于分位点内侧的区域，相反：     

`P{X > λ} = α`     

则λ为X分布的上侧分位数，表示λ以外的区域的概率。    

显然`P{X <= λ} = 1 - P{X > λ} = 1 - α`      

即λ为原分布的`1-α`分位数。     

**上侧分位数计算时需要使用`1 - λ`转换成默认形式的下侧分位数才能去查表**       

* 双侧分位数       

设有`P{|T| > λ} = α`,记`λ = tα/2(n)`          

称为自由度为n的t分布双侧α分位数。    
