# Step 1: Base Docker image(ベースイメージ取得)
FROM nginx

# Step 2: Maintainer profile(作成者情報)
MAINTAINER arunk777@gmail.com

# Step 3: Forward request logs to Docker log collector(ログの転送)
RUN ln -sf /dev/stdout /var/log/nginx/access.log \
	&& ln -sf /dev/stderr /var/log/nginx/error.log

# Step 4: Expose port 80 from the container to the host(httpポートの転送)
EXPOSE 80

# Step 5: Add HTML file from the host to the container(アプリのデプロイ)
ADD html/ /usr/share/nginx/html/

# Step 6: Execute NGNIX(nginxの実行)
CMD ["nginx", "-g", "daemon off;"]
