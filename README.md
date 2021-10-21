# supermall
##项目的初始化工作
### 一.划分目录结构
```
1.新建views视图
2.components里放公共组件
  common:放一些可以跨越项目的组件（完全公用的）
  content:放一些本项目内的组件（本项目公用）
3.新建router：路由
4.新建store：vuex状态管理
5.新建network：网络封装
6.新建common：公共的js文件
```
### 二.创建vue.config.js配置别名
```
module.exports = {
  configureWebpack: {
    resolve: {
      // 别名的配置
      alias: {
        'assets' : '@/assets',
        'common' : '@/common',
        'components' : '@/components',
        'network' : '@/network',
        'views' : '@/views',
      }
    }
  }
}
```

### 三.创建.editorconfig来统一代码规范
```
root = true

[*]
charset = utf-8
indent_style = space
indent_size = 2
end_of_line = lf
insert_final_newline = true
trim_trailing_whitespace = true
```

### 四.创建两个css文件
```
// 自己写的base.css
base.css
// github上导入的默认浏览器书写规范
normalize.css
```

## 搭建项目基本框架
### 一.components里面搭建TabBar
```
root = true

[*]
charset = utf-8
indent_style = space
indent_size = 2
end_of_line = lf
insert_final_newline = true
trim_trailing_whitespace = true
```

### 三.创建.editorconfig来统一代码规范
```
root = true

[*]
charset = utf-8
indent_style = space
indent_size = 2
end_of_line = lf
insert_final_newline = true
trim_trailing_whitespace = true
```

### 三.创建.editorconfig来统一代码规范
```
root = true

[*]
charset = utf-8
indent_style = space
indent_size = 2
end_of_line = lf
insert_final_newline = true
trim_trailing_whitespace = true
```

### 三.创建.editorconfig来统一代码规范
```
root = true

[*]
charset = utf-8
indent_style = space
indent_size = 2
end_of_line = lf
insert_final_newline = true
trim_trailing_whitespace = true
```

### 三.创建.editorconfig来统一代码规范
```
root = true

[*]
charset = utf-8
indent_style = space
indent_size = 2
end_of_line = lf
insert_final_newline = true
trim_trailing_whitespace = true
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).
