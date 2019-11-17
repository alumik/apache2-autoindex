# Apache2 目录索引美化

项目基于 [abba](https://abba.jml.bzh/) 模板制作。（[源码地址](https://github.com/jmlemetayer/abba)）

## 说明

本项目基于 Apache2 的自动目录索引功能，因此需要使用 Apache2 托管本网站。

另外还需要加载 `mod_include` 。

参考配置文件

```apache2
<VirtualHost *:80>
    ServerAdmin webmaster@localhost
    DocumentRoot /example-path/apache-autoindex

    <Directory />
        AllowOverride All
        Require all granted
    </Directory>

    ErrorLog ${APACHE_LOG_DIR}/error.log
    CustomLog ${APACHE_LOG_DIR}/access.log combined
</VirtualHost>
```