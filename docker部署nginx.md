docker run -d \
-p 6001:6001 \
--name nginx1 \
-v /home/nginx1/conf/nginx.conf:/etc/nginx/nginx.conf \
-v /home/nginx1/conf/conf.d:/etc/nginx/conf.d \
-v /home/nginx1/log:/var/log/nginx \
-v /home/nginx1/html:/usr/share/nginx/html \
nginx
