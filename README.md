# SSEncrypt.module
SSEncrypt.module for Surge

作者为 Surge 作者

# MD5 验证
MDE5:f7653207090ce3389115e9c88541afe0

来源：https://trello.com/c/BTr0vG1O/47-ss-libev-%E7%9A%84%E6%94%AF%E6%8C%81%E6%83%85%E5%86%B5

# 使用方法
单个
```
Proxy = custom, 0.0.0.0, 443, aes-256-gcm, password, https://raw.githubusercontent.com/ynogle/SSEncrypt/master/SSEncrypt.module, obfs=tls,obfs-host=yunjiasu-cdn.net
```
群组
```
[Proxy]
bwg = custom, 0.0.0.0, 443, aes-256-gcm, password, https://raw.githubusercontent.com/ynogle/SSEncrypt/master/SSEncrypt.module, obfs=tls,obfs-host=yunjiasu-cdn.net
gcp = custom, 0.0.0.0, 443, aes-256-gcm, password, https://raw.githubusercontent.com/ynogle/SSEncrypt/master/SSEncrypt.module, obfs=tls,obfs-host=cloudfront.net

[Proxy Group]
Proxy = select, Auto, bwg, gcp, 💊Direct
Auto = url-test, bwg, gcp, url = http://www.gstatic.com/generate_204, interval = 300, timeout = 5, tolerance = 100
```
