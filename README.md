<div align="center">
  <img src="assets/title.svg" alt="Zhijian Reader" height="48">
</div>

纸间阅读器（Zhijian Reader）是一款本地优先的离线电子书 Web 应用。

所有书籍、阅读进度、书签与配置仅保存在浏览器本地（IndexedDB 与 localStorage），不会上传至任何外部服务器。无需后端服务，仅一个静态 HTML 文件，内置所需组件，运行时无需联网。

> 在线体验：[https://LC-0001.github.io/zhijian-reader/](https://LC-0001.github.io/zhijian-reader/)

## 功能
- 书架管理，支持 TXT、EPUB、PDF 导入，支持 ZIP 批量导入（自动解压其中的 TXT / EPUB / PDF）
- 导入时按书名去重，同名书籍会被跳过
- 阅读进度记录、目录跳转、书签、书摘卡片
- 阅读样式自定义：字号、行间距、纸张配色、自定义字体导入（支持 woff2、woff、ttf、otf）
- 主题控制，支持手动切换深浅色，或跟随系统主题自动变化
- 阅读数据备份与恢复（导出为 JSON 文件）
- 移动端与桌面端自适应布局

## 使用
1. 下载仓库根目录下的 `index.html`
2. 用浏览器打开即可使用

> 提示：直接双击打开本地文件（`file://`）时，部分功能可能受浏览器限制，建议使用静态网页服务访问。

## 数据说明
- **数据只保存在当前浏览器和当前设备上，不会跨设备同步。** 换手机、换电脑或换浏览器后，书架不会自动出现，需要通过备份文件迁移。
- **清除网站数据会丢失所有书籍和阅读进度**，请定期使用"备份"功能导出。
- 备份文件为 JSON 格式，PDF 内容会以数组形式写入其中。书籍较多或 PDF 较大时，备份文件会很大，导出与恢复也会较慢。

## 部署
本项目仅依赖静态资源，支持 GitHub Pages、Vercel、Netlify 等任意静态托管平台。

### GitHub Pages 部署步骤
1. Fork 本仓库到自己的账号
2. 进入仓库 Settings → Pages
3. Source 选择 `Deploy from a branch`，分支选择 `main`，目录选择 `/ (root)`，保存
4. 等待 1–2 分钟，访问 `https://<你的用户名>.github.io/zhijian-reader/`

## 本地开发
本项目为单文件静态页面，无依赖，无需安装任何包。

```bash
git clone https://github.com/LC-0001/zhijian-reader.git
cd zhijian-reader
python3 -m http.server 8000
```

访问 `http://localhost:8000`。

> 手机端开发：可在 Termux 中执行上述命令；或直接下载 `index.html`，用浏览器打开即可测试。

## 限制
- 数据存储依赖浏览器 IndexedDB，清除网站数据会丢失本地书籍，请定期导出备份。
- 大体积书籍导入时，性能取决于当前浏览器环境与设备内存。
- PDF 通过浏览器内嵌方式显示，显示效果取决于浏览器对 PDF 的支持程度。
- 不支持 DRM 加密电子书。

## 致谢
- 内置 [JSZip](https://stuk.github.io/jszip/) v3.10.1，用于 ZIP 解压，依据 MIT 协议使用。

## License
[

![License](https://img.shields.io/badge/License-MIT-%23829a91)

](https://opensource.org/licenses/MIT)

本项目源码使用 MIT 协议开源，详见 [LICENSE](LICENSE)。

## 反馈
Bug 反馈与功能建议，请提交 [GitHub Issues](https://github.com/LC-0001/zhijian-reader/issues)。