# 2048 游戏

这个项目是一个使用Python和PyQt5编写的2048游戏，它采用MVC设计模式。

Other文件夹下的是命令行版本的2048，不影响Pyqt版本的正常运行

## 如何运行游戏

1. 确保您已经安装了Python3和PyQt5。
2. 克隆本仓库到本地。
3. 进入克隆下来的文件夹。
4. 运行 `python3 main.py` 命令启动游戏。

## 游戏规则

1. 游戏开始时，屏幕上会出现两个数字方块，数字为2或4。
2. 玩家可以使用上下左右箭头键移动方块。
3. 每次移动，屏幕上的所有方块都会朝着移动的方向滑动，直到遇到边界或者另一个方块。
4. 如果两个相同数字的方块碰撞在一起，它们会合并成一个数字更大的方块。例如，两个数字为2的方块碰撞后会合并成一个数字为4的方块。
5. 每次移动后，屏幕上会随机出现一个新的数字方块，数字为2或4。
6. 如果屏幕上的方块填满了整个游戏区域，并且没有可以合并的方块，游戏结束。

## 代码文件

### `model.py`

这个文件定义了 `Model` 类，它代表了2048游戏的数据模型。它维护了游戏区域的状态，包括方块的位置和数字。它还包含了检查游戏是否结束的方法，以及添加新方块的方法。

### `view.py`

这个文件定义了 `View` 类，它代表了2048游戏的用户界面。它绘制了游戏区域和数字方块，并响应玩家的操作。它还包含了显示分数和游戏结束信息的方法。

### `block.py`

这个文件定义了 `Block` 类，它是游戏当中的数字方块，本来想着设置一些动画滑动的，由于身体状态的原因，暂时弃坑。

### `message_box.py`

这个文件是一个自定义的QMessageBox类，用来给胜利和失败弹窗所复用。

### `main.py`

这个文件是游戏的入口点。它创建了 `Model`、`View` 和 `Controller` 对象，并启动了游戏。

## 改进的想法

以下是可能的改进点（未实现点）：

- 添加音效和动画效果。
- 添加更多难度级别。
- 实现保存和加载游戏进度的功能。
- 支持多种主题和颜色方案。
- 添加网络对战功能（分数比较等等）。
