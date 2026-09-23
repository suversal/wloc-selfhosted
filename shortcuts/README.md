# 自托管快捷指令源码

- `WLOC设置位置-自托管.plist`：地图分享入口，解析接口已改为 `https://wloc-selfhosted.suyang219.workers.dev/api/parse`。
- `WLOC恢复定位-自托管.plist`：清除代理工具本机持久化坐标，不依赖解析 Worker。

这里保留的是便于审计和版本控制的 plist 源码，不是可直接导入的 Apple 签名文件。可导入版本应在“快捷指令”App 中从原始已签名版本复制、按此源码修改并由自己的 Apple ID 重新生成 iCloud 分享链接。

两个快捷指令仍使用 `gs-loc.apple.com/wloc-settings/save`。该 URL 是代理模块的本机拦截入口，不应替换成 Worker 域名。
