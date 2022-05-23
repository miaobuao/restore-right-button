电脑更新windows11之后，右键需要点击展开才能显示全部的选项，你是否也有这样的困扰呢？？

使用如下指令即可默认展开右键：

```sh
# 修改注册表
reg.exe add "HKCU\Software\Classes\CLSID\{86ca1aa0-34aa-4e8b-a509-50c905bae2a2}\InprocServer32" /f /ve 
# 重启explorer，免得重启计算机
taskkill /f /im explorer.exe & start explorer.exe

```

想要恢复win11的样式，只需要：
```sh
reg.exe delete "HKCU\Software\Classes\CLSID\{86ca1aa0-34aa-4e8b-a509-50c905bae2a2}\InprocServer32" /va /f
taskkill /f /im explorer.exe & start explorer.exe

```

参考[知乎回答](https://www.zhihu.com/question/480356710/answer/2279799895)以及评论区给出的重启explorer的建议

感谢万能的互联网。