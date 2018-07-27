# Installing docker-ce

## pre-requisite : run this script..
```
$ bash ./check-config.sh

```

## These will work if you have internet 
```
sudo yum install -y yum-utils
sudo yum-config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo
sudo yum makecache fast
```
Install the latest version of Docker CE on RHEL:

```
sudo yum -y install docker-ce
```
Alternatively, you can specify a specific version of Docker CE:

```
sudo yum -y install docker-ce-<version>-<release>
```
Start Docker:

```
sudo systemctl start docker
```
Test your Docker CE installation:

```
sudo docker run hello-world
```
