# Codex Remote 0.6.6 交付记录

## 版本与目录约定

- Android 正式包名 `com.galasports.codexremote`，版本 `0.6.6` / `versionCode 12`，minSdk 23，沿用既有共同签名。
- 两发布仓库都按项目目录隔离。Gitee `mrzhaobh/my-releases/CodexRemote/` 保存最新与历史清单；GitHub `MrZhaobh/my-releases/CodexRemote/dist/0.6.6/` 保存本版本五个正式文件。
- Android 读取 Gitee `CodexRemote/version.json`；安装包固定为 GitHub raw HTTPS 地址，限制同一仓库、项目和版本目录。完整发布页是 GitHub 对应版本目录，不使用 GitHub Release。
- 先前不符合目录约定的 `codexremote-v0.6.5` Release 及标签已按用户要求删除，未激活过 Gitee 更新清单。本版本替代该次撤回发布，不覆盖旧版安装包，不提供旧更新源过渡适配。

## 更新内容

- 自动与手动检查共用更新说明，显示版本、发布时间和安装包大小；以 versionCode 判断新旧，支持忽略单个版本及独立重新检查。
- 前台服务管理下载，支持收起、取消和重试；Activity 重建继续已有任务。进程终止后下次打开可从头重新下载恢复，不承诺系统强停后持续下载，不实现 Range 断点续传。
- 下载完成和安装前核对大小、SHA-256、包名、版本、最低系统与共同签名。安装由用户点击后交给 Android 系统确认，不自动安装。
- 发布入口保留 Prepare、Upload、Activate 三阶段：先提交并核验 GitHub 项目版本目录，最后一次 Gitee 提交同时更新最新及历史清单。重复发布只复用完全相同的目录，内容冲突或远端并发变更时停止，不覆盖已发布版本。
- Windows 发布包保持当前 Bridge/IPC 与连接能力；本轮未部署、重启或切换正在运行的桌面、中继或共享引擎。

## 产物

- `CodexRemote-0.6.6.apk`。
- `CodexRemote-Windows-0.6.6.zip`。
- `Configuration.zh-CN.md`：简体中文配置说明。
- `Delivery.zh-CN.md`：本交付记录。
- `SHA256SUMS.txt`：覆盖前四个文件的 SHA-256。

运行凭据、个人配置、聊天内容、截图和测试数据不进入产物；正式目录及校验值保留在源码仓库 `releases/0.6.6/`。

## 验证范围

共同签名构建、协议/下载契约、发布器离线检查与正式五文件独立核验在发布前执行。本文件只记录打包时已经核实的行为和边界；实际 GitHub/Gitee 提交、匿名下载与模拟器完整公网更新的结果另记在源码仓库补充验收记录，不通过覆盖已上传附件补写。

模拟器基线是包含新目录协议的开发验收包，随后通过真实 Gitee/raw 链路更新；该结果不代表旧更新源迁移、Android 6–8.1 真机、目标手机网络或未知来源权限拒绝/授权切换已验证。未操作真机，不提交或推送源码仓库。
