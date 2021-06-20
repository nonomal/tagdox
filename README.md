# 我的文库



#### 介绍

「我的文库」用于对本地各类文档（格式不限）通过标签进行管理，提高文档的管理效率。

![image-20210620113000923](_img/image-20210620113000923-1624159802338.png)



#### 主要功能



##### 文件索引

对指定文件夹内部所有文件（包括子目录的文件）进行汇集，并以 # 号作为标签分隔符，对所有文件进行标签化管理。

例如，「某某通知#通知#会议记录#发布.pdf」会识别为 「某某通知.pdf 」+ 「标签：通知、会议记录、发布」

对于文件名包括#号的，也会识别为标签。所以如果有些文件拥有相同的主题，可以直接放在叫做「#主体名称」文件夹内，会自动识别为批量标签。



##### 文件查询

支持按照标签对文件进行筛选和检索。

也可以通过文件名和路径进行搜索。



##### 添加标签

通过标签输入框，可以为指定的文件添加标签。标签将通过 # 号分隔。

标签将以重命名的方式添加到文件名中。

注意：如果文件名不可随意修改，则不建议采用本方法。



#### 软件架构



本程序采用Python实现，程序界面通过tkinter实现自动生成。

通过pyinstaller转制为exe可执行程序。

其中，我的文库.py 文件是全部的源代码。



#### 安装教程



将dist文件复制到本地，运行其中的「我的文库.exe」即可。

部分高分屏会出现模糊，可以通过右击 - 属性 - 兼容性标签页 - 更改高DPI设置

![image-20210620112912083](_img/image-20210620112912083-1624159754431.png)

然后在下面“替代高DPI缩放行为”处打钩，确定即可。

![image-20210620112928566](_img/image-20210620112928566-1624159770944.png)



#### 更新说明

##### v0.5.2 2021年6月20日

支持对最末2层文件夹名称进行解析，如果文件夹名称包括#号也可以解析为标签（层数默认2层、分隔号默认#号，都可以自定义）。

微调UI。



##### v0.5.1 2021年6月20日

将分隔符（原来的#号）独立出来，设置为可以调整的符号。

在data.json里面可以设置。



##### v0.5.0： 2021年6月19日

实现添加标签、自由搜索、结果计数的功能。



##### v0.4.0： 2021年6月18日

实现按照中文音序排序标签。

将检索目录的设定方案调整到外接 json 文件中，实现程序外自定义。

优化UI、优化程序架构。



##### v0.1.0： 2021年6月17日

实现文件检索、标签拆分等基础功能。
