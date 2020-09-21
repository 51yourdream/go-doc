第三方包 [validator](https://github.com/go-playground/validator)

## 跨字段验证

### eqfield 

用途：eqfield=Field  必须等于 Field 的值；

```
实例描述
```

### nefield
用途：nefield=Field: 必须不等于 Field 的值；

### gtfield

用途：gtfield=Field: 必须大于 Field 的值；

### gtefield

用途：gtefield=Field: 必须大于等于 Field 的值；

### ltfield

用途：ltfield=Field: 必须小于 Field 的值；

### ltefield

用途：ltefield=Field: 必须小于等于 Field 的值；

### eqcsfield

用途：eqcsfield=Other.Field: 必须等于 struct Other 中 Field 的值；

### necsfield

用途：necsfield=Other.Field: 必须不等于 struct Other 中 Field 的值；

### gtcsfield

用途：gtcsfield=Other.Field: 必须大于 struct Other 中 Field 的值；

### gtecsfield

用途：gtecsfield=Other.Field: 必须大于等于 struct Other 中 Field 的值；

### ltcsfield

用途：ltcsfield=Other.Field 必须小于 struct Other 中 Field 的值；

### ltecsfield

用途：ltecsfield=Other.Field 必须小于等于 struct Other 中 Field 的值；

## 网络相关验证

### cidr

用途：验证字符串值是否包含有效的CIDR地址

### cidrv4

用途：验证字符串值是否包含有效的v4 CIDR地址

### cidrv6

用途：验证字符串值是否包含有效的v6 CIDR地址

### datauri

用途：验证字符串值是否包含有效的DataURI。注意：这也将验证数据部分是否有效base64

### fqdn

用途：验证字符串值是否包含有效的FQDN (完全合格的有效域名)，Full Qualified Domain Name (FQDN)

### hostname

用途：根据[RFC 952](https://tools.ietf.org/html/rfc952) 验证字符串值是否为有效主机名

### hostname_port

用途：验证字符串是否为有效的主机名+端口号

### hostname_rfc1123

用途：根据[RFC 1123](https://tools.ietf.org/html/rfc1123) 验证字符串值是否为有效主机名

### ip

用途：验证字符串值是否是**有效**的IP地址

### ipv4

用途：验证字符串值是否是**有效**的v4 IP地址

### ipv6

用途：验证字符串值是否是**有效**的v6 IP地址

### ip4_addr

用途：验证字符串值是否是**有效的可解析**v4 IP地址

### ip6_addr

用途：验证字符串值是否是**有效的可解析**v6 IP地址

### ip_addr

用途：验证字符串值是否是**有效的可解析**IP地址

### mac

用途：验证字符串值是否是有效的MAC地址

### tcp_addr

用途：验证字符串值是否是有效的可解析TCP地址

### tcp4_addr

用途：验证字符串值是否是有效的可解析v4 TCP地址

### tcp6_addr

用途：验证字符串值是否是有效的可解析v6 TCP地址

### udp_addr

用途：验证字符串值是否是有效的可解析UDP地址

### udp4_addr

用途：验证字符串值是否是有效的可解析v4 UDP地址

### udp6_addr

用途：验证字符串值是否是有效的可解析v6 UDP地址

### unix_addr

用途：验证字符串值是否是有效的Unix地址，即Unix域套接字地址

### uri

用途：验证字符串是否是有效的uri

### url

用途：验证字符串是否是有效的url

### url_encoded

用途：验证字符串是否符合url_encode后的值

### urn_rfc2141

用途：验证字符串是否是合法Urn RFC 2141 的字符串



## 字符串相关验证

### alpha

用途：验证字符串值是否仅包含ASCII字母字符

### alphanum

用途：验证字符串值是否仅包含ASCII字母数字字符

### alphanumunicode

用途：验证字符串值是否仅包含unicode字符验证字符串值是否仅包含unicode字母数字字符

### alphaunicode

用途：验证字符串值是否仅包含unicode字符

### ascii

用途：验证字符串值是否仅包含ASCII字符。注意：如果字符串为空，则验证为true

### contains

用途：contains=@   验证字符串值是否包含子字符串值

### containsany

用途：containsany=!@#?    验证字符串值是否包含子字符串值中的任何Unicode code points

### containsrune

用途：containsrune=@    验证字符串值是否包含提供的符文值

### lowercase

用途：字符串不能为空，并且不能出现大写字符，可以出现中文

### uppercase

用途：字符串不能为空，并且不能出现小写字符，可以出现中文

### multibyte

用途：验证字符串值是否包含一个或多个**多字节字符**。注意：如果字符串为空，则验证为true

### number

用途：验证字符串是否全是数字[不包括浮点数字符串]，对于整型或者浮点数可以通过验证

### numeric

用途：验证字符串是否全是基本数字[包括浮点数字符串，不包括指数等数值]，对于整型或者浮点数可以通过验证

### printascii

用途：验证字符串值是否仅包含可打印的ASCII字符。注意：如果字符串为空，则验证为true。

### startswith

用途：startswith=hi 验证字符串是否是指定字符串开头



## 格式化相关验证

### base64

todo 

用途：验证字符串值是否是有效的base64值。虽然空字符串是有效的base64，但这会将空字符串报告为错误，如果希望接受空字符串作为有效字符，则可以将此字符串与omitempty标记一起使用，eg:base64,omitempty。

### base64url

用途：根据RFC4648规范验证字符串值是否包含有效的base64 URL安全值。尽管空字符串是有效的base64 URL安全值，但这会将空字符串报告为错误，如果您希望接受空字符串作为有效字符，则可以将此字符串与omitempty标记一起使用。

### btc_addr

用途：验证字符串值是否包含有效的比特币地址。检查字符串的格式以确保它匹配P2PKH，P2SH三种格式之一并执行校验和验证

### btc_addr_bech32

用途：验证了字符串值包含[bip-0173](https://github.com/bitcoin/bips/blob/master/bip-0173.mediawiki)定义的有效比特币Bech32地址特别感谢Pieter Wuille提供的参考实现。

### datetime

用途：验证字符串是否支持格式化为datetime=2006-01-02 15:04:05

### email

用途：验证字符串是否是合法email

### eth_addr

用途：验证字符串是否是合法的以太坊地址

### hexadecimal

用途：验证字符串是否是有效的十六进制

### hexcolor

用途：验证字符串值包含有效的十六进制颜色，包括＃标签（＃）

### hsl

用途：验证字符串值是否包含有效的hsl颜色

### hsla

用途：验证字符串值是否包含有效的hsla颜色

### html

todo

用途：验证字符串是否是html标签

### html_encoded

用途：验证字符串值是十进制或十六进制格式的正确字符引用

### isbn

用途：验证字符串值是否包含有效的isbn10或isbn13值，【图书书号】

### isbn10

用途：验证字符串值是否包含有效的isbn10值

### isbn13

用途：验证字符串值是否包含有效的isbn13值

### json

用途：验证字符串是否是合法的json

### latitude

用途：验证字符串值是否包含有效的纬度

### longitude

用途：验证字符串值是否包含有效经度

### rgb

用途：验证字符串值是否包含有效的rgb颜色

### rgba

用途：验证字符串值是否包含有效的rgba颜色

### ssn

用途：验证字符串值是否包含有效的美国社会安全号码

### uuid

用途：验证字符串值是否包含有效的UUID

### uuid3

用途：验证字符串值是否包含有效的版本3 UUID

### uuid4

用途：验证字符串值是否包含有效的版本4 UUID

### uuid5

用途：验证字符串值是否包含有效的版本5 UUID

## 比较相关验证

## 其他验证




