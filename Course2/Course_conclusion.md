# Pandas

## The Series

Recording my work about Pandas，in a real example.

It is an example about the data of climates,. My purpose is to get the Max and Min temperature of some stations during 2004-2014 except the leap days. After that turn these data into a line graph with record high and record low.

### First

merge two datasets, one is about the location information and the other is about the temperature information. 

pandas code , when we have two datasets and want to merge them together, the first step is to take a look of them. 

`df.head()`is a term to display top five rows of the dataframe

when we are sure about the dataframe , now merge them!

```python
# these are pandas code
import pandas as pd
# there are two dataframes, df1 and df2
pd.merge(left=df1,right=df2, how='inner',left_on = , right_on= )
```

A simple instance above, `pd.merge()`is a very powerful function in pandas.

i conclusion the usage and some parameters of this function

#### pd.merge()

it is a database-style join operation, and it takes many parameters.

`DataFrame.merge`(*right*, *how='inner'*, *on=None*, *left_on=None*, *right_on=None*, *left_index=False*, *right_index=False*, *sort=False*, *suffixes=('_x'*, *'_y')*, *copy=True*, *indicator=False*, *validate=None*)[[s]](http://github.com/pandas-dev/pandas/blob/v0.23.4/pandas/core/frame.py#L6379-L6389)

a part of official documention

right: DateFrame # 就是说右边连接的是那个dataframe, 其实这个函数还可以这么写

`pandas.merge(*left, right*,  *how='inner'*, *on=None*, *left_on=None*, *right_on=None*, *left_index=False*, *right_index=False*, *sort=False*, *suffixes=('_x'*, *'_y')*, *copy=True*, *indicator=False*, *validate=None*)

第一种写法就是 A.merge(right=B), 第二种写法，pandas.merge(left=A, right=B),效果是一样的。

left_on, right_on:	左侧表或右侧表的一个column or index.

left_index, right_index: 左侧或右侧的index

sort : 是否排序

suffixes : 用于修改重名的列， 比如左右都叫x 那么就添加一个后缀

copy:   ***i'm not clear about it***

indicator: ***i have never use it***

validate: ***not clear***

***







