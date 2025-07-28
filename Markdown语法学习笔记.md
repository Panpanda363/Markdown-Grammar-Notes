<span style="font-size:1.8em; font-weight:bold;">**Markdown语法笔记**</span>



[TOC]



## Markdown简介



Markdown 是一种轻量级的 **标记语言**，用通俗的话来说就是在一些文本编辑工具里通过添加或控制一些符号来设置文本格式，它的设计目标是 **易读易写**，适合日常写作、文档编写和网络内容创作，并能轻松转换为结构化的 HTML、PDF或其他格式。



## 文本编辑工具

软件名称：<a id="TY"><span style="color:#000000;">Typora</span></a>（目前我用的是这个，还有很多其他支持markdown语法的软件）



![image-20250728154933911](C:/Users/HUAWEI/AppData/Roaming/Typora/typora-user-images/image-20250728154933911.png)

软件下载：目前正版Typora在官网下载需要付费，可以去Bilibili找破解版

## Markdown语法示意

> 以下全部用字母“<span style="color:#CC0000; font-weight:bold; font-size:1.1em;">A</span>”示例markdown语法演示效果，且以下所提及符号都需在英文输入法下完成



### 标题语法

Markdown总共有六级标题，语法为在需要设置成标题的字体前面加 <span style="font-weight:bold; background:#E0E0E0;">#</span> 和 <span style="font-weight:bold; background:#E0E0E0;">空格</span>，输入几个<span style="font-weight:bold; background:#E0E0E0;">#</span>就代表为要设置成几级标题样式，从二级标题开始软件会自动编号，前面会默认带上阿拉伯数字

例如在Typora输入# A，会变成如下显示：

![image-20250728155109568](C:/Users/HUAWEI/AppData/Roaming/Typora/typora-user-images/image-20250728155109568.png)

输入## A：



![image-20250728155222434](C:/Users/HUAWEI/AppData/Roaming/Typora/typora-user-images/image-20250728155222434.png)

全部标题列表：

![image-20250728155352371](C:/Users/HUAWEI/AppData/Roaming/Typora/typora-user-images/image-20250728155352371.png)

### 加粗语法

在需要加粗的字体前后各加2个**

例如\**A**,会显示：<span style="font-weight:bold;">A</span>

### 倾斜语法

在需要倾斜的字体前后各加1个*

例如\*A*,会显示：<span style="font-style:italic;">A</span>

### 删除语法

在需要删除的字体前后各加2个~~

例如\~\~A\~\~,会显示：<span style="text-decoration:line-through;">A</span>

### 高亮语法

在需要高亮的字体前后各加2个=

例如\==A==,会显示：<span style="background:#FFFF00;">A</span>

### 下划线语法

在需要添加下划线的字体前加\<u>，后面加\</u>

例如\<u>A\</u>,会显示：<span style="text-decoration:underline;">A</span>

### 超链接语法

#### 链接网址（2种方式）

- 把需要添加超链接的文本先放在[]里面，链接放在()里面，合起来就是\[文本](链接)

  例如\[A](网址)，会显示[A](https://www.baidu.com/?tn=sitehao123_15)，按住ctrl键再点击超链接后的文本可以跳转到对应网址

- 通过**自定义**第二个[]内容来设置超链接，再对第二个[]进行**补充说明**（也就是网址链接）

  例如：\[文本][1]     \[文本][2]    \[文本][甲]，最终会显示以下界面，按住ctrl键再点击超链接后的文本也可以跳转到对应网址

  ![image-20250728160115013](C:/Users/HUAWEI/AppData/Roaming/Typora/typora-user-images/image-20250728160115013.png)

####  文内链接(2种方式)

- 如果需要在同一个文档内实现不同位置跳转（**段落内文字**），比如<span style="background:#E0E0E0; font-weight:bold;">点击此处</span>跳转到本文档第2点<span style="background:#E0E0E0; font-weight:bold;">Typora</span>处


1. 创建锚点（目标位置）
   - 在目标位置前输入格式：\<a id="TY">\</a>
2. 设置跳转的文本（点击后跳转到锚点）
   - 格式：\[点击此处](#TY)，会显示[点击此处](#TY)，按住ctrl键再点击可以跳转到对应锚点位置 

- 如果需要跳转到文档的标题（**针对标题**），则语法相对简单，如<span style="background:#E0E0E0; font-weight:bold;">点击此处</span>跳转到本文档Markdown简介
  - 语法为：\[点击此处]\(#Markdown简介)，会显示[点击此处](#Markdown简介)，按住ctrl键再点击可以跳转到对应标题位置 



### 引用语法

在引用的文本前面加**>**

例如>A,会显示：

> A

### 脚注语法

在文本A后面添加\[^1]，再在文档末尾对其解释说明即可

A[^1]

[^1]:解释脚注

### 分割线语法

在需要插入分割线的地方输入3个-，会按以下显示

---



### 代码语法

#### 行内代码

在代码前后各加一个`

如\`代码`，会显示：

`代码`

#### 代码块

在代码块前加```和对应语言，如：

\```python

def hello():
    print("Hello Typora!")

hello()

会显示以下界面：

```python
def hello():
    print("Hello Typora!")

hello()
```



### 有序/无序列表

无序列表：语法是输入一个-再按空格，如：

- 

有序列表：按下数字再加一个**.** 再加空格，如：

1. 



> [!NOTE]
>
> 如果需要再降一级，则在原来层级上再按Tab键，可实现多级效果



### 任务列表

待办事项：语法是-**␣**[**␣**]**␣**待办事项内容，**␣**为1个空格，如

\- [ ] 待办，会显示：

- [ ] 待办

已办事项：语法语法是-**␣**[x]**␣**已办事项内容，在方括号里面加个x就行

\- [x] 已办，会显示：

- [x] 已办

### 公式

- **行内公式**

分别用一个$$包裹整个公式

例如：\$Z=x^2 + y_{n}$，会显示：

$Z=x^2 + y_{n}$​

- **块公式（独立公式，居中显示）**

用两个美元符号 \$\$包裹整个公式，并各独占一行；也可以先输入2个\$\$，再按回车键后输入公式

例如：

\$$

\sqrt{x}

\$$

会显示：
$$
\sqrt{x}
$$



### 上标/下标

- 上标

如要实现X^2^效果，先输X2，再选中2按键盘上的^即可实现上标效果

- 下标

如果要实现H~2~O效果，可先输入H2O，再选中2按键盘上的~即可实现下标效果



### 目录

如果要给文档生产目录，直接在要插入目录的地方写上[TOC]加空格，typora会自动根据文档多级标题生成可跳转的目录 



## 图片/表格

Typora插入图片和表格等也有对应语法，我个人目前是直接鼠标右键插入图片和表格，再做相应调整，或者直接复制黏贴进去，感觉更快捷简单，像有些流程图、思维导图等也可以用typora制作，貌似语法也比较复杂，这部分我没有详细了解，感觉用其他工具去制作这些更简单

<img src="C:/Users/HUAWEI/AppData/Roaming/Typora/typora-user-images/image-20250728160822502.png" alt="image-20250728160822502" style="zoom:50%;" />

## 其他

1. 冒号加对应英文描述可以显示部分图标，如​\:one    \:red     \:ballon

​      :one:       :red_circle:         :balloon:

2. 语法符号前面加 \ ，即可显示符号本身，typora不会进行渲染，如：

![image-20250728161921841](../../Typora里面自动保存的图片/image-20250728161921841.png)

> [!TIP]
>
> 在Typora顶部菜单栏和鼠标右键，也有很多可调节文档的操作，有时忘记markdown语法可直接在菜单栏找对应编辑操作






