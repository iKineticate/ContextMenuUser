<h3 align="center"> 简体中文 | <a href='./README-en.md'>English</a></h3>

## 介绍

搭配[Custom Context Menu](https://github.com/ikas-mc/ContextMenuForWindows11)来自定义Windows11上下文菜单，本仓库仅为个人使用

举例的应用请前往对应仓库下载，本仓库只提供编译为[ARM64的软件](https://github.com/iKineticate/ContextMenuUser/tree/main/windows-arm64-app)（感谢原仓库的作者们）

## 说明

1.下列使用的可执行程序（.exe）均添加至环境变量（网上均有教程）

2.除了举例的软件，还有许多相似或更优秀功能的命令行软件

3.除了可执行程序，也可cmd或powershell来实现简单功能，不足地方可能会出现一闪而过的终端窗口

4.本例只提供了简单的思路和功能，根据思路也可个性化自定义需要的功能

## 例子
![image](https://github.com/iKineticate/ContextMenuUser/blob/master/screenshots/image.png)

### （1）图片转换
转换为ico : [icogen](https://github.com/hamaluik/icogen)（手动将icogen.exe添加至环境变量）
```
程序：icogen
```
```
参数："{path}"
```
转换为其他格式图片：[ImageMagick](https://imagemagick.org/script/download.php#windows)（安装时选择添加至环境变量）
```
程序：magick
```
```
参数："{path}" "{nameNoExt}.jpeg"
参数："{path}" "{nameNoExt}.png"
参数："{path}" "{nameNoExt}.bmp"
....
```
```
匹配文件夹：目录（x）背景（x）桌面（x）
匹配文件（扩展名）：.jpg|.jpeg|.gif|.png|.bmp|.tiff|.ico|.svg|.webp
匹配多文件：每个
```

### （2）TinyPNG 压缩图片
软件：[TinyPNG](https://github.com/wyhaya/tinypng)（添加至环境变量）
```
程序：tinypng
```
```
参数："{path}"
```
```
匹配文件夹：目录（x）背景（x）桌面（x）
匹配文件（扩展名）：.jpg|.jpeg|.png|.webp
匹配多文件：每个
```
### （3）发送到 OneDrive
```
程序：PowerShell
```

```PowerShell
参数："Copy-Item -Path {path} -Destination OneDrive路径 "
```

### （4）发送到 WSA共享文件夹
```
程序：PowerShell
```
```PowerShell
参数："Move-Item -Path {path} -Destination WSA共享文件夹路径 "
```

### （5）分析磁盘空间
软件：[deskonaut](https://github.com/imsnif/diskonaut)（添加至环境变量）
```
程序：diskonaut
```
```
参数："{path}"
```
```
匹配文件夹：目录（√）背景（√）桌面（√）
匹配文件：关闭
匹配多文件：禁用
```

### （6）清理桌面缓存图标
