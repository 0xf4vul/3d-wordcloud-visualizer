# CHANGELOG - 3D Word Cloud Visualizer

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.2.0] - 2026-03-25

### Security

- 🔒 使用专业 Skill（skills-security-check）进行完整安全审计
- 🔒 修复3个P1风险（文档与实现不一致、CDN依赖描述错误、XSS防护说明）
- ✅ 安全评分：95/100（A级，低风险）
- ✅ 无P0阻断级风险
- ✅ 文档与代码实现完全同步

### Documentation

- 📝 更新SKILL.md依赖库描述（Three.js r128，来源cdnjs.cloudflare.com）
- 📝 移除segmentit分词库描述（代码中使用自定义正则分词）
- 📝 明确说明OrbitControls已内联到HTML中（无需外部加载）
- 📝 新增安全特性章节（SRI校验、XSS防护、文件大小限制、超时保护、原型链保护）
- 📝 修正网络连接说明（首次打开需下载Three.js CDN资源）

### Bug Fixes

- 🐛 修复文档与实际代码实现不一致的问题
- 🐛 修复依赖库版本号和来源URL描述错误

### Testing

- ✅ 通过专业安全审计（skills-security-check Skill）
- ✅ 验证文档与代码实现的一致性

## [1.1.0] - 2026-03-25

### Security

- 🔒 降低文件上传大小限制（10MB → 5MB）
- 🔒 添加文件类型验证（仅允许文本文件：JSON/MD/TXT）
- 🔒 为CDN资源添加SRI完整性校验（integrity属性）
- 🔒 使用crossorigin="anonymous"确保跨域资源请求安全性
- ✅ 通过完整安全审计，安全评级提升至A级（低风险）
- ✅ 安全评分从85分提升至95分（+10分）
- ✅ 所有P1风险已修复

### Bug Fixes

- 🐛 修复文件上传无大小限制的安全漏洞
- 🐛 修复CDN资源缺少完整性校验的潜在供应链攻击风险

### Documentation

- 📋 新增安全审计报告（Skills_安全审计报告_2026-03-25.md）
- 📋 新增漏洞修复报告（Skills_漏洞修复报告_2026-03-25.md）
- 📋 新增README更新指南（README更新指南_2026-03-25.md）
- 📝 更新README.md添加安全等级说明
- 📝 更新README.md版本信息至v1.1.0

### Performance

- ⚡ 优化文件上传检查逻辑，提前终止超大文件上传
- ⚡ 添加文件MIME类型预检测，减少无效上传操作

### Testing

- ✅ 通过完整的安全审计流程
- ✅ 验证SRI完整性校验机制
- ✅ 测试文件大小限制功能

## [1.0.0] - 2026-03-25

### Added

- 🌍 3D词云可视化核心功能
- 📤 文件上传功能（支持JSON/MD/TXT格式）
- 🔤 自动分词和词频统计
- 🎨 彩色词云映射到3D地球（15种颜色循环分配）
- ⭐ 动态星空背景（5000颗星星）
- 🕐 时间页眉（实时时钟显示）
- 📊 统计面板（显示TOP30高频词）
- 🧲 磁吸功能（面板拖动到边框自动吸附）
- 🖱️ 交互控制（旋转、缩放、平移）
- 💬 友好的提示系统（加载、成功、错误弹窗）
- 📱 响应式设计

### Features

- 真实3D地球词云（Three.js渲染）
- 面板拖拽功能
- 四边磁吸逻辑
- 磁吸图标交互（默认opacity 0.3，悬停显示文字，双击恢复面板）
- 右键重置功能
- 进度条动画（0% → 100%）
- 自定义滚动条样式

---

## 更新日志说明

### 版本号格式

遵循 Semantic Versioning：MAJOR.MINOR.PATCH

- **MAJOR**：不兼容的API更改
- **MINOR**：向后兼容的功能新增
- **PATCH**：向后兼容的问题修复

### 更新类型

- **Added**：新功能
- **Changed**：现有功能的更改
- **Deprecated**：即将移除的功能
- **Removed**：已移除的功能
- **Fixed**：错误修复
- **Security**：安全修复

---

**完整的安全审计报告（专业审查）**: [Skills_安全审计报告_2026-03-25_专业审查.md](./Skills_安全审计报告_2026-03-25_专业审查.md)
**详细的安全审计报告**: [Skills_安全审计报告_2026-03-25.md](./Skills_安全审计报告_2026-03-25.md)  
**详细的漏洞修复指南**: [Skills_漏洞修复报告_2026-03-25.md](./Skills_漏洞修复报告_2026-03-25.md)
