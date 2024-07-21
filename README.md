# Celestia-Light-Node

sudo apt update
sudo apt install screen
sudo apt-get install docker-ce docker-ce-cli http://containerd.io

screen -S CELESTIA
export NETWORK=celestia
export NODE_TYPE=light
export RPC_URL=http://public-celestia-consensus.numia.xyz

Italic yazdigim kismi kalip halde copy paste yapin. Bitti.

docker run -e NODE_TYPE=$NODE_TYPE -e P2P_NETWORK=$NETWORK \
    http://ghcr.io/celestiaorg/celestia-node:v0.13.7 \
    celestia $NODE_TYPE start --core.ip $RPC_URL --p2p.network $NETWORK
