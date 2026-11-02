红果短剧桌面版 0.2.141（macOS / Windows）

本版与统一主线同步，桌面更新版本码为 78。

- 播放取源请求补上签名，修复上游对无签名请求返回空正文导致的 `VIDEO_MODEL_EMPTY` 无法播放。
- 保留有界兼容回退：签名原主机 → 签名备用主机 → 原无签名请求；连续空响应的匿名身份更换和总请求预算不变，不会无限重试。
- 预取分集的加载提示分阶段显示，减少切集时的提示闪动。

- 账号签名、播放 UA、清晰度筛选和 HTML5 播放路径不变；保留播放控件按需刷新、启动页面设置、搜索建议及侧栏焦点改进。
- 竖屏播放可在设置中选择动态模糊背景延伸；默认仍为黑色，不改变视频画面和播放器行为。
- 空播放响应的匿名身份恢复保持有上限；不会切换登录账号，也不会对普通网络或解码错误触发恢复。

macOS 通用 ZIP 支持 Intel / Apple Silicon，最低 macOS 11；Windows x64 需要 Microsoft Edge WebView2 Runtime。Windows 播放 HEVC 还需要安装 HEVC Video Extensions；商店无法获取时，可参考 https://github.com/Ayx03/HEVCVideoExtension。Linux x86_64 AppImage 测试版通过容器实播检查后在独立的 `linux-v0.2.141-test.1` 预发行版中提供，依赖系统 WebKitGTK 和 GStreamer。

通过设置检查更新并下载 ZIP，退出后手动替换完整程序。账号及本地记录保存在独立用户目录。
未做 Apple 公证或 Windows 代码签名。Windows 实体播放仍待实测。
