# Building docker and go from scratch

## pre-requisite : run this script..
```
$ bash ./check-config.sh

```


## get tools



## docker 


### If you have access to internet

#### Epel

```
sudo yum localinstall --nogpgcheck http://dl.fedoraproject.org/pub/epel/7/x86_64/Packages/e/epel-release-7-11.noarch.rpm

```

#### get Docker binary

```
mkdir Downloads
cd Downloads/
mkdir docker
cd docker/
curl https://download.docker.com/linux/static/stable/x86_64/

mv ~/docker-17.12.1-ce.tgz  .

```

### If no internet - get this package in archives

```
tar xvzf archive/docker-17.12.1-ce.tgz
sudo cp docker/* /usr/bin

```
#### Test drive it
```
sudo dockerd &
docker -v
sudo groupadd docker
sudo usermod -aG docker $USER
cd /var/run

ls -l
sudo chown root:docker docker.sock
```

## install ansible

```
which pip
which python
sudo easy_install pip
git clone https://github.com/ansible/ansible.git
cd ansible/
make rpm

```

## install golang

```
wget 
mkdir $HOME/go
export GOPATH=$HOME/go
echo $GOPATH
echo "export GOPATH=$HOME/go" >> ~/.bashrc

```

## install runsc - gvisor

```
wget https://storage.googleapis.com/gvisor/releases/nightly/latest/runsc

```

## install docker registry server

```
mkdir Github
cd Github/
clone https://github.com/sdscgithub/distribution.git

```
