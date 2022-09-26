# ht_object_detection_labelimg
数据集标注软件使用说明（给小白）

# 代码环境配置

- 下载labelImg 源码包（下载压缩包或者git都行）

  - 压缩包本文件夹已包含
  - git方式

  ```
  git clone https://github.com/heartexlabs/labelImg.git
  ```

- 安装依赖库

  具体安装方式与系统平台有关

  - ubuntu

  ```
  sudo apt-get install pyqt5-dev-tools
  sudo pip3 install -r requirements/requirements-linux-python3.txt
  make qt5py3
  ```

  - windows+anaconda

  ```
  conda install pyqt=5
  conda install -c anaconda lxml
  pyrcc5 -o libs/resources.py resources.qrc
  ```

  - 其他参考[labelImg-master\README.rst](https://github.com/HT-hlf/ht_object_detection_labelimg/blob/master/labelImg-master/labelImg-master/README.rst)

# 标注

- 先将labelImg-master\data\predefined_classes.txt 文件中的类别修改为自己的类别

- 启动UI界面

  ```
  python3 labelImg.py
  ```

- 按UI界面的**打开目录**选择标注图片文件夹，按UI界面的**改变存放目录**选定保存标注的文件夹

- 标注物体

  - 创建标注框 : 按键w 
  - 在图片中框出物体，并选择对应的类别，标出所有物体
  - 标完所有物体后，按ctrl +s 保存标注文件
  - 切换下一张图片：按键a向前切换，按键d 向后切换

- 简单演示视频：labelImg-master\演示.mp4

- 快捷键

  - 常用快捷键

  ```
  w :创建标注框
  a/d:向前/后切换图片
  ctrl+s: 保存标注文件
  ctrl+鼠标滑轮：放大或者缩小图片
  del: 选定标注框，按del删除标注框
  ↑→↓←： 选定标注框，按↑→↓←移动标注框
  ```

  - 全部快捷键

  ```
  +--------------------+--------------------------------------------+
  | Ctrl + u           | Load all of the images from a directory    |
  +--------------------+--------------------------------------------+
  | Ctrl + r           | Change the default annotation target dir   |
  +--------------------+--------------------------------------------+
  | Ctrl + s           | Save                                       |
  +--------------------+--------------------------------------------+
  | Ctrl + d           | Copy the current label and rect box        |
  +--------------------+--------------------------------------------+
  | Ctrl + Shift + d   | Delete the current image                   |
  +--------------------+--------------------------------------------+
  | Space              | Flag the current image as verified         |
  +--------------------+--------------------------------------------+
  | w                  | Create a rect box                          |
  +--------------------+--------------------------------------------+
  | d                  | Next image                                 |
  +--------------------+--------------------------------------------+
  | a                  | Previous image                             |
  +--------------------+--------------------------------------------+
  | del                | Delete the selected rect box               |
  +--------------------+--------------------------------------------+
  | Ctrl++             | Zoom in                                    |
  +--------------------+--------------------------------------------+
  | Ctrl--             | Zoom out                                   |
  +--------------------+--------------------------------------------+
  | ↑→↓←             |  Keyboard arrows to move selected rect box   |
  +--------------------+--------------------------------------------+
  ```

  



