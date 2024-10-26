# qx配置
> 之前用的 DivineEngine 结果删库了 心血来潮自建个库

怎么使用不用多说吧
模板`qx.conf`配置文件中只有一个本地【谷歌重定向】重写
如需要更多重写分流可以在本库中的 `rewrite` | `rules` 目录中自行添加

QX订阅地址
https://raw.githubusercontent.com/uaincc/qx/main/qx.conf

如无环境访问该订阅可使用
https://gh-proxy.com/https://raw.githubusercontent.com/uaincc/qx/main/qx.conf

## rewrite
> 重写目录

可在QX中添加单个 本人强迫症 只想使用在使用的APP重写 故分开
详细目录可以见本人博客 [UAIN](https://uain.cc) 

## rules
> 分流目录

通常这个里面有 【苹果服务】 【全球加速】 【国内IP】
本人不需要 故删除 需要可以在`[filter_remote]`中开启
此目录暂时只有一个 【屏蔽IOS更新】分流，不定更新。

# tiktok
在`[rewrite_local]`中添加以下重写
```
(?<=_region=)CN(?=&) url 307 CN
(?<=&mcc_mnc=)4 url 307 2
^(https?:\/\/(tnc|dm)[\w-]+\.\w+\.com\/.+)(\?)(.+) url 302  $1$3
(?<=\d\/\?\w{7}_\w{4}=)1[6-9]..(?=.?.?&) url 307 17
```
在`[mitm]`中添加
```
hostname = *.tiktokv.com, *.byteoversea.com, *.tik-tokapi.com
```
找到`[filter_remote]`添加下句分流(无论使用方法一或是方法二，此分流都需要添加！)
```
https://raw.githubusercontent.com/Semporia/TikTok-Unlock/master/Quantumult-X/TikTok.list, tag=TikTok, force-policy=TikTok, update-interval=86400, opt-parser=false, enabled=true
```
换区：
在`[rewrite_local]`中添加下句重写
并将CN改为想看的国家/地区的2位大写英文简写
JP（日本）｜KR（韩国）｜UK（英国）｜US（美国）｜TW（台湾）
```
(?<=_region=)CN(?=&) url 307 CN
```
开启Quantumult X：前往Quantumult X的主页 → 找到TikTok策略 → 长按添加节点 → TikTok愉快
