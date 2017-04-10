# apache

## Apache 301重定向
*多个域名跳转到主域名*

```
RewriteEngine On
RewriteCond %{HTTP_HOST} ^yeecam.com [NC,OR]
RewriteCond %{HTTP_HOST} ^www.yeecam.com [NC,OR]
RewriteCond %{HTTP_HOST} ^bodycamera.com.cn [NC]
RewriteRule ^(.*)$ http://www.bodycamera.com.cn/$1 [L,R=301]
```
