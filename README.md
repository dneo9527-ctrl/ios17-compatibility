# iOS 17.0 兼容记录

针对 **iPhone 15 Pro / iOS 17.0 / TrollStore** 的三个指定版本，记录现有反馈、已知问题和本地文件校验值。

**下载内容仅为说明、JSON 清单与 SHA-256 校验值。** 完整 IPA 保留在原本的本机环境，本仓库不提供应用二进制、第三方应用源码或签名服务。

| 应用 | 固定版本 | 已确认的范围 | 保留的问题 |
| --- | --- | --- | --- |
| Muse | 14.4.0 / 补丁 4.3 | 4.2 的旁聊路径此前有成功反馈 | 4.3 的 Review 修复尚缺真机成功确认，不能套用 14.3 的反馈 |
| ChatGPT | 1.2026.300 / 候选 10 | 输入、聊天正常，设置顶部空白行已修复 | Codex → Settings → Profile 无限卡死，App 内 Logo 动画缺失仍存在 |
| 3X Client | 1.2 / 兼容版 2（Build 1202） | VPS → Xray Config 可以打开并复制 | 尚未逐项验收所有页面、全部配置字节或长期稳定性 |

ChatGPT 诊断候选 13、Claude 和 ServerCat 均不在此清单。记录更新于 2026-11-19；本次整理没有新增设备、安装或签名验收。

## 校验记录

[compatibility.json](compatibility.json) 包含相对文件名、版本、字节数与 SHA-256；[IPA-SHA256SUMS](IPA-SHA256SUMS) 可核对自己合法持有的对应文件。校验一致只证明与记录文件相同，不表示签名有效、安装兼容或功能全部通过。

在自己保存对应文件的目录，macOS 可执行 `shasum -a 256 -c IPA-SHA256SUMS`，Linux 可执行 `sha256sum -c IPA-SHA256SUMS`。本目录不提供这些 IPA，因此直接在仓库目录运行会提示找不到文件。

可从 [文档发行](https://github.com/dneo9527-ctrl/ios17-compatibility/releases) 下载完整记录快照；发行附件中的 DOCUMENTS-SHA256SUMS 校验文档附件，与 IPA-SHA256SUMS 的用途不同。

## 适用边界

范围固定为上述设备、系统和既有 TrollStore 环境，不推广到其他系统、安装工具或机型。安装及账号状态会受原应用和设备环境影响；不要因这份清单删除现用 App、退出账号或公开设备信息。

本仓库不含原始构建清单中的本机绝对路径、诊断日志、截图、设备数据、账号或凭据。反馈时请同样去除这些信息。第三方名称、商标和应用权利属于各自权利人；本库未给这些应用添加 MIT 或其他再分发许可，见 [NOTICE.md](NOTICE.md)。
