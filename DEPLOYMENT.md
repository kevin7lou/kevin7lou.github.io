# 🚀 GitHub Pages 部署指南

## 第一步：启用GitHub Pages

1. **进入仓库设置**：
   - 访问你的GitHub仓库：https://github.com/kevin7lou/kevin7lou.github.io
   - 点击 `Settings` 标签页

2. **配置Pages设置**：
   - 在左侧菜单找到 `Pages`
   - 在 `Source` 部分选择 `GitHub Actions`
   - 保存设置

## 第二步：推送代码触发部署

```bash
# 添加所有文件
git add .

# 提交更改
git commit -m "feat: add cyberpunk portfolio with auto-deploy"

# 推送到GitHub
git push origin master
```

## 第三步：查看部署状态

1. **监控构建过程**：
   - 去仓库的 `Actions` 标签页
   - 查看 "Deploy Astro site to Pages" 工作流
   - 等待构建完成（通常2-3分钟）

2. **访问部署的网站**：
   - 构建成功后访问：https://kevin7lou.github.io
   - 首次部署可能需要额外几分钟生效

## 工作流特性

✅ **自动触发**：每次推送到 `master` 或 `main` 分支时自动部署  
✅ **智能包管理**：自动检测使用npm还是yarn  
✅ **优化构建**：包含缓存和优化配置  
✅ **手动触发**：可以在Actions页面手动运行  
✅ **安全部署**：使用GitHub官方Actions和适当权限

## 故障排除

### 如果部署失败：
1. 检查 `Actions` 页面的错误日志
2. 确保 `package.json` 中包含所有依赖
3. 确认分支名称是 `master` 或 `main`

### 常见问题修复：

**npm ci 依赖同步错误**：
- ✅ 已修复：workflow现在使用 `npm install` 而不是 `npm ci`
- ✅ 已修复：删除了 `package-lock.json` 文件让系统重新生成
- ✅ 已修复：添加了缓存清理步骤确保依赖正确安装

### 如果页面不显示：
1. 确保GitHub Pages设置为使用 `GitHub Actions`
2. 等待DNS传播（可能需要10-15分钟）
3. 检查浏览器缓存，尝试硬刷新

## 自定义域名（可选）

如果你有自定义域名：
1. 在仓库根目录创建 `public/CNAME` 文件
2. 文件内容写入你的域名（如：`portfolio.yourdomain.com`）
3. 在域名DNS设置中添加CNAME记录指向 `kevin7lou.github.io` 