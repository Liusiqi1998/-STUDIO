# 核樂不煩 · STUDIO

只做文玩核桃与菩提籽手串。手机打开就是全部内容，不用装 App。

## 三个文件的分工

| 文件 | 作用 | 上线 |
|---|---|---|
| `index.html` | 客户看到的页面 | 上线 |
| `cfg.js` | 页面里的文字、图片、价格、配色 | 上线 |
| `admin.html` | 你自己改内容的后台（在 prototype 目录里） | 不上线 |

页面内容全部由 `cfg.js` 决定。改 `index.html` 不会改内容，改 `cfg.js` 才会。

## 第一次上线

1. GitHub 新建仓库，设成 **Public**（免费版 Pages 需要公开仓库）
2. 把本目录所有文件传上去
3. **Settings → Pages** → Source 选 `Deploy from a branch` → 分支 `main`、目录 `/ (root)` → Save
4. 等一两分钟，访问 `https://你的用户名.github.io/仓库名/`

## 平时改内容

1. 本地用浏览器打开 `prototype/admin.html`，账号 `admin` / `123456`
2. 改完点右侧「**导出配置上线**」，下载一个 `cfg.js`
3. 用它覆盖本目录的 `cfg.js`
4. 提交推送，网站就更新了

会用命令行的：

```
git add cfg.js
git commit -m "更新内容"
git push
```

不想碰命令行：GitHub 网页里点开 `cfg.js` → 铅笔图标 → 全选删除 → 粘贴新内容 → Commit changes。

## 几条要注意的

- 推送后 GitHub 有 1–2 分钟缓存，看到的还是旧版就按 `Ctrl+F5` 强制刷新
- 后台密码写在前端代码里，所以 `admin.html` 不发布到网上，只在本地开
- 目前没有后端：下单、支付都是演示流程，真实成交还是「加企微 → 转账」
- 后台改的东西只存在你这台电脑的浏览器里；**不导出就等于没发布**

## 图片

`assets/` 下 14 张，900×900 JPEG，全站 1.6MB。
在后台「页面管理」里换图，导出时会把图片一起写进 `cfg.js`，不用单独传。
