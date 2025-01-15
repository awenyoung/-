

# 安装完clash-verge打不开，不显示界面。而后台进程却显示的有的解决方法：

1. 使用 Windows 7 兼容模式启动：[win7怎么设置兼容性 win7设置兼容模式的方法[多图\] - Win7 - 教程之家](https://www.jiaochengzhijia.com/win7/20953.html)。（笔者尝试失败）

2. 系统WebView2问题，原因：程序依赖系统的WebView2，当WebView2不存在时，将启动失败。

Windows WebView2 Download：https://developer.microsoft.com/en-us/microsoft-edge/webview2/?form=MA13LH#download；

https://developer.microsoft.com/zh-cn/microsoft-edge/webview2/#download

如果是WebView2不存在，下载安装即可。

如果显示的是：![](C:\Users\honor\AppData\Roaming\Typora\typora-user-images\image-20250114101637363.png)

按照**[如何卸载并重装edge webview2]()**进行操作即可，重装完WebView2，再次打开clash-verge,界面就可以显示了。

![image-20250114103131640](C:\Users\honor\AppData\Roaming\Typora\typora-user-images\image-20250114103131640.png)