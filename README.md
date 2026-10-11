# 解剖 dsh：系列实操样例

本仓库保存《解剖 dsh》系列的可复现实操样例，面向第一次用 dsh 完成任务的读者。每个样例固定软件版本，并附任务输入、独立验收程序和下载文件校验值。

## 第 3 篇：六个真实痛点

对应文章《dsh 能解决什么？拿一个小网站，实测六个真实痛点》。

- 固定 dsh 版本：`0.2.1-alpha.2`。
- 实测日期：2026-10-10；发布样例日期：2026-10-11。
- 实测环境：Windows / Node v24.16.0 / PowerShell 7.6.5。
- 任务：检查六页普通 HTML/CSS 网站的缺图、缺文件链接、缺锚点。教学样例故意包含错误。

**[直接下载样例 ZIP](https://github.com/redants-101/dsh-article-samples/releases/download/article-03-dsh-v0.2.1-alpha.2-v1/article-03-dsh-v0.2.1-alpha.2-samples.zip)** · **[查看版本与附件说明](https://github.com/redants-101/dsh-article-samples/releases/tag/article-03-dsh-v0.2.1-alpha.2-v1)**

下载文件名：`article-03-dsh-v0.2.1-alpha.2-samples.zip`。页面底部的 Source code 归档不是这个练习包。

下载后解压，先读 `实操样例/README.md`；按说明配置模型凭证，再在 `实操样例/site` 目录运行任务。不要把包含答案的上一层目录作为模型工作区。

ZIP 共 16 个文件，包含六页网站及资源、检查和续接任务、独立验收、标准答案、原始文件校验值，以及只读拒写探针。没有依赖、API Key 或作者运行报告。调用远程模型可能产生费用；只读实验应在样例上进行。

检查与验收覆盖本地静态引用，不代表浏览器效果、外链、脚本路由或整个网站可上线。

## 文件校验

SHA-256：
```text
23fc4576a25566f9bc4700c4dca8827f1dc0faabb7521a834ccaf81bde4030af  article-03-dsh-v0.2.1-alpha.2-samples.zip
```

后续修订会发布新的版本附件，保留已发布版本，便于读者复现文章。