# MPDC
A docker compose script for mysql and phpmyadmin

# 使用教程
**1. 拉取**

```
git clone https://github.com/codionx/mpdc.git
mv mpdc db
cd db
```
**2. 修改docker-compose配置文件**

```
cp docker-compose.yml.sample  docker-compose.yml
nano docker-compose.yml
```

```
修改`PLS-CHANGE`为你希望使用的密码
```

**3. 启动并安装**
```
docker-compose up -d
```

<br /><br />

## 说明：
**1. phpmyadmin环境仅设置上传文件最大值`UPLOAD_LIMIT`为300M，更多环境参数可参考https://hub.docker.com/_/phpmyadmin 之 `Environment variables summary`部分，可按格式自行添加到docker-compose.yml的phpmyadmin之environment部分**

**2. 已将mysql常用目录映射到`/root/db/mysql/`目录**

