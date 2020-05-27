# oldwangBlog
个人博客项目

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
待添加模块
- 邮箱验证
