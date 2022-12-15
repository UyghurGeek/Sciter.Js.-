# HTML

Sciter 使用元素、功能和更简单的处理方式扩展常规 HTML.

该表显示了如何使用 Sciter 方式完成工作:

| Sciter | 常规 HTML |
| ------ | ------------ |
| `<input #id />`   | `<input id="id" />`
| `<input .class />` | `<input class="class" />`
| `<input \|text />` | `<input type="text" />`
| `<input (name) />` | `<input name="name" />`

_NOTE_ 在 Sciter 中，元素后面的空格是可选的。常规 html 和 Sciter html 可以混合在同一个文档中。

## 元素

这些是 Sciter 特定的元素，其中大多数都有自定义 [behavior](behaviors/README.md) 已分配.

| Element | Description |
| ------- | ----------- |
| `<popup>` | 弹出元素 (preferred to be placed in `<head>`)
| [`<menu .context>`](behaviors/behavior-menu.md)  | [context-menu styled](CSS/css-sciter.md) 元素
| [`<menu .popup>`](behaviors/behavior-menu.md)  | [context-menu styled](CSS/css-sciter.md) 元素
| [`<plaintext>`](behaviors/behavior-plaintext.md) | 多行文本编辑器
| [`<htmlarea>`](behaviors/behavior-richtext.md) | WYSIWYG/richtext/html 编辑
| [`<frameset>`](behaviors/behavior-frame-set.md) | 子元素是可调整大小的窗口块
| [`<select\|tree>`](behaviors/behavior-tree-view.md) | 树列表选择元素，其中之一 [行为选择](behaviors/README.md) 类型
| `<include src="some.html"/>` | 将 HTML 片段文件插入到位。


## 属性

| Attribute  | Description |
| ---------  | ----------- |
| `spellcheck` | true/false启用或禁用拼写检查
| `selectable` | allow内容选择（行为）
| `novalue`    | 同义词 `placeholder`
| `role="window-caption"` | 允许通过此元素拖动窗口
| `role="window-minimize"` | 指示元素表现为窗口最小化按钮
| `role="window-maximize"` | 指示元素表现为窗口最大化按钮
| `role="window-close"` | 指示元素作为窗口关闭按钮
| `role="window-icon"` | 指示元素作为窗口图标 -在 Windows 上，它在单击它时显示窗口菜单。


## 窗口属性

Window (`<html>`) 具体属性

| Attribute | Description |
| --------- | ----------- |
| `window-frame` | `default\|standard\|solid\|solid-with-shadow\|extended\|transparent` 定义窗口类型
| `window-icon`  | 窗口图标 URL
| `window-title` | 窗口标题
| `window-width` | 窗口的初始宽度，CSS 长度单位
| `window-height`| 窗口的初始高度，CSS 长度单位
| `window-min-width` | 窗口的最小宽度，CSS 长度单位
| `window-min-height`| 窗口的最小高度，CSS 长度单位
| `window-max-width` | 窗口的最大宽度，CSS 长度单位
| `window-max-height`| 窗口的最大高度，CSS 长度单位
| `window-resizable`  | `true\|false\|LENGTH-UNIT` i.e. `10px` 从窗框向内数
| `window-minimizable` | `true\|false`
| `window-maximizable` | `true\|false`
| `window-blurbehind` | `auto\|dark\|light\|ultra-dark\|ultra-light` 半透明效果。
| `window-corners` | `default\|not-round\|round\|round-small` - 在支持的操作系统（例如 Win11）上定义窗口角圆度。
| `window-state` | `shown\|minimized\|maximized\|full-screen\|hidden` - HTML 窗口的初始状态
| `lang` | ISO 639-1 值, 为拼写检查定义字典，日期...
| `disable-debug` | 不要连接到检查员


## Misc

- **不支持属性事件 (onclick..)。 （除非你实现了它的工作方法）。**
- Sciter 允许使用自定义元素标签，确保给它们一个默认样式。
- 你可以显示弹出窗口 [`Element.popup`](Element.md#popup).
- 字符串 `&platform-cmd-mod;` 被替换为 `Ctrl/CMD...`
- [输入元素列表](https://sciter.com/developers/for-web-programmers/input-elements-map/)
