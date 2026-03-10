# 🚀 网站部署指南

## 方案选择

### 推荐：Vercel（最简单）

**优点：**
- 完全免费（个人版够用）
- 自动部署（连接 GitHub 后每次推送自动更新）
- 支持自定义域名（免费 SSL）
- 全球 CDN 加速

**部署步骤：**

1. **注册 Vercel**
   - 访问 https://vercel.com
   - 用 GitHub 账号登录（没有就先注册 GitHub）

2. **上传代码到 GitHub**
   ```bash
   # 在 website 文件夹内执行
   git init
   git add .
   git commit -m "Initial commit - AK 工具箱"
   
   # 在 GitHub 创建新仓库，然后
   git remote add origin https://github.com/YOUR_USERNAME/ak-toolbox.git
   git push -u origin main
   ```

3. **连接 Vercel**
   - 在 Vercel 点击 "Add New Project"
   - 选择刚才的 GitHub 仓库
   - 点击 "Deploy"
   - 完成！你会得到一个 `https://ak-toolbox.vercel.app` 的域名

4. **绑定自定义域名（可选）**
   - 在 Vercel 项目设置 → Domains
   - 添加你的域名（如 `tools.ak.com`）
   - 按提示配置 DNS

---

### 备选：GitHub Pages（完全免费）

**部署步骤：**

1. **创建 GitHub 仓库**
   - 仓库名：`你的用户名.github.io`
   - 设为公开仓库

2. **推送代码**
   ```bash
   cd website
   git init
   git add .
   git commit -m "Initial commit"
   git branch -M main
   git remote add origin https://github.com/YOUR_USERNAME/YOUR_USERNAME.github.io.git
   git push -u origin main
   ```

3. **访问网站**
   - `https://你的用户名.github.io`

---

### 备选：Cloudflare Pages

**部署步骤：**

1. 注册 https://cloudflare.com
2. 进入 Pages → Create a project
3. 连接 GitHub 仓库
4. 点击 Deploy

---

## 文件结构

```
website/
├── index.html          # 首页
├── calculator.html     # 充电桩计算器
├── DEPLOY.md          # 本文件
└── (后续添加的其他工具)
```

---

## 后续添加新工具

1. 在 `website/` 文件夹内创建新的 HTML 文件
2. 在 `index.html` 的工具网格中添加新卡片
3. 提交到 GitHub（Vercel 会自动部署）

```bash
git add .
git commit -m "Add new tool: XXX 计算器"
git push
```

---

## 自定义域名建议

- `ak.tools` - 简洁专业
- `tools.akai.xyz` - 用免费子域名
- `calculator.akai.xyz` - 如果只做计算器

---

## 成本

| 项目 | 费用 |
|-----|------|
| Vercel 托管 | 免费 |
| GitHub | 免费 |
| 自定义域名 | 约 60-100 元/年（可选） |
| SSL 证书 | 免费（Vercel 自动提供） |

**总计：0 元/年（不用自定义域名）**

---

## 需要帮忙？

遇到问题可以：
1. 检查 Vercel 部署日志
2. 确保 HTML 文件没有语法错误
3. 在 GitHub Issues 提问

🧅 Good luck!
