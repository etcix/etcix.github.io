# 前提
- 换源 
- ruby版本问题
- gem update --system 

- gem install rails
- rails new demo

- rails server
- rails generate scaffold title:string content:text # ? 什么意思

# 设计原则
- coc (约束大于配置)
- mvc
- dry 
- software engineering patterns
- assets
- restful
- testing
- deployment
- automation
- 敏捷开发 agile development

# 快速上手
1. 创建 circles 项目
2. mvc rails 目录结构
3. controller
4. bootstrap 框架
 
- rails new circles 
- cd circles
- rails server
# vim Gemfile
- in Gemfile
```gemfile
# to add 
source 'https://ruby.taobap.org/'
```
- bundle install 
 
 
- rails server -p 4001
- rails g controller welcome index # welcome is name of - controller

# 文件目录结构
- routes.rb 
```ruby
  add in do {} root 'welcome#index'
```
- controller.welcome 就需要定义一个 index 方法

- 然后再view.welcome目录下还需要一个index.html.erb文件
 
- 如果可以正确显示页面
 
- rails g controller user new
- 修改 routes.rb 文件 加入 resources :user 项
- 查看 /user/new
 

# db层 model
- orm mapping
- xml
- ruby style: gem active record 
- active record support
- sqlite (default) 
- mysql 
- postgresql
- oracle
- sqlserver

- mongoid / mongomapper
- mongodb 

# 配置成mysql(生产环境)

1. 先配置database.yml文件

```bash
brew install mysql
brew services start mysql
mysql -u root
```

# rake db:create # rake -T 查看更多task
- 会在本地 mysql 产生 数据库
- 如果出错，立刻 drop database <db name>


#  建立 user model , 就是一个表

1. rails g model user

2. 修改 db/migrate/ 的文件

3. rake db:migrate

4. rails console 的使用(非常强大的数据操作能力）

