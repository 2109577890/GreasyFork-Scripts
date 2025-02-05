# [**GreasyFork-Scripts**](https://f9y4ng.github.io/GreasyFork-Scripts/) - F9y4ng -  [![WIKI](https://img.shields.io/badge/WIKI-GREASYFORK%20SCRIPTS-brightgreen.svg?logo=github "wiki")](https://github.com/F9y4ng/GreasyFork-Scripts/wiki)

[![LICENSE](https://img.shields.io/badge/License-GPL--3.0--only-blue.svg?style=for-the-badge&logo=github "LICENSE")](https://github.com/F9y4ng/GreasyFork-Scripts/blob/master/LICENSE) [![LAST COMMIT](https://img.shields.io/github/last-commit/F9y4ng/GreasyFork-Scripts?color=blue&logo=github&style=for-the-badge "LAST COMMIT")](https://github.com/F9y4ng/GreasyFork-Scripts/commits/master) [![ISSUES](https://img.shields.io/github/issues/F9y4ng/GreasyFork-Scripts?logo=github&style=for-the-badge "ISSUES")](https://github.com/F9y4ng/GreasyFork-Scripts/issues) [![STARS](https://img.shields.io/github/stars/F9y4ng/GreasyFork-Scripts?color=brightgreen&logo=github&style=for-the-badge "STARS")](https://github.com/F9y4ng/GreasyFork-Scripts/stargazers)

请先根据你的浏览器安装一个**用户脚本管理器**扩展(如TamperMonkey, ViolentMonkey) 然后再**安装脚本**。

(不建议使用AdGuard安装脚本，因为脚本设置功能将无法查看。如有配置需要，请使用“键盘快捷键”。)

***

# 字体渲染（自用脚本） [**Font Rendering.user.js**](https://github.com/F9y4ng/GreasyFork-Scripts/blob/master/Font%20Rendering.user.js)
简介：无需安装MacType，优化浏览器字体显示，让每个页面的中文字体变得有质感，默认使用微软雅黑字体，亦可自定义设置多种中文字体，附加字体描边、字体重写、字体阴影、字体平滑、对特殊样式元素的过滤和许可等效果，脚本菜单中可使用设置界面进行参数设置，亦可对某域名下所有页面进行排除渲染，兼容常用的 Greasemonkey 脚本和浏览器插件。

`version 2022.10.05.1` 【🔥 [安装此脚本](https://github.com/F9y4ng/GreasyFork-Scripts/raw/master/Font%20Rendering.user.js)】

[`!!! 重大版本更新，请使用前仔细查看脚本使用说明(WIKI) !!!`](https://github.com/F9y4ng/GreasyFork-Scripts/wiki/%E5%AD%97%E4%BD%93%E6%B8%B2%E6%9F%93%EF%BC%88%E8%87%AA%E7%94%A8%E8%84%9A%E6%9C%AC%EF%BC%89) `New!`

`!!! 脚本错误、异常请反馈至[Issues], 字体、渲染样式、乱码问题请反馈至[Discussions] !!!`

`!!! 为保证您的数据安全，请及时备份您的本地数据！请勿使用来源未知的备份文件 !!!`

```text
@ 临时修正TM4.18.0的ISSUE#1607造成的菜单消失问题。
@ 修正拾色器在Firefox102以上版本的识别bug.
# 注意：在Firefox下如需字体缩放功能，强烈建议您使用浏览器缩放替代(ctrl++/ctrl+-)。
@ 精简及优化部分功能，提升代码执行效率。
@ 修正一些已知的问题，优化代码。
```

## 特别注意
Chromium内核低于88.0的浏览器将不再被兼容，Manifest V3后低版本浏览器兼容性会进一步降低。

需继续使用低版本Chromium内核浏览器的用户请安装 [v2022.09.03.1](https://greasyfork.org/scripts/416688?version=1089117) 版本。

## 关于问题反馈
**注意**：使用浏览器或脚本管理器的`Beta`、`Dev`、`Canary`、`Nightly`等测试分支版本有可能造成未知的兼容性问题或异常错误，本脚本将不会针对测试版本错误进行修正，**需使用测试版本的用户请停用本脚本选择其他同类脚本**。因有极小概率发生因数据兼容性错误造成本地数据被异常初始化，**为确保数据安全，请及时且定期备份您的本地数据。**

请反馈问题的朋友注意：反馈脚本错误或样式显示问题，请把**仅使用本脚本的情况下**发生问题的**具体访问网址**、使用的**浏览器版本**、**脚本运行器版**、**相关错误的截图**、以及**具体操作流程**或**错误提示**（如果有的话）发出来，你遇到的问题不一定能在其他地方复现。

* [关于个别网站样式错误修正的设置分享，不定期更新，自取自用。](https://github.com/F9y4ng/GreasyFork-Scripts/discussions/42)

* [分享：关于分别设置英文字体和中文字体的方法。](https://github.com/F9y4ng/GreasyFork-Scripts/discussions/83)

* 字体表字体及其他中文字体分享：[点这里下载字体包](https://github.com/F9y4ng/GreasyFork-Scripts/discussions/46)

## 关于字体的添加
**如果您需要向字体表添加自定义字体，请按[帮助说明的指引](https://github.com/F9y4ng/GreasyFork-Scripts/discussions/64)进行操作。**

如果您需要增加新的字体进入代码字体表，请将 **完整且准确** 的字体 **中英文名称** 及 **PostScript名称** 按 **预设格式** 添加进自定义字体列表。

格式如右：`{"ch":"鸿蒙黑体", "en":"HarmonyOS Sans SC", "ps":"HarmonyOS_Sans_SC"}`
* 新增字体，一般只接受字重为 **标准体/Regular** 的字体，需调整字重粗体请使用字体描边进行设置。
* “ps:”表示字体PostScript名称，此为可选属性。为实现字体全局生效，请尽量填写"ps:"属性。
* 网络上很多字体存在各种修改版、Hack 版，非原版字体会造成字体名不一致，从而使得代码无法识别。

每当计算机安装了新字体，要使其**立即生效**，请在“**高级核心功能设置**”中重建字体列表全局缓存。
* 注1：由于操作系统字体缓存，在计算机安装新字体后请**重启浏览器**，确保系统字体缓存在浏览器中生效。
* 注2：自定义字体表的**编辑保存操作**会自动触发字体列表全局缓存的重建，无需额外手动处理。
* 注3：若仅安装**内置字体表**定义的字体，重启浏览器后，需要**手动**重建字体列表全局缓存。

## 关于字体缩放
字体比例缩放（实验性功能）Beta版，默认关闭，请在 **高级核心功能设置** 中打开字体缩放功能。
* **已知问题一：** Firefox/Gecko内核下，仅修正了坐标偏移问题，针对 `Position:fixed/sticky` 的样式修正因性能问题已终止。**强烈建议**：Firefox用户使用浏览器缩放替代(`Ctrl++`, `Ctrl+-`)。
* **已知问题二：** 针对视窗单位 `vw, vh, vm*` 的全局修正因性能问题及跨域问题已终止，会对部分网站在字体缩放时造成居中样式错误，建议在此类网站中停用字体缩放（即：设置参数为1.000），使用浏览器缩放替代(`Ctrl++`, `Ctrl+-`)。
* **未知情况：** 如遇到非以上情况的样式异常或坐标偏移，请及时向我[反馈](https://github.com/F9y4ng/GreasyFork-Scripts/issues)。

## 字体渲染（自用脚本）新版本，使用前请注意以下事项：
新版脚本中 **内置了默认的字体渲染样式，该样式为我本地配置，并不能完美适配于你的计算机**。所以，首次使用时，如果出现渲染效果没有达到理想状态，属于**正常情况**。请根据**自有显示器的配置及设置**，通过**脚本配置界面**修正相关参数来达到最佳显示效果。如在使用过程中遇到错误或使用问题，请及时向我[反馈](https://github.com/F9y4ng/GreasyFork-Scripts/issues)。

***

# 优雅的搜索引擎跳转助手 [**Google & Baidu Switcher.user.js**](https://github.com/F9y4ng/GreasyFork-Scripts/blob/master/Google%20%26%20Baidu%20Switcher.user.js)
简介：优雅的搜索引擎跳转助手，更美观、更便捷。新版本增加去重定向功能、自定义搜索引擎选取功能，提供可视化搜索参数设置，及自动更新检测等高级功能。

`version 2022.10.05.1` 【🔥 [安装此脚本](https://github.com/F9y4ng/GreasyFork-Scripts/raw/master/Google%20%26%20Baidu%20Switcher.user.js)】

[`!!! 重大版本更新，请使用前仔细查看脚本使用说明(WIKI) !!!`](https://github.com/F9y4ng/GreasyFork-Scripts/wiki/%E4%BC%98%E9%9B%85%E7%9A%84%E6%90%9C%E7%B4%A2%E5%BC%95%E6%93%8E%E8%B7%B3%E8%BD%AC%E5%8A%A9%E6%89%8B) `New!`

`!!! 自动更新检测默认开启，如无更新提示需求，可在“功能设置开关”中关闭它 !!!`

```text
+ 新增百度开发者搜索Beta引擎跳转。
@ 临时修正TM4.18.0的ISSUE#1607造成的菜单消失问题。
@ 优化百度，Google，搜狗,360的广告屏蔽规则。
@ 修正一些已知的问题，优化代码。
```
## 最新功能介绍
* 新增去除搜索结果及侧栏广告功能。
* 新增自定义搜索引擎选取功能（包含：百度、Google、Bing、Duckduckgo、搜狗、F搜、Yandex、360搜索、头条搜索、百度开发者搜索等常见的搜索引擎）
* 新增搜索结果链接去重定向功能。
* 更智能的更新检测功能。

## 重要说明
新版本“**自动更新**”功能默认开启，如不需要更新检测，请在脚本菜单“功能设置开关”中，关闭 **更新检测** 即可。
* 请反馈问题的朋友注意：反馈脚本错误或样式显示问题，请把发生问题的**具体访问网址**、使用的**浏览器版本**、**脚本运行器版**、**相关错误的截图**（仅开本脚本的情况下的）、以及**具体操作流程**或**错误提示**（如果有的话）发出来，你遇到的问题不一定能在其他地方复现。
* 一般来说，最新及测试版的发布将在**Github**进行，**GreasyFork**会在24小时内自动同步。已开启自动更新检测功能的用户，客户端代码会根据更新频率设置进行自动更新。
