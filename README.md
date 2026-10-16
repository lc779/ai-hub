# AI Hub

> **唯一官方仓库与下载地址**：[github.com/lc779/ai-hub](https://github.com/lc779/ai-hub)
>
> 任何其他域名、镜像、fork 的安装包均非官方发布。下载后请用 Release 附带的 `SHA256SUMS` 校验。
> 核对方法：程序内「检查更新」指向的地址应与本页一致；本页以外任何"官网"都是钓鱼站。

[![Release](https://img.shields.io/github/v/release/lc779/ai-hub)](https://github.com/lc779/ai-hub/releases/latest)

AI Hub 是一个 Windows 桌面启动器：统一管理与启动多个 AI 编程 CLI
（Claude Code、Codex、Qwen Code、Kimi、OpenCode、Crush、DeepSeek Shell 等），
并把模型端点、参数与更新通道集中配置 —— 所有 CLI 保持**官方原生**行为，
AI Hub 只做启动与配置的编排。

## 下载

| 场景 | 下载 |
|---|---|
| 首次安装 | Release 里的 `AI Hub_<版本>_x64-setup.exe`（用户目录安装，**无需管理员权限**） |
| 已安装用户 | 应用内「检查更新」（自动换入，失败自动回滚） |

系统要求：Windows 10 / 11（x64）。

## 校验

每个 Release 附带 `SHA256SUMS`（安装包与更新程序的 sha256）。下载后在 PowerShell 里：

```powershell
Get-FileHash .\AI Hub_*_x64-setup.exe -Algorithm SHA256
```

与 `SHA256SUMS` 里的对应行比对，一致即未被篡改。

## 本仓库包含什么

这个仓库**只用于分发**，不含源码：

* 每个 Release 的安装包与 `SHA256SUMS`；
* 两份**数据文件**（`adapter/cli-params.json`、`sources.json`）及其 Ed25519 签名
  （`.sig`）—— AI Hub 会周期性匿名读取它们，用于在不发版的情况下适配上游
  CLI 的变化。程序内置公钥，签名不符的文件一律不采用。

## 说明

* 本软件为个人作品，源码不公开；保留所有权利。
* 发现安全问题请按 [SECURITY.md](SECURITY.md) 的方式私下报告，不要在公开处披露。
