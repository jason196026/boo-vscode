# 安装git
``` 
下载git，https://git-scm.com/downloads 
```

# Git基础配置
```
git config --global user.name jason196026
git config --global user.email 381799338@qq.com

注：git的配置，均在git bash命令行中完成
```

# 生产SSH公私钥
```
https://docs.github.com/en/github/authenticating-to-github/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent

$ ssh-keygen -t rsa -b 4096 -C "381799338@qq.com"
 在用户家目录下会看到.ssh中有id_rsa和id_rsa.pub两个文件

增加SSH key 到ssh-agent
$ eval "$(ssh-agent -s)"
  Agent pid 2029

$ ssh-add ~/.ssh/id_rsa
```

# 将公钥添加到github
```
登入github，在setting > SSH and GPG keys 选择new ssh key， 把id_rsa.pub中的内容拷贝进来，保存即可
```
# 测试SSH
```
$ ssh -T git@github.com
```


```
> Connecting to GitHub with SSH
https://docs.github.com/en/github/authenticating-to-github/connecting-to-github-with-ssh
````
