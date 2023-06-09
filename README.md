# 0. 引入

层次分析法主要用于选A还是选B的问题。

# 1. 问题
假设小冯要去旅游，有三个备选地点：苏杭、北戴河、桂林。怎么选？
小冯个人主要考虑的旅游目的入选要素：景色、花费、居住、饮食、交通。

# 2. 思路
## 2.1 首先考虑5个要素那个比较重要，两两比较进行赋分，重要程度分别用数字1~9表示
![图1 考虑要素重要程度分级表](https://img-blog.csdnimg.cn/ac8c3804e6784a0b80ea38dadea1a2f9.png)
## 2.2 两两比较要素后得到要素的**判断矩阵**

![图2 判断矩阵](https://img-blog.csdnimg.cn/25393d76ad114cc2a434099594cac957.png)
## 2.3  两两比较旅游地后，得到旅游地的要素的**判断矩阵**
![要素判断矩阵](https://img-blog.csdnimg.cn/4cfe6581a2d3455fae2189cf461860d9.png)![在这里插入图片描述](https://img-blog.csdnimg.cn/02a15ff5e6094e5281a38666bb57c217.png)
![旅游目的地判断矩阵](https://img-blog.csdnimg.cn/035ebbe18bd048cd91246127c857bceb.png)
> 这里需要有一个注意的地方，比如判断景色：苏杭>北戴河，苏杭=桂林，北戴河>桂林，这样就会出现矛盾，也为下一步一致性检验埋下伏笔

## 2.4  一致性检验

> 这里一致性检验的方法感觉没有一棍子打死，按道理来说一个矩阵是否是一致矩阵，只需要判断其最大特征值是否等与$n$（$n$为维度）。但在实际计算中，允许有一定偏离。以上纯属个人理解，因为我对特征值和特征向量理解不够深入。

![在这里插入图片描述](https://img-blog.csdnimg.cn/576c1e245c18469d8a40133ea5cd9b00.png)
## 2.5  通过一致性检验以后，就可以计算得到权重。

1、算术平均法

![在这里插入图片描述](https://img-blog.csdnimg.cn/f7ab6cae453b4eaf88797f3e6e9037ca.png)

2、几何平均法

![在这里插入图片描述](https://img-blog.csdnimg.cn/21d4a37749f747b2a5fe10470cee2066.png)


3、特征值法

![在这里插入图片描述](https://img-blog.csdnimg.cn/49e1756e638d4010b1b3c8101f9d89d4.png)
##  2.6 将某种方法（如特征值法）计算的权重填入权重矩阵，相乘获得旅游地得分
![在这里插入图片描述](https://img-blog.csdnimg.cn/7fc5c687b538420bb1c3e2c1a59f30b8.png)
# 3. 流程图
   ![在这里插入图片描述](https://img-blog.csdnimg.cn/bcfd069299c64c33ba63d62be9c6c0c6.png#pic_center)

> 资料数据来源：“数学建模学习交流”

