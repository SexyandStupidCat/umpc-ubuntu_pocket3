# 介绍

这是从 https://github.com/wimpysworld/umpc-ubuntu fork而来的脚本（tql）

上述所适配的版本比较旧了，难以适配24.04版本的pocket3，所以我做了一丢丢更改，使其更加适配

后续也会讲述关于其他应用程序（包括输入法、虚拟键盘等）配置


# 更改

1. 修改了umpc-display-rotate.c当中transforms的顺序，解决了新安装Ubuntu Mate触屏便宜问题

2. 修改了上述文件中screens中的名字

3. 优化了orientation_changed翻转算法，现在翻转屏幕的检测更加人性化了（by gemini2.5）

# 使用说明

以下为我自身使用时的方法

1. 安装Ubuntu Mate 24.04

2. 下载本脚本，运行`umpc-ubuntu.sh`

3. 完事啦

# 其他说明

自己配置软件时踩过的一些坑

1. 输入法使用fcitx5，中文输入法使用官方的pinyin输入法即可 (fcitx的英文输入法会导致桌面系统崩溃)
```
sudo apt install fcitx5 fcitx5-chinese-addons
```

2. onboard设置
```
Layout : Phone
Keyboard :
  Advanced :
    Long press action : Key-repeat
    Modifier behavior : Push button
    Modifier auto...delay in seconds : 1.00
    Modifier auto...hide in seconds : 1.00
    Touch Input : multi-touch
    Input event source : GTK
```
实际上onboard还是会有些问题：有时虚拟键盘无法收起，需要关闭onboard才行