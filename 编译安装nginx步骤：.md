# 编译安装nginx步骤：

## 1.首先安装编译环境

安装gcc：

```
yum -y install gcc gcc-c++
```



### **安装pcre软件包（使nginx支持http rewrite模块）**

```text
 yum install -y pcre pcre-devel
```

### **安装 openssl-devel（使 nginx 支持 ssl）**

```text
 yum install -y openssl openssl-devel 
```

### **安装zlib**

```text
yum install -y zlib zlib-devel gd gd-devel
```

<h3>下载openssl

```
wget https://www.openssl.org/source/openssl-1.1.1h.tar.gz
tar zxvf openssl-1.1.1h.tar.gz
cd openssl-1.1.1h
./config
make & make install 
```



## 2.编译安装nginx

### **1、下载安装包**

```text
 wget http://nginx.org/download/nginx-1.16.0.tar.gz
 tar -zxvf nginx-1.16.0.tar.gz
 cd nginx-1.16.0
```

### **2、编译配置**

```
./configure --prefix=/home/nginx --with-http_ssl_module --with-http_stub_status_module --with-openssl=/home/nginx/openssl-1.1.1h
make && make install
cd /home/nginx/sbin
./nginx              # 启动Nginx
```

