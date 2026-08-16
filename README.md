# pdf-outline-generator (PDF 目录/书签骨架注入工具)

[English](#english) | [简体中文](#简体中文)

---

<a name="简体中文"></a>
## 简体中文

### 📖 项目简介
在处理扫描版 PDF 或缺少/损坏书签的电子书时，重新手动逐条添加目录耗时耗力。本项目是一个基于 PyMuPDF (`fitz`) 的轻量级 Python 自动化工具。

它通过解析带有空格缩进格式的纯文本（TXT）目录，自动将结构化的多级书签骨架注入到 PDF 文件中，并统一重置初始页码，为后续使用 Adobe Acrobat 或鼠标宏进行精准物理对齐提供支撑。

### ✨ 核心功能
- **旧书签彻底清理**：支持一键清空原 PDF 中损坏或乱码的旧书签。
- **智能层级解析**：根据 TXT 目录文本的空格缩进（默认 4 个空格递进一级）自动计算书签层级（Level 1, Level 2...）。
- **文本清洗与剥离**：自动识别并剥离标题末尾的原始页码，将跳转页码统一归一化。
- **体积压缩与优化**：在保存时开启 PyMuPDF 垃圾回收（Garbage Collection）与流压缩（Deflate），优化 PDF 文件体积。

### 🛠️ 环境要求与安装

需要安装 `PyMuPDF` 依赖库：

```bash
# 安装 PyMuPDF 依赖库
pip install PyMuPDF
```

<a name="English"></a>
📖 Introduction
When dealing with scanned PDFs or ebooks with missing/corrupted bookmarks, manually adding a full table of contents (TOC) is tedious. This project is a lightweight Python automation tool built on PyMuPDF (fitz).

It parses indented plain-text (TXT) TOC files, injects structured multi-level bookmark skeletons into the PDF, and unifies initial target pages to streamline post-processing (e.g., aligning actual page numbers using Adobe Acrobat or mouse macros).

✨ Features
Purge Corrupted TOC: Cleanly wipe existing, broken, or corrupted bookmarks from the source PDF.

Auto-Level Indentation: Automatically detect bookmark depth based on text indentation (default: 4 spaces per level).

Page Number Stripping: Automatically clean up raw trailing page numbers from text lines.

File Optimization: Apply PyMuPDF garbage collection (garbage=3) and stream compression (deflate=True) on file export.

```bash
# instail PyMuPDF package
pip install PyMuPDF
```
