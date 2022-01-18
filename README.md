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

# 如何运行特定功能

要运行 [特定功能](https://docs.microsoft.com/zh-cn/powershell/module/microsoft.powershell.core/about/about_operators#dot-sourcing-operator-) 的点源的 `Yi.ps1` 第一个文件： 

```powershell
# 以点开始
.\Yi.ps1
```

- 现在你可以这样做（需要引导）

```powershell
.\Yi.ps1 <tab>
.\Yi.ps1 -Functions <tab>
.\Yi.ps1 -Functions KeepSpace <tab>
.\Yi.ps1 -Functions "FirstExperience -Force", "KeepSpace -Disable", DiskCleanup
```

- 或者使用没有 TAB 功能自动完成功能的旧式格式（需要引导）

```powershell
.\Yi.ps1 -Functions RestorePointCreate "FirstExperience -Force",  DiskCleanup
```

***

# 如何自定义

- 参阅 Template.ps1，在 #Go 处添加自定义代码。
- 或允许首次预体验，按计划，运行：

```powershell
.\Yi.ps1 -FirstExperience
```

参阅：Modules\Functions\Engine.FirstExperience.psm1

***

# 核心功能

* 更改用户文件夹的位置 
  * 桌面
  * 文档
  * 下载
  * 音乐
  * 图片
  * 视频

* 添加桌面图标
  * 计算机
  * 回收站
  * 用户的文件
  * 控制面板
  * 网络
  * 上帝模式
  * Internet Explorer

* 优化

  * 系统类
    * 禁用 TPM 安装检查
    * 禁用 TPM 阻止您升级系统
    * 保留空间
    * 休眠
    * 电源模式：高性能
    * "此应用正在阻止关机或重新启动" 屏幕
    * NumLock 键开机后自动亮起
    * 用户账户控制 (UAC)：从不通知我
    * 禁用 Smart Screen 应用和文件检查
    * 禁用 SmartScreen 下载的文件标记为不安全
    * 禁用 轻松访问键盘的东西
    * 自动维护计划
    * 客户体验改善计划
    * 禁用 磁盘碎片整理计划
    * 程序兼容性助手
    * 优化视觉动画效果
    * Windows 错误恢复
    * DEP 和 PAE
    * 断电后自动修复功能
    * 密码最长使用时间为无限
    * 降低 RAM 使用处理器数量
    * 禁用存储感知
    * 禁用 传递优化
    * 照片预览
    * "Windows 保护了您的 PC" 对话框
    * 错误报告
    * F8 启动菜单选项
    * SSD
    * 内存压缩
    * 预取预启动


  * 优化网络
    * 恢复 IE 设置代理不生效
    * 禁用 IE 自动检查设置
    * 禁用 网络发现文件和打印机共享
    * 禁用 关闭网络适配器以节省电量
    * 禁用 Internet 协议版本 6 (TCP/IPv6)组件
    * QOS 服务
    * 网络调优功能
    * ECN 功能


  * 文件资源管理器
    * 启用 每个资源管理器窗口使用单独进程
    * 启用 登录后重启应用
    * 启用 项目复选框
    * 禁用 缩略图缓存删除
    * 将默认资源管理器视图设置为：此 PC
    * 禁用 Aero Shake 摇一摇降到最低功能
    * 显示 已知文件类型的扩展名
    * 常见文件类型安全警告
    * 设置 文件传输对话框：详细信息
    * 在导航窗格中打开 "显示所有文件夹"
    * 自动播放
    * 自动运行所有驱动器
    * 禁用 "快速访问" 中显示最近使用的文件
    * 禁用 "快速访问" 和显示常用文件夹
    * 删除快捷方式小箭头和后缀
    * 从这台 PC 上删除：桌面、文档、下载、音乐、图片、视频、3D 对象

  * 上下文菜单
    * 启用经典风格
    * 取得所有权
    * 添加 复制路径
    * 增加 15 个文件选择限制

  * 通知中心
    * 关闭通知中心（完全、部分）

  * 系统盘分页大小（重启生效）
    * 设置系统分页大小（8G、16G）

  * 个性化
    * 将深色应用到：应用程序、系统
    * 禁用 透明效果
    * 禁用 Snap 辅助

  * 开始菜单和任务栏
    * 将任务栏圣齐设置为：居中、左对齐
    * 隐藏 任务栏小组件图标
    * 删除 小组件
    * 禁用 Microsoft Teams 自动启动
    * 禁用 Microsoft Teams 聊天图标
    * 禁用 开始菜单中的 Bing 搜索
    * 隐藏 在 "设置" 应用中向我推荐内容
    * 禁用 有关如何设置设备的建议
    * 设置 任务栏：显示搜索图标
    * 合并任务栏按钮：从不
    * 通知区域：始终显示所有图标
    * 在任务栏上隐藏 Cortana 按钮
    * 在任务上隐藏 任务视图 按钮

  * 游戏
    * 禁用 Xbox 游戏栏
    * 禁用 Xbox 游戏栏提示
    * 禁用 Xbox 游戏模式
    * 禁用 Xbox DVR

  * 隐私设置
    * 禁用 诊断跟踪计划任务
    * 禁用 向 MS 发送语音、墨迹和打字样本
    * 禁用 向 MS 发送联系人
    * 禁用 让网站通过访问我的语言列表来提供本的相关内容
    * 禁用 让应用使我的广告 ID 进行跨应用体验
    * 禁用 位置感知打印
    * 禁用 设置同步
    * 禁用 墨迹书写和打字个性化
    * 禁用 与未配对设备共享信息
    * 禁用 位置传感器
    * 禁用 Windows Hello 生物识别
    * 禁用 兼容性遥测
    * 禁用 诊断数据
    * 禁用 量身定制的体验
    * 禁用 反馈通知
    * 禁用 位置追踪
    * 禁用 互联用户体验和遥测
    * 禁用 默认应用的后台访问
    * 禁用 向 MS 提交 Windows Defend 调查结果
    * 禁用 时间轴时间
    * 禁用 收集活动历史记录

  * 其它
    * 启用 3389 远程桌面
    * 打开 SMB 文件共享

  * 清理
    * 发送到
    * 系统日志
    * 磁盘清理
    * WinSxS 

  * 优化服务

 * 系统自带软件
    * 关闭 Windows 更新
      * 禁用 自动下载和安装 Windows 更新
      * 隐藏 在更新后向我展示 Windows 欢迎体验
      * 隐藏 升级后的首次动画
      * 禁用 通过组策略禁用对其它计算机的更新种子
      * 禁用 自动驱动程序更新
      * 禁用 有可用更新消息
      * 禁用 TPM 阻止您升级系统

    * Microsoft Defender 防病毒
      * 禁用 Defend 提供的有关登录 Microsoft 帐户的信息
      * 禁用 Defend 提供的有关打开 Microsoft Edge 的 SmartScreen 过滤器的信息

    * Microsoft Defender 防火墙
    * 删除 OneDrive
    * 删除 Edge
    * 删除 小组件

* 删除 UWP 应用
    * 阻止重新安装应用程序
    * 隐藏 在 "设置" 应用中向我推荐内容
    * 关闭 Microsoft Store 自动下载 
    * 阻止安装“建议的应用程序”
    * 禁用 有关如何设置设备的建议




