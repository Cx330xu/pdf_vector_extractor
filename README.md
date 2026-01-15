# PDF Vector Extractor (PDF 矢量截取工具)

![Version](https://img.shields.io/badge/version-1.0.0-blue) ![License](https://img.shields.io/badge/license-MIT-green) ![Status](https://img.shields.io/badge/build-passing-brightgreen) ![Platform](https://img.shields.io/badge/platform-Web%20%7C%20Browser-orange)

[English](#english) | [中文](#chinese)

---

<a name="english"></a>

## 🇬🇧 English

### 1. Project Overview

**PDF Vector Extractor** is a high-precision, web-based tool designed to extract specific regions from PDF documents while preserving their original vector format. Unlike traditional snapshot tools that convert content to raster images (PNG/JPG), this tool generates cropped PDF files. This ensures that text remains selectable, and the content retains infinite scalability without pixelation, making it ideal for academic research, professional document processing, and high-quality archiving.

### 2. Features

- **Vector Preservation**: Extracts content as PDF files, maintaining vector graphics and selectable text.
- **Precision Cropping**: Supports custom bounding boxes, axis locking (X-axis lock for header/footer removal), and keyboard fine-tuning.
- **Batch Processing**: Capture multiple regions across different pages and merge them into a single PDF export.
- **Productivity Tools**: Auto-paging, page jumping, and keyboard shortcuts (Space to capture, Arrow keys to navigate/adjust).
- **State Persistence**: Automatically saves work progress locally using IndexedDB/SessionStorage; recover your session after closing the browser.
- **Privacy First**: Purely client-side processing; no files are uploaded to any server.

### 3. Installation Guide

#### Prerequisites

- A modern web browser (Chrome, Edge, Firefox).
- (Optional) Python 3.x for running a local server.

#### Installation Methods

**Method 1: Clone and Run (Recommended)**

```bash
# 1. Clone the repository
git clone https://github.com/your-username/pdf-vector-extractor.git

# 2. Navigate to the project directory
cd pdf_vector_extractor

# 3. Start a simple HTTP server (Recommended for best performance)
python -m http.server 8000
```

Then open `http://localhost:8000/index4右键重置.html` in your browser.

**Method 2: Direct File Open**
Simply locate `index4右键重置.html` in your file explorer and double-click to open it in your browser.
*Note: Some features (like loading external resources) might be restricted by browser security policies when using the `file://` protocol.*

### 4. Usage Instructions

#### Interface Overview

- **Sidebar**: Load files, control settings, view captured list, and export.
- **Main Area**: PDF viewer with overlay crop box.
- **Toolbar**: Zoom, navigation, auto-paging controls.

#### Basic Workflow

1. **Load PDF**: Click "Load File" (加载文件) in the sidebar.
2. **Select Region**: 
   - Drag the red crop box to your desired area.
   - Use "Lock X-axis" (锁定X轴) to fix the width to the page width.
3. **Capture**: Press **Spacebar** or click "Capture" (截取).
4. **Export**: Click "Export PDF" (导出PDF) to download the merged file.

#### Keyboard Shortcuts

| Key                   | Action                    |
| --------------------- | ------------------------- |
| `Space`               | Capture current selection |
| `←` / `→`             | Previous / Next page      |
| `↑` / `↓`             | Fine-tune crop box height |
| `PageUp` / `PageDown` | Previous / Next page      |

### 5. Development Guide

#### Project Structure

```
pdf_vector_extractor/
├── index4右键重置.html    # Main Application (Latest Version)
├── bbox_tool.html        # Bounding Box Annotation Tool
├── assets/               # Icons and styles (if applicable)
└── README.md             # Documentation
```

#### Contributing

1. Fork the repository.
2. Create your feature branch (`git checkout -b feature/AmazingFeature`).
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`).
4. Push to the branch (`git push origin feature/AmazingFeature`).
5. Open a Pull Request.

#### Testing

Since this is a client-side tool, testing involves:

- Loading various PDF types (Text-heavy, Image-heavy, Large files).
- Verifying vector output quality in Adobe Acrobat or standard PDF readers.
- Checking browser compatibility.

### 6. License

Distributed under the **MIT License**. See `LICENSE` for more information.

### 7. Support

If you encounter any issues or have questions:

- **Issues**: Please file a bug report in the GitHub Issues section.
- **Contact**: email@example.com

---

<a name="chinese"></a>

## 🇨🇳 中文

### 1. 项目概述

**PDF Vector Extractor (PDF 矢量截取工具)** 是一款基于 Web 的高精度 PDF 处理工具，专为从 PDF 文档中提取特定区域而设计，同时完整保留原始矢量格式。与将内容转换为位图（PNG/JPG）的传统截图工具不同，本工具生成的是裁剪后的 PDF 文件。这确保了文本可选、内容可无损缩放且不失真，非常适合学术研究、专业文档处理和高质量归档。

### 2. 功能特性

- **矢量保留**：截取结果为 PDF 格式，保持矢量图形清晰度和文本的可选/可复制性。
- **精准截取**：支持自定义截取框、轴锁定（锁定宽度以去除页眉页脚）和键盘微调。
- **批量处理**：支持跨页面截取多个区域，并自动合并导出为一个 PDF 文件。
- **效率工具**：支持自动连续翻页、页码跳转和丰富的快捷键（空格截取、方向键导航）。
- **状态持久化**：使用 IndexedDB/SessionStorage 自动保存工作进度；关闭浏览器后重新打开可恢复现场。
- **隐私安全**：纯客户端处理，所有文件均在本地浏览器中运行，不会上传至任何服务器。

### 3. 安装指南

#### 系统要求

- 现代网页浏览器（Chrome, Edge, Firefox）。
- （可选）Python 3.x，用于启动本地服务器。

#### 安装/运行方式

**方式一：克隆并运行（推荐）**

```bash
# 1. 克隆仓库
git clone https://github.com/your-username/pdf-vector-extractor.git

# 2. 进入项目目录
cd pdf_vector_extractor

# 3. 启动简单 HTTP 服务器（推荐，以获得最佳性能）
python -m http.server 8000
```

然后在浏览器中访问 `http://localhost:8000/index4右键重置.html`。

**方式二：直接打开**
在文件管理器中找到 `index4右键重置.html`，直接双击使用浏览器打开。
*注意：由于浏览器安全策略，直接使用 `file://` 协议打开时，某些功能（如加载外部资源或特定跨域操作）可能会受限。*

### 4. 使用说明

#### 界面概览

- **侧边栏**：文件加载、截取设置、已截取列表和导出控制。
- **主区域**：PDF 视图窗口，包含红色的截取选框。
- **工具栏**：缩放、翻页导航、自动翻页设置。

#### 基本流程

1. **加载 PDF**：点击侧边栏的 "加载文件" 按钮。
2. **设置选区**：
   - 拖动红色选框到目标位置。
   - 使用 "锁定X轴(宽)" 功能将宽度固定为页面宽度（适合整页截取）。
3. **截取**：按 **空格键** 或点击 "截取选中区域" 按钮。
4. **导出**：点击 "导出PDF" 下载合并后的文件。

#### 快捷键列表

| 按键                  | 功能            |
| --------------------- | --------------- |
| `空格`                | 截取当前选区    |
| `←` / `→`             | 上一页 / 下一页 |
| `↑` / `↓`             | 微调选区高度    |
| `PageUp` / `PageDown` | 翻页            |

### 5. 开发指南

#### 项目结构

```
pdf_vector_extractor/
├── index4右键重置.html    # 主应用程序（最新版）
├── bbox_tool.html        # BBox 标注工具
└── README.md             # 项目文档
```

#### 测试方法

由于是纯前端工具，测试主要包含：

- 加载不同类型的 PDF（纯文本、扫描件、大文件）。
- 验证导出的 PDF 在 Adobe Acrobat 或其他阅读器中的显示质量（确认矢量特性）。
- 检查主流浏览器的兼容性。

