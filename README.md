# 木犀前端Workflow

## CSS

### Style Guide

[Muxi CSS Style Guide](https://github.com/Muxi-Studio/muxife-conf/blob/master/cssconf/README.md)

### 预处理器-SASS

Lint工具：[sass-lint](https://github.com/sasstools/sass-lint)

格式化工具：[csscomb](https://github.com/csscomb/csscomb.js)

配置文件

+ [`.scss-lint.yml`](https://github.com/Muxi-Studio/muxife-conf/blob/master/cssconf/.sass-lint.yml)

+ [`.csscomb.json`](https://github.com/Muxi-Studio/muxife-conf/blob/master/cssconf/.csscomb.json)



## JavaScript

Lint工具：ESLint

`.eslintrc`文件:

+ [es5](https://github.com/Muxi-Studio/muxife-conf/blob/master/jsconf/eslint-es5/.eslintrc.js)
+ [es6](https://github.com/Muxi-Studio/muxife-conf/blob/master/jsconf/eslint-es6/.eslintrc.js)


代码规范(基于Google ES5，AirBnb ES6)

+ No semicolons
+ Double quote
+ 60 characters max in a line
+ Add trailing comma

## 构建工具

展示为主的项目

`gulp+http-server+sass-lint+eslint`

有富交互组件的项目

`webpack+babel+webpack-dev-server+sass-lint+eslint`

## Boilerplate

+ `muxife_gulp_boilerplate`
+ `muxife_webpack_boilerplate`