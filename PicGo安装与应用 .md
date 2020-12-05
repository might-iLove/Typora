# PicGo + GitHub 搭建个人图床工具





## 1. PicGo 特色功能

* 支持拖拽图片上传
* 支持快捷键上传剪切板里第一张图片
* Windows 和 macOS 支持右键图片文件通过菜单上传 (v2.1.0+)
* 上传图片后自动复制链接到剪贴板
* 支持自定义复制到剪贴板的链接格式
* 支持修改快捷键，默认快速上传快捷键：`command+shift+p` (macOS) | `control+shift+p` (Windows\Linux)
* 支持插件系统，已有插件支持 Gitee、青云等第三方图床
  * 更多第三方插件以及使用 PicGo 底层的应用可以在 [Awesome-PicGo](https://github.com/PicGo/Awesome-PicGo) 查询

* 支持通过发送 HTTP 请求调用 PicGo 上传 (v2.2.0+)



---



## 2. GitHub 仓库设置

​	**流程：**GitHub上新建repository(public) --> 创建token --> 复制token备用(可存储于.ssh文件中)



### 2.1 新建repository

* 点击GitHub主页上的`+` --> 创建`new repository`
* 填写repository信息 --> 设置为public(需要客户端访问 --> 客户端访问属于外部访问 --> 即无法访问private --> 则上传到repository中的图片只能存储，不能正常显示)





### 2.2 创建Token复制保存

* repository已经创建 -->  点击右上角的头像 --> 进入settings![](https://raw.githubusercontent.com/might-iLove/clouding/main/img/math 2.2 1.jpg)



* 找到Developer settings --> 点击进入!![2](https://raw.githubusercontent.com/might-iLove/clouding/main/img/math 2.2 2.png)



* 创建 token![3](https://raw.githubusercontent.com/might-iLove/clouding/main/img/math 2.2 3.png)



* 填写description --> 勾选复选框repo --> 直接点击页面底部 `Generate token`即可![4](https://raw.githubusercontent.com/might-iLove/clouding/main/img/math 2.2 4.png)

* 复制生成的一串字符 Token (只出现一次) --> 复制保存(可存储于.ssh文件夹中)



---



## 3. PicGo 客户端配置



### 3.1 下载&安装

* GitHub下载地址：[git地址]([Release 2.3.0-beta.3 · Molunerfinn/PicGo (github.com)](https://github.com/Molunerfinn/PicGo/releases/tag/v2.3.0-beta.3))



### 3.2 PicGo配置

![配置](https://raw.githubusercontent.com/might-iLove/clouding/main/img/math 3.2 1.png)

* 设定仓库名：**GitHub用户名 / GitHub新建的repository名称**
* 设定分支：**默认分支填写 main (同步于repository上的分支名)**
* 设定Token：**粘贴保存的token个人令牌**
* 指定存储路径：**默认填写 img/**
* 设定自定义域名：**https://raw.githubusercontent.com/[username(GitHub用户名)]/[仓库名]/master**

**最后，点击设为`默认图床`和`确定`即可**



---



## 4. PicGo设置



### 4.1 Server设置

​	进入PicGo设置 --> 点击**设置Server** --> 将**设置监听端口**改为 **-36677**![Server](https://raw.githubusercontent.com/might-iLove/clouding/main/img/math 4.1.jpg)

​	

### 4.2 快捷键设置

​	**上传快捷键设置：**默认的是 Mac 按键 --> 推荐更改为`Ctrl + Alt + C`![快捷键](https://raw.githubusercontent.com/might-iLove/clouding/main/img/math 4.1.jpg)



---



## 5. PicGo应用

* PicGo 安装完毕后 --> 在Typora中找到偏好设置 --> 点击**图像，前两项打钩 √**  --> 将**上传服务改为PicGo(app)** --> PicGo路径改为**本地PicGo安装目录中的PicGo.exe文件**   ![路径](https://raw.githubusercontent.com/might-iLove/clouding/main/img/math 5.2.jpg)



![本地路径](https://raw.githubusercontent.com/might-iLove/clouding/main/img/math 5.1..jpg)

* Typora中插入图片后点击上传 --> 图片将通过PicGo上传到GitHub的repository --> 传输Typora文件时不需要将图片打包上传



---



## 6.  GitHub 图片显示

​	**问题描述：**PicGo上传到GitHub的repository中图片还是无法正常显示![](https://raw.githubusercontent.com/might-iLove/clouding/main/img/PG 6.1.png)

​	

​	**问题解决：**

* 打开文件 --> 选择偏好设置 --> 点击图像 --> 在`插入图片时`选择`上传图片`

即可![](https://raw.githubusercontent.com/might-iLove/clouding/main/img/PG 6.2.png)

* PicGo上传图片后，会生成在GitHub中的img/文件存储的图片对应的链接，即图片的链接格式如下

  ![](https://raw.githubusercontent.com/might-iLove/clouding/main/img/PG 6.3.png)