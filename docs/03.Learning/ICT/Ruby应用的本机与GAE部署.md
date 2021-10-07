# Ruby应用的本机与GAE部署

**2020-07-05 21:23:00**  

## 1. Ruby应用准备

下载[Markdown Journal](https://github.com/maciakl/MarkdownJournal)并修改配置：  
1.1 项目根目录下新增 ./config.yml 内容为：  
```
key: your-dropbox-app-key-string
secret: your-dropbox-app-secret-string
url: http://localhost:4567/write
```
1.2 ./views/layout.erb 第83行 href 值修改为：  
```
http://localhost:4567/write
```

## 2. Ruby本机部署

> [Ruby](https://www.ruby-lang.org/en/)Windows运行环境  
> [Gem](http://rubygems.org/)是Ruby的套件安装工具^[1]^，类似于Python的pip  
> [Bundler](http://gembundler.com/)是Ruby的套件，可以從gem上面下載。他是用來解決gem套件相依性問題的套件。^[2]^  

2.1 安装Ruby2.6.6（2.7存在兼容问题），它内置Gem  
2.2 安装bundler，本应用需要特定版本：  
```
gem install bundler:1.13.6
```
2.3 进入项目根目录下，安装依赖包：  
因为已经写好了Gemfile，以下命令不用执行：  
```
bundle init
```
直接执行以下命令：  
```
bundle install
```
2.4 安装之后即可运行应用：  
```
ruby app.rb
```
2.5 最后通过本机浏览器访问应用：
```
http://localhost:4567/
```
[1][2]Ref: 林克融. 20160505. [\[筆記\]Ruby的RVM,GEM,Bundler是什麼？](http://sayaku.github.io/blog/2016/05/05/rubyde-rvm-gem-bundler/)  
