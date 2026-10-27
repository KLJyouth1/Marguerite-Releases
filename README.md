# Marguerite Releases

**Marguerite 桌面工作台的官方安装包仓库。** 本仓库不含源码——源码在
[Marguerite](https://github.com/KLJyouth1/Marguerite)，配套模型在
[KLJyouth-office-Modle](https://github.com/KLJyouth1/KLJyouth-office-Modle)。

所有二进制发布在 **[Releases](https://github.com/KLJyouth1/Marguerite-Releases/releases)**。

## 版本一览

| 版本 | 状态 | 文件 |
|---|---|---|
| **0.2.17** | 最新 | `Marguerite_0.2.17_x64_en-US.msi`（WiX，372.7 MB）<br>`Marguerite_0.2.17_x64-setup.exe`（NSIS，352.8 MB） |
| 0.2.13 | 历史 | `Marguerite_0.2.13_x64_en-US.msi`（WiX，251.7 MB）<br>`Marguerite_0.2.13_x64-setup.exe`（NSIS，240.5 MB） |
| 0.2.12 | 历史 | `Marguerite_0.2.12_x64_en-US.msi`（251.1 MB）<br>`Marguerite_0.2.12_x64-setup.exe`（240.0 MB） |

0.2.17 的主要变化：插件 / MCP / 工具 / 技能四类扩展的独立管理界面（启停、重载、MCP 子进程
真实调用），能力路由（能力卡 + 18 项固定工具面 + 反脚本纠偏），会话可移植（JSON / Markdown
无损导入导出）与任务复盘，多项目工作区与终端多根，电脑操控的 UIA 结构化动作矩阵与
observe → act → verify 回执。逐条说明见源码仓库的 `CHANGELOG.md`。

## 下载与安装

| 形态 | 适用场景 |
|---|---|
| `.msi`（WiX） | **推荐**。支持静默安装（`msiexec /i <file>.msi /qn`）与企业分发 |
| `-setup.exe`（NSIS） | 双击安装，可自选安装目录，适合个人用户 |

安装包内已含：Rust 引擎、前端控制台、Python 侧车、内置技能，以及 **WebView2 离线安装器**
（`webviewInstallMode: offlineInstaller`），因此**断网也能装**。

## 校验

每个 Release 附带 `SHA256SUMS.txt`；仓库根目录也保留一份汇总。核对方式：

```powershell
Get-FileHash .\Marguerite_0.2.17_x64_en-US.msi -Algorithm SHA256
# 与 SHA256SUMS.txt 中同名行比对（大小写不敏感）
```

## 相关仓库

| 仓库 | 内容 |
|---|---|
| [Marguerite](https://github.com/KLJyouth1/Marguerite) | 工作台源码（Rust 引擎 / TUI / Tauri 桌面端 / 回环 Web 控制台 / Python 侧车） |
| **Marguerite Releases**（本仓库） | 安装包与发布产物 |
| [KLJyouth-office-Modle](https://github.com/KLJyouth1/KLJyouth-office-Modle) | 配套本地智能体模型：fp16 GGUF / safetensors、7-Zip 分卷 |

## 第三方许可

安装包内含第三方组件；许可清单见源码仓库 `THIRD_PARTY_NOTICES` 与
`pyengine/THIRD_PARTY_NOTICES.md`。

