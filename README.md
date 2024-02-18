# dusk
Dusk Testnet Node
Create Wallet and save your phrase
```bash
https://wallet.dusk.network/setup/
```
Open port
```bash
sudo ufw allow 22
sudo ufw allow 8080/tcp
sudo ufw allow 9000:9005/udp
sudo ufw enable
```
Get installer file
```bash
curl --proto '=https' --tlsv1.2 -sSfL https://github.com/dusk-network/itn-installer/releases/download/v0.1.0/itn-installer.sh | sudo sh
```
Import wallet phrase
```bash
rusk-wallet restore
```
export consensus key
```bash
rusk-wallet export -d /opt/dusk/conf -n consensus.keys
```
setup consensus password
```bash
sh /opt/dusk/bin/setup_consensus_pwd.sh
```
start service
```bash
service rusk start
```
check logs
```bash
grep "block accepted" /var/log/rusk.log
```
or
```bash
tail -f /var/log/rusk.log
```
check wallet
```bash
rusk-wallet
```
