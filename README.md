# 解剖 dsh：系列实操样例

本仓库保存《解剖 dsh》系列的可复现实操样例，面向第一次用 dsh 完成任务的读者。每个样例固定软件版本，并附任务输入、独立验收程序和下载文件校验值。

## 第 3 篇：六个真实痛点

对应文章《dsh 能解决什么？拿一个小网站，实测六个真实痛点》。

- 固定 dsh 版本：`0.2.1-alpha.2`。
- 实测日期：2026-10-10；v1 发布：2026-10-11；**v2 修订：2026-10-12；实际上传：2026-10-13**。
- 作者实测：Windows / Node v24.16.0 / PowerShell 7.6.5；读者复测：Node v22.22.2 / **Windows 自带 PowerShell 5.1（zh-CN，GBK 码页 936）编码修复后通过**。
- 任务：检查六页普通 HTML/CSS 网站的缺图、缺文件链接、缺锚点。教学样例故意包含错误。

**[直接下载样例 ZIP（v2 修订版）](https://github.com/redants-101/dsh-article-samples/releases/download/article-03-dsh-v0.2.1-alpha.2-v2/article-03-dsh-v0.2.1-alpha.2-samples.zip)** · **[查看版本与附件说明](https://github.com/redants-101/dsh-article-samples/releases/tag/article-03-dsh-v0.2.1-alpha.2-v2)**

下载文件名：`article-03-dsh-v0.2.1-alpha.2-samples.zip`。页面底部的 Source code 归档不是这个练习包。

下载后解压，先读 `实操样例/README.md`；按说明配置模型凭证，再在 `实操样例/site` 目录运行任务。不要把包含答案的上一层目录作为模型工作区。

ZIP 共 16 个文件，包含六页网站及资源、检查和续接任务、独立验收、标准答案、原始文件校验值，以及只读拒写探针。没有依赖、API Key 或作者运行报告。调用远程模型可能产生费用；只读实验应在样例上进行。

检查与验收覆盖本地静态引用，不代表浏览器效果、外链、脚本路由或整个网站可上线。

### Windows PowerShell 编码提示

README 的三处 PowerShell 命令序列都包含两行 UTF-8 设置，**都不能省**：

- `[Console]::OutputEncoding` 管输出方向（dsh 吐出的 JSON 按 UTF-8 解码）
- `$OutputEncoding` 管输入方向（中文任务按 UTF-8 传进管道）

Windows 自带的 PowerShell 5.1 默认按 GBK 解码子进程输出。缺少 `[Console]::OutputEncoding` 时中文会乱码，UTF-8 中文尾字节还会吞掉路径反斜杠，导致 JSON 转义失效、`ConvertFrom-Json` 报"无法识别的转义序列"、结果文件不可逆损坏。PowerShell 7 默认即 UTF-8，不受影响。

v1（2026-10-11 发布）缺该行，已保留在原 Release 页便于对照；请使用 v2。

## 文件校验

SHA-256（v2）：
```text
7a3370668703e7b044a3072de5401728af4c75750763b0d99ef722e2ede75679  article-03-dsh-v0.2.1-alpha.2-samples.zip
```

后续修订会发布新的版本附件，保留已发布版本，便于读者复现文章。

<!-- article-04-current:start -->
## 第 4 篇：都能加插件，dsh 到底还能改什么？

- [固定发行页（v2）](https://github.com/redants-101/dsh-article-samples/releases/tag/article-04-dsh-v0.2.1-alpha.2-opencode-v1.19.0-v2)
- [直接下载第 4 篇 ZIP](https://github.com/redants-101/dsh-article-samples/releases/download/article-04-dsh-v0.2.1-alpha.2-opencode-v1.19.0-v2/article-04-dsh-v0.2.1-alpha.2-opencode-v1.19.0-samples.zip)
- [SHA-256 校验文件](https://github.com/redants-101/dsh-article-samples/releases/download/article-04-dsh-v0.2.1-alpha.2-opencode-v1.19.0-v2/SHA256SUMS.txt)
- 固定版本：dsh 0.2.1-alpha.2 / OpenCode 1.19.0；Windows / Node 24 / PowerShell 7。
- 33 文件、45804 字节；六页网站、共享邮箱规则、两产品工具与独立验收。
- 同一任务实际调用、工具结果、final、会话关联与时序、八文件不变性分别验收。Web 是 Session 接口实验；未验网页按钮。
- 下载后先读 README.md；模型凭证自行提供。不含作者凭证、私有 home 或运行结果。
- SHA-256：`5692e13271b7695c10e73682875bffb4e0b4f8e52bfd5dfc31b7164eaece416d`

保留第 3 篇 v1/v2 和第 4 篇 v1；第 4 篇使用独立扩展包，不能用第 3 篇 ZIP 代替。
<!-- article-04-current:end -->
