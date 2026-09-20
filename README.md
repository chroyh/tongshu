# 顺天 TONGSHU · 静态演示版

> Gitee Pages 公网演示版本(自动降级 demo 模式)

## 🚀 5 分钟部署到 Gitee Pages

### 步骤 1:创建 Gitee 仓库
1. 登录 https://gitee.com(账号:18022078539)
2. 右上角 `+` → `新建仓库`
3. 仓库名:`tongshu-mvp`(会得到 `tongshu-mvp.gitee.io`)
4. **路径会自动**:`用户名仓库名.json`(这里就是 `gitee.io` 二级域)
5. 选**公开** + **使用 README** + **添加 .gitignore: None**
6. 创建

### 步骤 2:上传文件
**方式 A · 网页上传**(最简单)
1. 进入新仓库
2. 点 `上传文件` → 把 `index.html` 拖进去
3. 提交信息写:`init demo`
4. 点 `提交`

**方式 B · git push**(需要 token)
```bash
cd /home/o/projects/tongshu-gitee
git init
git remote add origin https://gitee.com/您的用户名/tongshu-mvp.git
git add .
git commit -m "init demo"
git push -u origin master
# 输入 Gitee 用户名 + 密码(或私人 token)
```

### 步骤 3:开启 Gitee Pages
1. 仓库页面 → **服务** → **Gitee Pages**
2. 部署分支:`master`(或 `main`)
3. 部署目录:`/(根目录)`
4. 点 `启动`
5. **等 1-2 分钟** → 得到 URL:**`https://您的用户名.gitee.io/tongshu-mvp/`**

### 步骤 4:验证
打开 URL → 应该看到 `顺天 · TONGSHU` 落地页 → 点 `开始` → 输入任意生日 → 显示示例八字(辛丑/丁酉/癸亥/丙辰)

---

## 📁 文件清单(本目录)
```
tongshu-gitee/
├── index.html        # 22.7KB · 完整前端 + demo 数据 fallback
├── public/
│   └── index.html    # 副本(子路径兼容)
└── README.md         # 本文件
```

---

## ⚙️ 当前功能(静态版)

| 功能 | 状态 |
|---|---|
| 落地页 / Hero / 关于 | ✅ 完整 |
| 八字表单 | ✅ 完整 |
| **真实八字计算** | ❌ 静态 demo(展示刘德华示例) |
| 五行图 | ✅ demo 数据 |
| 解读文案 | ✅ demo 文案 |
| CTA / 商业化 | ✅ 占位 |

## 🔄 升级到完整版
后端在 `192.168.2.12:8080`(Node.js + wisdom BaziEngine),可通过 Cloudflare Tunnel 拿到公网 URL 后,改前端 `API_BASE` 即可对接。

---

## 📊 部署情况
- 文件大小:22.7KB(单 HTML,含 Tailwind CDN + 全部样式)
- 访问速度:Gitee 国内 CDN,极快
- 维护成本:0(纯静态)