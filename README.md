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

### Options

#### options.tpsmatePath
Type: `String`
Default value: `~/github/tpsmate/src/cli.py`

your tpsmate `cli.py` path.

#### options.argv
Type: `String`
Default value: `--inplace`


the options which allows you to set the arguments to the cli.py

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
