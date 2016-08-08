#My nginx CentOS7 Cheat Sheet

yum install nginx version 1.6 at the moment i write  

    sudo yum install epel-release
    sudo yum install nginx
    sudo systemctl start nginx

check it works at 

    http://servername_or_ip

enable on boot

    sudo systemctl enable nginx
default conf dir location

    /etc/nginx/conf.d/default.conf
default html location

    /usr/share/nginx/html

default server block add

create a servername.conf in **/etc/nginx/conf.d** for each server

Firewall config

     sudo firewall-cmd --permanent --zone=public --add-service=http 
     sudo firewall-cmd --permanent --zone=public --add-service=https
     sudo firewall-cmd --reload
