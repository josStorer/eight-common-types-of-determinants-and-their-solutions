# 八大常见类型的行列式及其解法

>[原文地址及作者](https://zhuanlan.zhihu.com/p/34685081)
>
>已整合调整原文中的一些问题
>
>本文记录了八大常见类型的行列式及其解法,解法从一般性到特殊性都有,分享给大家,例子都特别经典好用,希望对线代、高代初学者以及考研党有用.
>
>关于一些解法步骤有童鞋表示看不懂,我的建议是顺着文章顺序一个一个题往下看,有些地方需要你跟着文章自己用笔写一下.因为有些题用到了前题的结论,有些步骤做了精简.还是那句话,看是看不懂的,写一写才能懂.

**类型总览:**

1. [箭型行列式](#%E4%B8%80%E7%AE%AD%E5%9E%8B%E8%A1%8C%E5%88%97%E5%BC%8F--------------------%E8%BF%94%E5%9B%9E%E7%9B%AE%E5%BD%95)
2. [两三角型行列式](#%E4%BA%8C%E4%B8%A4%E4%B8%89%E8%A7%92%E5%9E%8B%E8%A1%8C%E5%88%97%E5%BC%8F--------------------%E8%BF%94%E5%9B%9E%E7%9B%AE%E5%BD%95)
3. [两条线型行列式](#%E4%B8%89%E4%B8%A4%E6%9D%A1%E7%BA%BF%E5%9E%8B%E8%A1%8C%E5%88%97%E5%BC%8F--------------------%E8%BF%94%E5%9B%9E%E7%9B%AE%E5%BD%95)
4. [范德蒙德型行列式](#%E5%9B%9B%E8%8C%83%E5%BE%B7%E8%92%99%E5%BE%B7%E5%9E%8B%E8%A1%8C%E5%88%97%E5%BC%8F--------------------%E8%BF%94%E5%9B%9E%E7%9B%AE%E5%BD%95)
5. [Hessenberg型行列式](#%E4%BA%94%E5%9E%8B%E8%A1%8C%E5%88%97%E5%BC%8F--------------------%E8%BF%94%E5%9B%9E%E7%9B%AE%E5%BD%95)
6. [三对角型行列式](#%E5%85%AD%E4%B8%89%E5%AF%B9%E8%A7%92%E5%9E%8B%E8%A1%8C%E5%88%97%E5%BC%8F--------------------%E8%BF%94%E5%9B%9E%E7%9B%AE%E5%BD%95)
7. [各行元素和相等型行列式](#%E4%B8%83%E5%90%84%E8%A1%8C%E5%85%83%E7%B4%A0%E5%92%8C%E7%9B%B8%E7%AD%89%E5%9E%8B%E8%A1%8C%E5%88%97%E5%BC%8F--------------------%E8%BF%94%E5%9B%9E%E7%9B%AE%E5%BD%95)
8. [相邻两行对应元素相差K倍型行列式](#%E5%85%AB%E7%9B%B8%E9%82%BB%E4%B8%A4%E8%A1%8C%E5%AF%B9%E5%BA%94%E5%85%83%E7%B4%A0%E7%9B%B8%E5%B7%AEk%E5%80%8D%E5%9E%8B%E8%A1%8C%E5%88%97%E5%BC%8F--------------------%E8%BF%94%E5%9B%9E%E7%9B%AE%E5%BD%95)

**方法总览:**

1. 拆行法
2. 升阶法
3. 方程组法
4. 累加消点法
5. 累加法
6. 递推法（特征方程法）
7. 步步差法

## 一:箭型行列式 ------------------> [返回目录](#%E5%85%AB%E5%A4%A7%E5%B8%B8%E8%A7%81%E7%B1%BB%E5%9E%8B%E7%9A%84%E8%A1%8C%E5%88%97%E5%BC%8F%E5%8F%8A%E5%85%B6%E8%A7%A3%E6%B3%95)

最常见最常用的行列式,特征很好辨识,必须掌握,请看下例(空白处都为0):

<div><p align="center">
<img src="http://latex.codecogs.com/gif.latex?eg%3AD_n%3D%5Cbegin%7Bbmatrix%7D%20x_1%261%261%20%26...%20%261%5C%5C%201%26x_2%26%26%26%5C%5C%201%26%26x_3%5C%5C%20...%26%26%26...%5C%5C%201%26%26%26%26x_n%20%5Cend%7Bbmatrix%7D"/>
</p></div>

<img src="http://latex.codecogs.com/gif.latex?Solution"/>:
将第一列元素依次减去第<img src="http://latex.codecogs.com/gif.latex?i"/> 列的<img src="http://latex.codecogs.com/gif.latex?\frac{1}{x_i},i=2...n"/>

得:

<div><p align="center">
<img src="http://latex.codecogs.com/gif.latex?D_n%3D%5Cbegin%7Bbmatrix%7D%20x_1-%5Cfrac%7B1%7D%7Bx_2%7D-...-%5Cfrac%7B1%7D%7Bx_n%7D%261%261%20%26...%20%261%5C%5C%200%26x_2%26%26%26%5C%5C%200%26%26x_3%5C%5C%20...%26%26%26...%5C%5C%200%26%26%26%26x_n%20%5Cend%7Bbmatrix%7D"/>
</p></div>

所以:

<div><p align="center">
<img src="http://latex.codecogs.com/gif.latex?D_n=\prod_{i=2}^{n}x_i(x_1-\sum_{i=2}^{n}\frac{1}{x_i})"/>
</p></div>

## 二:两三角型行列式 ------------------> [返回目录](#%E5%85%AB%E5%A4%A7%E5%B8%B8%E8%A7%81%E7%B1%BB%E5%9E%8B%E7%9A%84%E8%A1%8C%E5%88%97%E5%BC%8F%E5%8F%8A%E5%85%B6%E8%A7%A3%E6%B3%95)

### 1.特征为对角线上方元素均为<img src="http://latex.codecogs.com/gif.latex?a"/> ,下方元素均为<img src="http://latex.codecogs.com/gif.latex?b"/>

当 <img src="http://latex.codecogs.com/gif.latex?a=b"/>  时可化为箭型行列式计算,当 <img src="http://latex.codecogs.com/gif.latex?a\not=b"/> 时采用**拆行法**计算,请看下面两例

<div><p align="center">
<img src="http://latex.codecogs.com/gif.latex?eg1%28a%3Db%29%3AD_n%3D%5Cbegin%7Bbmatrix%7D%20x_1%26b%26b%20%26...%20%26b%5C%5C%20b%26x_2%26b%26...%26b%5C%5C%20b%26b%26x_3%26...%26b%5C%5C%20...%26...%26...%26...%26...%5C%5C%20b%26b%26b%26...%26x_n%20%5Cend%7Bbmatrix%7D"/>
</p></div>

<img src="http://latex.codecogs.com/gif.latex?Solution"/>: 将第<img src="http://latex.codecogs.com/gif.latex?i,i=2...n"/> 行都减去第一行 得:
<div><p align="center">
<img src="http://latex.codecogs.com/gif.latex?D_n%3D%5Cbegin%7Bbmatrix%7D%20x_1%26b%26b%20%26...%20%26b%5C%5C%20b-x_1%26x_2-b%260%26...%260%5C%5C%20b-x_1%260%26x_3-b%26...%260%5C%5C%20...%26...%26...%26...%26...%5C%5C%20b-x_1%260%260%26...%26x_n-b%20%5Cend%7Bbmatrix%7D"/>
</p></div>

即化成了箭型行列式,所以:

<div><p align="center">
<img src="http://latex.codecogs.com/gif.latex?D_n%3D%5B%5Cprod_%7Bi%3D2%7D%5E%7Bn%7D%28x_i-b%29%5D%5Ctimes%5Bx_1-b%28b-x_1%29%5Csum_%7Bi%3D2%7D%5E%7Bn%7D%5Cfrac%7B1%7D%7Bx_i-b%7D%5D"/>
</p></div>

***

<div><p align="center">
<img src="http://latex.codecogs.com/gif.latex?eg2%28a%5Cnot%3Db%29%3AD_n%3D%5Cbegin%7Bbmatrix%7D%20x_1%26a%26a%20%26...%20%26a%5C%5C%20b%26x_2%26a%26...%26a%5C%5C%20b%26b%26x_3%26...%26a%5C%5C%20...%26...%26...%26...%26...%5C%5C%20b%26b%26b%26...%26x_n%20%5Cend%7Bbmatrix%7D"/>
</p></div>

<img src="http://latex.codecogs.com/gif.latex?Solution"/>:  采用拆行法,目的是为了降阶

<div><p align="center">
<img src="http://latex.codecogs.com/gif.latex?D_n%3D%5Cbegin%7Bbmatrix%7D%20x_1%26a%26a%20%26...%20%26a&plus;0%5C%5C%20b%26x_2%26a%26...%26a&plus;0%5C%5C%20b%26b%26x_3%26...%26a&plus;0%5C%5C%20...%26...%26...%26...%26...%5C%5C%20b%26b%26b%26...%26x_n&plus;b-b%20%5Cend%7Bbmatrix%7D"/>
</p></div>

<div><p align="center">
<img src="http://latex.codecogs.com/gif.latex?D_n%3D%5Cbegin%7Bbmatrix%7D%20x_1%26a%26a%20%26...%20%26a%5C%5C%20b%26x_2%26a%26...%26a%5C%5C%20b%26b%26x_3%26...%26a%5C%5C%20...%26...%26...%26...%26...%5C%5C%20b%26b%26b%26...%26b%20%5Cend%7Bbmatrix%7D_%7B%28*%29%7D&plus;%20%5Cbegin%7Bbmatrix%7D%20x_1%26a%26a%20%26...%20%260%5C%5C%20b%26x_2%26a%26...%260%5C%5C%20b%26b%26x_3%26...%260%5C%5C%20...%26...%26...%26...%26...%5C%5C%20b%26b%26b%26...%26x_n-b%20%5Cend%7Bbmatrix%7D"/>
</p></div>

将<img src="http://latex.codecogs.com/gif.latex?(*)"/>第 <img src="http://latex.codecogs.com/gif.latex?i,i=1...n-1"/> 列都减去最后一列,得:

<div><p align="center">
<img src="http://latex.codecogs.com/gif.latex?D_n%3D%5Cbegin%7Bbmatrix%7D%20x_1-a%260%260%20%26...%20%26a%5C%5C%20b-a%26x_2-a%260%26...%26a%5C%5C%20b-a%26b-a%26x_3-a%26...%26a%5C%5C%20...%26...%26...%26...%26...%5C%5C%200%260%260%26...%26b%20%5Cend%7Bbmatrix%7D&plus;%28x_n-b%29D_%7Bn-1%7D"/>
</p></div>

所以:
<div><p align="center">
<img src="http://latex.codecogs.com/gif.latex?D_n%3Db%5Cprod_%7Bi%3D1%7D%5E%7Bn-1%7D%28x_i-a%29&plus;%28x_n-b%29D_%7Bn-1%7D%281%29"/>
</p></div>

再由行列式转置不变性得到:

<div><p align="center">
<img src="http://latex.codecogs.com/gif.latex?D_n%3Da%5Cprod_%7Bi%3D1%7D%5E%7Bn-1%7D%28x_i-b%29&plus;%28x_n-a%29D_%7Bn-1%7D%282%29"/>
</p></div>

联立<img src="http://latex.codecogs.com/gif.latex?(1)(2)"/> ,得通式:

<div><p align="center">
<img src="http://latex.codecogs.com/gif.latex?D_n%3D%5Cfrac%7B1%7D%7Ba-b%7D%5Ba%5Cprod_%7Bi%3D1%7D%5E%7Bn%7D%28x_i-b%29-b%5Cprod_%7Bj%3D1%7D%5E%7Bn%7D%28x_j-a%29%5D"/>
</p></div>

### 2.通过适当变换可以化为两三角型行列式的,描述不如大家自己看例子揣摩,也很容易理解的,请看下例

<div><p align="center">
<img src="http://latex.codecogs.com/gif.latex?eg3%3AD_n%3D%5Cbegin%7Bbmatrix%7D%20d%26b%26b%20%26...%20%26b%5C%5C%20c%26x%26a%26...%26a%5C%5C%20c%26a%26x%26...%26a%5C%5C%20...%26...%26...%26...%26...%5C%5C%20c%26a%26a%26...%26x%20%5Cend%7Bbmatrix%7D"/>
</p></div>

<img src="http://latex.codecogs.com/gif.latex?Solution"/>: 将第一行乘上 <img src="http://latex.codecogs.com/gif.latex?\frac{a}{b}"/> ,第一列乘上 <img src="http://latex.codecogs.com/gif.latex?\frac{a}{c}"/> ,得:

<div><p align="center">
<img src="http://latex.codecogs.com/gif.latex?D_n%3D%5Cfrac%7Bbc%7D%7Ba%5E2%7D%5Cbegin%7Bbmatrix%7D%20%5Cfrac%7Ba%5E2d%7D%7Bbc%7D%26a%26a%20%26...%20%26a%5C%5C%20a%26x%26a%26...%26a%5C%5C%20a%26a%26x%26...%26a%5C%5C%20...%26...%26...%26...%26...%5C%5C%20a%26a%26a%26...%26x%20%5Cend%7Bbmatrix%7D"/>
</p></div>

即化成了两三角型行列式

### 3.一些每行上有公因子但是无法向上式那样在保持行列式不变得基础上能提出公因子的,采用**升阶法**,请看下例

<div><p align="center">
<img src="http://latex.codecogs.com/gif.latex?eg4%3AD_n%3D%5Cbegin%7Bbmatrix%7D%201&plus;x_%7B1%7D%5E2%26x_1x_2%26x_1x_3%20%26...%20%26x_1x_n%5C%5C%20x_2x_1%261&plus;x_%7B2%7D%5E2%26x_2x_3%26...%26x_2x_n%5C%5C%20x_3x_1%26x_3x_2%261&plus;x_%7B3%7D%5E2%26...%26x_3x_n%5C%5C%20...%26...%26...%26...%26...%5C%5C%20x_nx_1%26x_nx_2%26x_nx_3%26...%261&plus;x_%7Bn%7D%5E2%20%5Cend%7Bbmatrix%7D"/>
</p></div>

<img src="http://latex.codecogs.com/gif.latex?Solution"/>:  加边升阶,得:

<div><p align="center">
<img src="http://latex.codecogs.com/gif.latex?D_n%3D%5Cbegin%7Bbmatrix%7D%201%26x_1%26x_2%26x_3%26...%26x_n%5C%5C%200%261&plus;x_%7B1%7D%5E2%26x_1x_2%26x_1x_3%20%26...%20%26x_1x_n%5C%5C%200%26x_2x_1%261&plus;x_%7B2%7D%5E2%26x_2x_3%26...%26x_2x_n%5C%5C%200%26x_3x_1%26x_3x_2%261&plus;x_%7B3%7D%5E2%26...%26x_3x_n%5C%5C%200%26...%26...%26...%26...%26...%5C%5C%200%26x_nx_1%26x_nx_2%26x_nx_3%26...%261&plus;x_%7Bn%7D%5E2%20%5Cend%7Bbmatrix%7D"/>
</p></div>

再将第 <img src="http://latex.codecogs.com/gif.latex?i,i=2...n+1"/> 都减去第一行的<img src="http://latex.codecogs.com/gif.latex?x_i,i=1...n"/> 倍,得:

<div><p align="center">
<img src="http://latex.codecogs.com/gif.latex?D_n%3D%5Cbegin%7Bbmatrix%7D%201%26x_1%26x_2%26x_3%26...%26x_n%5C%5C%20-x_1%261%260%260%20%26...%20%260%5C%5C%20-x_2%260%261%260%26...%260%5C%5C%20-x_3%260%260%261%26...%260%5C%5C%200%26...%26...%26...%26...%26...%5C%5C%20-x_n%260%260%260%26...%261%20%5Cend%7Bbmatrix%7D"/>
</p></div>

即又化成了箭型行列式,可得通式:

<div><p align="center">
<img src="http://latex.codecogs.com/gif.latex?D_n%3D1&plus;%5Csum_%7Bi%3D1%7D%5E%7Bn%7Dx_%7Bi%7D%5E%7B2%7D"/>
</p></div>

## 三:两条线型行列式 ------------------> [返回目录](#%E5%85%AB%E5%A4%A7%E5%B8%B8%E8%A7%81%E7%B1%BB%E5%9E%8B%E7%9A%84%E8%A1%8C%E5%88%97%E5%BC%8F%E5%8F%8A%E5%85%B6%E8%A7%A3%E6%B3%95)

特征是除了主(次)对角线或与其相邻得一条斜线所组成的任意一条线加四个顶点中的某个顶点外,其他元素均为<img src="http://latex.codecogs.com/gif.latex?0"/>,这类行列式可以直接展开降阶.这段描述有点繁琐,但其实也并不复杂,请看下例理解(空白处都为0):

<div><p align="center">
<img src="http://latex.codecogs.com/gif.latex?eg%3AD_n%3D%5Cbegin%7Bbmatrix%7D%20a_1%26b_1%26%20%26...%20%26%5C%5C%20%26a_2%26b_2%26...%26%5C%5C%20%26%26a_3%26...%26%5C%5C%20%26%26%26%5C%5C%20%26%26...%26a_%7Bn-1%7D%26b_%7Bn-1%7D%20%5C%5C%20b_n%26%26...%26%26a_n%20%5Cend%7Bbmatrix%7D"/>
</p></div>

<img src="http://latex.codecogs.com/gif.latex?Solution"/>: 按照第一列两个非<img src="http://latex.codecogs.com/gif.latex?0"/>元素拉普拉斯展开即可

<div><p align="center">
<img src="http://latex.codecogs.com/gif.latex?D_n%3D%5Cprod_%7Bi%3D1%7D%5E%7Bn%7Da_i&plus;%28-1%29%5E%7Bn&plus;1%7D%5Cprod_%7Bi%3D1%7D%5E%7Bn%7Db_i"/>
</p></div>

## 四:范德蒙德型行列式 ------------------> [返回目录](#%E5%85%AB%E5%A4%A7%E5%B8%B8%E8%A7%81%E7%B1%BB%E5%9E%8B%E7%9A%84%E8%A1%8C%E5%88%97%E5%BC%8F%E5%8F%8A%E5%85%B6%E8%A7%A3%E6%B3%95)

范德蒙德行列式大家应该熟悉,而范德蒙德型行列式的特征就是有逐行(列)元素按幂递增(减),可以将其转化为范德蒙德行列式来计算,请看下例

<div><p align="center">
<img src="http://latex.codecogs.com/gif.latex?eg%3AD_n%3D%5Cbegin%7Bbmatrix%7D%20a_%7B1%7D%5En%26%20a_%7B1%7D%5E%7Bn-1%7Db_1%26...%20%26a_1b_1%5E%7Bn-1%7D%26b_1%5En%5C%5C%20a_%7B2%7D%5En%26a_%7B2%7D%5E%7Bn-1%7Db_2%26...%26a_2b_2%5E%7Bn-1%7D%26b_2%5En%5C%5C%20...%26...%26...%26...%26...%5C%5C%20a_%7Bn%7D%5En%26a_%7Bn%7D%5E%7Bn-1%7Db_n%26...%26a_nb_n%5E%7Bn-1%7D%26b_n%5En%5C%5C%20a_%7Bn&plus;1%7D%5En%26a_%7Bn&plus;1%7D%5E%7Bn-1%7Db_%7Bn&plus;1%7D%26...%26a_%7Bn&plus;1%7Db_%7Bn&plus;1%7D%5E%7Bn-1%7D%26b_%7Bn&plus;1%7D%5En%20%5Cend%7Bbmatrix%7D"/>
</p></div>

<img src="http://latex.codecogs.com/gif.latex?Solution"/>:  将每行都提出 <img src="http://latex.codecogs.com/gif.latex?a_i^{n},i=1...n+1"/> 倍,得:

<div><p align="center">
<img src="http://latex.codecogs.com/gif.latex?D_n%3D%5Cprod_%7Bi%3D1%7D%5E%7Bn&plus;1%7Da_i%5En%5Cbegin%7Bbmatrix%7D%201%26%20%5Cfrac%7Bb_1%7D%7Ba_1%7D%26...%20%26%28%5Cfrac%7Bb_1%7D%7Ba_1%7D%29%5E%7Bn-1%7D%26%28%5Cfrac%7Bb_1%7D%7Ba_1%7D%29%5E%7Bn%7D%5C%5C%201%26%5Cfrac%7Bb_2%7D%7Ba_2%7D%26...%26%28%5Cfrac%7Bb_2%7D%7Ba_2%7D%29%5E%7Bn-1%7D%26%28%5Cfrac%7Bb_2%7D%7Ba_2%7D%29%5E%7Bn%7D%5C%5C%20...%26...%26...%26...%26...%5C%5C%201%26%5Cfrac%7Bb_n%7D%7Ba_n%7D%26...%26%28%5Cfrac%7Bb_n%7D%7Ba_n%7D%29%5E%7Bn-1%7D%26%28%5Cfrac%7Bb_n%7D%7Ba_n%7D%29%5E%7Bn%7D%5C%5C%201%26%5Cfrac%7Bb_%7Bn&plus;1%7D%7D%7Ba_%7Bn&plus;1%7D%7D%26...%26%28%5Cfrac%7Bb_%7Bn&plus;1%7D%7D%7Ba_%7Bn&plus;1%7D%7D%29%5E%7Bn-1%7D%26%28%5Cfrac%7Bb_%7Bn&plus;1%7D%7D%7Ba_%7Bn&plus;1%7D%7D%29%5E%7Bn%7D%20%5Cend%7Bbmatrix%7D"/>
</p></div>

上式即为范德蒙德行列式,所以通式为:

<div><p align="center">
<img src="http://latex.codecogs.com/gif.latex?D_n%3D%5Cprod_%7B1%5Cle%20i%3Cj%5Cle%20n&plus;1%7D%28a_ib_j-b_ia_j%29"/>
</p></div>

## 五:<img src="http://latex.codecogs.com/gif.latex?%5Cfn_jvn%20%5Clarge%20Hessenberg"/>型行列式 ------------------> [返回目录](#%E5%85%AB%E5%A4%A7%E5%B8%B8%E8%A7%81%E7%B1%BB%E5%9E%8B%E7%9A%84%E8%A1%8C%E5%88%97%E5%BC%8F%E5%8F%8A%E5%85%B6%E8%A7%A3%E6%B3%95)

特征为除了主(次)对角线及与其相邻的斜线,再加上第一行(列)或第<img src="http://latex.codecogs.com/gif.latex?n"/>行(列)外,其余元素均为<img src="http://latex.codecogs.com/gif.latex?0"/>.这类行列式有点像前面说的两条线型行列式,但是还是有一点区别的.这类行列式都用**累加消点法**,即通常将某一行(列)都化简到只有一个非<img src="http://latex.codecogs.com/gif.latex?0"/>元素,以便于降阶计算,请看下例

<div><p align="center">
<img src="http://latex.codecogs.com/gif.latex?eg%3AD_n%3D%5Cbegin%7Bbmatrix%7D%201%262%263%20%26...%20%26n-1%26n%5C%5C%201%26-1%26%26%26%26%5C%5C%20%262%26-2%26...%5C%5C%20...%26...%26...%26...%26...%26...%5C%5C%20%26%26%26n-2%262-n%26%5C%5C%20%26%26%26...%26n-1%261-n%20%5Cend%7Bbmatrix%7D"/>
</p></div>

<img src="http://latex.codecogs.com/gif.latex?Solution"/>:  将各列都加到第一列,得到:

<div><p align="center">
<img src="http://latex.codecogs.com/gif.latex?D_n%3D%5Cbegin%7Bbmatrix%7D%20%5Cfrac%7Bn%28n&plus;1%29%7D%7B2%7D%262%263%20%26...%20%26n-1%26n%5C%5C%200%26-1%26%26%26%26%5C%5C%200%262%26-2%26...%5C%5C%20...%26...%26...%26...%26...%26...%5C%5C%200%26%26%26n-2%262-n%26%5C%5C%200%26%26%26...%26n-1%261-n%20%5Cend%7Bbmatrix%7D"/>
</p></div>

降阶之后再重复上述步骤即可得到通式:

<div><p align="center">
<img src="http://latex.codecogs.com/gif.latex?D_n%3D%28-1%29%5E%7Bn-1%7D%5Cfrac%7B%28n&plus;1%29%21%7D%7B2%7D"/>
</p></div>

注:需要说明的是,上面举的例子比较容易看出如何实施**累加消点法**就可以实现将某一行(列)都化简到只有一个非<img src="http://latex.codecogs.com/gif.latex?0"/>元素从而达到降阶的目的,但是还有很多<img src="http://latex.codecogs.com/gif.latex?Hessenberg"/>型行列式并不这么容易就做到,还需要大家找找技巧稍微变换一下,只要始终记得你要用**累加消点法**来消元来降阶就可以了

## 六:三对角型行列式 ------------------> [返回目录](#%E5%85%AB%E5%A4%A7%E5%B8%B8%E8%A7%81%E7%B1%BB%E5%9E%8B%E7%9A%84%E8%A1%8C%E5%88%97%E5%BC%8F%E5%8F%8A%E5%85%B6%E8%A7%A3%E6%B3%95)

这是一种递推结构的行列式,特征为所有主子式都有相同的结构,从而以最后一列展开,将所得的<img src="http://latex.codecogs.com/gif.latex?(n-1)"/> 阶行列式再展开即得递推公式,即**递推法(特征方程法)**,请看下例

<div><p align="center">
<img src="http://latex.codecogs.com/gif.latex?eg%3AD_n%3D%5Cbegin%7Bbmatrix%7D%20a%26b%26%20%26%26...%20%26%26%26%5C%5C%20c%26a%26b%26%26...%26%26%26%5C%5C%20%26c%26a%26b%26...%26%26%5C%5C%20...%26...%26...%26...%26...%26%5C%5C%20%26%26%26%26...%26a%26b%5C%5C%20%26%26%26%26...%26c%26a%20%5Cend%7Bbmatrix%7D"/>
</p></div>

<img src="http://latex.codecogs.com/gif.latex?Solution"/>: 按第一列拉普拉斯展开,得:

<div><p align="center">
<img src="http://latex.codecogs.com/gif.latex?D_n%3DaD_%7Bn-1%7D-bcD_%7Bn-2%7D"/>
</p></div>

解特征方程: <img src="http://latex.codecogs.com/gif.latex?x^2=ax-bc"/> ,得:

<div><p align="center">
<img src="http://latex.codecogs.com/gif.latex?x_1%3D%5Cfrac%7Ba&plus;%5Csqrt%7Ba%5E2-4bc%7D%7D%7B2%7D"/>
</p></div>

<div><p align="center">
<img src="http://latex.codecogs.com/gif.latex?x_2%3D%5Cfrac%7Ba-%5Csqrt%7Ba%5E2-4bc%7D%7D%7B2%7D"/>
</p></div>

即可得通式:

<div><p align="center">
<img src="http://latex.codecogs.com/gif.latex?D_n%20%3D%20%5Cfrac%7Bx_1%5E%7Bn&plus;1%7D-x_2%5E%7Bn&plus;1%7D%7D%7Bx_1-x_2%7D"/>
</p></div>

注:特征根相等以及没有特征根时的解法.建议大家去复习一下高中数列的解法,其中有一个方法叫特征方程法,也叫不动点法,这个方法说明了特征根相等的时候怎么做.三对角型行列式的解法本质就是求一个数列的通项公式.

## 七:各行元素和相等型行列式 ------------------> [返回目录](#%E5%85%AB%E5%A4%A7%E5%B8%B8%E8%A7%81%E7%B1%BB%E5%9E%8B%E7%9A%84%E8%A1%8C%E5%88%97%E5%BC%8F%E5%8F%8A%E5%85%B6%E8%A7%A3%E6%B3%95)

这个特征已经很清楚了吧,方法就是**累加法**,很简单,直接看下例

<div><p align="center">
<img src="http://latex.codecogs.com/gif.latex?eg%3AD_n%3D%5Cbegin%7Bbmatrix%7D%201&plus;x_1%26x_1%20%26...%20%26x_1%5C%5C%20x_2%261&plus;x_2%26...%26x_2%5C%5C%20...%26...%26...%26...%5C%5C%20x_n%26x_n%26...%261&plus;x_n%20%5Cend%7Bbmatrix%7D"/>
</p></div>

<img src="http://latex.codecogs.com/gif.latex?Solution"/>:  将第<img src="http://latex.codecogs.com/gif.latex?i,i=2...n"/> 行都加到第一行去,得:

<div><p align="center">
<img src="http://latex.codecogs.com/gif.latex?D_n%3D%5Cbegin%7Bbmatrix%7D%201&plus;%5Csum_%7Bi%3D1%7D%5E%7Bn%7Dx_i%261&plus;%5Csum_%7Bi%3D1%7D%5E%7Bn%7Dx_i%20%26...%20%261&plus;%5Csum_%7Bi%3D1%7D%5E%7Bn%7Dx_i%5C%5C%20x_2%261&plus;x_2%26...%26x_2%5C%5C%20...%26...%26...%26...%5C%5C%20x_n%26x_n%26...%261&plus;x_n%20%5Cend%7Bbmatrix%7D"/>
</p></div>

所以:

<div><p align="center">
<img src="http://latex.codecogs.com/gif.latex?%5Cdpi%7B200%7D%20%5Ctiny%20D_n%3D%281&plus;%5Csum_%7Bi%3D1%7D%5E%7Bn%7Dx_i%29%5Cbegin%7Bbmatrix%7D%201%261%20%26...%20%261%5C%5C%20x_2%261&plus;x_2%26...%26x_2%5C%5C%20...%26...%26...%26...%5C%5C%20x_n%26x_n%26...%261&plus;x_n%20%5Cend%7Bbmatrix%7D%3D%20%281&plus;%5Csum_%7Bi%3D1%7D%5E%7Bn%7Dx_i%29%20%5Cbegin%7Bbmatrix%7D%201%260%26...%20%260%5C%5C%20x_2%261%26...%260%5C%5C%20...%26...%26...%26...%5C%5C%20x_n%260%26...%261%20%5Cend%7Bbmatrix%7D%20%3D1&plus;%5Csum_%7Bi%3D1%7D%5E%7Bn%7Dx_i"/>
</p></div>

## 八:相邻两行对应元素相差K倍型行列式 ------------------> [返回目录](#%E5%85%AB%E5%A4%A7%E5%B8%B8%E8%A7%81%E7%B1%BB%E5%9E%8B%E7%9A%84%E8%A1%8C%E5%88%97%E5%BC%8F%E5%8F%8A%E5%85%B6%E8%A7%A3%E6%B3%95)

这个要用**步步差法**

(1)大部分元素为数字,且相邻两行对应元素相差为<img src="http://latex.codecogs.com/gif.latex?1"/>,采用逐步作差的方法,即可出现大量 <img src="http://latex.codecogs.com/gif.latex?\pm1"/> 元素,进而出现大量<img src="http://latex.codecogs.com/gif.latex?0"/>元素

(2)若相邻两行相差<img src="http://latex.codecogs.com/gif.latex?K"/>倍,采用逐步作<img src="http://latex.codecogs.com/gif.latex?k"/>倍差得方法,即可出现大量<img src="http://latex.codecogs.com/gif.latex?0"/>元素

请看下面两个例子

<div><p align="center">
<img src="http://latex.codecogs.com/gif.latex?%5Cdpi%7B200%7D%20%5Ctiny%20eg1%3AD_n%3D%5Cbegin%7Bbmatrix%7D%200%261%262%20%26...%26n-2%20%26n-1%5C%5C%201%260%261%26...%26n-3%26n-2%5C%5C%202%261%260%26...%26n-4%26n-3%5C%5C%20...%26...%26...%26...%26...%26...%5C%5C%20n-2%26n-3%26n-4%26...%260%261%5C%5C%20n-1%26n-2%26n-3%26...%261%260%20%5Cend%7Bbmatrix%7D"/>
</p></div>

<img src="http://latex.codecogs.com/gif.latex?Solution"/>: 从第一行开始,依次用前一行减去后一行,得:

<div><p align="center">
<img src="http://latex.codecogs.com/gif.latex?%5Cdpi%7B200%7D%20%5Ctiny%20D_n%3D%5Cbegin%7Bbmatrix%7D%20-1%261%261%20%26...%261%20%261%5C%5C%20-1%26-1%261%26...%261%261%5C%5C%20-1%26-1%26-1%26...%261%261%5C%5C%20...%26...%26...%26...%26...%26...%5C%5C%20-1%26-1%26-1%26...%26-1%261%5C%5C%20n-1%26n-2%26n-3%26...%261%260%20%5Cend%7Bbmatrix%7D"/>
</p></div>

再将第一列加到第<img src="http://latex.codecogs.com/gif.latex?i,i=2...n"/> 列,得:

<div><p align="center">
<img src="http://latex.codecogs.com/gif.latex?%5Cdpi%7B200%7D%20%5Ctiny%20D_n%3D%5Cbegin%7Bbmatrix%7D%20-1%260%260%26...%260%260%5C%5C%20-1%26-2%260%26...%260%260%5C%5C%20-1%26-2%26-2%26...%260%260%5C%5C%20...%26...%26...%26...%26...%26...%5C%5C%20-1%26-2%26-2%26...%26-2%260%5C%5C%20n-1%262n-3%262n-4%26...%26n%26n-1%20%5Cend%7Bbmatrix%7D%3D%28-1%29%5E%7Bn-1%7D%28-2%29%5E%7Bn-2%7D%28n-1%29"/>
</p></div>

***

<div><p align="center">
<img src="http://latex.codecogs.com/gif.latex?%5Cdpi%7B200%7D%20%5Ctiny%20eg2%3AD_n%3D%5Cbegin%7Bbmatrix%7D%201%26a%26a%5E2%20%26...%26a%5E%7Bn-2%7D%20%26a%5E%7Bn-1%7D%5C%5C%20a%5E%7Bn-1%7D%261%26a%26...%26a%5E%7Bn-3%7D%20%26a%5E%7Bn-2%7D%20%5C%5C%20a%5E%7Bn-2%7D%20%26a%5E%7Bn-1%7D%20%261%26...%26a%5E%7Bn-4%7D%20%26a%5E%7Bn-3%7D%20%5C%5C%20...%26...%26...%26...%26...%26...%5C%5C%20a%5E2%26a%5E3%26a%5E4%26...%261%26a%5C%5C%20a%26a%5E2%26a%5E3%26...%26a%5E%7Bn-1%7D%261%20%5Cend%7Bbmatrix%7D"/>
</p></div>

<img src="http://latex.codecogs.com/gif.latex?Solution"/>:  从第一行开始,依次用前一行加上后一行的<img src="http://latex.codecogs.com/gif.latex?(-a)"/> 倍,得:

<div><p align="center">
<img src="http://latex.codecogs.com/gif.latex?%5Cdpi%7B200%7D%20%5Ctiny%20D_n%3D%5Cbegin%7Bbmatrix%7D%201-a%5En%260%260%26...%260%260%5C%5C%20a%5E%7Bn-1%7D%261-a%5En%260%26...%260%20%260%5C%5C%200%20%260%20%261-a%5En%26...%260%260%20%5C%5C%20...%26...%26...%26...%26...%26...%5C%5C%200%260%260%26...%261-a%5En%260%5C%5C%20a%26a%5E2%26a%5E3%26...%26a%5E%7Bn-1%7D%261%20%5Cend%7Bbmatrix%7D"/>
</p></div>

所以:

<div><p align="center">
<img src="http://latex.codecogs.com/gif.latex?D_n%3D%281-a%5En%29%5E%7Bn-1%7D"/>
</p></div>
