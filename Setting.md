# 前言

​	**setting中主要讲解了一些列关于Typora编辑器的进阶功能的实现问题**

---



# 一、标题自动编号(setting)

## 1.主题文件夹

​	**找到主题文件夹：**

​			文件-->设置-->偏好设置-->外观-->打开主题文件夹![主题文件夹](Pictures/20190404161453831.png)



---

## 2.base.user文件(css)

​	**在主题文件夹中新建一个名称为base.user的css文件**



---

## 3.css文件中的代码

```css
/** initialize css counter */
#write {
    counter-reset: h1
}

h1 {
    counter-reset: h2
}

h2 {
    counter-reset: h3
}

h3 {
    counter-reset: h4
}

h4 {
    counter-reset: h5
}

h5 {
    counter-reset: h6
}

/** put counter result into headings */
#write h1:before {
    counter-increment: h1;
    content: counter(h1) ". "
}

#write h2:before {
    counter-increment: h2;
    content: counter(h1) "." counter(h2) ". "
}

#write h3:before,
h3.md-focus.md-heading:before /** override the default style for focused headings */ {
    counter-increment: h3;
    content: counter(h1) "." counter(h2) "." counter(h3) ". "
}

#write h4:before,
h4.md-focus.md-heading:before {
    counter-increment: h4;
    content: counter(h1) "." counter(h2) "." counter(h3) "." counter(h4) ". "
}

#write h5:before,
h5.md-focus.md-heading:before {
    counter-increment: h5;
    content: counter(h1) "." counter(h2) "." counter(h3) "." counter(h4) "." counter(h5) ". "
}

#write h6:before,
h6.md-focus.md-heading:before {
    counter-increment: h6;
    content: counter(h1) "." counter(h2) "." counter(h3) "." counter(h4) "." counter(h5) "." counter(h6) ". "
}

/** override the default style for focused headings */
#write>h3.md-focus:before,
#write>h4.md-focus:before,
#write>h5.md-focus:before,
#write>h6.md-focus:before,
h3.md-focus:before,
h4.md-focus:before,
h5.md-focus:before,
h6.md-focus:before {
    color: inherit;
    border: inherit;
    border-radius: inherit;
    position: inherit;
    left:initial;
    float: none;
    top:initial;
    font-size: inherit;
    padding-left: inherit;
    padding-right: inherit;
    vertical-align: inherit;
    font-weight: inherit;
    line-height: inherit;
}
```



---

## 4.重启Typora

​	**重启Typora，即可实现标题自动编号**



---

## 5.说明

### 标题自动编号官方说明

​	**官方地址：[Auto Numbering for Heading]([Auto Numbering for Headings (typora.io)](http://support.typora.io/Auto-Numbering/))**

### 添加CSS说明(源代码)

​	**源代码URL：[Add-Custom-CSS]([Auto Numbering for Headings (typora.io)](http://support.typora.io/Auto-Numbering/))**



---



# 二、Typora代码高亮配置

## 1.Typora高亮模式

​	**打开方式：**文件-->偏好设置-->Markdown-->Markdown扩展语法中选择代码高亮-->重启Typora即可
​		![动图](https://img-blog.csdnimg.cn/20200920101054257.gif#pic_left)

​	**背景颜色、字体颜色的编号**

​	![编号](Pictures/background.png)



---

## 2.更改代码高亮配色

​	**打开方式：**文件 --> 偏好设置 --> 外观 --> 打开主题文件夹 --> night.css文件 --> Ctrl+F 搜索 mark --> 修改background(背景颜色)和color(字体颜色) --> 保存
​	![动图](Pictures/20200920104332324.gif)




---
## 3.设置高亮快捷键

​	**设置方式:**文件 --> 偏好设置 --> 通用 --> 打开高级设置 --> 存在两个json文件(打开其中一个) --> 在 “keyBinding” 中添加 “Highlight”:“Ctrl+Shift+H” --> 保存 --> 另一个json文件也在 “keyBinding” 中添加 “Highlight”:“Ctrl+Shift+H” --> 保存
​	![动图](Pictures/20200920110453114.gif)



---



# 三、自定义快捷键

## 1.设置方式

​	文件 --> 偏好设置 --> 通用 --> 打开高级设置 --> 存在两个json文件(打开其中一个) --> 在 “keyBinding” 中添加快捷键代码  --> 保存 --> 另一个json文件也在 “keyBinding” 中添加快捷键代码 --> 保存

## 2.快捷键代码

* "Always On Top": "Ctrl+Shift+P",   

* "Code Fences": "Ctrl+Alt+Z", 

* "Oedered List": "Ctrl+Alt+o",   

* "Unordered List": "Ctrl+Alt+u"













