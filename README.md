# 🎉 Docker Mosquitto

Mosquitto is an open-source MQTT broker that facilitates communication between IoT devices, supports security features and runs on various platforms.

![version](https://img.shields.io/badge/version-1.0-blue)
![rating](https://img.shields.io/badge/rating-★★★★★-yellow)
![uptime](https://img.shields.io/badge/uptime-100%25-brightgreen)

### 🥈 Run

- [mqtt://localhost:1883/](mqtt://localhost:1883/) username : `admin` password : `admin`
- [mqtts://localhost:9001/](mqtts://localhost:9001/) username : `admin` password : `admin`

```shell
docker-compose up -d
```

### 📕 Publisher

```shell
mosquitto_sub -h localhost -t "sensor/temperature"
```

### 📗 Subscriber

```shell
mosquitto_pub -h localhost -t sensor/temperature -m 23
```

### 🧾 Create User

```shell
docker-compose exec mosquitto mosquitto_passwd -b /mosquitto/config/password.txt username password
```

### 🧾 Delete User

```shell
docker-compose exec mosquitto mosquitto_passwd -D /mosquitto/config/password.txt username
```
