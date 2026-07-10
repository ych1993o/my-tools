# 在线工具箱 - 部署指南

## 项目说明

这是一个免费的在线工具箱网站，包含以下工具：
- JSON 格式化/压缩
- Base64 编解码
- 二维码生成器

所有工具均为纯前端实现，无需后端服务器，数据在浏览器本地处理，保护隐私。

---

## 部署步骤（小白跟着做就行）

### 第一步：把代码上传到 GitHub

1. 打开 GitHub 网站，登录你的账号
2. 点击右上角 `+` 号，选择 **New repository**
3. 仓库名称填 `my-tools`（或其他你喜欢的名字）
4. 选择 **Public**（公开）
5. 点击 **Create repository**
6. 在创建好的仓库页面，点击 **uploading an existing file**
7. 把本文件夹里的所有文件拖进去上传：
   - index.html
   - json-formatter.html
   - base64-tool.html
   - qr-generator.html
   - about.html
   - privacy.html
   - css/style.css
8. 点击 **Commit changes**

> 如果你会用 Git，也可以 `git push` 上传。

---

### 第二步：部署到 Vercel

1. 打开 [vercel.com](https://vercel.com)
2. 点击 **Sign Up**，选择 **Continue with GitHub** 用 GitHub 账号登录
3. 登录后点击 **Add New...** → **Project**
4. 找到你刚才创建的 `my-tools` 仓库，点击 **Import**
5. 不需要改任何设置，直接点击 **Deploy**
6. 等待 1-2 分钟，Vercel 会自动帮你部署好
7. 部署完成后，Vercel 会给你一个网址，例如 `https://my-tools.vercel.app`

---

### 第三步：绑定你的阿里云域名

1. 在 Vercel 项目页面，点击顶部 **Settings** 标签
2. 左侧选择 **Domains**
3. 输入你的阿里云域名（例如 `yourdomain.com`），点击 **Add**
4. Vercel 会提示你需要添加的 DNS 记录（通常是两个 A 记录或 CNAME 记录）
5. 打开 [阿里云域名控制台](https://dc.console.aliyun.com)
6. 找到你的域名，点击 **解析**
7. 按照 Vercel 提示添加对应的解析记录
8. 等待几分钟（通常 5-30 分钟），域名解析生效
9. 回到 Vercel 点击 **Refresh**，显示 Valid 就成功了

---

### 第四步：申请 Google AdSense

1. 访问 [Google AdSense](https://www.google.com/adsense)
2. 注册账号，填写你的网站域名
3. Google 会给你一段验证代码，类似这样：
   ```html
   <script async src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js?client=ca-pub-XXXXXXXXXXXXXXXX"
        crossorigin="anonymous"></script>
   ```
4. 把这段代码粘贴到每个 HTML 文件的 `<head>` 标签内（放在其他 `<script>` 前面）
5. 提交审核，等待 1-14 天
6. 审核通过后：
   - 在 AdSense 后台创建广告单元
   - 把广告代码替换掉代码中所有 `广告位预留` 的区块
   - 把 `ads.txt` 文件放到网站根目录（AdSense 会提供内容）

---

### 第五步：持续添加新工具（长期运营）

等网站稳定后，可以继续添加更多工具页面：
- 单位换算器
- 密码生成器
- 颜色转换器
- 时间戳转换
- MD5/SHA 加密
- URL 编码解码

每个新工具都复制现有工具页面的结构，改一下标题和功能代码即可。

---

## 文件结构

```
my-tools/
├── index.html              # 首页
├── json-formatter.html     # JSON 格式化工具
├── base64-tool.html        # Base64 编解码工具
├── qr-generator.html       # 二维码生成器
├── about.html              # 关于我们（AdSense 必备）
├── privacy.html            # 隐私政策（AdSense 必备）
├── css/
│   └── style.css           # 共享样式文件
└── README.md               # 本文件
```

---

## 注意事项

1. **所有数据在本地处理**：工具不会上传用户数据到服务器，可以放心使用
2. **广告位已预留**：代码中已经预留了 AdSense 广告位，审核通过后直接替换即可
3. **SEO 已优化**：每个页面都有独立的 title 和 description，利于搜索引擎收录
4. **响应式设计**：网站在手机、平板、电脑上都能正常显示

---

## 需要帮助？

如果在部署过程中遇到问题，可以随时询问。
