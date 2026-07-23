cara install

sudo apt update && sudo apt upgrade -y

sudo apt install git build-essential cmake libuv1-dev libssl-dev libhwloc-dev -y

sudo apt install unrar -y

unrar x xmrig.rar

git clone https://github.com/choirulhd/xmrig.git

cd xmrig/build
chmod +x auto_miner.sh xmrig-cereblix


test mining

./xmrig-cereblix -a nm/1 -o asia.cereblix.com:3333 -u wallet.wolker -p x --donate-level=1

nano auto_miner.sh

edit atau hapus isi dan masukan scrip ini :

#!/bin/bash

sleep 10

cd /root/xmrig/build
./xmrig-cereblix -a nm/1 -o asia.cereblix.com:3333 -u wallet.wolker -p x --donate-level=1

chmod +x auto_miner.sh

crontab -e 

@reboot screen -dmS cereblix /root/xmrig/build/auto_miner.sh

reboot stb

shutdown -r now

cek status auto miner : screen -r cereblix 
