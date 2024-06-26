# markdown语法

## 基础语法(一)

### 1 加粗

**第一种加粗 **  不加粗对比

__第二种加粗__      #不推荐使用

### 2 斜体

*斜体*      无斜体字体

### 3 组合使用

***斜体+加粗字体***

### 4 删除线

~~此代码已经过期~~

### 5 分割线

***

### 6 各级标题

使用#表示一级标题，二级标题是##  三级用### 以此类推

### 7  无序列表

* 第一项       可用*  或 + 或 -  如果混合使用会间隔开
* 第二项
* 第三项
- 笛
+ 五
- 地

### 8 有序列表以及下级列表使用
1. 第一件事
    * 其一
    * 其二
        * 三级列表
        * 其二

2. 第二件事情
    1. 其一

    2. 其二

    3. 三级列表
        1. 其一

        2. 其二

        3. 其三

3. 第三件事情


### 9 复选框
* [x] 第一件事
1. * [ ] 第二件事

### 10 代码块

```java
public class Main() {
    public static void main(String[] args) {
        System.out.println("Hello World");
    }
}
```
#### 行内代码块
比较两个对象时 使用`equals()`方法来鉴别

### 11 引用
> 对于负数，补码表示方式也是人脑无法直观看出其数值的.  
> 通常也需要转换成原码在计算其数值  
> 补码解决了0的符号以及两个编码的问题，让计算机的减法可以直接转为加法运算(计算机内部都是用补码直接运算，只有负数与原码不一致)

**对于引用中说明中想要转行**
1. 在其转行尾部两个空格
2. 回车或可以每行都加>

### 12超链接

1. 简单链接：如果想购买xxx请前往[官网](https://www.baidu.com)含税单
2. 引用链接：[如果][a]想[购买][b]xxx请前往[官网][c]

[a]:https://www.baidu.com
[b]:https://www.baidu.com
[c]:https://www.baidu.com

### 13脚注
神罗天正[^1]  
万象天引[^2]

[^1]: 佩恩大招

### 14插入图片

第一种插入方式：  
![p1.jpg](https://s2.loli.net/2024/04/19/8xWlPnisEgJKQVb.jpg)
第二种变量法插入方式：  
![pp1.jpg][cc] 

[cc]:https://s2.loli.net/2024/04/19/8xWlPnisEgJKQVb.jpg

### 15表格插入
|  姓名  | 年龄 | 性别 |
|:----:|:-:|:-:|
| 吴  |200|男|
| 人员D  |20000000|男|
| 人员A  |211|男|

> 对于代码中”:“所在位置表示左对齐或右对齐  
> 当两边都有符号”:“表示居中


### 16 HTML相关使用（图片插入修改|字体修改|网页插入|等。。）

1. 插入网页 <span style="color: red;font-size: 40px">注意：</span>
2. >有些网站，比如像Github、知乎、简书等，它们就无法设置这种功能。不过像有的网站，比如像CSDN，它的Markdown编辑器做了很好的扩展、支持HTML语法，就有这样的功能  
3. <img style="width: 600px;height: 400px" src="https://s2.loli.net/2024/04/19/8xWlPnisEgJKQVb.jpg">

<iframe src="//player.bilibili.com/player.html?aid=1252624739&bvid=BV1eJ4m157kC&cid=1489709802&p=10" scrolling="no" border="0" frameborder="no" framespacing="0" allowfullscreen="true" height="500px" weigh="1000px"> </iframe>


### 17 其他扩展语法
#### 17.1高亮文本
==我是高亮文本==

#### 17.2上标
2^234^

#### 17.3下标
2~888~

#### 17.4公式
$ x + y =10 $   #单行公式这样使用$

$$
\frac{x}{y}
$$

<span style="color: red">注意：</span>在$$里公式换行使用\\

$x^2$

$x_2$

$x_2^{2x}$

$\sqrt[y]{\{[x+(z+2)]\}}$
$$
\not = 不等于 \\
\approx 约等于 \\
\leq 小于等于 \\
\geq 大于等于 \\
\times 乘号 \\
\div 除号 \\
\pm 正负号 \\
\sum 求和  \\\\
90^\circ \\
\sin  \\
\pi  \\
\cos \\
\infty \\
\int \\
\iint \\
y\prime   求导 \\
\lim \\
\emptyset   空集  \\
\in   属于\\
\notin  不属于\\
\supset  真包含\\
\supseteq 包含\\
\bigcap 交集 \\
\bigcup 并集 \\
\alpha \\
$$

$$
\lim_{n\rightarrow+\infty}\frac{1}{n}
$$