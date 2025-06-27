# 🎯 Portfolio页面预览指南

## 方法1: GitHub Pages部署（推荐）

1. **推送代码到GitHub**：
   ```bash
   git add .
   git commit -m "feat: add portfolio page with cyberpunk design"
   git push origin master
   ```

2. **查看部署状态**：
   - 去GitHub仓库的 `Actions` 页面
   - 等待构建完成（大约2-3分钟）
   - 访问：https://kevin7lou.github.io

## 方法2: 本地预览

1. **克隆到本地**：
   ```bash
   git clone https://github.com/kevin7lou/kevin7lou.github.io.git
   cd kevin7lou.github.io
   ```

2. **安装依赖**：
   ```bash
   npm install
   ```

3. **启动开发服务器**：
   ```bash
   npm run dev
   ```

4. **访问预览**：
   - 打开浏览器访问：http://localhost:4321

## 方法3: 在线代码预览

如果你在Cursor/VSCode中使用GitHub Codespaces：

1. 在终端运行：
   ```bash
   npm install && npm run dev
   ```

2. 等待端口转发提示，点击"Open in Browser"

## 🎨 页面效果预览

你将看到：
- 🌌 深色背景和赛博朋克网格动画
- ✨ 霓虹色彩渐变（蓝、紫、粉、绿）
- 🎭 浮动粒子效果
- 💫 几何图形动画（旋转圆圈、六边形、轨道粒子）
- 🔥 发光按钮（"技术博客"和"知识库"）
- 📱 响应式设计，适配手机和桌面

## 🛠️ 自定义调整

编辑以下文件来调整效果：
- `src/pages/index.astro` - 主页内容
- `tailwind.config.mjs` - 颜色和动画
- `src/components/` - 各种视觉组件 