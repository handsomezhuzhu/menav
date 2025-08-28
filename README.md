# Menav - 个人导航页面

这是一个基于 [rbetree/menav](https://github.com/rbetree/menav) 的个人导航页面项目。

## 🎯 简化策略

- **只维护 main 分支**：所有更改都在 main 分支上进行
- **自动部署**：推送到 main 分支时自动构建和部署到 GitHub Pages
- **简单同步**：需要时手动从原仓库拉取更新

## 🚀 快速开始

1. 克隆仓库：
```bash
git clone https://github.com/handsomezhuzhu/menav.git
cd menav
```

2. 安装依赖：
```bash
npm install
```

3. 本地开发：
```bash
npm run dev
```

4. 构建网站：
```bash
npm run generate
```

## 📝 自定义配置

- 编辑 `config/user/site.yml` 修改网站基本信息
- 编辑 `config/user/navigation.yml` 修改导航菜单
- 编辑 `config/user/pages/` 下的文件添加或修改页面

## 🔄 获取原仓库更新

当需要获取原仓库的新功能或bug修复时：

```bash
# 添加原仓库作为上游
git remote add upstream https://github.com/rbetree/menav.git

# 获取更新
git fetch upstream

# 合并到main分支
git checkout main
git merge upstream/main

# 推送更新
git push origin main
```

## 📚 书签功能

如果需要使用书签功能：

1. 将书签HTML文件放入 `bookmarks/` 目录
2. 运行书签处理脚本：
```bash
node src/bookmark-processor.js
```
3. 提交生成的配置文件

## 🌐 部署

- 网站会自动部署到 GitHub Pages
- 访问地址：`https://handsomezhuzhu.github.io/menav/`

## 📄 许可证

本项目基于原仓库的许可证。