webpack脚手架，通过此来梳理一些知识点。


# 知识点 #

## babel ##
配置放在.babelrc里面。

### babel-cli ###
在命令行下使用Babel编译文件的简单方法。

- -o-file/-o 写到指定文件
- --out-dir/-d 把一个目录编译到一个新的目录

### babel-core ###
以编程的方式来使用Babel。

### babel-preset-es2015 ###
把es6编译成ES5。

### babel-preset-react ###

### babel-polyfill ###
polyfill即是在当前运行环境中用来复制（模拟性的复制，而不是拷贝）尚不存在的原生api的代码。

### babel-runtime ###
更新到plugins去。

### 插件选项 ###

- 宽松模式： {"loose": true}
- 基于环境配置Babel：<pre>
	<code>
	{
		"presets": ["es2015"],
		"plugins": [],
		"env": {
			"development": {
				"plugins": [...]
			},
			"production": {...}
		}
	}
	</code>
 </pre>

### transform-remove-strict-mode ###
[babel6默认添加use strict引发的问题和解决方案](https://github.com/shanggqm/blog/issues/1)

### transform-class-properties ###
[transform-class-properties](http://babeljs.io/docs/plugins/transform-class-properties/)

### jsx-control-statements ###
[jsx-control-statements](https://www.npmjs.com/package/jsx-control-statements)

## gulp ##
gulpfile.js

### .src(globs[,options]) ###
输出匹配文件。
<pre>
globs: String/Array

options: {
	// 支持node-glob和glob-stream所支持的参数
	buffer,	// 默认true;false:将以stream方式返回
	read,	//默认true,
	base	//
}
</pre>

### .dest(path[,options]) ###
能被 pipe 进来，并且将会写文件。并且重新输出（emits）所有数据

<pre>
path: String / Function
options: {
	cwd,	// 默认process.cwd
	mod	// 默认0777
}
</pre>

### .task(name[,deps],fn) ###
默认的，task将以最大的并发数执行。
<pre>
deps: Array	//一个包含任务列表的数组，这些任务会在当前任务运行之前完成
</pre>

### .watch(glob[,opts],tasks)/.watch(glob[,opts,cb]) ###

## webpack ##
[github](https://github.com/webpack/webpack)

[文档](https://webpack.js.org/configuration/)

[中文文档](https://doc.webpack-china.org/configuration/)

### dll ###

[实践 DllPlugin 来优化 webpack 打包速度](https://juejin.im/entry/57a6dee4a633bd00604d0e73)


[Babel 用户手册](https://github.com/thejameskyle/babel-handbook/blob/master/translations/zh-Hans/user-handbook.md "Babel 用户手册")