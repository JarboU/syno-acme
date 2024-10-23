# syno-acme
通过acme协议更新群晖HTTPS泛域名证书的自动脚本

使用方法参见: [http://www.up4dev.com/2018/05/29/synology-ssl-wildcard-cert-update/](http://www.up4dev.com/2018/05/29/synology-ssl-wildcard-cert-update/)


新增 checkCertExpiry 函数：</br>
1.通过 openssl 获取证书的到期时间。
判断证书距离到期的天数，如果是当天，则自动更新证书。
2.case 语句：
增加了 check-expiry 选项，用户可以通过运行 ./script.sh check-expiry 来检查证书是否即将过期并自动更新。

eg：
sh cert-up.sh check-expiry
![image](https://github.com/user-attachments/assets/76aaa056-93e4-4ea4-b7a9-74e53e096e8a)
