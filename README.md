# Dnest
## Windoes系统上的文件暂存工具，类似MacOs上的Yoink 

### 科研需要从 Mac 转 Windows，发现没有好用的文件暂存工具。为了快乐科研 : ) 就用 Python 写了一个小工具。

#### 源码是用 Python 写的，界面用了 PyQt5，编译用了 Nuitka
#### 由于太懒，文件预览功能直接调用的 Seer / QuickLook , 需要文件预览的建议挑一个配合使用。

 由于编程水平实在是烂，Python 写的也不优雅，源码就不放了 &#x1F61B;
 
 ***
 ## 以下是使用介绍：
 ### 基本功能：
 - **基本界面**：文件以路径索引形式暂存软件，不会造成文件丢失或生成文件缓存 （删除文件只是删除软件中的文件路径索引，不会删除原始文件）
> ![UI](https://user-images.githubusercontent.com/23145087/184356091-e1655629-09a7-454d-b509-911e7a3d494e.png)
 - 程序没有任务栏图标，退出需要通过程序托盘 
> <img width="90" alt="Snipaste_2022-08-12_20-14-33" src="https://user-images.githubusercontent.com/23145087/184351825-4e38f2ed-b2f6-4305-bee6-7af75886e0c0.png">
 - **鼠标右键！ 推拽文件进入软件**
 > ![Drag](https://user-images.githubusercontent.com/23145087/184354127-dd168e58-93a6-437e-ae2b-69d3c291ff8f.gif)
- 删除按钮：从软件移除文件 ；</br> 定位按钮：打开文件所在位置并定位 ；</br> **锁定按钮：默认拖拽出软件自动删除文件**，此按钮可以设置拖拽后依然保存，如下所示： </br>
> ![ulock](https://user-images.githubusercontent.com/23145087/184358514-a0e86636-f990-46bf-a1b4-fbd6b4df51cc.gif) </br> 
> ![lock](https://user-images.githubusercontent.com/23145087/184358563-2c485f14-a580-4b46-9122-67106796bad4.gif) </br> 
- 双击文件会使用默认程序打开文件文件，通过悬停选择文件，悬停 1s 会显示文件路径和大小
> ![hover](https://user-images.githubusercontent.com/23145087/184359519-5c33f25c-1508-4bca-b36d-b2f2422493e2.gif)
- 选择文件时按下空格可以预览文件内容 （需安装 seer / QuickLook , 程序默认支持图片、TXT、CSV、Json 的预览）
> ![View](https://user-images.githubusercontent.com/23145087/184362554-2593b1ab-40f6-42cd-9fd2-51fc0084825c.gif)
- 对于多文件拖拽，默认以集合形式放置，点击文件图标可以预览内容，点击解包按钮可以切换为单文件形式呈现
> ![Pack](https://user-images.githubusercontent.com/23145087/184361818-1f020e51-79c4-42c3-b324-712353f24048.gif)
- 框选多个文件可以编组
> ![split](https://user-images.githubusercontent.com/23145087/184362159-9c6cdeb6-b81b-4056-850e-35866ea55a65.gif)
- 差不多就这样吧，还有其他的试试就会了 : )
 ### 软件设置：
 - **基本界面**
 > ![Menu](https://user-images.githubusercontent.com/23145087/184364371-a576f15e-2bed-4397-b92b-c5cd7923e720.png)
 - 为了适配不同分辨率的设备，可以自己调节UI大小
 > ![UI](https://user-images.githubusercontent.com/23145087/184365544-1ee2db09-152f-4313-a79a-ab3bfc5a0100.gif)
 ### 由于没有条件，未做多屏测试 &#x1F61B;
 ### 希望喜欢，Peace and Love 

 ***
 ### 近期计划以及问题说明：（ps：由于科研比较忙，所以更新会慢点）
 #### 问题说明：
 - ~~鼠标设置界面大小时延迟严重：由于使用了 Win11 的模糊特效，鼠标修改界面大小时确实存在延迟和卡顿，这也是为什么我设置了右下角停靠按钮的原因，未来计划发布两个版本解决~~
 - ~~托盘字体过大问题： 其实还是分辨率和缩放的问题，这个锅甩给Qt，未来考虑在设置中增加对应UI的调整，让大家自己控制显示大小~~
 - ~~设置界面显示不全问题： 同上个问题，也怪我写设置界面时偷懒没好好写，我重新写写~~
 - ~~鼠标靠近自动显示 需求： 没有添加是因为怕担心全屏时拖动右侧滑动条会误触，导致频繁显示和隐藏， 当然右键拖拽不会有问题，未来考虑加进去~~
 - 文件名显示问题：不同文件文件名不一样长，全显示会影响排版，从头显示遇到类似于 【Dnest - 1】【Dnest - 2】这样的格式就都只显示 【Dnest】也不容易看出那个是哪个，所以我就折中取中间了。未来考虑增加列表模式解决；
 - 可能大家理解的意思是每次退出都会自动保存当前位置和大小，但是其实不是，因为担心要是界面出现显示不全的问题，自动保存会导致每次都显示不全，所以在设定里是比较保守的。
 
 #### 近期计划：
 - ~~对于 鼠标设置界面大小时延迟严重 问题： 计划发布移除模糊特效的版本，等我技术进步了再想想怎么解决 : )~~
 - ~~对于 托盘字体过大 问题： 计划在设置中增加调整选项，以满足不同分辨率需求~~
 - ~~对于 设置界面显示不全 问题：计划重写设置界面 UI~~
 - ~~对于 鼠标靠近自动显示 需求：计划添加~~
 - 增加列表模式 和 图标模式
 - 增加退出时默认记录当前位置和大小
 - 根据目录层级生成文件功能 计划添加
 - 快捷键唤醒界面功能 计划添加 （难点是常用的快捷键都被其他软件注册了，非常容易出现问题）
 - 软件内常用快捷键功能 计划添加
 - 优化启动位置保存等UI调整功能的实现
 
 ***
 ### 致谢：
 - PyQt5/PyQt 各种各样的PyQt测试和例子
 > https://github.com/PyQt5/PyQt
 - zhiyiYo/PyQt-Frameless-Window A cross-platform frameless window based on pyqt5, support Win32, X11, Wayland and macOS.
 > https://github.com/zhiyiYo/PyQt-Frameless-Window#pyqt-frameless-window
 - Zuzu-Typ/winput Capture and send keyboard and mouse input on Windows
 > https://github.com/Zuzu-Typ/winput
