# 范家荣 - 交互式AI人才简历网站

专为AI领域求职设计的交互式简历网站，每个经历都可关联作品集PDF。

## 核心特性
- ✅ **经历-作品集联动**：点击任意实习/项目经历，直接查看相关PDF作品
- ✅ **响应式设计**：完美适配手机和电脑端
- ✅ **极简更新**：通过编辑YAML文件即可添加新经历和作品集
- ✅ **免费部署**：基于GitHub Pages，零成本永久托管

## 网站结构
```
interactive_resume/
├── _config.yml              # 网站配置
├── _data/
│   └── experiences.yml      # 所有经历和作品集映射
├── assets/
│   ├── css/main.scss        # 自定义样式
│   └── pdfs/                # 作品集PDF存放目录
├── index.html               # 主页面（动态生成）
└── README.md                # 部署指南
```

## 部署步骤

### 1. 创建GitHub仓库
- 访问 https://github.com/new
- 仓库名：`你的用户名.github.io`（例如：`fanjiarong.github.io`）
- 选择Public（公开）

### 2. 上传文件
- 下载本项目所有文件
- 上传到新建的GitHub仓库

### 3. 启用GitHub Pages
- Settings → Pages → Source: "Deploy from branch" → Branch: main → Save

### 4. 访问网站
- 几分钟后访问 `https://你的用户名.github.io`

## 添加作品集

### 步骤1：上传PDF
将PDF文件放入 `assets/pdfs/` 目录，例如：
- `assets/pdfs/qingshiquan_research.pdf`
- `assets/pdfs/andjun_consulting.pdf`

### 步骤2：编辑经历配置
修改 `_data/experiences.yml`，在对应经历下添加 `portfolio` 字段：

```yaml
- title: "投研实习生"
  company: "清泉石资本"
  period: "2025.09 - 2026.03"
  portfolio:
    - file: "qingshiquan_research.pdf"
      title: "煤炭行业深度研报"
    - file: "ota_analysis.pdf"
      title: "OTA行业调研报告"
```

网站会自动在该经历下方显示"查看作品"按钮。