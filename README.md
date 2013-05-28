# grunt-tps

> taobao pictures system grunt plugin

## Getting Started
This plugin requires Grunt `~0.4.1`

If you haven't used [Grunt](http://gruntjs.com/) before, be sure to check out the [Getting Started](http://gruntjs.com/getting-started) guide, as it explains how to create a [Gruntfile](http://gruntjs.com/sample-gruntfile) as well as install and use Grunt plugins. Once you're familiar with that process, you may install this plugin with this command:

```shell
npm install grunt-tps --save-dev
```

One the plugin has been installed, it may be enabled inside your Gruntfile with this line of JavaScript:

```js
grunt.loadNpmTasks('grunt-tps');
```

## The "tps" task

### Base

本插件基于[tpsmate](https://github.com/sodabiscuit/tpsmate)

使用之前请仔细阅读[tpsmate文档](http://me.tardoc.com/tpsmate/)

#### tpsmate配置

```shell
tpsmate config --username "username"
tpsmate config --password "password"
tpsmate config --encoding "utf-8,gbk,big5"
tpsmate config --logdir "/path/to/save/csv/log/"
tpsmate login --username "username" --password "password"
tpsmate logout
```

这里的`tpsmate`指向的就是你本机的`xx/tpsmate/src/cli.py`文件

第一次使用tpsmate，需要登录下，之后tpsmate就会记住你的登录信息，一般不需要再次登录

### Options

#### options.tpsmatePath
Type: `String`
Default value: `~/github/tpsmate/src/cli.py`

tpsmate的运行脚本绝对地址。

#### options.argv
Type: `String`
Default value: `--inplace`

tpsmate的参数

- --inpace 对原文件做替换操作
- --force 强制上传任意文件中的内联样式背景图片或者src属性，导出或显示替换后的文件
- --no-log 不输出csv
- --no-interactive 不在终端输出上传信息

### Usage Examples

### normal

```js
grunt.initConfig({
  tps: {
    options: {
        tpsmatePath:"~/github/tpsmate/src/cli.py",
        argv: "--inplace",
    },
    all: ['test.css', 'lib/**/*.css', 'test/**/*.scss','index.htm']
  },
})
```

## Contributing
In lieu of a formal styleguide, take care to maintain the existing coding style. Add unit tests for any new or changed functionality. Lint and test your code using [Grunt](http://gruntjs.com/).

## Release History

2013-05-28   v0.1.1   First official release

2013-05-02   v0.1.0   Work in progress, not yet officially released.
