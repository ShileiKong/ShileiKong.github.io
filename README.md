# OJO 连接器原型预览

这是 2026-11-23 当前完整交互原型的静态构建，供设计评审使用。

- [打开项目原型](https://shileikong.github.io/p/local-dev-canvas?mockLogin=1&connectorsPreview=1&connectorFusion=1)
- [打开首页与连接器](https://shileikong.github.io/dashboard?dashboardPreview=1&connectorFusion=1)
- [演示代码 ZIP 准备失败与重试](https://shileikong.github.io/p/local-dev-canvas?mockLogin=1&connectorsPreview=1&connectorFusion=1&downloadDemo=fail-once)

保留原生 OJO 页面和现有交互。账号授权、外部资源读取与平台导出均使用模拟逻辑；代码 ZIP 下载是可下载的样例文件。无需启动本地服务。

本仓库只包含构建产物，不包含项目源码、PRD、环境文件或本地凭据。源码继续保存在私有原型仓库。当前版本来自本地最终原型，包含最新下载 Toast 与失败重试更新。

## 发布说明

GitHub Pages 从 main 分支根目录发布。404.html 作为 SPA 深层路由回退，mockServiceWorker.js 提供模拟业务请求。刷新项目地址会由 GitHub 返回 404 状态但加载完整应用，这是静态 Pages 的路由限制。

重新发布前，应重新构建当前原型，检查账号管理、Agent 提示词/复制、GitHub/Figma 导出、链接识别、下载失败重试，并扫描环境凭据与 source map。
