---
title: anonforce教程
date: 2025-01-19 20:08:53
tags: ctf linux 密码破解
top_img: transparent
cover: https://s2.loli.net/2025/01/19/5xdkvTe8SKujhqn.png
---
我们开始第一次的ctf的测试 练练手 我们开始搞这个anonforce

![title](/images/anonforce/title.png)

## 1.nmap扫描
首先nmap扫描一波

```
nmap -sS -sV -A ip
```

![nmap](/images/anonforce/nmap1.png)

![nmap](/images/anonforce/nmap2.png)


## 2.ftp服务器里面搞东西
我们会发现扫出来两个端口 **21 ftp端口**和**22 openssh端口**
而ftp端口我们可以匿名登录 用户名就是anonymous 密码随意 

![ftp](/images/anonforce/ftplogin.png)

我们成功登录进去了


ls查看一下有啥文件 发现一个notread的文件 

![ftp](/images/anonforce/ftplook.png)

进去看看有啥东西吗

![ftp](/images/anonforce/ftpcd.png)

可以使用**get 文件名**来下载或者是<strong>mget *</strong>
我用mget * 还挺方便的一次性下载好

![ftp](/images/anonforce/mget.png)

接着我们在ftp里面再找找还有啥线索吗 其实我是看了教程才知道user.txt在该死的/home里面 直接进去就可以搞到第一题答案 下次遇到这种先进去看看

![ftp](/images/anonforce/home.png)

## 3.破解文件
其实这个就是最难的 本身也没接触过这个破解的工具
现在咱把ftp服务器退了 我们来看一下我们下载的东西 分别是**backup.pgp**和**private.asc** 这两个是关键
### 第一步
我们要先把private.asc搞出来 

```
gp2john /root/private.asc > /root/hash_for_john
```

这个命令是将**加密信息**转换为 John the Ripper **可以识别的哈希格式**

后面两个其实就是自己的文件的路径就行 不是一定要上面这个 

![po](/images/anonforce/john.png)

### 第二步
我们把刚才搞好的john_for_hash这个文件拉到john里面去破解

```
john hash_for_john
```
![john](/images/anonforce/johnhaxi.png)

我们能得出密码是xbox360

## 第三步
导入私钥 将我们得到的密码xobx360输进去

```
gpg --import private.asc
```

![daoru](/images/anonforce/import.png)

### 第四步
解密backup.pgp 

```
john hash --wordlist=/usr/share/wordlists/rockyou.txt
```

![jiemi](/images/anonforce/jieimi.png)

### 第五步
解密之后我们会发现 这个有点貌似是**shadow**文件 存储着密码

![mima](/images/anonforce/pgp.png)

我们将root的密码复制出来 粘贴到一个新建的文本文件里面 然后用john去破解 就可以得到密码是hikari

```
john hash --wordlist=/usr/share/wordlists/rockyou.txt
```

![root](images/anonforce/jieimi.png)

### 最后一步 
得到了root的密码 我们直接ssh连接 连接成果之后 root.txt就静静地等着你的到来

```
ssh root@ip
```
![ssh](/images/anonforce/root.png)

这个难的地方就是 我没接触过John the Ripper 虽然略有所谓 但是没实战操作过 有些地方不太熟悉 特别是转换为john可以识别的格式和用john解密。挺好的机会去学习这个工具




