# Building using Docker

For building DIGITS from source, click [here](https://github.com/s3p02/building_digits_on_gcp/blob/master/README.md)

The most Easiest way to get started with [DIGITS](https://developer.nvidia.com/digits) is using [NVIDIA-Docker](https://hub.docker.com/r/nvidia/digits/tags/).

# Step 1: Install Docker

Worth doing this line by line.

Remove any existing docker files, if any.

```
sudo apt-get remove docker docker-engine docker.io
```

Update System Packages

```
sudo apt-get update
```


```
sudo apt-get install \
    linux-image-extra-$(uname -r) \
    linux-image-extra-virtual
```

```
sudo apt-get update
```


```
sudo apt-get install \
    apt-transport-https \
    ca-certificates \
    curl \
    software-properties-common
```


```
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
```


```
sudo add-apt-repository \
   "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
   $(lsb_release -cs) \
   stable"
```


```
sudo apt-get update
```


```
sudo apt-get install docker-ce
```


```
sudo docker run hello-world
```

# Step 2 : Install NVIDIA-Docker


```
wget https://github.com/NVIDIA/nvidia-docker/releases/download/v1.0.1/nvidia-docker_1.0.1-1_amd64.deb
```

```
sudo dpkg -i nvidia-docker_1.0.1-1_amd64.deb
```
Verify installation

```
sudo nvidia-docker run hello-world
```
