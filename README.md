# oldwangBlog
个人博客项目

[oldwangBlog地址](http://112.124.26.204/)

# 简介

- [配置文件](https://github.com/witcherwjl/oldwangBlog/blob/master/my_blog/settings.py)
## [主页管理]
1. 搜索
2. 分页

## [文章管理](https://github.com/witcherwjl/oldwangBlog/tree/master/article)
实现功能：
1. 文章列表展示（也是主页）
2. 写文章
   - 位置在用户下拉表格中
    - 添加图片功能
    - 使用markdown进行书写
3. 发表文章在文章列表
4. 修改/删除文章权限设置
5. 浏览总数，评论总数，发表时间
6. 无需登录即可点赞

## [评论功能管理](https://github.com/witcherwjl/oldwangBlog/tree/master/comment)
1. 需登陆评论
2. 二级评论
3. 通知被评论人
## [用户管理](https://github.com/witcherwjl/oldwangBlog/tree/master/userprofile)
1. 登陆
2. 注册及发送邮件
3. 个人信息修改
4. 退出登录
## [通知管理](https://github.com/witcherwjl/oldwangBlog/tree/master/notice)
1. 评论通知
2. 点击通知通过锚点实现跳转
## [前端文件](https://github.com/witcherwjl/oldwangBlog/tree/master/templates)

# 待改进
1. 待添加模块
   - 邮箱验证
   - 第三方登录
   - 个人信息查看
   - 待续
2. 界面改进
   - 好好学学前端改进一下
   - 待续
# 需要添加的文件
在根目录下添加'email.txt'，用于发送邮件

# 部署笔记
- 由于阿里云学生服务器默认系统盘，所以nginx权限不够，需要在/etc/nginx/nginx.conf第一行
```bash
user www.data
# 改为 
user root
```
使用时
```bash
source env/bin/activate
sudo service nginx reload
gunicorn --bind unix:/tmp/118.31.35.48.socket my_blog.wsgi:application
```
# 2020年5月27日 记录

