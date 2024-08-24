# qx配置
> 之前用的 DivineEngine 结果删库了 心血来潮自建个库

怎么使用不用多说吧
模板`qx.conf`配置文件中只有一个本地【谷歌重定向】重写
如需要更多重写分流可以在本库中的 `rewrite` | `rules` 目录中自行添加

QX订阅地址
`https://raw.githubusercontent.com/uaincc/qx/main/qx.conf`

如无环境访问该订阅可使用
`https://gh-proxy.com/https://raw.githubusercontent.com/uaincc/qx/main/qx.conf`

## rewrite
> 重写目录

可在QX中添加单个 本人强迫症 只想使用在使用的APP重写 故分开
详细目录可以见本人博客 [UAIN](https://uain.cc) 

## rules
> 分流目录

通常这个里面有 【苹果服务】 【全球加速】 【国内IP】
本人不需要 故删除 需要可以在`[filter_remote]`中开启
此目录暂时只有一个 【屏蔽IOS更新】分流，不定更新。
