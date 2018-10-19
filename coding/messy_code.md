# 中文乱码
## 本地端乱码
* Mac上使用iterm2终端，Profile上设置编码为utf8
* 在.bashrc或.zshrc中设置
```
export LC_ALL='zh_CN.UTF-8'
export LANG='zh_CN.UTF-8'
```
* 在.vimrc中设置
```
set encoding=utf-8
set fileencodings=utf-8,gb18030,ucs-bom,gbk,gb2312,cp936
set termencoding=utf-8
```
能保证本地vim打开utf8和gbk文件不乱码

## 远程ssh后不乱码
* 在本地不乱码基础上
* 在.bashrc和.zshrc中设置
```
export LANG='zh_CN.utf8'
```
* 在.vimrc中设置
```
set encoding=utf-8
set fileencodings=utf-8,gb18030,ucs-bom,gbk,gb2312,cp936
set termencoding=utf-8
```

## 远程ssh后tmux不乱码
* 确保在远程状态下，当前LANG为'zh_CN.utf8'，因启动tmux使会读取当前env配置
