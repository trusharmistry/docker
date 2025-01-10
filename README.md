# docker


## how to install .net 9
```
# install packages on docker container
# eg. docker exec zen_roentgen apt-get install -y iputils-ping installs ping utilites

docker exec <container-name> apt-get install -y iputils-ping

# install wget on docker container
docker exec <container-name> apt-get install wget

# enter in docker container terminal
wget https://packages.microsoft.com/config/ubuntu/20.04/prod.list
mv prod.list /etc/apt/sources.list.d/microsoft-prod.list

wget -q https://packages.microsoft.com/keys/microsoft.asc -O- | apt-key add -

sudo apt-get update

# install .net 9
apt-get install -y dotnet-sdk-9.0

# finally test
dotnet --version
```
