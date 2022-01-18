# YiOpt
Yi's Windows system optimization script, PowerShell.

这是从 Yi’s Solutions 里拆分出来的项目，详见 Yi’s Solutions 完整的解决方案。

优化系统是一项很特殊的任务，稍有不慎将“万劫不复”；别担心，绿色部分可优化，可还原。

使用前，建议您在全新系统下运行此脚本。

***

# 主要特征：
- 遵循开源协议，不受版权限制
- 使用 PowerShell 脚本开发，全模块化开发，支持热刷新模块，热更新
- 可“在线升级”和修复，多服务器可选
- 可根据用户需求定制的优化脚本，可制作专属升级包

***

# 已预置语言包：
* United States – English
* 中文（简体）
* 中文（繁体）
* 대한민국 – 한국어
* 日本 - 日本語
* 俄语

***

# 如何下载

* 从 GitHub 里下载
* 从作者官方网站下载

***

# 支持的操作系统

* Windows 10
	* PowerShell 5.1
	* PowerShell 7.1

* Windows 11
	* PowerShell 5.1
	* PowerShell 7.1

或系统自带 PowerShell 5.1 以上的操作系统

***

## 如何使用：

* 解压压缩包
* 鼠标指向开始菜单上的微标，点击右键，打开
  * Windows 10：打开 Windows PowerShell
  * Windows 11：Windows Terminal (Admin)

* 打开后，输入以下代码将执行策略更改为“绕过”
```powershell
Set-ExecutionPolicy -ExecutionPolicy Bypass -Scope Process -Force
```

* 获取 Yi.ps1 所在路径，例如复制文件路径，再在 PowerShell 会话中运行文件名路径

* 绝对路径：d:\Yi\Yi.ps1
  * 运行：`Set-Location -Path "D:\Yi"`
  * 运行：`.\Yi.ps1`

***

### 如何运行特定功能

要运行 [特定功能](https://docs.microsoft.com/zh-cn/powershell/module/microsoft.powershell.core/about/about_operators#dot-sourcing-operator-) 的点源的 `Yi.ps1` 第一个文件： 

```powershell
# 以点开始
.\Yi.ps1
```

### 现在你可以这样做（需要引导）

```powershell
.\Yi.ps1 <tab>
.\Yi.ps1 -Functions <tab>
.\Yi.ps1 -Functions KeepSpace <tab>
.\Yi.ps1 -Functions "FirstExperience -Force", "KeepSpace -Disable", DiskCleanup
```

### 或者使用没有 TAB 功能自动完成功能的旧式格式（需要引导）

```powershell
.\Yi.ps1 -Functions RestorePointCreate "FirstExperience -Force",  DiskCleanup
```

# 如何自定义

- 参阅 Template.ps1，在 #Go 处添加自定义代码。
- 或允许首次预体验，按计划，运行：

```powershell
.\Yi.ps1 -FirstExperience
```

参阅：Modules\Functions\Engine.FirstExperience.psm1
