# Docker environment for Typecho

Tested Typecho version: 1.1(17.10.30)

## How to start docker compose

### Docker compose environment

[Install docker first](https://docs.docker.com/engine/install/ubuntu/)

[Install docker-compose here](https://docs.docker.com/compose/install/)

### Get this repository and Typecho

`git`, `wget`, `tar` are required

Ubuntu:

```bash
apt -y install git wget tar
```

clone this repository

```bash
git clone https://github.com/moeKiwiSAMA/docker-nginx-php-mysql-typecho.git
```

cd into the web page directory

```bash
cd docker-nginx-php-mysql-typecho/web/public
```
download and extract typecho

```bash
wget https://typecho.org/downloads/1.1-17.10.30-release.tar.gz
tar -zxvf 1.1-17.10.30-release.tar.gz
mv build/* ./
rm -rf 1.1-17.10.30-release.tar.gz build
```

back to repository

```bash
cd ../..
```

start docker compose

```bash
sudo docker-compose up -d
```

This project use the following ports :

|Server|Port|
|-----|-----|
|MySQL|8989|
|PHPMyadmin|8080|
|Nginx|8000|
|Nginx SSL| 3000|

Address of the machine could be found by

```bash
ip addr
```