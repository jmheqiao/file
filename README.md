# D-File

基于 GitHub API 的文件管理系统前端页面。

> 本项目基于 [@dhjz/file](https://github.com/dhjz/file) 进行二次开发，主要对UI和配色方案进行了重新设计，保持原有功能逻辑不变。感谢原作者的开源贡献！

## 最新更新 (v20250101-1)

1. UI 和配色改造
   - 采用 Pornhub 风格配色:
     - 主背景: 黑色 (#000)
     - 主文字: 白色 (#fff)
     - 强调色: 橙色 (#ff9000)
     - 次要文字: 灰色 (#999)
     - 边框和分割线: 深灰色 (#333)
   - 按钮和交互优化:
     - 添加悬停效果
     - 圆角设计
     - 平滑过渡动画

2. CDN 加速源更新
   - 移除失效的加速源:
     - staticaly 加速
     - kgithub 加速
     - fastgit 加速
   - 保留可用加速源:
     - 本站直连
     - gitmirror 加速
     - jsdelivr 加速
     - jsdelivr1 加速

## 使用说明

- 可以直接访问本地址, 设置好仓库和token后, 进行文件的上传下载和地址查看
- 也可以把`index.html`复制到自己的仓库, 开启github pages后访问自己的页面即可
- 全部功能实现都在`index.html`里面
- github token新建地址: [https://github.com/settings/tokens?type=beta](https://github.com/settings/tokens?type=beta)
- 建议开启仓库的pages功能, 可以直接访问文件

### 快速开始

1. 配置 GitHub Token
   - 需要有 repo 权限的 Personal Access Token
   - 点击右上角"设置Token"进行配置

2. 配置目标仓库
   - 点击右上角"设置Repo"
   - 格式为 `owner/repo`，如 `dhjz/file`

3. 测试加速源
   - 在根目录上传 `init.jpg`(50kb以内)
   - 系统会自动测试各个加速源的延迟

## 功能特性

- 支持文件上传下载删除
- 支持目录新增
- 支持自定义仓库repo和token
- 支持常见的github镜像加速地址一键查看及延时查看(需要在仓库根目录上传init.jpg)
- 支持分列查看和文件名搜索过滤
- 支持常见文件类型的类型查看和高亮显示
- 支持文件类型识别和图标显示
- 响应式设计，支持移动端
- 支持文件预览和下载

## 技术实现

- 纯前端实现，无需后端服务器
- 使用 GitHub REST API 进行文件操作
- 使用 Base64 处理文件编码
- 使用 localStorage 存储配置信息

## 注意事项

- 主页文件(index.html)受保护，不可删除
- 需要确保有足够的仓库权限
- 大文件上传时请耐心等待
