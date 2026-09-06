# soulforge-pathfinder-web

《铸魂领路者》(Soulforge Pathfinder) 官方落地页 —— 《铸魂迷途》(Soulforge Lost Path) 的 BepInEx 体验增强模组。

**线上地址**: https://abevol.github.io/soulforge-pathfinder-web/

## 站点结构

纯静态单页，无构建步骤、无外部依赖，推送 `main` 分支后 GitHub Pages 自动部署。

```
index.html    # 落地页（结构 + 样式 + 脚本 + 中英文案字典全部内联）
favicon.svg   # 站点图标
```

## 常见修改

### 1. 替换下载链接（当前为 `#` 占位）

在 `index.html` 中搜索 `TODO`，共两处（Hero 与"快速开始"区的下载按钮），将 `href="#"` 替换为真实安装器下载链接。

### 2. 修改文案

页面文案集中在 `index.html` 底部 `<script>` 内的 `DICT` 对象中，`zh` / `en` 两个键分别对应中文与英文。修改后两份文案需同步更新。

### 3. 中英文切换机制

- 首次访问按浏览器语言自动选择（`zh*` → 中文，其余 → 英文）
- 用户手动切换后通过 `localStorage`（键 `sfp-lang`）记忆，优先于自动检测

## 相关链接

- Discord 社区: https://discord.gg/SPQCAVA9R
- 模组发布页 (Gitee): https://gitee.com/floss/SoulforgePathfinder/releases/latest
- Steam:《铸魂迷途》 https://store.steampowered.com/app/3839250
