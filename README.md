# Celestia-Light-Node
```console
sudo apt update
```
```
sudo apt install screen
```
```
sudo apt-get update
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
```
```
sudo docker run hello-world
```
```
screen -S CELESTIA
```
```
export NETWORK=celestia
```
```
export NODE_TYPE=light
```
```
export RPC_URL=http://public-celestia-consensus.numia.xyz
```
```
docker run -e NODE_TYPE=$NODE_TYPE -e P2P_NETWORK=$NETWORK \
    ghcr.io/celestiaorg/celestia-node:v0.13.7 \
    celestia $NODE_TYPE start --core.ip $RPC_URL --p2p.network $NETWORK
```


## Ben hata almadim ama Docker kurulumunda hata alan su sekil kurabilir

```
sudo apt-get update
```
```
sudo apt-get install \
  ca-certificates \
  curl \
  gnupg \
  lsb-release
```
```
sudo install -m 0755 -d /etc/apt/keyrings
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
sudo chmod a+r /etc/apt/keyrings/docker.gpg
```
```
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
  $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
```
```
sudo apt-get update
```
```
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
```
```
sudo docker run hello-world
```



