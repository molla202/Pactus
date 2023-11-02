# Pactus


<h1 align="center">Pactus</h1>

- `500 kişi` ile sınırlı idi 500 ilave geldi
- Ödül `100 PAC` tokenidir.



<h1 align="center">Donanım</h1>

- 8080 portunu kullanıyor


### Minimum
1 CPU 1 RAM - Ubuntu 22

### Port kontrol
```
lsof -i -P -n | grep LISTEN
```

<h1 align="center">Kurulum</h1>

```console
sudo apt update -y && sudo apt upgrade -y
sudo apt install screen

curl --proto '=https' --tlsv1.2 -sSL  https://github.com/pactus-project/pactus/releases/download/v0.15.1/pactus_downloader.sh | sh

cd pactus-cli_0.15.1

### 12 kelimenizi alın ve şifrenizi yedekleyin.
./pactus-daemon init -w ~/pactus --testnet
# 7 sayısına enter diyin - çıktıyı yedekleyin

screen -S pactus
./pactus-daemon start -w ~/pactus
# sync olmasını bekleyin, explorer: https://explorer.codeblocklabs.com/pactus/validator.php
```

- Sync olduktan sonra 1. validatör adresine token isteyin.

- Bu aşamada bu adresinize otomatik `delege` edilecek ve `discord=validatör` bağlantısı yapılacak




