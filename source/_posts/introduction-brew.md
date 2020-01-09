---
title: Mac OS的软件包管理器--Homebrew
date: 2020-01-09
tags:
---
软件开发总会碰到需要使用的软件包依赖于各种各样的其它软件包，而如果需要人们手动去查询这些依赖包难免会效率低下，因此大多数主流操作系统都有提供相应的软件包管理器，如Ubuntu的apt-get，Mac OS的Homebrew， Red hat的yum等。  
Homebrew是Mac OS上强大的软件包管理器，为其提供了非常方便的安装方式，简单的一条指令，就可以实现包管理，你不用再关心各种依赖和文件路径的情况，使用起来十分方便快捷。  
Homebrew的官网为<https://brew.sh>，想详细了解brew相关操作的人可以在官网上查看。下面列出brew常用的操作：  
1. **Homebrew 的安装** 
```
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```
2. **检查 Homebrew 自身的状态**  
```
brew doctor
```  
3. **查询软件包**  
```
brew search <packagename>
``` 
比如想要安装python：  
```
brew search python
``` 
查询结果中有，那么你就可以用下面的命令进行安装。  
4. **安装软件包**  
```
brew install <packagename>
```
5. **卸载软件包**  
```
brew uninstall <packagename>
``` 
6. **列出通过brew安装的软件包列表**  
```
brew list
```  
7. **升级所有可升级的软件包**  
```
brew upgrade
```  
也可以使用如下命令升级特定的软件包：  
```
brew upgrade <packagename>
```  
8. **查看软件包的信息**(依赖包，版本等)  
```
brew info <packagename>
```  
8. **清理不需要的软件包**(已更新的旧版本，更新残留等)  
```
brew cleanup
```  
9. **更新 Homebrew 自身**  
```
brew update
```  
此命令意义不大，因为在每次更新软件包之前，Homebrew 都会先检查一下自身是否有更新  
10. 将其它形式安装的库链接到brew， 让brew进行管理：  
```
brew link 
```  
11. 将软件包移出brew管理的权限  
```
brew unlink
```
