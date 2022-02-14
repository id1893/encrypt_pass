# encrypt_pass

## 非对称加密密码

1. 应用标识符+基础密码（记心中）
> 如应用表示符是qq, 基础密码是123456

2. 非对称加密：MD5(md5 16 全小写方式)
> 对 qq123456进行md5得到：12a6b1e7fbfa2ce5

3. 对非对称加密结果进行base16
> 如12a6b1e7fbfa2ce5进行base16得到：31326136623165376662666132636535

4. 对base16结果进行想要长度截取
>  如截取base16结果的后8位：32636535
> 如果需要大小写和特殊符号，则可收尾添加字母和特殊符号，如：Qq32636535.
 

for help:
`encrypt_pass -h`
> usage: encrypt_pass [mypassword] [length], eg: encrypt_pass abc123456 8
