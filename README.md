# Dnest
## Windoes系统上的文件暂存工具，类似MacOs上的Yoink 

### 科研需要从 Mac 转 Windows，发现没有好用的文件暂存工具。为了快乐科研 : ) 就用 Python 写了一个小工具。

#### 源码是用 Python 写的，界面用了 PyQt5，编译用了 Nuitka
#### 由于太懒，文件预览功能直接调用的 Seer / QuickLook , 需要文件预览的建议挑一个配合使用。

 由于编程水平实在是烂，Python 写的也不优雅，源码就不放了 &#x1F61B;
 
 ***
 ## 以下是使用介绍：
 ### 基本功能：
 - **基本界面**：文件以路径索引形式暂存软件，不会造成文件丢失或生成文件缓存
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
