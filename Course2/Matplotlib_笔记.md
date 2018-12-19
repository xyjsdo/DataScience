# Matplotlib

matplotlib是一个python的绘图库，支持2D和3D，主要是2D。

## 主要架构

### BACK END(后端层)

提供了抽象接口类的具体实现，例如：

`FigureCanvas`这封装了要一个画布

`Renderer` 绘图对象（画笔）

`Event`处理用户输入，如键盘事件和鼠标事件(有点类似JS，H5里的EVENT事件):

​	*pick* 取数据点的一个方法

​	当然还有很多其他方法，以后再补充



### Artist layer (艺术层)

Artist是matplotlib的一个中间层，这里提供了很多的方法，比如说，`Figure`是Artist的一个实例，

![img](http://www.aosabook.org/images/matplotlib/artists_tree.png)

在Figure之上就是各种其他的对象了，都是属于Artist层的。

### Script layer (脚本层)

脚本层，说白了其实就是 matplotlib.pyplot, 这个子库，它对下面两层做了一个封装

一个`matplotlib.pyplot.plot`的例子，以说明pyplot函数如何在matplotlib的面向对象核心中进行封装功能。

```python
@autogen_docstring（Axes.plot）
def plot（* args，** kwargs）：
    ax = gca（）

    ret = ax.plot（* args，** kwargs）
    draw_if_interactive（）

    return ret		
```

****

以上是对Matplotlib这个库的基础原理的一些简单的解释，那么在实际的实践过程中，还有很多很多很多的函数，方法需要进行学习，需要进行记录。

***

那么关于二维图，我也简单做几个介绍与总结。

### 散点图

```python
import matplotlib.pyplot as plt
plt.figure()
plt.scatter(x,y)
```

***一些python的技巧***

```python
zip([],[]) #zip函数将两个列表转换成，一个列表，并且其中的元素就是一个个的元组，
# e.g. zip([1,2,3,4,5],[6,7,8,9,10])
# $: [(1, 6), (2, 7), (3, 8), (4, 9), (5, 10)]

```



### 折线图

```
plt.
```



### 条形图



### 分组图 Subplots



### 直方图

### 箱型图

### 热图









