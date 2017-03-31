Sublime Text 是程序员们公认的编码神奇，拥有漂亮的用户界面和强大的功能，例如代码缩略图，多重选择，快捷命令等。还可自定义键绑定，菜单和工具栏。Sublime Text 的主要功能包括：拼写检查，书签，即时项目切换，多选择，多窗口等等。

更重要的是，Sublime Text 易于扩展，众多开发人员为其贡献插件，而且通过包管理工具——Package Control 可以方便安装和管理。这里分享的这个网站是 Package Control 的作者整理的 Sublime Text 插件集合，前端开发的民工们再也不用去网上一个个找了。赶紧收藏起来吧。

![sublime text](http://images2015.cnblogs.com/blog/490251/201703/490251-20170330210458133-1567277629.jpg)

## Sublime Text的安装与使用

官网：[http://www.sublimetext.com/](http://www.sublimetext.com/)

#### 安装Package Control

首先通过快捷键 *ctrl+`*  或者 *View > Show Console* 打开控制台，然后粘贴相应的 Python 安装代码。

Sublime Text 2 安装代码：

	import urllib2,os; pf='Package Control.sublime-package'; ipp = sublime.installed_packages_path(); os.makedirs( ipp ) if not os.path.exists(ipp) else None; urllib2.install_opener( urllib2.build_opener( urllib2.ProxyHandler( ))); open( os.path.join( ipp, pf), 'wb' ).write( urllib2.urlopen( 'http://sublime.wbond.net/' +pf.replace( ' ','%20' )).read()); print( 'Please restart Sublime Text to finish installation')

Sublime Text 3 安装代码：

	import urllib.request,os; pf = 'Package Control.sublime-package'; ipp = sublime.installed_packages_path(); urllib.request.install_opener( urllib.request.build_opener( urllib.request.ProxyHandler()) ); open(os.path.join(ipp, pf), 'wb').write(urllib.request.urlopen( 'http://sublime.wbond.net/' + pf.replace(' ','%20')).read())

## Sublime Text必备插件

- Emmet

Emmet 项目的前身是前端开发人员熟知的 Zen Coding（快速编写 HTML/CSS 代码的方案）。在 Sublime Text 编辑器中搭配 Emmet 插件真的是让你编码快上加快。

- Alignment

代码对齐插件(=号对齐)：变量定义太多，长短不一，可一键对齐。默认快捷键Ctrl+Alt+A和QQ截屏冲突，可设置其他快捷键如：Ctrl+Shift+Alt+A；先选择要对齐的文本

- AutoFileName

快捷输入文件名：自动完成文件名的输入，如图片选取。使用：输入”/”即可看到相对于本项目文件夹的其他文件

- Bracket​Highlighter

括号高亮匹配；

- Bracket Highlighter

代码匹配插件：可匹配[], (), {}, “”, ”, <tag></tag>，高亮标记，便于查看起始和结束标记

- jQuery

代码智能提示插件：快捷输入jQ函数，是偷懒的好方法

- Js​Format

JavaScript 代码格式化插件：在已压缩的JS文件中，右键选择`jsFormat`或者使用默认快捷键（`Ctrl+Alt+F`）

- CssFormat

Css 代码格式化插件：在css文件中，右键选择`cssFormat`

- DocBlockr

生成优美注释：如果你遵循的编码的风格很严格，这款插件能够使你的任务更容易。DocBlokr 帮助你创造你的代码注释，通过解析功能，参数，变量，并且自动添加基本项目。输入/*、/**然后回车，还有很多用法，请参照[https://sublime.wbond.net/packages/DocBlockr](https://sublime.wbond.net/packages/DocBlockr)

- ConvertToUTF8

文件转码成utf-8：通过本插件，您可以编辑并保存目前编码不被 Sublime Text 支持的文件，特别是中日韩用户使用的 GB2312，GBK，BIG5，EUC-KR，EUC-JP ，ANSI等。ConvertToUTF8 同时支持 Sublime Text 2 和 3。安装插件后文件自动转换为utf-8格式。

- Trailing spaces

检测并一键去除代码中多余的空格，让你的代码规范清爽起来。一键删除多余空格：CTRL+SHITF+T（需配置），更多配置请点击标题。快捷键配置：在Preferences / Key Bindings – User加上代码（数组内）

- MarkdownPreview

使用浏览器来preview效果，安装完后你便可以用sublime来编写Markdown语法了并使用浏览器预览了。当你想查看效果的时候，键入ctrl + shift + p，控制板中键入Markdown，选择preview in browser，再选择github。这时候效果就会在显示器中显示了。

- Sublime CodeIntel

代码自动提示插件

- Sublime​Linter

代码校验插件：一个支持lint语法的插件，可以高亮linter认为有错误的代码行，也支持高亮一些特别的注释，比如“TODO”，这样就可以被快速定位。安装教程：[https://gaohaoyang.github.io/2015/03/26/sublimeLinter/](https://gaohaoyang.github.io/2015/03/26/sublimeLinter/)

	安装方法：

	1.按下 Ctrl+Shift+p 进入 Command Palette
	2.输入install进入Package Control: Install Package
	3.输入`SublimeLinter`安装Linter
	4.输入`SublimeLinter-jshint`安装jshint
	5.输入`SublimeLinter-csslint`安装csslint
	6.下载并安装[Node.js](https://nodejs.org/en/)
	7.打开命令行，输入`sudo npm install -g jshint`，通过 npm 安装 jshint
	8.输入`jshint -v`，查看 jshint 版本，已确认jshint安装完成
	9.打开命令行，输入`sudo npm install -g csslint`，通过 npm 安装 csslint
	10.输入`csslint --version`，查看 csslint 版本，已确认 csslint 安装完成


## Sublime Text选装插件

- Color​Picker

跨平台取色器插件：通常，如果你想使用一个颜色选择器则可能打开 Photoshop 或 GIMP。而在 Sublime Text 中，你可以使用内置的颜色选择器。安装完成后，只要按下Ctrl / Cmd + Shift + C 快捷键。

- Git

整合 Git 功能的插件：在工作中，版本控制软件最常用的软件之一，而最流行的 VCS 是 Git。你是否厌倦了保存文本文件，并切换回终端运行一些 Git 命令。如果你能从文本编辑器本身执行 Git 命令，岂不是很好？

- GitGutter

Sublime Text 有了 Git 插件之后，GitGutter 更好的帮助开发者查看文件之前的改动和差异，提升开发效率。

- LESS

LESS高亮插件：用LESS的同学都知道，sublime没有支持less的语法高亮，所以这个插件可以帮上我们

- Nodejs

node代码提示：教程：https://sublime.wbond.net/packages/Nodejs

- FileDiffs

强大的比较代码不同工具：比较当前文件与选中的代码、剪切板中代码、另一文件、未保存文件之间的差别。可配置为显示差别在外部比较工具，精确到行。使用：右键标签页，出现FileDiffs Menu或者Diff with Tab…选择对应文件比较即可

## Sublime Text 配色方案

- Material Theme

很漂亮的一款sublime主题，看着很舒服，护眼。

## Sublime Text 编程字体

- Source Code Pro

下载地址：[https://github.com/adobe-fonts/source-code-pro](https://github.com/adobe-fonts/source-code-pro)