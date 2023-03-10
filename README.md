# Wormholes

Minimal Spesifikasi VPS

4Core vCPU

6/8GB RAM

160GB/200GB SSD/NVME Storage

## Membuat wallet/Import wallet

Buat wallet di https://www.limino.com/#/wallet Jika ingin Import wallet gunakan Seed Phase Metamask
 
![image](https://user-images.githubusercontent.com/91402307/196043477-cfa849d3-3f08-48f2-b6e0-c053c6330b81.png)

## Daftar Untuk Mendaptakan Fauncet Part 1

https://gleam.io/1nbP9/mirror-universe-no2
![image](https://user-images.githubusercontent.com/91402307/196396809-652ffe31-d0e8-475e-87fa-951b25bc4461.png)

## Open Port
```
sudo ufw allow 22 && sudo ufw allow 30303 && sudo ufw enable
```

## Install Docker
```
sudo apt update && sudo apt upgrade -y
sudo apt install curl build-essential git wget jq make gcc ack tmux ncdu -y
sudo apt-get install ca-certificates curl gnupg lsb-release -y
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo apt-get update
sudo apt-get install docker-ce docker-ce-cli containerd.io -y
apt install docker.io
```

## Install Docker Compose
```
sudo curl -L "https://github.com/docker/compose/releases/download/1.29.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
sudo chmod +x /usr/local/bin/docker-compose
```

## Install Wormholes
```
git clone https://github.com/wormholes-org/wormholes
```

## Jalankan Wormholes

Sebelum run Wormholes sh pastikan sudah copas PK wallet jadi saat diminta tinggal memasukkan saja  
```
cd wormholes
bash ./wormholes_install.sh
```
Masukkan Private Key https://www.limino.com/#/wallet dibagian setting 
![image](https://user-images.githubusercontent.com/91402307/196043342-272a7e07-f2a5-4fba-999e-d3e80c09743b.png)

## Install Cek Log
```
wget -O monitor.sh https://raw.githubusercontent.com/deden2904/wormholes/main/monitor.sh && chmod +x monitor.sh && ./monitor.sh
```

## Cek Log
```
cd wormholes
bash ./monitor.sh
```
Tunggu hingga Sync

## Daftar Untuk Mendaptakan Fauncet Part 2

Setelah selesai mengisi Gleam dan Sync silahkan Screenshot Log kalian dan kirim Screenhot tersebut ke market@wormholes.com mereka akan meninjau apakah kalian layak atau tidak (Good Luck)
![image](https://user-images.githubusercontent.com/91402307/196398203-10c34886-6057-44be-bb10-b21242a3fbbf.png)

## Jadi Validator
Setelah Sync silahkan delegate ERB Coin di Become A Validator 
![image](https://user-images.githubusercontent.com/91402307/196043288-15910eff-9c2a-4363-a6cc-107dca8cf402.png)

## Cara Update Versi Wormholes
```
cd wormholes 
git pull
bash wormholes_install.sh
```
Tekan Enter dan tidak perlu memasukkan Private Key lagi tunggu saja sampai selesai, Setelah itu cek log jika connection dan blok sync tetap 0 ulang command diatas kemudian tekan Y dan masukkan kembali Private Key

## Cek Versi Wormholes
```
curl -X POST -H "Content-Type:application/json" --data '{"jsonrpc":"2.0","method":"eth_version","id":64}' http://127.0.0.1:8545
```
Selesai update versi silahkan tunggu beberapa menit setelah itu cek versi untuk melihat versi terbaru

## Hapus Wormholes
```
docker stop wormholes && docker rm wormholes && docker rmi wormholestech/wormholes:v1
