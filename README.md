# fireworks-tech-graph — 技术图表生成
> Jarvis 外部插件：生成高质量 SVG 技术图表（架构图 / 流程图 / 序列图等），
> 支持七种视觉样式，辅助脚本验证并导出 PNG。

## 功能特性

| 功能 | 说明 |
| --- | --- |
| 🎨 七种视觉样式 | flat-icon / dark-terminal / blueprint / notion-clean / glassmorphism / claude-official / openai |
| 📐 图表类型 | 架构图、流程图、序列图、部署图等 |
| 🛠️ 辅助脚本 | `scripts/` 提供 generate-diagram.sh、generate-from-template.py、validate-svg.sh（SVG 验证） |
| 📚 参考规范 | `rules/fireworks-tech-graph/references/` 提供样式参考与 SVG 布局最佳实践 |

## 安装

### 从插件市场安装（推荐）
在 Jarvis 插件管理面板的「市场」页签搜索 `fireworks-tech-graph`，一键安装。

### 命令行安装
```bash
# 从源码仓库安装
jarvis --install-plugin https://github.com/skyfireitdiy/jarvis-plugin-fireworks-tech-graph
# 或从本地目录安装
jarvis --install-plugin /path/to/fireworks-tech-graph
```

安装后重启 Jarvis 使插件注册生效：
```bash
jarvis --list-plugins   # 确认 fireworks-tech-graph 插件已注册
```

## 使用
安装并重启后，直接让 Agent 生成技术图表：
> 用技术图谱风格画一个微服务架构图（dark-terminal 风格）

插件通过 `rules_load_dirs` 加载 `rules/fireworks_tech_graph.md` 使用规则，Agent 会自动遵循。

## 插件结构
```
fireworks-tech-graph/
├── config.yaml          # 插件配置：logo、rules_load_dirs
├── README.md
├── assets/
│   └── fireworks-tech-graph-icon.svg   # 插件图标
└── rules/
    ├── fireworks_tech_graph.md
    └── fireworks-tech-graph/
        ├── references/   # 七种样式参考 + SVG 布局最佳实践
        └── scripts/      # 生成/验证辅助脚本
```

## 环境要求
- Jarvis（支持外部插件）

## 许可证
MIT
