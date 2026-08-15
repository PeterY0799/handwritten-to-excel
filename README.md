# 墨格 · 手写图片转 Excel

一个纯前端的本地工具：上传手写图片，在浏览器内完成手写识别（OCR），校对后一键导出为 Excel 表格。

## 特性

- ✍️ 本地识别：基于 [Tesseract.js](https://github.com/naptha/tesseract.js)，图片与数据绝不上传服务器
- 🌏 支持中文 + 英文识别
- 🎚️ 亮度 / 对比度调节，提升识别准确率
- 📝 识别文本可编辑校对
- 📊 自动按行拆分表格、单元格可点击编辑、可增删行列
- ⬇️ 一键导出 `.xlsx`（基于 [SheetJS](https://sheetjs.com)）

## 使用

直接打开页面即可。首次识别需联网下载识别模型，之后浏览器会缓存，可离线使用。

### 本地预览

```bash
cd handwritten-to-excel
python3 -m http.server 8080
# 打开 http://localhost:8080
```

## 部署到 GitHub Pages

1. 将本目录内容推送到 GitHub 仓库
2. 在仓库 Settings → Pages 中，选择分支 `main` 与根目录 `/` 作为发布源
3. 访问 `https://<用户名>.github.io/<仓库名>/`

## 技术栈

- Tesseract.js（OCR）
- SheetJS（xlsx 导出）
- 原生 HTML / CSS / JavaScript（无构建步骤）