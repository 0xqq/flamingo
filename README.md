# Flamingo -基于Ansible的自动化代码发布工具
***目的***： 通过Ansible实现统一的代码发布方式，思路基于Capistrano

Flamingo对Ansistrano进行了二次修改和整理以实现根据不同的语言环境,主机组(应用组/灰度机组等)代码库,分支,项目名来自动化构建打包发布的需求;</br>
```
ansible-playbook  deploy.yml  --extra-vars='flamingo_git_repo=git@github.com:geekwolf/flamingo.git flamingo_product_name=flamingo'

```
***代码回滚***：回滚即发布,通过结合jenkins选择已发布的release重新构建即可，详细参数可通过defaults/main.yml文件了解
***TODO***:增加前端构建及JAVA打包功能
