# GitHub 上传和发布指南

## 步骤 1：在 GitHub 上创建新仓库

1. 登录 GitHub (https://github.com)
2. 点击右上角的 "+" 号，选择 "New repository"
3. 填写仓库信息：
   - **Repository name**: 输入仓库名称（例如：merry-christmas 或 christmas-2024）
   - **Description**: 可选，填写项目描述
   - **Visibility**: 选择 Public（公开）或 Private（私有）
   - ⚠️ **不要**勾选 "Add a README file"、"Add .gitignore" 或 "Choose a license"（因为我们已经有了这些文件）
4. 点击 "Create repository" 创建仓库

## 步骤 2：将代码推送到 GitHub

在 PowerShell 或命令行中运行以下命令（将 `你的用户名` 和 `仓库名` 替换为实际值）：

```bash
# 添加远程仓库（替换下面的 URL 为你的实际仓库地址）
git remote add origin https://github.com/你的用户名/仓库名.git

# 推送代码到 GitHub
git branch -M main
git push -u origin main
```

如果提示输入用户名和密码，请使用：
- **用户名**: 你的 GitHub 用户名
- **密码**: 使用 Personal Access Token（不是 GitHub 密码）

### 如何创建 Personal Access Token：
1. GitHub → Settings → Developer settings → Personal access tokens → Tokens (classic)
2. 点击 "Generate new token (classic)"
3. 勾选 `repo` 权限
4. 生成后复制 token，在推送时作为密码使用

## 步骤 3：启用 GitHub Pages

1. 在 GitHub 仓库页面，点击 "Settings"（设置）标签
2. 在左侧菜单中找到 "Pages"（页面）
3. 在 "Source"（来源）部分：
   - 选择 "Deploy from a branch"
   - Branch（分支）选择 `main`
   - Folder（文件夹）选择 `/ (root)`
4. 点击 "Save"（保存）

## 步骤 4：访问你的网站

等待几分钟后，你的网站将在以下地址可用：

```
https://你的用户名.github.io/仓库名/
```

例如：如果用户名是 `john`，仓库名是 `merry-christmas`，则访问地址为：
```
https://john.github.io/merry-christmas/
```

## 注意事项

- GitHub Pages 可能需要几分钟时间来部署你的网站
- 如果看不到更改，尝试清除浏览器缓存或使用无痕模式
- 确保 `index.html` 文件在仓库的根目录
- 如果需要更新网站，只需再次运行 `git push` 即可

