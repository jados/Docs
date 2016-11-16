> 写在前边：我又来了，这次给大家推荐的是一种相当流行的标记语言 -- Markdown。先别急着抵触，这玩意适用于所有人，我相信你可以在5分钟之内学会他，因为他的宗旨就是实现一种易读易写的书写方法。

> 注：本人所有个人文档皆为Markdown编写。

## Markdown是什么
Markdown是一种纯文本格式的轻量级标记语言，可以用工具方便的转换成HTML及很多其他格式。Markdown的语法由一些简单的符号组成，其作用通俗易懂、一目了然。

Markdown对于那些喜欢快速笔记甚至是喜欢写作的人来说，我可以说，那就是为你而生。

来个简单的例子：
``` markdown
# 标题1
## 标题2
#表示标题，1个表示大标题，对应HTML中的h1标签，2个表示二级标题，对应HTML中的h2，当然还可以写3个、4个...
```

再来一个例子：
[竞彩网](http://www.sporttery.cn)
这个链接的实现如下
``` markdown
[竞彩网](http://www.sporttery.cn)
```
当然Markdown的格式还包括很多，比如字体、列表、图片、引用、表格等，都是用简单的符号来实现。So easy，对不对？

## Markdown语法参考
> 以下内容仅作为使用中的一个快速语法参考，如果需要更完善的markdown语法说明，请google。

### 参考目录
+ [标题](#标题)

+ [文字修饰](#文字修饰)

+ [列表](#列表)

+ [链接](#链接)

+ [图片](#图片)

+ [语法高亮](#语法高亮)

+ [表格](#表格)

+ [引用](#引用)

+ [分割线](#分割线)

+ [换行](#换行)


## 标题

```markdown
# H1
## H2
### H3
#### H4
##### H5
###### H6
```

## 文字修饰

```markdown
这是*斜体*，也可以_这样_
这是**粗体**，也可以__这样__
这是**粗体 和 _粗斜体_**
这是~~删除线~~
```

这是*斜体*，也可以_这样_

这是**粗体**，也可以__这样__

这是**粗体 和 _粗斜体_**

这是~~删除线~~

## 列表

```markdown
1. 有序列表的第一项
2. 第二项
   * 无序子列表
   * 子列表第二项
3. 第三项

* 无序列表用星号开头
- 也可以用减号
+ 或者用加号也行
```

1. 有序列表的第一项
2. 第二项
   * 无序子列表
   * 子列表第二项
3. 第三项

* 无序列表用星号开头
- 也可以用减号
+ 或者用加号也行

## 链接

创建链接有以下两种方式。

```markdown
[标准链接](http://www.sporttery.cn)
[带标题的链接](http://www.sporttery.cn "竞彩网")
[引用的链接][sporttery]
[用数字引用链接][1]
[文字本身]

引用的链接可在当前文档内的任意地方定义：
[sporttery]: http://www.sporttery.cn
[1]: http://www.sporttery.cn/football/index.html
[文字本身]: http://www.sporttery.cn/basketball/index.html
```

[标准链接](http://www.sporttery.cn)
[带标题的链接](http://www.sporttery.cn "竞彩网")
[引用的链接][sporttery]
[用数字引用链接][1]
[文字本身]

引用的链接可在当前文档内的任意地方定义：
[sporttery]: http://www.sporttery.cn
[1]: http://www.sporttery.cn/football/index.html
[文字本身]: http://www.sporttery.cn/basketball/index.html

## 图片

图片的用法和链接类似，也是两种方式。

```markdown
基本样式：
![竞彩网](http://static.sporttery.cn/images/i2015/v2/logo.jpg "竞彩网")

引用样式：
![竞彩网][logo]
引用也可以定义到文档的任何位置
[logo]: http://static.sporttery.cn/images/i2015/v2/logo.jpg "竞彩网"
```

基本样式：
![竞彩网](http://static.sporttery.cn/images/i2015/v2/logo.jpg "竞彩网")

引用样式：
![竞彩网][logo]
引用也可以定义到文档的任何位置
[logo]: http://static.sporttery.cn/images/i2015/v2/logo.jpg	"竞彩网"

## 语法高亮

Markdown本身支持代码块的引用，但并不支持代码高亮。但很多Markdown的渲染器却支持，但不同渲染器对于代码命名的定义却可能存在出入。

```markdown
语句中的`代码` 用反引号(`)来实现。
```

语句中的`代码` 用反引号(`)来实现。

代码块用三个反引号将内容包裹起来实现。

```
​```javascript
var s = "Hello world!";
alert(s);
​```

​```python
s = "Hello world!"
print s
​```

​```php
$s = "Hello World!";
echo $s;
​```

​```
//未指定语言，不显示语法高亮
var s = "Hello World!";
alert(s);
​```
```

```javascript
var s = "Hello world!";
alert(s);
```

```python
s = "Hello world!"
print s
```

```php
$s = "Hello World!";
echo $s;
```
```
//未指定语言，不显示语法高亮
var s = "Hello World!";
alert(s);
```
## 表格

```markdown
使用冒号操作列的对齐方式。
| Name   |Age   | Gender |
|--------|:----:|-------:|
| Jack   |20    | Male   |
| Rose   |20    | Female |

每个网格的分隔符至少要3个减号，有些Markdown阅读器甚至不需要你写最外侧的“|”。在编写表格时，不用排的很好看，完全可以像下面这样

|Name|Age|Gender|
|---|:---:|---|
|Jack|20|Male|
|Rose|20|Female|
```
| Name | Age  | Gender |
| ---- | :--: | ------ |
| Jack |  20  | Male   |
| Rose |  20  | Female |

## 引用

``` markdown
> 就像email中一样，引用通过“>”来实现。
> 这是同一个引用的令一行。
空行会停止引用。
> 我们来写个长句子，他会帮你自动换行，当然这句话可能要非常非常非常非常非常非常非常非常非常非常非常非常非常非常非常非常非常非常非常非常非常非常非常非常非常非常非常非常非常非常非常非常非常长，才能换行。
```

> 就像email中一样，引用通过“>”来实现。
>
> 这是同一个引用的令一行。

空行会停止引用。

> 我们来写个长句子，他会帮你自动换行，当然这句话可能要非常非常非常非常非常非常非常非常非常非常非常非常非常非常非常非常非常非常非常非常非常非常非常非常非常非常非常非常非常非常非常非常非常长，才能换行。

## 分割线

```markdown
以下符号输入至少三个即可。
---
减号
***
星号
___
下划线
```

以下符号输入至少三个即可。

---

减号

***

星号

___

下划线

## 换行

至于如何换行，或者说退出当前格式，我个人建议大家还是亲手体会一下。当你在书写一个列表的时候，按一下回车，看看什么效果，然后再按一下回车，你自然就明白了。

