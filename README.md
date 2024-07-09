# ContextMenuUser

<h3 align="center"> 简体中文 | <a href='./README-en_US.md'>English</a></h3>

## 介绍

搭配[Custom Context Menu](https://github.com/ikas-mc/ContextMenuForWindows11)来自定义Windows11上下文菜单，本仓库仅为个人使用。

举例的应用请前往对应仓库下载，本仓库只提供编译为[ARM64的软件](https://github.com/iKineticate/ContextMenuUser/windows-arm4-apps)（感谢原仓库的作者们）。

## 说明

1.下列使用的可执行程序（.exe）均添加至环境变量，添加.json至**Custom Context Menu**文件夹时，请注意设置的程序路径。

2.除了举例的软件，还有许多相似或更优秀功能的命令行软件。

3.除了可执行程序，也可cmd或powershell来实现简单功能，不足地方可能会出现一闪而过的终端窗口。

4.本例只提供了简单的思路，根据思路也可自定义需要的功能。

## 例子

### （1）图片转换为 ICO
[icogen](https://github.com/hamaluik/icogen)

### （2）TinyPNG 压缩图片

### （3）复制到 OneDrive
```PowerShell
"Copy-Item -Path {path} -Destination OneDrive路径 "
```

### （4）剪切到 WSA共享文件夹
```PowerShell
"Move-Item -Path {path} -Destination WSA共享文件夹路径 "
```

### （5）分析磁盘空间
[deskonaut](https://github.com/imsnif/diskonaut)

### （6）摸鱼
[genact](https://github.com/svenstaro/genact)

### （7）清理桌面缓存图标
