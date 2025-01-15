# **如何卸载并重装edge webview2**



**一、使用 Windows 自带的注册表编辑器（regedit）**

1. 按下 `Win + R` 键，打开 “运行” 对话框。
2. 在 “运行” 对话框中输入 `regedit`，然后点击 “确定” 按钮，打开注册表编辑器。
3. 在注册表编辑器中，通过左侧的树形目录结构，找到 `HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Microsoft\EdgeUpdate\Clients\{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}` 路径。
4. 右键点击该注册表项，选择 “删除”。

**注意事项：**

- 在修改注册表之前，强烈建议你备份注册表。你可以在注册表编辑器中，点击 “文件” 菜单，选择 “导出”，将整个注册表或者仅将涉及修改的部分导出为 `.reg` 文件，以便在出现问题时可以恢复。
- 错误地修改注册表可能会导致系统不稳定甚至无法正常启动，因此操作时需要谨慎。如果对注册表操作不熟悉，建议在进行删除操作前，先在网上搜索相关信息，确保删除该注册表项不会对系统造成严重影响。

**二、使用命令行工具（reg delete）**
你可以使用 Windows 命令行工具 `reg delete` 来删除注册表项。打开命令提示符（以管理员身份运行），输入以下命令：

```plaintext
reg delete "HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Microsoft\EdgeUpdate\Clients\{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}" /f
```

**命令解释：**

- `reg delete`：表示要执行删除注册表项的操作。
- `"HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Microsoft\EdgeUpdate\Clients\{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}"`：是要删除的注册表项的完整路径，使用双引号包裹是为了防止路径中包含空格或特殊字符导致的问题。
- `/f`：强制删除，不会出现确认提示，因此使用时请确保你确实想要删除该注册表项，因为一旦删除无法恢复。

**三. 打开电脑控制面板，选择程序->程序和功能，找到Microsoft Edge WebView2 Runtime，右键点击，“更改”，按电脑指示操作执行。再次安装MicrosoftEdgeSetup程序，即可成功安装。**（方法一和二是针对在方法三中找不到Microsoft Edge WebView2 Runtime而采用的方法，这三种方法最终实现的效果是一样的）
