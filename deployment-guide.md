# GitHub Pages 部署指南

这是一份详细的部署指南，适合不熟悉技术的用户。按照以下步骤，您可以在 5-10 分钟内将网站部署到互联网上。

## 准备工作

您需要：
- 一个 GitHub 账号（免费）
- `index.html` 文件
- 10 分钟时间

## 第一步：创建 GitHub 账号

如果您还没有 GitHub 账号：

1. 访问 [github.com](https://github.com)
2. 点击右上角的 "Sign up"（注册）
3. 填写邮箱、密码和用户名
4. 验证邮箱
5. 完成注册

## 第二步：创建新仓库

1. 登录 GitHub 后，点击右上角的 "+" 号
2. 选择 "New repository"（新建仓库）
3. 填写信息：
   - **Repository name**（仓库名称）：`book-of-answers`（或任何您喜欢的名字）
   - **Description**（描述）：可选，例如 "NFC Divination Website"
   - **Public**（公开）：选择这个选项（必须是公开的才能使用 GitHub Pages）
   - **Initialize this repository with**（初始化）：不要勾选任何选项
4. 点击 "Create repository"（创建仓库）

## 第三步：上传文件

创建仓库后，您会看到一个空白页面。

### 方法 A：通过网页上传（推荐，最简单）

1. 在仓库页面，点击 "uploading an existing file"（上传现有文件）链接
2. 将 `index.html` 文件拖拽到上传区域
3. 在页面底部，填写提交信息：
   - Commit message: "Add divination website"
4. 点击 "Commit changes"（提交更改）

### 方法 B：使用 Git 命令行（适合熟悉终端的用户）

```bash
# 克隆仓库
git clone https://github.com/YOUR_USERNAME/book-of-answers.git
cd book-of-answers

# 复制 index.html 到这个文件夹

# 提交并推送
git add index.html
git commit -m "Add divination website"
git push origin main
```

## 第四步：启用 GitHub Pages

1. 在您的仓库页面，点击顶部的 "Settings"（设置）
2. 在左侧菜单中，找到并点击 "Pages"
3. 在 "Source"（源）部分：
   - Branch（分支）：选择 "main"
   - Folder（文件夹）：选择 "/ (root)"
4. 点击 "Save"（保存）
5. 等待 30-60 秒

## 第五步：获取网站链接

1. 刷新页面
2. 在 Pages 设置页面顶部，您会看到一个绿色的提示框
3. 里面显示："Your site is live at `https://YOUR_USERNAME.github.io/book-of-answers/`"
4. 点击这个链接，您的网站就上线了！

## 第六步：自定义域名（可选）

如果您有自己的域名：

1. 在 Pages 设置中，找到 "Custom domain"（自定义域名）
2. 输入您的域名，例如 `answers.yourdomain.com`
3. 点击 "Save"
4. 在您的域名提供商处，添加 CNAME 记录：
   - Name: `answers`
   - Value: `YOUR_USERNAME.github.io`

## 更新网站内容

当您需要更新网站（例如更改答案内容）：

### 通过网页更新

1. 进入您的仓库
2. 点击 `index.html` 文件
3. 点击右上角的铅笔图标（Edit this file）
4. 修改内容
5. 滚动到页面底部，填写提交信息
6. 点击 "Commit changes"
7. 等待 1-2 分钟，网站自动更新

### 通过 Git 更新

```bash
# 进入仓库文件夹
cd book-of-answers

# 修改 index.html 文件

# 提交并推送
git add index.html
git commit -m "Update answers"
git push origin main
```

## 常见问题

### Q: 网站显示 404 错误？
**A:**
- 检查 Pages 是否已启用（Settings → Pages）
- 确保文件名是 `index.html`（小写）
- 等待几分钟，GitHub 需要时间部署

### Q: 修改后网站没有更新？
**A:**
- 清除浏览器缓存（Ctrl+Shift+R 或 Cmd+Shift+R）
- 等待 1-2 分钟让 GitHub Pages 重新部署
- 检查 Git 提交是否成功

### Q: 想要更好的网址？
**A:**
- 使用自定义域名（见第六步）
- 或者使用短链接服务（如 bit.ly）缩短 GitHub Pages 链接

### Q: 网站加载很慢？
**A:**
- GitHub Pages 通常很快
- 检查您的网络连接
- 清除浏览器缓存

### Q: 可以设置密码保护吗？
**A:**
- GitHub Pages 本身不支持密码保护
- 可以使用其他服务如 Netlify（提供密码保护功能）

## 替代部署方案

如果您不想使用 GitHub Pages，还有这些选择：

### Netlify（推荐）
1. 访问 [netlify.com](https://netlify.com)
2. 注册账号
3. 拖拽 `index.html` 到网页
4. 获得一个 `.netlify.app` 域名
5. 支持密码保护和自定义域名

### Vercel
1. 访问 [vercel.com](https://vercel.com)
2. 注册账号
3. 导入 GitHub 仓库或上传文件
4. 自动部署

### Cloudflare Pages
1. 访问 [pages.cloudflare.com](https://pages.cloudflare.com)
2. 连接 GitHub 账号
3. 选择仓库
4. 自动部署

## 部署检查清单

在告诉用户访问之前，请确认：

- [ ] 网站可以正常打开
- [ ] 点击按钮可以获取新答案
- [ ] 语言切换功能正常
- [ ] 手机访问显示正常
- [ ] 已替换为真实的占卜句子（不是示例内容）
- [ ] 链接已保存并分享给用户或写入 NFC 标签

## 获取帮助

- GitHub Pages 文档：https://docs.github.com/en/pages
- GitHub 社区：https://github.community
- 遇到问题？在仓库创建一个 Issue

---

**恭喜！您的占卜网站已经上线了！** 🎉

现在您可以将网址写入 NFC 标签，或直接分享给朋友。
