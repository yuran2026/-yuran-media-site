# 余然科技·门窗定制 H5 营销小程序

> 专业门窗定制营销工具 | 断桥铝 · 系统窗 · 阳光房 · 推拉门  
> **零服务器、零后端、一键部署、微信可直接打开**

---

## 🚀 一键部署教程

### 方式一：Netlify（推荐，最快）

1. 打开 [app.netlify.com](https://app.netlify.com)，注册/登录（免费）
2. 点击 **"Add new site" → "Deploy manually"**
3. 将整个 `yuren-windows-app` 文件夹**拖拽**到部署区域
4. 等待 10-30 秒，自动生成外网链接，如：  
   `https://amazing-einstein-123456.netlify.app`
5. 可在 **Site settings → Domain management** 自定义域名

> ✅ 生成的 `https://` 链接可直接在**微信内打开**，无需任何公众号认证。

---

### 方式二：Vercel（速度快）

1. 打开 [vercel.com](https://vercel.com)，注册/登录（免费）
2. 点击 **"Add New → Project"**
3. 选择 **"Browse"** 上传整个文件夹，或拖拽 zip 包
4. Framework 选 **"Other"**，Root Directory 保持默认
5. 点击 **"Deploy"**，30 秒内生成链接：  
   `https://yuren-windows.vercel.app`

---

### 方式三：GitHub Pages（适合长期维护）

```bash
# 1. 创建仓库后推送代码
git init
git add .
git commit -m "init: 余然科技门窗H5"
git remote add origin https://github.com/你的用户名/yuren-windows.git
git push -u origin main

# 2. 仓库 Settings → Pages → Source → main 分支 → Save
# 3. 访问：https://你的用户名.github.io/yuren-windows/
```

---

## 📁 文件结构

```
yuren-windows-app/
├── index.html          ← 核心应用（全部功能在此，单文件）
├── manifest.json       ← PWA 配置（支持"添加到主屏幕"）
├── favicon.ico         ← 网站图标（多尺寸）
├── favicon.svg         ← 矢量图标
├── netlify.toml        ← Netlify 部署配置（已配置好）
├── vercel.json         ← Vercel 部署配置（已配置好）
├── _redirects          ← Netlify 路由重定向规则
├── icons/
│   ├── icon-192.png    ← PWA 图标（Android）
│   └── icon-512.png    ← PWA 图标（启动屏）
└── README.md           ← 本说明文件
```

---

## 📱 功能模块

| 模块 | 功能 |
|------|------|
| **首页** | Hero、统计数字、产品分类、快捷入口、服务承诺、热销产品、精选案例 |
| **产品展示** | 5分类8款产品，Tab筛选，点击查看规格详情 |
| **报价计算器** ⭐ | 型材系列×玻璃配置×尺寸×数量×安装选配，**实时算价** |
| **预约量尺** | 姓名/电话/地址/需求/时间选择，表单验证，数据本地存储 |
| **案例展示** | 6个案例，底部弹层详情，一键跳预约 |
| **留资表单** | 浮层填写，数据存入 localStorage |
| **我的** | 门店联系、服务承诺、关于我们 |

---

## ✏️ 自定义修改指南

打开 `index.html`，搜索以下关键词快速定位并修改：

| 修改内容 | 搜索关键词 |
|----------|------------|
| 门店电话 | `400-888-9999` |
| 品牌名称 | `余然科技·门窗定制` |
| 产品数据 | `const products = [` |
| 案例数据 | `const cases = [` |
| 报价基准价格 | `const priceTable = {` |
| 主题颜色 | `--primary: #1a4d8c` |

---

## 📊 技术规格

- **体积**：单文件 ~80KB（含全部样式+逻辑）
- **依赖**：零外部依赖，纯原生 HTML/CSS/JS
- **兼容**：iOS Safari、Android Chrome、微信内置浏览器
- **数据存储**：localStorage（预约记录、留资数据）
- **PWA**：支持"添加到主屏幕"，离线可用

---

## 💡 微信分享设置

部署后，在微信内访问链接时：

1. 点击右上角 **"..."** → **"发送给朋友"** 或 **"分享到朋友圈"**
2. 分享标题/描述来自 `index.html` 中的 `og:title` / `og:description`
3. 如需自定义微信分享卡片，需接入**微信公众号 JSSDK**（可选升级）

---

## 🔮 后续升级建议

| 阶段 | 升级内容 |
|------|----------|
| Phase 2 | 接入云数据库（如 Supabase），真正存储预约/留资数据，管理员后台查看 |
| Phase 3 | 转为微信小程序（代码结构已适配，迁移成本低） |
| Phase 4 | 接入微信支付，支持定金预约 |
| Phase 5 | 对接 CRM 系统，自动推送线索给销售 |

---

*由余然科技出品 · WorkBuddy AI 生成 · 2026年6月*
