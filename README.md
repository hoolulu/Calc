<p align="center">
  <a href="#zh"><b>[中文]</b></a> · <a href="#en"><b>[English]</b></a>
</p>

---

<a name="zh"></a>

# Hoolulu Calc v1.0

一个简洁、美观、全平台可用的计算器。单 HTML 文件，零依赖部署。

> 🖥️ 演示站点：[https://js.p55.top](https://js.p55.top)

## 功能

- 基础四则运算：`+` `−` `×` `÷`
- `%` 百分比、`±` 正负切换
- 退格 `←`、全部清除 `C`
- 键盘快捷键支持（数字、运算符、Enter、Backspace、Esc）
- 历史记录（自动保存至浏览器本地 `localStorage`）
  - 点击条目回填结果
  - ✏️ 编辑表达式并自动重算
  - 🗑 单条删除 / 清空全部
- 千分位逗号格式化（结果和记录）
- 超长数字自适应字号缩放（最大 40 位有效数字）
- 任意精度计算（基于 `decimal.js`）：
  - 精确处理 `0.1 + 0.2 = 0.3` 等浮点运算
  - 40 位以内整数运算无精度损失
- 响应式布局
  - 移动端：全屏计算器 + 侧滑历史面板
  - 桌面端：计算器与历史并排
- 深色主题

## 技术栈

|          |                                    |
| -------- | ---------------------------------- |
| 框架     | 无（纯静态 HTML）                  |
| 响应式   | [Alpine.js](https://alpinejs.dev/) |
| 样式     | [Tailwind CSS](https://tailwindcss.com/) (CDN) |
| 计算引擎 | [decimal.js](https://github.com/MikeMcl/decimal.js) |
| 持久化   | `localStorage`                     |

所有依赖均通过 CDN 加载，无需构建步骤。

## 使用

直接在浏览器中打开 `index.html`，或部署到任意静态托管服务。

### 键盘快捷键

| 按键       | 功能       |
| ---------- | ---------- |
| `0` – `9`  | 输入数字   |
| `.`        | 小数点     |
| `+` `-` `*` `/` | 运算符 |
| `Enter` / `=` | 计算结果 |
| `Backspace` | 退格       |
| `Escape` / `Delete` | 全部清除 |
| `%`        | 百分比     |

## 部署

### GitHub Pages

1. 在 GitHub 创建仓库
2. 将 `index.html` 和 `README.md` 推送到仓库
3. 进入 Settings → Pages → Source 选择 `main` 分支
4. （可选）绑定自定义域名

### Cloudflare Pages

1. 登录 Cloudflare Dashboard → Pages
2. 创建项目 → 连接到 Git 仓库
3. 构建设置：框架预设选 **None**，构建命令留空，输出目录填 `.`
4. （可选）绑定自定义域名

### 其他静态托管

任何支持静态文件的托管服务均可，直接将 `index.html` 上传即可。

> **关于多人使用的历史数据隔离**：`localStorage` 按域名隔离。你用自己的域名访问，别人用 fork 后的域名访问，数据完全独立，互不干扰。

## 隐私

- 所有计算均在浏览器本地执行
- 历史记录仅存储在浏览器 `localStorage` 中
- 不发送任何网络请求（除加载 CDN 脚本外）
- 无后端、无数据库、无追踪

---

<a name="en"></a>

<p align="center">
  <a href="#zh"><b>[中文]</b></a> · <a href="#en"><b>[English]</b></a>
</p>

# Hoolulu Calc v1.0

A clean, responsive calculator that works everywhere. Single HTML file, zero dependencies.

> 🖥️ Live demo: [https://js.p55.top](https://js.p55.top)

## Features

- Basic arithmetic: `+` `−` `×` `÷`
- `%` percent, `±` negate
- Backspace `←`, Clear `C`
- Keyboard shortcuts (digits, operators, Enter, Backspace, Escape)
- Calculation history (persisted in `localStorage`)
  - Click to reload result
  - ✏️ Edit expression & auto-recalculate
  - 🗑 Delete single / Clear all
- Thousands separator formatting
- Dynamic font scaling for long numbers (up to 40 significant digits)
- Arbitrary precision arithmetic (powered by `decimal.js`):
  - Accurate `0.1 + 0.2 = 0.3`
  - Exact integer operations up to 40 digits
- Responsive layout
  - Mobile: full-width calculator + slide-in history panel
  - Desktop: side-by-side calculator & history
- Dark theme

## Tech Stack

|              |                                                |
| ------------ | ---------------------------------------------- |
| Framework    | None (vanilla HTML)                            |
| Reactive UI  | [Alpine.js](https://alpinejs.dev/)             |
| Styling      | [Tailwind CSS](https://tailwindcss.com/) (CDN) |
| Math Engine  | [decimal.js](https://github.com/MikeMcl/decimal.js) |
| Persistence  | `localStorage`                                 |

All dependencies loaded via CDN — no build step required.

## Usage

Open `index.html` in a browser, or deploy to any static hosting service.

### Keyboard Shortcuts

| Key          | Function    |
| ------------ | ----------- |
| `0` – `9`    | Digit input |
| `.`          | Decimal point |
| `+` `-` `*` `/` | Operator |
| `Enter` / `=` | Calculate |
| `Backspace`  | Backspace   |
| `Escape` / `Delete` | Clear all |
| `%`          | Percent     |

## Deployment

### GitHub Pages

1. Create a repository on GitHub
2. Push `index.html` and `README.md`
3. Settings → Pages → Source → `main` branch
4. (Optional) Bind a custom domain

### Cloudflare Pages

1. Cloudflare Dashboard → Pages
2. Create project → Connect Git repo
3. Build settings: Framework **None**, build command empty, output directory `.`
4. (Optional) Bind a custom domain

### Other Static Hosting

Any service that serves static files works — just upload `index.html`.

> **History data isolation**: `localStorage` is scoped per domain. Your data stays on your domain; fork users' data stays on theirs.

## Privacy

- All computation happens locally in the browser
- History stored only in browser `localStorage`
- No network requests (except CDN scripts on first load)
- No backend, no database, no tracking
