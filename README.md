### 2021-11-12 更新

亲测在 Ubuntu 20.04 和 RStudio RStudio 2021.09.0+351 "Ghost Orchid" Release QtWebEngine/5.12.8 中可用。

不過，要把文件復制的位置改一下：

```
sudo mv libfcitxplatforminputcontextplugin.so.for.RStudio /usr/lib/rstudio/plugins/platforminputcontexts/libfcitxplatforminputcontextplugin.so
```

这个文件避免了編譯  **Qt5** 和  **fcitx-qt5** 的問題。

----

如果像我上面这样出现无法切换或者卡死的情况，重启电脑就好了。

### 2018-12-08 更新

最新的 RStudio 版本为 1.2.1114，Qt 版本为 Qt-5.11.1。RStudio 自带的 `libQt5*` 文件保存在 `/usr/lib/rstudio/lib` 下，`2018-08-16 更新`的方法移除这些文件的办法又失效了。
所以现在又一次需要自己编译了。NOT Peace...

### 2018-08-16 更新
现在这个问题似乎有了新的办法，详见我的博客 [解决 Debian 中 RStudio 和 Mendeley 下 Fcitx 输入法不能使用的问题 #12](https://github.com/JackieMium/my_blog/issues/12) 开头部分的更新。

希望这是一个真正的稳定的办法，那样的话我这个 repo 大概也就没有存在的必要了吧，这也是我希望看到的。Peace...


# 解决 Fcitx 输入法在一些 qt5 程序下无法使用的问题。
我提供的 `libfcitxplatforminputcontextplugin.so` 都是在 Debian sid 中编译通过。详细支持的应用和 QT 版本见文件夹下的 `README` 内容。
目前支持应用：

- Mendeley Desktop
- RStudio
