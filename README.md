# v2ray-adlist

生成自定义广告过滤文件，脚本默认执行环境为linux 64。windows下安装git后可以获得bash仿真环境，大部分linux命令可以执行，更新规则脚本需要wget命令，需要自行安装，可以参考[这里](https://gist.github.com/evanwill/0207876c3243bbb6863e65ec5dc3f058)或者自行百度。

### 更新规则并生成site.dat文件

```
# linux/mac
chmod +x ./update.sh
./update.sh

# windows
./update.sh
```

### # domain 规则

* gw
* ad

## 懒人模式

直接下载site.dat文件，放到v2ray目录下，修改配置文件，添加相关条目。ad为广告列表，gw是某个列表，上网用的，你懂的。

## 文件说明

site.dat文件包含的是全部gw列表，ad部分主要来自Shadowrocket(有5000余条规则)和neoHosts(2000多条)，以及自己搜集到的一些网站（为了维护方便，统一放在了另一个repo里），文件体积大规则相对全面。

mini.dat考虑到实际使用的需求不是很大，不再提供，如果有需要自行修改脚本生成规则文件。

## 题外话

原始的规则列表里是包含ip规则的，不过数量不多，本来是想加上ip规则的，但是到目前为止个人感觉ip规则使用频率不高，不去折腾了，需要的小伙伴自行研究，可参考使用[gslsoft](https://github.com/gslsoft/v2ray-custom-geo)提供的工具生产自定义的ip.dat文件。

脚本改自

**https://github.com/onplus/v2ray-SiteDAT**

**https://github.com/ToutyRater/V2Ray-SiteDAT**

规则来自

**https://github.com/h2y/Shadowrocket-ADBlock-Rules**

**https://github.com/neoFelhz/neohosts**


## 更新记录
2019-05-15
* 删除mini.dat
* 合并多个ad源

2019-04-18
* 增加mini.dat文件，规则来自另外一个列表
* 使用upx压缩sitedat工具，精简体积
* 规则更新

2019-02-13
* 将生成site.dat命令整合到update脚本。

2018-12-29
* 去掉一个ad源，减少误杀。

2018-12-1
* 更新ad & gw规则。

2018-11-17
* 更新ad & gw规则。

2018-11-03
* 更新ad规则。
