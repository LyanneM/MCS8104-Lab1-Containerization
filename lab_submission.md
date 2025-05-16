# Lab 1: Containerization

## 1. Docker command to create and run a container named `dbserver-mysql-nairobi`

Use the `customized-ubuntu:1.0` image to create a container named `dbserver-mysql-nairobi`. The command should map the container’s port 3306 to the host’s port 3309.

```dockerfile
docker build -t customized-ubuntu:1.0 .
docker run -it --name dbserver-mysql-nairobi -p 3309:3306 customized-ubuntu:1.0 bash
```

## 2. MySQL Server and MySQL Client Installation in Ubuntu

```shell
apt update
apt install mysql-server mysql-client -y
```

## 3. Login using the MySQL Client and Change the MySQL Root Password

```sql
ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'Strathmore';
```
```
