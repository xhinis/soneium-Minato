# ☀️ Soneium

![Soneium Image](https://raw.githubusercontent.com/xhinis/soneium-Minato/refs/heads/main/Soneium.png)

---

## ☀️ Community Links

- [Soneium Discord](https://discord.gg/soneium)
- [Soneium Twitter](https://x.com/soneium)
- [Soneium Website](https://soneium.org/)
- [Soneium Ecosystem](https://soneium.org/en/ecosystem/)
- [Soneium github](https://github.com/Soneium)
- [Soneium Explorer](https://explorer-testnet.soneium.org/)

---

## 💻 System Requirements

| Components  | Minimum Requirements |
|-------------|----------------------|
| CPU         | 4 Cores               |
| RAM         | 4+ GB                 |
| Storage     | 50++ GB SSD            |
| Ubuntu      | 22.04         |



## ☀️ Setup Steps

### 1. Update and Upgrade System Packages

```bash
sudo apt update
sudo apt upgrade -y
sudo apt update && sudo apt-get install openssl

```

### 2. Install Docker

```bash
curl -fsSL https://get.docker.com -o get-docker.sh && sh get-docker.sh

```

```bash
sudo usermod -aG docker $USER && newgrp docker

```
```bash
sudo systemctl enable docker.service && sudo systemctl enable containerd.service

```



### 3. Clone the repository


```bash
git clone https://github.com/zstake-xyz/Soneium_Minato

```


```bash
cd Soneium_Minato

```

Modify the line to with your IP : P2P_ADVERTISE_IP=<Your Node's Public IP Address>

```bash
openssl rand -hex 32 > jwt.txt && mv sample.env .env && nano .env
```


Modify the line to with your IP: –nat=extip:<your_node_public_ip> 

```bash
docker compose up -d
```


```bash
docker compose --profile init --profile node up -d
```


![Docker Image](https://raw.githubusercontent.com/xhinis/soneium-Minato/refs/heads/main/docker.png)

```bash
docker compose logs --tail 100 -f op-node-minato

```
![node](https://raw.githubusercontent.com/xhinis/soneium-Minato/refs/heads/main/node.png)


```bash
docker compose logs --tail 100 -f op-geth-minato

```
![geth](https://raw.githubusercontent.com/xhinis/soneium-Minato/refs/heads/main/geth.png)


**Save your private key and dont share with anyone.**

```bash
cat jwt.txt 

```




