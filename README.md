# mmwx-css

MiaoMiaoWuX（MMWX）主控自定义 CSS，保留 Wyatt 当前使用的奶油底、浅蓝按钮、薄荷绿强调色、圆角描边和偏移硬阴影风格。

本仓库发布的是当前自定义样式，不是 MMWX 程序，也不包含节点、服务器、账号或许可证配置。

## 主题

| 主题 | 主控 CSS | 说明 |
| --- | --- | --- |
| Wyatt | [controller.css](themes/wyatt/controller.css) | [安装与使用](themes/wyatt/README.md) |

当前样式版本：`v2026.10.18-01`。更新记录见 [CHANGELOG.md](CHANGELOG.md)。目前仅提供主控 CSS，不提供 TG Bot Mini App CSS。

## 安装

1. 先完整备份「系统设置 → 外观 → 自定义 CSS」中的旧代码。
2. 打开 [controller.css](themes/wyatt/controller.css)，点击 GitHub 的 **Raw**，复制完整内容。
3. 粘贴到 MMWX 的自定义 CSS 编辑框，保存并刷新页面。

也可以把该文件的 Raw 链接填入自定义 CSS 的「来源链接」，点击「从链接更新」，确认内容后再保存。不要把本 README 或 GitHub 文件页面的 HTML 当作 CSS 粘贴。

CSS 直链：[controller.css（Raw）](https://raw.githubusercontent.com/Wyatt323/mmwx-css/main/themes/wyatt/controller.css)

每个配置只使用一套完整主题，不要和其他主题叠加，以免出现选择器冲突。此 CSS 不会升级 MMWX，也不会修改节点顺序或其他业务数据。

## 外观与适配

- 奶油色背景、浅蓝辅助按钮、薄荷绿强调色及深色描边。
- 包含浅色、深色配色变量和桌面、窄屏布局规则。
- 包含节点选中背景、菜单间距、服务器地址列、弹窗和节点搭建表单等适配。
- 排序模式显示节点左侧的拖动手柄；普通模式继续隐藏空白手柄列。窄屏下的入口位于「菜单 → 排序模式」。

2026-10-18 已在当前 MMWX 页面验证排序手柄恢复、普通模式列宽不变以及刷新后样式持久化；这不代表所有版本和所有功能都已完整回归测试。MMWX 升级后如果组件结构或 `data-slot` 属性变化，可能需要同步适配。

## 使用限制

- 需要 MMWX 自定义 CSS 功能可用，并使用支持 CSS 嵌套、`:has()` 和 `color-mix()` 的现代浏览器。
- 主控自定义 CSS 上限为 **65,536 个 UTF-8 字节**，不是字符数。当前 `controller.css` 文件为 **65,498 字节**，非常接近上限；保存前请查看编辑框字节计数。
- 样式通过 Google Fonts 加载字体，加载失败时回退到系统字体。
- 仓库中的 CSS 与 2026-10-18 网站生效版本一致，仅保留文件末尾换行。为了不超过容量限制，版本信息放在说明与更新记录中，不额外加入 CSS 文件头。
- 发布内容仅含样式和说明，不上传真实节点截图、后台数据或历史调试文件。

## 参考

目录和文档组织方式参考 [chnnic/Bettmmwx](https://github.com/chnnic/Bettmmwx)。本次整理未用参考仓库的主题替换现有样式，也未复制其图片或 TG Bot 样式。
