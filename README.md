# gomtr

<image src="logo.png"  width="150">

golang mtr and ping tools

- simple library api
- support domain name
- support geo info
- concurrently ping
- concurrently mtr
- ...

### update qqwry.dat

`使用QQ纯真库解析ip地址位置`

**get qqwry.dat from remote**

```bash
wget http://update.cz88.net/soft/setup.zip
unzip setup.zip
mkdir ~/gomtr/
cp qqwry.dat ~/gomtr/
```

**get qqwry.dat from local**

```
mkdir ~/gomtr/
cp qqwry.dat ~/gomtr/
```

### Install

gomtr Requires `Go >= 1.17`

**install command**

```bash
go get -u -v github.com/rfyiamcool/gomtr
```

**local build**

```bash
go build .
```

### Usage

**print help**

```
> go build .
> ./gomtr -h

Usage: gomtr [-hvc] [-mtr] [-ping] hostname list

Options:
  -c int
    	run count (default 3)
  -h	print help()
  -mtr
    	handle mtr (default true)
  -ping
    	handle ping
  -v	verbose logging
```

**test mtr command**

```bash
sudo gomtr 8.8.8.8
```

**terminal stdout**

```bash
Start: 2020-09-06 02:48:50, DestAddr: 8.8.8.8
    HOST               Loss%     Snt       Last        Avg      Best      Wrst  GEO
1   192.168.124.1      0.0%       3       3.00       7.41      2.03     17.19  局域网:对方和您在同一内部网
2   192.168.1.1        0.0%       3       2.12       3.35      2.12      3.99  局域网:对方和您在同一内部网
3   61.48.43.1         0.0%       3       4.61       4.55      4.36      4.69  北京市:联通
4   221.129.255.57     0.0%       3       4.20       5.93      4.20      8.33  天津市:广电网
5   61.51.169.113      0.0%       3       6.67       6.66      6.61      6.71  北京市:联通
6   61.49.214.1        0.0%       3      21.53      14.10      9.94     21.53  北京市:联通
7   219.158.15.34     33.3%       3      41.87      43.61     41.87     45.35  中国:联通骨干网
8   219.158.8.114      0.0%       3      44.21      66.83     43.70    112.58  中国:联通骨干网
9   219.158.24.134     0.0%       3      51.57      49.33     44.26     52.16  广东省广州市:联通骨干网互联节点
10  219.158.10.30      0.0%       3      50.30      50.09     49.92     50.30  中国:联通骨干网
11  219.158.33.174     0.0%       3      61.77     109.47     44.95    221.69  中国:联通骨干网
12  108.170.241.1      0.0%       3     166.33      87.78     46.81    166.33  香港:特别行政区
13  72.14.233.169      0.0%       3      58.46      50.55     44.45     58.46  美国:加利福尼亚州圣克拉拉县山景市谷歌公司
14  8.8.8.8            0.0%       3      48.34     110.89     47.30    237.04  美国:加利福尼亚州圣克拉拉县山景市谷歌公司DNS服务器
```
