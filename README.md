### package.json

```
{
	// 插件项目名
    "name": "firstextension",
	// 显示在应用市场的插件名，支持中文
    "displayName": "FirstExtension插件教程",
	// 插件描述
    "description": "a tutorial for extension",
	// 版本号
    "version": "0.0.1",
	// 表示插件最低支持的vscode版本
    "engines": {
        "vscode": "^1.50.0"
    },
	// 插件应用市场分类
    "categories": [
        "Other"
    ],
	// 插件图标，至少128x128像素（可选配）
    // "icon": "images/icon.png",
	// 插件的被动激活事件，可配*来保持在后台持续运行
    "activationEvents": [
        "onCommand:firstExt.hello"
    ],
	// 插件的主入口文件
    "main": "./out/extension.js",
	// 贡献点，整个插件最重要最多的配置项
    "contributes": {
		// 命令
        "commands": [
            {
                "command": "firstExt.hello",
                "title": "Hello World"
            }
        ],
		// 快捷键绑定，分为mac和win操作系统；when是触发的先决条件，可不配；
        "keybindings": [
            {
                "command": "firstExt.hello",
                "key": "ctrl+w",
                "mac": "cmd+shift+w",
                "when": "editorTextFocus"
            }
        ],
		// ---- 下面配置在后面小说案例中说明
		// 菜单
        "menus": {
			// 编辑器鼠标右键菜单
            "editor/context": [],
			// 编辑器右上角图标，不配置图片就显示文字
            "editor/title": [],
			// 编辑器标题右键菜单
            "editor/title/context": [],
			// 资源管理器右键菜单
            "explorer/context": []
        },
		// 自定义新的activitybar图标，也就是最左侧 图标栏
        "viewsContainers": {},
		// 自定义左侧侧边栏内view树的实现
        "views": {},
        // 插件自定义设置项，由用户配置后传参进入代码逻辑里，暂不展示
		"configuration": {},
    }
}
```
