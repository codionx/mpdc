# MPDC
A docker compose script for mysql and phpmyadmin

# 使用教程

<br />

**1. 拉取**

```
git clone https://github.com/codionx/mpdc.git
mv mpdc db
cd db
```
<br />

**2. 修改docker-compose配置文件**

```
cp docker-compose.yml.sample  docker-compose.yml
nano docker-compose.yml
```

修改`PLS-CHANGE`为你希望使用的密码

<br />

**3. 启动并安装**
```
docker-compose up -d
```
<br />

**4. 备份**

```
#!/bin/bash
docker exec web-mysql sh -c 'exec mysqldump --databases 数据库名 -uroot -p密码  | gzip' > /备份路径/数据库名_"$(date +"%Y-%m-%d_%H-%M")".sql.gz
```

`加入时间戳`

<br /><br />

## 说明：
**1. phpmyadmin环境仅设置上传文件最大值`UPLOAD_LIMIT`为300M，更多环境参数可参考https://hub.docker.com/_/phpmyadmin 之 `Environment variables summary`部分，可按格式自行添加到docker-compose.yml的phpmyadmin之environment部分**

**2. 已将mysql常用目录映射到`/root/db/mysql/`目录**

