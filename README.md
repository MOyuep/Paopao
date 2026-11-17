[PaoPao-仓库README.md](https://github.com/user-attachments/files/34978728/PaoPao-.README.md)
# PaoPao · 陪伴 Agent 的可审计长期记忆模块

面向陪伴 Agent 的可审计长期记忆模块，内置冲突消解、中文检索补丁、契约测试与运行时护栏。

> **本仓库是一份设计报告，不是软件。**
> 完整报告在 [`paopao-memory-report-2026-11-17/`](./paopao-memory-report-2026-11-17/)。

---

## 直接开始

| 想干什么 | 去哪 |
|---|---|
| **读报告（网页版）** | [report.html](./paopao-memory-report-2026-11-17/report.html) |
| **下载定版 PDF** | [Releases](../../releases) |
| 知道这一夜改了什么 | [01-报告.md](./paopao-memory-report-2026-11-17/01-报告.md) |
| 理解系统怎么组织 | [02-架构.md](./paopao-memory-report-2026-11-17/02-架构.md) |
| 核对设计依据 | [03-文献.md](./paopao-memory-report-2026-11-17/03-文献.md) |
| 看运行时护栏 | [06-工程防御护栏.md](./paopao-memory-report-2026-11-17/06-工程防御护栏.md) |
| 交接前必读 | [05-安全说明.md](./paopao-memory-report-2026-11-17/05-安全说明.md) |

---

## 一句话

把记忆系统从「会静默损坏数据」改造成「写入与检索各有单一收口、阈值全部有实测依据、关键不变量有断言保护」，并加了一层运行时防御护栏。

- 契约测试：**354 项**，全绿
- 检索评估：26 条 golden query，hit@1 **19/26**、MRR **0.816**
- 定版 PDF：**63 页**

---

## 完整性校验

所有文件的 SHA-256 记录在 [`SHA256SUMS.txt`](./paopao-memory-report-2026-11-17/SHA256SUMS.txt)。

```bash
# Linux / macOS
cd paopao-memory-report-2026-11-17 && sha256sum -c SHA256SUMS.txt
```

```powershell
# Windows
Get-FileHash .\paopao-memory-report-2026-11-17\泡泡记忆模块报告-2026-11-17.pdf -Algorithm SHA256
```

任何文件被改动，哈希即不符。

---

## 声明

- 这是**工程原型**，不能直接商用或大规模上线。
- 思路参考了 TOKI、NeuSymMS 等论文，**不是官方实现**，也没有原作者背书。
- 报告是**脱敏版**：不含密钥、账号、聊天内容、本机路径。脱敏方法与验证见 [05-安全说明.md](./paopao-memory-report-2026-11-17/05-安全说明.md)。

---

## 许可证

[GNU General Public License v3.0](./LICENSE)
