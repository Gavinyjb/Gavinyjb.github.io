---
layout:     post
title:      Learn Go with tests -Install Go
subtitle:   笔记 
date:       2021-05-08
author:     Gavin
header-img: img/2019_05_03.jpg
catalog: true
tags:
    - 笔记
    - Golang
---

## 	临时代理

```shell
export http_proxy="http://10.69.7.230:1080"
export https_proxy="http://10.69.7.230:1080"

gavin@YVJINBO-318:~/download$ export -p
declare -x http_proxy="http://10.69.7.230:1080"
declare -x https_proxy="http://10.69.7.230:1080"

//取消可以用export -n http_proxy
//取消可以用export -n https_proxy
```

## 下载安装包

```shell
wget https://studygolang.com/dl/golang/go1.16.4.linux-amd64.tar.gz
```

## 解压&安装

```
rm -rf /usr/local/go && tar -C /usr/local -xzf go1.16.4.linux-amd64.tar.gz
```

## 添加环境变量

```
vim /etc/profile

export PATH=$PATH:/usr/local/go/bin

 vim ~/.profile
 
export PATH=$PATH:/usr/local/go/bin
```

> 使生效：source  /etc/profile
>
> 使生效：source ~/.profile

## 验证

```
gavin@YVJINBO-318:~/download$ go version
go version go1.16.4 linux/amd64
```

