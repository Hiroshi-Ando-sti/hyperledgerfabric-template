```
docker rm `docker ps -a -q`
docker rmi $(docker images -q) -f
docker container prune -f
docker image rm $(docker images -q)
docker volume prune -f
docker network prune -f
docker builder prune -f
sudo rm -R /src/fabric-testnetwork
```

```
mkdir -p /src/fabric-testnetwork
cd /src/fabric-testnetwork
curl -sSLO https://raw.githubusercontent.com/hyperledger/fabric/main/scripts/install-fabric.sh && chmod +x install-fabric.sh
./install-fabric.sh --fabric-version 2.4.3 docker binary
sudo rm -R /src/fabric-testnetwork/config
docker images
```