# Jupyter Notebook 键盘快捷键练习
Keyboard Shortcuts Learning for Jupyter Notebook

> 随着机器学习，深度学习，神经网络等概念的不断变热，数据科学家们分享交流的web应用程序 Jupyter Notebook也走入了千家万户。你可能已经正在使用 Jupyter Notebook 了，但也许并不知道它还有这么多小技巧。这些小技巧将帮助你更加高效地使用 Jupyter Notebook，帮助你进行数据处理以及分享你的模型。它们非常简单，但足够实用。



# 更多内容

可以访问 [我的个人博客](https://qsctech-sange.github.io/jupyter-notebook-tips/) 来查看更多精彩内容。 将仓库下载后，使用 Jupyter Notebook 打开 `Jupyter-Notebook-tips.ipynb` 来做练习。



# 键盘快捷键

## 运行并进入下一个单元格
当我们写好一个单元格，想要运行并进入下一个单元格的时候，可以不用上方的菜单栏。

我们可以通过按`Enter + Shift`到下一个单元格。

不管是 Markdown 还是代码，都可以使用这个快捷键。使用 Markdown 就相当于，渲染这个单元格并进入下一个单元格


```python
# 选中单元格，并按 Shift + Enter
3**2
```

`Shift + Enter` 运行单元格之后会自动选中下一个单元格，或者根据需要创建新的单元格。你也可以通过 `Ctrl + Enter` 在运行之后仍然选中当前单元格。

单元格中的代码运行的结果将会显现在单元格下方。它和正常的 Python shell 一样打印出代码的运行结果，但是只会打印最后一个运行结果。如果你想打印所有结果，你需要使用 `print()` 。

> **练习：** 运行下方两个代码单元格测试以上所学内容。先预测你的猜想，然后运行它。


```python
3**2
4**2
```


```python
print(3**2)
4**2
```

## 代码补全

当你在写代码的时候，代码补全可以大大节省你使用变量或者函数的时间，因为你只需要键入名称的一部分，然后按 `tab` 。

> **练习：** 先运行下一个cell，然后将你的鼠标点击更下一个cell的 apple 最后，然后按 `tab`


```python
# 运行一下这个
applepie = "apple-pie"
```


```python
# 在这儿做练习
apple
```

如果有多个以apple开头的变量名，那么会出现一下下拉菜单供你选择。
> **练习：** 先运行下一个cell，然后将你的鼠标点击更下一个cell的 apple 最后，然后按 `tab`


```python
# 运行一下这个
appletree = "apple-tree"
```


```python
# 在这儿做练习
apple
```

记住，在一个单元格中赋值的变量可以在所有单元格中访问。这包括你之前运行的单元格和变量赋值前面的单元格。

当你想使用一个模块但不太记得你想使用的函数，或者有哪些函数可以使用，代码补全的功能将非常方便。我将通过 [random](https://docs.python.org/3/library/random.html) 模块来展示这种用法。这个模块提供了生成随机数的函数，在创建虚拟数据或从列表中随机挑选的时候特别有用。

> **练习：** 先运行下面的单元格，然后将鼠标点击至更下面一个单元格的 random. 后并按 `tab` 来触发该模块的代码补全菜单。从列表中选择 random.randint ，你可以使用上下键来选择。


```python
# 运行一下这个
import random
```


```python
# 在这儿做练习
random.
```

通过以上方法你可以看到 random 模块中的所有可用函数。比如你可能在寻找从 [高斯分布](https://en.wikipedia.org/wiki/Normal_distribution) 中生成随机数的方法。高斯分布又称为“正态分布”或者“钟曲线”。

## 快速查看文档

你看到有一个函数叫作 random.gauss() 但如何使用它呢？你可以点击 [文档](https://docs.python.org/3/library/random.html)，但更快捷的方法是直接在notebook里看，使用`shift+tab`。

> **练习：** 在如下单元格中，将鼠标点击至 random.gauss 并按 `shift + tab` 显示调用方法。


```python
random.gauss
```

你将看到类似如下的简单的文档内容：

    Signature: random.gauss(mu, sigma)
    Docstring:
    Gaussian distribution.

该函数需要两个参数 mu 和 sigma。这是高斯分布中均值和标准差的标准符号。如果你需要知道更多的信息。你可以按 `shift + tab` 两次显示更多的信息。

> **练习：** 在如下代码单元格中，通过按两次 `shift + tab` 显示全部文档。


```python
random.gauss
```

你将看到类似如下的更加详细的信息：

    mu is the mean, and sigma is the standard deviation.  This is
    slightly faster than the normalvariate() function.

## 两种模式的切换

你可能已经注意到了，有时候我们的单元格左边是绿色的，有时候是蓝色的。这代表了单元格的两种模式。你可以通过单元格框线的颜色来分辨出你当前正在使用的模式。

1. 命令模式。在命令模式中，左边粗框线是蓝色的。可以理解为选中了这个单元格但是没有进入单元格内部。你可以敲击键盘来执行命令。例如创建一个新的单元格和打开一个命令面板。
2. 编辑模式。在编辑模式中，左边粗框线是绿色的。可以理解为进入了这个单元格内部。在编辑模式中，你能在单元格中看到一个光标。这时候你可以打字了。

要进入编辑模式，就是深入，按`Enter`。要从编辑模式返回到命令模式，就是出来，按`Escape`。

> **练习：** 点击下方单元格，在编辑模式和命令模式间来回切换几次练习


```python
# 练习切换模式
```

## 创建一个新的单元格

最常见的命令之一是创建一个新的单元格。你可以通过在命令模式按 `A` 在当前单元格上方创建一个单元格。按 `B` 在当前选定的单元格下方创建一个单元格。

> **练习：** 使用键盘命令在此单元格上方创建一个单元格。

> **练习：** 使用键盘命令在此单元格下方创建一个单元格。

## 在Markdown和代码间相互切换

通过使用键盘快捷键，可以很快很简单地在Markdown和代码单元格之间相互切换。从Markdown切换到单元格，按 `Y` 。从代码切换到Markdown，按 `M`。在命令模式下才可以切换哦。

> **练习：** 在Markdown和代码单元格之间相互切换单元格。


```python
## 在这里练习

def fibo(n): # 递归斐波拉契数列！
    if n == 0:
        return 0
    elif n == 1:
        return 1
    return fibo(n-1) + fibo(n-2)
```

## 删除单元格

连续按两次 `D` 可以删除单元格。这是为了防止出现意外的删除，所以你必须连续按两次键。

> **练习：** 删除下面的单元格。

球球您删了我吧！

也别放过我！


```python
# 代码块也是可以删除的
```

## 保存 Notebook

Notebook 每隔一段时间会自动保存
但是如果你想手动保存你的工作，按 `S` 去保存。如此简单！

> **练习：** 手动保存一下。

## 命令面板

通过按`Shift + Control + F` 或者 `Shift + Control + P` ，可以访问命令面板。

你可以在弹出的命令面板中搜索不能用键盘快捷键实现的命令。例如，工作栏上有按钮可以实现上下移动单元格的命令（上下箭头），但是没有相对应的键盘快捷键。要把一个单元格向下移动，你可以打开命令面板键入"移"就会出现移动命令。

> **练习：** 使用命令面板把单元格向下移动一个位置。


```python
# 下移此单元格
```


```python
# 至该单元格下方
```

## 显示行数

你可以在命令模式下使用`L`显示与关闭显示代码行数。

> **练习：** 显示下列代码的行数。


```python
def fibo(n): # 递归斐波拉契数列！
    if n == 0:
        return 0
    elif n == 1:
        return 1
    return fibo(n-1) + fibo(n-2)
```

## 查看所有快捷键

记住，如果你需要去查看快键键，只需要在命令模式中按 `H` 。

你还可以做更多，比如复制、剪切、粘贴单元格。我建议你要去习惯使用键盘快捷键，那么你能够更加便捷地在笔记本中工作。当你熟练地掌握这些快捷键后，你很少需要把你的手从键盘移开去使用鼠标，这会极大地提高你的工作效率。	
