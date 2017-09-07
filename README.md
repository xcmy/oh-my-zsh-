## oh-my-zsh使用配置


[oh-my-zsh gitHub地址](https://github.com/robbyrussell/oh-my-zsh)

### 安装
- 终端curl安装
```
    sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```

- 安装目录为

```
    ~/.oh-my-zsh
```
### 修改终端（或者item2）启动方式

- 终端>偏好设置>通用>Shell的打开方式>命令 修改为 
    
```        
    /bin/zsh

```
- iTerm 2>Preferences>Profiles>General>Command 选择Command输入
    
```
    /bin/zsh
```    
系统终端默认启动命令的是`/bin/bash`，要修改为`/bin/zsh`才能生效
    
配置文件为
```
    ~/.zshrc
```

### 主题修改

打开`oh-my-zsh`的配置文件
```
    vim ~/.zshrc
```   
可通过修改下面这行来修改主题，引号内为主题名字
```
    ZSH_THEME="robbyrussell"
``` 

安装成功后自带很多种主题，可根据自己喜好来选择，主题文件位于`~/.oh-my-zsh/themes`，也可以在<https://github.com/robbyrussell/oh-my-zsh/wiki/themes>查看

主题配置成功后执行使之生效。
```
    $ source ~/.zshrc
``` 
    

## 补充

若安装后系统的环境变量不能使用

检查环境变量

```
    $ echo $PATH
``` 
会输出当前系统的环境变量，比如：

```
/usr/local/sbin:/usr/local/bin:/sbin:/bin:/usr/sbin:/usr/bin:/root/bin
```
因为`zsh`不读取`.bash_profile`,而是读取`.zshrc`，所以需要把环境变量在`.zshrc`中配置一份。  
若存在`.bash_profile`,则copy里面的路径到`.zshrc`文件中，并`source ~/.zshrc`.

若不存在`.bash_profile`,将上面的` echo $PATH`命令输出的路径写入到`.zshrc`文件中，写法如下：

```
export PATH=/Users/xcmy/.nvm/versions/node/v7.10.0/bin:/usr/local/sbin:/usr/local/bin:/sbin:/bin:/usr/sbin:/usr/bin:/root/bin
```

然后使之生效
```
$ source ~/.zshrc
```



    
    
    
    

    
    