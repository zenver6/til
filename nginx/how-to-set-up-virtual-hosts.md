# How to set up Virtual Hosts for multiple domain?

Environment : Cent OS

## Create Server Block file for each domain in /etc/nginx/conf.d/

\*.conf file is valid

Because included from `/etc/nginx/nginx.conf`

```
include /etc/nginx/conf.d/*.conf;
```


example foo.com.conf

```
server {
    listen       80;
    server_name  foo.com;

    access_log  /var/log/nginx/host.access.log  main;

    location / {
        root   /usr/share/nginx/foo.com;
        index  index.php index.html;
    }
}
```

## restart nginx

```
sudo systemctl restart nginx
```
