# GitHub Pages 部署指南

## 📁 需要上传的文件

### 核心文件
- `index.html` - 主页面文件
- `CNAME` - 自定义域名配置
- `robots.txt` - 搜索引擎爬虫配置
- `sitemap.xml` - 网站地图

### 配置文件
- `.github/workflows/deploy.yml` - GitHub Actions 部署配置
- `_headers` - 安全头和缓存配置
- `_redirects` - 重定向配置

## 🚀 部署步骤

### 1. 创建 GitHub 仓库
1. 在 GitHub 上创建新仓库，命名为 `photontail.online` 或任何你喜欢的名字
2. 将仓库设置为 Public（GitHub Pages 免费版需要）

### 2. 上传文件
将以下文件上传到仓库根目录：
```
├── index.html
├── CNAME
├── robots.txt
├── sitemap.xml
├── _headers
├── _redirects
└── .github/
    └── workflows/
        └── deploy.yml
```

### 3. 配置 GitHub Pages
1. 进入仓库的 Settings 页面
2. 找到 "Pages" 选项
3. 在 "Source" 中选择 "GitHub Actions"
4. 保存设置

### 4. 配置自定义域名
1. 在 DNS 提供商处添加 CNAME 记录：
   - 类型：CNAME
   - 名称：www
   - 值：your-username.github.io
2. 添加 A 记录（可选）：
   - 类型：A
   - 名称：@
   - 值：185.199.108.153, 185.199.109.153, 185.199.110.153, 185.199.111.153

### 5. 启用 HTTPS
1. 在 GitHub Pages 设置中勾选 "Enforce HTTPS"
2. 等待 SSL 证书自动配置

## 🔧 文件说明

### index.html
- 主页面文件，包含完整的游戏网站
- 已优化 SEO 和性能
- 响应式设计，支持 PC 和移动端

### CNAME
- 自定义域名配置文件
- 告诉 GitHub Pages 使用 photontail.online 域名

### robots.txt
- 搜索引擎爬虫配置文件
- 允许所有爬虫访问
- 包含网站地图链接

### sitemap.xml
- 网站地图文件
- 帮助搜索引擎索引网站内容

### _headers
- 安全头和缓存配置
- 提升网站安全性和性能

### _redirects
- 重定向配置
- 确保所有路由都指向 index.html

### .github/workflows/deploy.yml
- GitHub Actions 自动部署配置
- 每次推送代码时自动部署

## ✅ 部署后检查

1. 访问 https://photontail.online 确认网站正常
2. 检查游戏 iframe 是否正常加载
3. 测试移动端响应式设计
4. 验证 SEO 元标签是否正确显示
5. 检查网站速度和安全评分

## 🐛 常见问题

### 游戏无法加载
- 检查 iframe 源地址是否正确
- 确认网络连接正常
- 查看浏览器控制台错误信息

### 域名无法访问
- 确认 DNS 配置正确
- 等待 DNS 传播（最多 24 小时）
- 检查 CNAME 文件是否正确

### HTTPS 证书问题
- 在 GitHub Pages 设置中启用 HTTPS
- 等待证书自动配置完成

## 📞 技术支持

如果遇到问题，请检查：
1. GitHub Actions 日志
2. 浏览器开发者工具
3. DNS 配置状态
4. GitHub Pages 设置

部署完成后，您的网站将在 https://photontail.online 上运行！
