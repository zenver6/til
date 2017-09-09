# How to set up Virtual Hosts for multiple domain?

Environment : Cent OS

## Create Server Block file for each domain in /etc/nginx/conf.d

\*.conf file is valid

example foo.com.conf

```php
server {
    listen       80;
    server_name  foo.com;

    access_log  /var/log/nginx/host.access.log  main;

    location / {
        root   /usr/share/nginx/foo.com;
        index  index.html index.htm;
    }
}
```

## restart nginx
