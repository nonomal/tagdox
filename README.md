<div align="center">
        <img src="_img/%E6%88%91%E7%9A%84%E6%96%87%E5%BA%93%E5%9B%BE%E6%A0%87%E8%AE%BE%E8%AE%A10630.png" height="200">
    <h1>
        <a src="https://github.com/HorseSword/tagdox">Tagdox</a> - 标签文库
    </h1>
    <a href="https://github.com/HorseSword/tagdox">
    <img src="https://img.shields.io/badge/Github-Click--Me-blue?logo=github&style=flat-square" height="20" alt="Github Ready-to-Code">
  </a>
    <a href="https://gitee.com/horse_sword/my-local-library">
    <img src="https://img.shields.io/badge/Gitee-Click--Me-blue?logo=gitee&style=flat-square&color=c71d23" height="20" alt="Gitee Ready-to-Code">
  </a>
    <!-- Short description: -->
  <div>Powered by Python and Tkinter</div>
</div>





## 简要介绍

Tagdox / 标签文库，是用于对文档进行「标签化管理」的免费开源工具。通过Python语言编写。

利用Windows系统NTFS文件流的特性，为文件加标签，并可实现标签的识别和查询等功能。

可实现对大量文件的标签化快速管理，可显著提升效率。



## 开发说明

本程序采用Python实现，程序界面主要依靠tkinter库完成开发。

通过pyinstaller转制为exe可执行程序，所以目前只支持 windows 系统。

程序完全开源，不上传任何数据。

其中，标签文库.py 文件是全部的源代码，options_for_tagdox.json是设置项，没有设置项时程序会自动生成。



## 程序界面

以 v0.20.3.3为例。

![image-20210911124858447](_img/image-20210911124858447.png)



其中：

左侧是关注的文件夹，可以将文件夹添加到这里，程序将自动对其中所有文件进行解析。支持分组管理。

右侧是文件列表，左起第二列就是本程序最核心的「标签」部分。



## 近期更新

#### v0.21.1.2 2021年10月6日

修复了在非NTFS磁盘上的兼容性bug。
文件夹区域也增加了鼠标指向效果。
修改自建模块位置。

#### v0.21.1.1 2021年10月4日

储备：优化标签类封装逻辑，关闭文件前一直占用文件。
储备：新增常用工具函数，直接对标签进行增加、删除、清空、查询。
储备：新增依赖说明requirements.txt。

#### v0.21.1.0 2021年10月4日

为文件列表的鼠标指向增加了高亮效果。

#### v0.21.0.0 2021年10月3日
优化标签逻辑，采用NTFS流模式，不再影响文件名（测试版）。
优化右键响应，现在可以正确在被点击的项目处出现右键菜单了。



**更多更新**，见「 [更新记录.md](更新记录.md) 」。




## 主要功能





### 文件管理



#### 为文件添加 / 删除标签。

可以为指定的文件快速添加标签，快捷键是 Ctrl+T。支持多文件批量操作。

添加标签的方式：

（1）右键，添加标签。

![image-20210907213438028](_img/image-20210907213438028.png)

（2）点击右下角按钮添加。

![image-20210911124938272](_img/image-20210911124938272.png)

（3）快捷键Ctrl+T添加。



当然，删除标签也是一键搞定。

![image-20210907214903690](_img/image-20210907214903690.png)





##### 补充：识别文件夹标签

（备注：本功能即将被移除或重做）

对于文件名包括标签识别符的，也会识别为标签。可以方便地进行大批量快速管理。

如果有些文件拥有相同的主题（公共标签），可以直接放在叫做「文件夹名称^标签名称」的文件夹内，程序会自动将「标签名称」识别为批量标签，为文件夹里面所有项都添加这个标签，而无需对每个文件进行重命名操作。

文件夹批量标签的识别层数可以通过设置进行自定义。



#### 按照标签快速查询文件

支持按照标签对文件进行筛选和检索。

![image-20210907110953223](_img/image-20210907110953223.png)



当前文件夹的标签会自动提取到标签列表中，便于按标签快速搜索。

也可以通过手动输入文件名和路径等任意关键词进行搜索。



#### 拖拽添加文件/文件夹

可以通过鼠标将任意文件或文件夹拖拽到右侧文件列表，被拖动的文件/文件夹将被移动（或复制）到当前打开的文件夹中。

![image-20210911125153412](_img/image-20210911125153412.png)

可以通过菜单设置项，设置拖拽操作是「移动」（不保留原始文件）还是「复制」。

![image-20210907105115950](_img/image-20210907105115950-16309830777422.png)

添加文件时，会自动为文件附带当前选中的标签。



这个功能非常适合管理微信的文件，从聊天列表中一拖拽就能保存到目标位置，而且可以快速添加标签，让管理更加轻松。



### 文件夹管理



#### 添加关注的文件夹

本程序主要分析目标是本机文件夹。

对任意文件夹添加关注之后，文件夹将出现在本程序左侧列表中，添加之后才能进行文件分析和管理操作。

添加的方式：

（1）可以通过点击顶部菜单按钮添加，

![image-20210911125021348](_img/image-20210911125021348.png)



（2）也可以直接将文件夹用鼠标拖动到列表区域，支持多文件夹拖动操作；

![image-20210911125110175](_img/image-20210911125110175.png)



（3）还可以通过右键菜单，将子文件夹快速添加到关注列表。

![image-20210907213657414](_img/image-20210907213657414.png)

#### 文件夹分组

可以通过**文件夹分组**，对相似功能的文件夹进行统一管理，比如查询搜索或者标签管理等。

如下图所示：

![image-20210907110442737](_img/image-20210907110442737.png)



分组可以通过右键菜单自定义。

![image-20210907213824717](_img/image-20210907213824717.png)



### 更多功能



#### 快速笔记

程序可以快速添加笔记，并以本地文件的方式实现笔记管理，

添加这个功能的主要原因是已经受够了在线笔记软件（如印X笔记、为X笔记、有X云笔记等）越来越差的使用体验，以及越来越麻烦的数据垄断。

笔记还是要掌握在用户自己手中！所以，这里的笔记坚决以本地文件的方式实现，完全自主可控。



![image-20210907105443565](_img/image-20210907105443565.png)



可以通过设置，选择笔记类型为 docx、md、rtf、txt等。

![image-20210907214121596](_img/image-20210907214121596.png)

新建笔记之后将首先输入名称，然后立刻自动打开笔记。







## 安装教程



请访问「[发行版](https://gitee.com/horse_sword/my-local-library/releases)」页面，下载最新版本并解压缩，运行其中的「标签文库.exe」文件即可。

![image-20210818124551314](_img/image-20210818124551314.png)

版本升级：

目前还没有制作专门的安装包，所以将最新版压缩包下载后，解压缩，直接覆盖旧版文件夹即可。

