# markdown 学习笔记

用来测试和显示README.md的各种markdown语法。

GitHub的markdown语法在标准的markdown语法基础上做了扩充，称之为GitHub Flavored Markdown。简称GFM，GFM在GitHub上有广泛应用，除了README文件外，issues和wiki均支持markdown语法。

|Author|Youyifeng|
|---|---|
|E-mail|852056007@qq.com|

****
## 目录
* [标题](#标题)
* [文本](#文本)
    * 单行文本
    * 多行文本
    * 文本强调
    * 换行
    * 文本中划线
    * 文字强调斜体
* [图片](#图片与链接)
    * 自动链接
* [代码与代码块](#代码与代码块)
* [列表](#列表)
* [分割线](#分割线)
* [转义](#转义)
* [复选框](#复选框)
* [引用](#引用)
* [diff语法](#diff语法)
* [典型使用](#典型使用)

**PS:每个标题项为界限，上面是输出，下面是markdown语法。**

- - - -
# 标题

总共有6级标题

# 一级标题
```
# 一级标题

或者

一级标题
===           \\两个等于就够了
```

## 二级标题
```
## 二级标题

或者

二级标题
---            \\两个-就够了
```

### 三级标题
`### 三级标题`

#### 四级标题
`#### 四级标题`

##### 五级标题
`##### 五级标题`

###### 六级标题
`###### 六级标题`

---

# 文本
### 普通文本
这是一行普通文本，行首没有缩进哦~
```
这是一行普通文本，行首没有缩进哦~
```
---

### 单行文本

在一行开头加入1个Tab或者4个空格。

        youyifeng 到此一游~
PS:上面是输出，下面是markdown语法

```
        youyifeng 到此一游~
```
---

### 多行文本(文本块)

在连续几行的文本开头加入1个Tab或者4个空格。

    欢迎到访
    很高兴见到您
    祝您，早上好，中午好，下午好，晚安
PS:上面是输出，下面是markdown语法
```
    欢迎到访
    很高兴见到您
    祝您，早上好，中午好，下午好，晚安
```


---
### 文本强调

**强调本文字**

__强调本文字__
```
**强调本文字**

或者

__强调本文字__

```
---
### 换行
直接回车不能换行，
可以在上一行文本后面补两个空格，
这样下一行的文本就换行了。

或者就是在两行文本直接加一个空行。

也能实现换行效果，不过这个行间距有点大。

---

### 文本中划线

~~中划线本文字~~

```
~~中划线本文字~~
```
---

### 文字强调斜体

强调分为粗体和斜体

粗体 ：用两个**将文本包裹起来即可

斜体 ：用两个*将文字包裹起来即可

粗体斜体 ：用三个***将文字包裹起来即可

***强调斜体本文字***

___强调斜体本文字___
```
***强调斜体本文字***

或者

___强调斜体本文字___

```

|语法|效果|
|----|-----|
|`*斜体1*`|*斜体1*|
|`_斜体2_`| _斜体2_|
|`**粗体1**`|**粗体1**|
|`__粗体2__`|__粗体2__|
|`这是一个 ~~删除线~~`|这是一个 ~~删除线~~|
|`***斜粗体1***`|***斜粗体1***|
|`___斜粗体2___`|___斜粗体2___|
|`***~~斜粗体删除线1~~***`|***~~斜粗体删除线1~~***|
|`~~***斜粗体删除线2***~~`|~~***斜粗体删除线2***~~|

PS:斜体、粗体、删除线可混合使用

---

# 图片与链接

插入链接与插入图片的语法很像，区别在一个!号
插入图片时需要图片的地址，如果你是在网上写blog等，必须使用url；如果你在本地使用MD编辑器做记录，可以使用本地路径
插入图片和链接的方式有两种：1.行内方式 2.关联方式

基本格式：

~~~
![alt](URL title)
~~~

alt和title即对应HTML中的alt和title属性（都可省略）：
- alt表示图片显示失败时的替换文本
- title表示鼠标悬停在图片时的显示文本（注意这里要加引号）

URL即图片的url地址，如果引用本仓库中的图片，直接使用相对路径就可了，如果引用其他github仓库中的图片要注意格式，即：仓库地址/raw/分支名/图片路径，如：

```
https://github.com/yifengyou/learn-markdown/master/image/demoimage.png
```

行内方式：
```
// 插入图片
![图片名称](图片url)

// 插入链接
[显示内容](链接地址)
```

关联方式：
```
// 插入图片
![图片名称][关联名称]

//插入链接
![显示内容][关联名称]

[关联名称]:url/本地路径
```

[yifengyou github地址](http://github.com/yifengyou) <br />
http://www.google.fr/ or <http://example.com/>

```
[链接名字](http://github.com/yifengyou) <br />
http://www.google.fr/ or <http://example.com/>
```

![demoimage](https://github.com/yifengyou/learn-markdown/master/image/demoimage.png)


---

### 自动链接

自动链接

MD支持以比较简短的自动链接形式来处理网址和电子邮件信箱，只要是用方括号包起来， Markdown 就会自动把它转成链接。一般网址的链接文字就和链接地址一样，例如：

<https://github.com/yifengyou/>

```
<https://github.com/yifengyou/>
```

---
# 表格

表格可能是MD中最不便利的标签了，几乎需要你手动的敲一遍表格，例子如下：

|First Header  | Second Header|
|------------- | -------------|
|Content Cell  | Content Cell|
|Content Cell  | Content Cell|


PS:上面是输出，下面是markdown语法

```
|First Header  | Second Header|
|------------- | -------------|
|Content Cell  | Content Cell|
|Content Cell  | Content Cell|
```

---
# 代码与代码块

如果你是程序员，对代码肯定足够的熟悉。一般使用两个 ` 或 两个 ``` 把代码包裹起来，包裹起来的文字会保持它原有的格式。使用一对各三个的反引号

代码：使用 ` 包裹起来的代码，可以显示在行内，代码不会高亮

代码块：使用 ``` 包裹起来的代码，另起一行显示，可以说明编程语言，可能会出现代码高亮

我们需要在代码的上一行和下一行用\`\`\`标记。\`\`\`不是三个单引号，而是数字1左边，Tab键上面的键。要实现语法高亮那么只要在 \`\`\` 之后加上你的编程语言即可（忽略大小写）。c++语言可以写成c++也可以是cpp。

```javascript
    var specificLanguage_code =
    {
        "data": {
            "lookedUpPlatform": 1,
            "query": "Kasabian+Test+Transmission",
            "lookedUpItem": {
                "name": "Test Transmission",
                "artist": "Kasabian",
                "album": "Kasabian",
                "picture": null,
                "link": "http://open.spotify.com/track/5jhJur5n4fasblLSCOcrTp"
            }
        }
    }
```
    `code...`
或者
    ```
      code...
    ```
分别针对行、字间代码和段落间代码




---
# 列表

无序列表：用 - 或 * 都可以，`字符后有一个空格`

有序列表：用 1.（数字后跟点）即可，`数字后有一个空格`

- 列表项1
- 列表项2
- 列表项3

```
- 列表项1
- 列表项2
- 列表项3
```

* 列表项1
* 列表项2
* 列表项3

```
* 列表项1
* 列表项2
* 列表项3
```

1. 列表项1
2. 列表项2
3. 列表项3

```
1. 列表项1
2. 列表项2
3. 列表项3
```

层级列表在此基础上开头加tab即可


1. 这是第一层
  1. 这是第一层里面第一层
  2. 这是第一层里面第二层
  3. 第一层里面第三层
2. 这是第二层
  1. 这是第二层里面第一层
  2. 这是第二层里面第二层
3. 这是第三层
  1. 这是第三层里面第一层
  2. 这是第三层里面第二层
    1. 这是第三层里面第二层的第一层
        1. 这是第三层里面第二层的第一层的第一层
            1. 这是第三层里面第二层的第一第一层
              1. 这是第三层里面~
                1. 这是第三层里面~~
                    1. 这是第三层里面~~

4. 这是第四层

```
1. 这是第一层
  1. 这是第一层里面第一层
  2. 这是第一层里面第二层
  3. 第一层里面第三层
2. 这是第二层
  1. 这是第二层里面第一层
  2. 这是第二层里面第二层
3. 这是第三层
  1. 这是第三层里面第一层
  2. 这是第三层里面第二层
    1. 这是第三层里面第二层的第一层
        1. 这是第三层里面第二层的第一层的第一层
            1. 这是第三层里面第二层的第一第一层
              1. 这是第三层里面~
                1. 这是第三层里面~~
                    1. 这是第三层里面~~

4. 这是第四层
```
---
# 分割线

html中的`<hr>`大家熟悉吧

在MD中使用 `***` 或者`~~~`，在开头行和结尾行都添加即可



---
# 转义

转义

在MD中，有一些符号是有特殊意义的，比如 # ，如果你直接输入“# 你好”，将会变成一级标题。这时候需要使用\来转义，可以在井号之前加入反斜杠，如\#，才能得到你想要的结果。

MD支持以下这些特殊符号前面加上反斜杠来帮助插入普通的符号
```
\   反斜线
`   反引号
*   星号
 _   底线
{}  花括号
[]  方括号
()  括弧
#   井字号
+   加号
-   减号
.   英文句点
!   惊叹号
```

---
# 复选框

- [ ] An uncompleted task
- [x] A completed task

~~~
- [ ] An uncompleted task
- [x] A completed task
~~~
---

# 引用

引用也可以层叠

>这行引用显示

```
>这行引用显示
```

>数据结构
>>树
>>>二叉树
>>>>平衡二叉树
>>>>>满二叉树

```
>数据结构
>>树
>>>二叉树
>>>>平衡二叉树
>>>>>满二叉树
```

---

# diff语法

版本控制的系统中都少不了diff的功能，即展示一个文件内容的增加与删除。 GFM中可以显示的展示diff效果。使用绿色表示新增，红色表示删除。

其语法与代码高亮类似，只是在三个反引号后面写diff， 并且其内容中，以 +开头表示新增，-开头表示删除。

效果如下：
```diff
+ 鸟宿池边树，僧敲月下门
- 鸟宿池边树，僧推月下门
```

PS:上面是输出，下面是markdown语法

~~~
```diff
+ 鸟宿池边树，僧敲月下门
- 鸟宿池边树，僧推月下门
```
~~~

---

# 典型使用

我们理解您需要更便捷更高效的工具记录思想，整理笔记、知识，并将其中承载的价值传播给他人，**Cmd Markdown** 是我们给出的答案 —— 我们为记录思想和分享知识提供更专业的工具。

```
我们理解您需要更便捷更高效的工具记录思想，整理笔记、知识，并将其中承载的价值传播给他人，**Cmd Markdown** 是我们给出的答案 —— 我们为记录思想和分享知识提供更专业的工具。

```


> * 整理知识，学习笔记
> * 发布日记，杂文，所见所想
> * 撰写发布技术文稿（代码支持）
> * 撰写发布学术论文（LaTeX 公式支持）

```
> * 整理知识，学习笔记
> * 发布日记，杂文，所见所想
> * 撰写发布技术文稿（代码支持）
> * 撰写发布学术论文（LaTeX 公式支持）
```


> 请保留此份 Cmd Markdown 的欢迎稿兼使用说明，如需撰写新稿件，点击顶部工具栏右侧的 **新文稿** 或者使用快捷键 `Ctrl+Alt+N`。

```
> 点击顶部工具栏右侧的**新文稿** 或者使用快捷键 `Ctrl+Alt+N`。
```


- [ ] 支持以 PDF 格式导出文稿
- [ ] 改进 Cmd 渲染算法，使用局部渲染技术提高渲染效率
- [x] 新增 Todo 列表功能
- [x] 修复 LaTex 公式渲染问题
- [x] 新增 LaTex 公式编号功能

```
- [ ] 支持以 PDF 格式导出文稿
- [ ] 改进 Cmd 渲染算法，使用局部渲染技术提高渲染效率
- [x] 新增 Todo 列表功能
- [x] 修复 LaTex 公式渲染问题
- [x] 新增 LaTex 公式编号功能
```




```python
@requires_authorization
class SomeClass:
    pass

if __name__ == '__main__':
    # A comment
    print 'hello world'
```

~~~
```python
@requires_authorization
class SomeClass:
    pass

if __name__ == '__main__':
    # A comment
    print 'hello world'
```
~~~



| 项目        | 价格   |  数量  |
| -----| -----:  | :----:  |
| 计算机      |  $1600 |   5     |
| 手机        |  $12   |   12   |
| 管线        |  $1    |  234  |


~~~
| 项目        | 价格   |  数量  |
| --------   | -----:  | :----:  |
| 计算机     | $1600 |   5     |
| 手机        |   $12   |   12   |
| 管线        |    $1    |  234  |
~~~
