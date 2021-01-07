# LATEX数学公式学习笔记

最近开始学习《视觉计算基础》这一本书，顿觉用pad记笔记有些麻烦，我又太顾及笔记的美观程度，在Goodnotes上做笔记经常写两笔就修改一次，效率很低，更别提书中公式的笔记排版了。这样一来，用Typora来做笔记是个不错的选择。或许能让我抛弃掉那些花里胡哨的笔记排版，追求简洁和高效。为了更好地记笔记，学习一下Typora中数学公式的写法（Typora对[Latex](https://www.latex-project.org/)进行了很好的支持）。

<img src="D:\MyNote\image\image-20210107112606865.png" alt="image-20210107112606865" style="zoom:150%;" />

关于工具：Chorme有一款数学公式的插件很好用，它可以直接把网页中的公式识别并转化成Latex公式语言。在这里推荐一下。

![image-20210107104911133](D:\MyNote\image\chormeMathTool)

如果是实在太复杂的公式可以拍照传到网页上让它自动识别一下，复制粘贴，岂不美哉？

![image-20210107143548114](D:\MyNote\image\image-20210107143548114.png)



[TOC]



## 1.LaTex基本语法元素

学习一门新的语言，最好先了解一下它的语法元素和结构特性。

### 1.1 数学公式的两种形式

- 公式块

写法：

```latex
$$
a^2+b^2=c^2
$$
```

$$
a^2+b^2=c^2
$$


- 行内公式

写法：先按$，再按esc

```latex
随着$a$增大，$a^2$不一定增大
```

效果：随着$a$增大，$a^2$不一定增大



### 1.2 常用的公式及代码

此处参照知乎用户点点星河的文章，将其中的表格公式又手敲了一遍加深记忆。附上链接：https://zhuanlan.zhihu.com/p/261750408?utm_source=wechat_session

#### 1.2.1 上下标和正负无穷

| 数学表达式 |  LaTex  |
| :--------: | :-----: |
|   $x^2$    |   x^2   |
|   $y_1$    |   y_1   |
|  $\infty$  | \infty  |
| $-\infty$  | -\infty |



#### 1.2.2 加减乘，分式，根号，省略号

|  数学表达式   |    LaTex    |
| :-----------: | :---------: |
|   $a+b-c*d$   |   a+b-c*d   |
|  $a\div{b}$   |  a\div{b}   |
|   $a\pm{b}$   |   a\pm{b}   |
| $\frac{a}{b}$ | \frac{a}{b} |
|  $\sqrt{b}$   |  \sqrt{b}   |
|   $\cdots$    |   \cdots    |



#### 1.2.3 三角函数

|   数学表达式   |    LaTex     |
| :------------: | :----------: |
| $\sin{\theta}$ | \sin{\theta} |
| $\cos{\theta}$ | \cos{\theta} |
| $\tan{\theta}$ | tan{\theta}  |
| $\cot{\theta}$ | \cot{\theta} |



#### 1.2.4 矢量，累加，累乘，极限

|            数学表达式             |              LaTex              |
| :-------------------------------: | :-----------------------------: |
|             $\vec{F}$             |             \vec{F}             |
|       $\sum_{i=1}^{n}{a_i}$       |       \sum_{i=1}^{n}{a_i}       |
|      $\prod_{i=1}^{n}{a_i}$       |      \prod_{i=1}^{n}{a_i}       |
| $\lim_{a\rightarrow+\infty}{a+b}$ | \lim_{a\rightarrow+\intfy}{a+b} |



#### 1.2.5 希腊字母

|  数学表达式   |    LaTex    |
| :-----------: | :---------: |
|   $\alpha$    |   \alpha    |
|    $\beta$    |    \beta    |
|   $\gamma$    |   \gamma    |
|   $\delta$    |   \delta    |
|  $\epsilon$   |  \epsilon   |
| $\varepsilon$ | \varepsilon |
|    $\eta$     |    \eta     |
|   $\theta$    |   \theta    |
|   $\kappa$    |   \kappa    |
|    $\iota$    |    \iota    |
|    $\zeta$    |    \zeta    |
|   $\lambda$   |   \lambda   |
|     $\mu$     |     \mu     |
|    $\phi$     |    \phi     |
|     $\pi$     |     \pi     |
|    $\rho$     |    \rho     |
|     $\xi$     |     \xi     |
|     $\nu$     |     \nu     |
|  $\upsilon$   |  \upsilon   |
|   $\varphi$   |   \varphi   |
|    $\chi$     |    \chi     |
|    $\psi$     |    \psi     |
|   $\omega$    |   \omega    |



#### 1.2.5 关系运算符

| 数学表达式 | LaTex |
| :--------: | :---: |
|   $\leq$   | \leq  |
|   $\geq$   | \geq  |



#### 1.2.6 矩阵和行列式


```latex
写法：\begin{matrix}...\end{matrix}
\\表示换行
元素用 & 表示间隔
\tag{1}表示序号

$$
\begin{matrix}
1	&2	&3	\\
4	&5	&6	\\
7	&8	&9
\end{matrix}\tag{1}
$$
```


$$
\begin{matrix}
1&2&3\\
4&5&6\\
7&8&9
\end{matrix}\tag{1}
$$

##### 大中小括号矩阵

```latex
法一：在前后分别添加左右括号的代码
{[()]}
$$
\left\{\begin{matrix}
1&2&3\\
4&5&6\\
7&8&9
\end{matrix}
\right\}\tag{2}
$$

法二：改matrix为{Bmatrix}或{bmatrix}
$$
\begin{Bmatrix}
1&2&3\\
4&5&6\\
7&8&9
\end{Bmatrix}\tag{3}
$$
```


$$
\left(\begin{matrix}
1&2&3\\
4&5&6\\
7&8&9
\end{matrix}
\right)\tag{2}
$$

$$
\begin{bmatrix}
1&2&3\\
4&5&6\\
7&8&9
\end{bmatrix}\tag{3}
$$

$$
\begin{Bmatrix}
1&2&3\\
4&5&6\\
7&8&9
\end{Bmatrix}\tag{4}
$$



##### 包含希腊字母和省略号

- 列省略号 \vdots    $\vdots$
- 行省略号 \cdots    $\cdots$
- 斜省略号 \ddots   $\ddots$

```latex
$$
 \left\{
 \begin{matrix}
 1      & 2        & \cdots & 5       \\
 6      & 7        & \cdots & 10      \\
 \vdots & \vdots   & \ddots & \vdots  \\
 \alpha & \alpha+1 & \cdots & \alpha+4 
 \end{matrix}
 \right\}
$$
```


$$
\left\{
 \begin{matrix}
 1      & 2        & \cdots & 5        \\
 6      & 7        & \cdots & 10       \\
 \vdots & \vdots   & \ddots & \vdots   \\
 \alpha & \alpha+1 & \cdots & \alpha+4 
 \end{matrix}
 \right\}
$$


##### 行列式

原理同上

```latex
$$
X=\left|
 \begin{matrix}
 x_{11}      & x_{12}       & \cdots & x_{1d}       \\
 x_{21}      & x_{22}        & \cdots & x_{2d}      \\
 \vdots & \vdots   & \ddots & \vdots  \\
 x_{m1} & x_{m2} & \cdots & x_{md} 
 \end{matrix}
 \right|
 $$
```


$$
X=\left|
 \begin{matrix}
 x_{11}      & x_{12}       & \cdots & x_{1d}       \\
 x_{21}      & x_{22}        & \cdots & x_{2d}      \\
 \vdots & \vdots   & \ddots & \vdots  \\
 x_{m1} & x_{m2} & \cdots & x_{md} 
 \end{matrix}
 \right|
$$

#### 1.2.7 方程组，条件表达式

##### 方程组

```latex
用cases
$$
\begin{cases}
3x + 5y +  z \\
7x - 2y + 4z \\
-6x + 3y + 2z
\end{cases}
$$
```

$$
\begin{cases}
3x + 5y +  z \\
7x - 2y + 4z \\
-6x + 3y + 2z
\end{cases}
$$

##### 条件表达式

```latex
$$
f(n) =
\begin{cases} 
n/2,  & \text{if }n\text{ is even} \\
3n+1, & \text{if }n\text{ is odd}
\end{cases}
$$
```

$$
f(n) =
\begin{cases} 
n/2,  & \text{if }n\text{ is even} \\
3n+1, & \text{if }n\text{ is odd}
\end{cases}
$$



## 笔记更新：2020/1/7

Name:Elmando

Email:1091992414@qq.com