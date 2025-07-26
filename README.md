# Tailwind CSS 响应式导航示例

这是一个使用 **Tailwind CSS v4** 构建的响应式导航栏示例项目，展示了现代前端开发的最佳实践。

参考入门教程：
[TailwindCSS 入门指南：从安装到实战的实用主义CSS方案](https://www.jeay.net/front/tailwind.html)

## ✨ 特性

- 🎨 **Tailwind CSS v4** - 最新的原子化CSS框架
- 📱 **完全响应式** - 移动端优先设计
- ♿ **无障碍友好** - 语义化HTML + ARIA属性
- 🎯 **零配置启动** - 无需复杂的构建配置
- 🚀 **快速开发** - 热重载 + 自动构建

## 🛠️ 技术栈

- **Tailwind CSS v4** - 样式框架
- **HTML5** - 语义化标记
- **现代浏览器原生JS** - 轻量级交互
- **pnpm** - 包管理器

## 📦 项目结构

```
mobile/
├── src/
│   └── common.css          # 主样式文件（Tailwind配置）
├── public/
│   ├── index.html          # 主页面
│   └── css/               # 构建后的CSS文件
├── package.json           # 项目配置
├── tailwind.md           # 详细文档
└── README.md             # 本文件
```

## 🚀 快速开始

### 1. 安装依赖

```bash
# 使用 pnpm（推荐）
pnpm install

# 或使用 npm
npm install

# 或使用 yarn
yarn install
```

### 2. 启动开发服务器

```bash
# 启动开发服务器（端口8080） 并监听文件变化
pnpm dev
```

### 3. 构建CSS

```bash
# 构建CSS（生产环境压缩）
pnpm build

# 开发模式监听文件变化
pnpm watch
```

## 📱 响应式特性

### 断点系统

- 📱 **Mobile**: < 768px
- 💻 **Desktop**: ≥ 768px

### 导航行为

| 设备类型 | 导航样式 | 交互方式 |
|---------|----------|----------|
| 移动端 | 垂直菜单 | 汉堡按钮 |
| 桌面端 | 水平导航 | 直接点击 |

## 🎨 自定义样式

项目使用了Tailwind CSS v4的现代化配置方式：

```css
/* src/common.css */
@import "tailwindcss";

@theme {
  --color-primary: #1E40AF;
  --color-secondary: #F59E0B;
}

/* 自定义组件 */
@layer components {
  .nav-item {
    @apply px-3 py-2 text-gray-700 hover:text-blue-600;
  }
}
```

## 📝 开发指南

### 添加新页面

1. 在 `public/` 目录创建新的HTML文件
2. 在 `src/common.css` 中添加自定义样式
3. 运行 `pnpm build` 重新构建CSS

### 修改导航

导航结构位于 `public/index.html` 中，支持完全响应式：

```html
<!-- 桌面端导航 -->
<div class="hidden md:flex items-center space-x-4">
  <a href="#" class="nav-item">首页</a>
  <!-- 更多导航项 -->
</div>

<!-- 移动端菜单 -->
<div class="md:hidden">
  <!-- 移动端导航内容 -->
</div>
```

## 🎯 最佳实践

### 性能优化

- ✅ 自动按需生成样式，只包含用到的CSS
- ✅ 自动移除未使用的CSS
- ✅ 生产环境CSS压缩

### 可访问性

- ✅ 语义化HTML标签
- ✅ 键盘导航支持
- ✅ 屏幕阅读器友好
- ✅ 焦点管理

## 📚 学习资源

- [Tailwind CSS 官方文档](https://tailwindcss.com/docs)
- [项目详细文档](./tailwind.md)
- [响应式设计指南](./tailwind.md#实战示例)

## 🤝 贡献指南

1. Fork 项目
2. 创建功能分支
3. 提交更改
4. 发起Pull Request

## 📄 许可证

MIT License - 详见 [LICENSE](LICENSE) 文件

## 🆘 支持

遇到问题？请查看：

- [项目文档](./tailwind.md)
- [Tailwind CSS 中文文档](https://www.tailwindcss.cn)
- 提交 [Issue](../../issues)