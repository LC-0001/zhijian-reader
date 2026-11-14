# Zhijian Reader

Zhijian Reader，纸间阅读器，本地优先的离线电子书 Web 应用。

所有书籍、阅读进度、书签与配置仅保存在浏览器本地，不会上传至外部服务器。
无需后端服务，仅单个静态 HTML 文件。

> 在线体验：[https://LC-0001.github.io/zhijian-reader/](https://LC-0001.github.io/zhijian-reader/)

## 功能
- 书架管理，支持 TXT、EPUB、PDF 导入，支持 ZIP 批量导入
- 阅读进度记录、目录跳转、书签、书摘卡片
- 阅读样式自定义：字号、行间距、纸张配色、自定义字体导入
- 主题控制，支持手动切换深浅色，或跟随系统主题自动变化
- 阅读数据备份与恢复
- 移动端与桌面端自适应布局

## 使用
1. 下载 `index.html`
2. 浏览器打开即可使用。
> 提示：部分浏览器直接双击打开文件会存在部分功能限制，建议优先使用静态网页服务访问。

## 部署
本项目仅依赖静态资源，支持 GitHub Pages、Vercel、Netlify 等任意静态托管平台。

### GitHub Pages 部署步骤
1. Fork 本仓库到自己账号
2. 进入仓库 Settings → Pages
3. Source 选择 `Deploy from a branch`，分支选择 `main`，目录选择 `/ (root)`，保存
4. 等待1‑2分钟，访问 `https://LC-0001.github.io/zhijian-reader/`

## 本地开发
本项目为单文件静态页面，无依赖，无需安装包。

```bash
git clone https://github.com/LC-0001/zhijian-reader.git
cd zhijian-reader
python3 -m http.server 8000
```
访问 `http://localhost:8000`

## 限制
- 数据存储依赖浏览器 IndexedDB，清除浏览器网站数据会丢失本地书籍，请定期导出备份。
- 大体积书籍导入时，性能取决于当前浏览器环境。
- 不支持 DRM 加密电子书。

## License
[![License](https://img.shields.io/badge/License-MIT-%23829a91)](https://opensource.org/licenses/MIT)

本项目源码使用 MIT 协议开源。

## 反馈
Bug反馈与功能建议，请提交 [GitHub Issues](https://github.com/LC-0001/zhijian-reader/issues)。
