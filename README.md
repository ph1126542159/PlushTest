# PlushTest
自动化发布测试

### 注意事项
    1. 当前只有
    name: "Desktop CI builds"
    on:
      push:
        tags:
      - "*"
      workflow_dispatch:
    只有在push tag时才会触发自动化发布测试，其他情况需要手动触发。
    3.QT_VERSION: "6.5.0"指定了Qt 版本
### tag命令
    git tag -d v1.0.0 # 删除tag
    git tag -a v1.0.0 -m "first release" # 打带注释的tag
    git push origin v1.0.0 # 推送tag到远程仓库

### 自动化发需要添加一个token
1. 登录GitHub账号，点击右上角头像，选择Settings
2. 点击Developer settings，选择Personal access tokens
3. 点击Generate new token，输入token描述，勾选repo权限，点击Generate token
4. 复制生成的token，在项目的Secrets中添加一个名为`MYTOKEN`的secret，值为刚才复制的token

