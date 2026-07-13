# 📍 在哪儿 · 东西放哪了随手记

> 给妈妈做的「东西放哪儿了」记忆助手 —— 拍照、记录、一秒找回。
> 纯前端 PWA，打开即用，断网也能用。

[![PWA](https://img.shields.io/badge/PWA-Ready-9b59b6)](https://web.dev/learn/pwa)
[![PWA-Installable](https://img.shields.io/badge/PWA-Installable-9b59b6)](https://web.dev/learn/pwa)
[![Host](https://img.shields.io/badge/Host-GitHub%20Pages-1f6feb)](https://pages.github.com/)
[![UI](https://img.shields.io/badge/UI-中文-ff69b4)](.)
[![Stack](https://img.shields.io/badge/Stack-No%20Backend-2ecc71)](.)

🌐 **线上地址：https://yydshy.github.io/zaunar/**

---

## ✨ 功能特性

- 📷 **拍照记位置** —— 一张图胜过千言万语，东西放哪儿拍下来最直观
- 🗂 **分类整理** —— 厨房 / 卧室 / 客厅 / 证件 / 药品 … 想加就加，常用可置顶
- 🔍 **极速搜索** —— 输入「遥控器」立刻定位，跨分类还会智能提示
- 🎤 **语音录入** —— 动动嘴就能记（安卓 / Chrome 完美支持）
- 💾 **一键备份** —— 导出 / 导入 JSON，换手机、清缓存也不怕丢
- 🌗 **亮色优先** —— 默认暖色亮色主题，护眼不刺眼
- 📱 **像 App 一样** —— 添加到主屏幕，全屏无地址栏、离线可用

---

## 🛠 技术栈

| 能力 | 实现 |
| --- | --- |
| 前端 | 原生 HTML / CSS / JS（单文件，零构建） |
| 数据存储 | `localStorage`（文字） + `IndexedDB`（照片，大容量） |
| 离线能力 | Service Worker 缓存策略 |
| 可安装性 | Web App Manifest + iOS / Android 安装元数据 |
| 部署 | GitHub Pages 静态托管 |

---

## 🚀 本地运行

```bash
# 任选其一启动静态服务器
python -m http.server 8080
# 或
npx serve .
```

浏览器打开 `http://localhost:8080` 即可。

> ⚠️ Service Worker 仅在 `https` 或 `localhost` 下生效；直接双击 `file://` 打开功能正常，但不会注册离线缓存。

---

## 📱 添加到主屏幕（让妈妈像用 App 一样）

| 平台 | 操作 |
| --- | --- |
| Android · Chrome | 打开网页 → 点顶部「添加到主屏幕」引导条 → 添加 |
| iPhone · Safari | 打开网页 → 底部「分享」→「添加到主屏幕」 |

---

## 🔒 隐私说明

默认情况下，所有数据**只存在你自己的手机浏览器里**——不联网、不上传、不经过任何服务器。换设备前，记得用右上角「导出备份」存一份 JSON 文件。

如需在家人之间共享（例如你录、妈妈看），可开启 **☁️ 云同步**：用同一个 GitHub Token + 同一个 Gist 编号，文字数据（物品名/位置/分类/备注）实时互相同步；**照片不进云端**，只留各自手机。同步采用「按 ID 合并、同条目取最新」，两边同时离线新增也不会互相覆盖丢失。Token 仅需 `gist` 权限，可随时在设置里断开。

---

## 📂 项目结构

```
.
├── index.html            # 主程序（单文件，含全部逻辑与样式）
├── manifest.webmanifest  # PWA 安装清单
├── sw.js                 # Service Worker（离线缓存）
└── icons/                # 192 / 512 / Apple Touch 图标
    ├── icon-192.png
    ├── icon-512.png
    └── apple-touch-icon.png
```

---

## ☁️ 部署（GitHub Pages）

仓库已开启 Pages，源码推送到 `main` 分支即自动更新：

```bash
git add -A
git commit -m "update"
git push origin main
```

🌐 线上地址：**https://yydshy.github.io/zaunar/**

---

> © 家庭自用 · 为爱发电 ❤️
