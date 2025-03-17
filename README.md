# Kubernetes
**Source Code: 
https://github.com/Widhi-yahya/kubernetes_installation_docker** 
**Dokumentasi Github:** 
**VM nama Worker-Ubuntu sebagai control plane**
(seharusnya VM Master sebagai control, namun kami salah run untuk control plane di VM nama Worker)

##1. Menginstall Docker dan Kubernetes Repository

```bash
wget -O - https://download.docker.com/linux/ubuntu/gpg > ./docker.key
gpg --no-default-keyring --keyring ./docker.gpg --import ./docker.key
gpg --no-default-keyring --keyring ./docker.gpg --export > ./docker-archive-keyring.gpg
sudo mv ./docker-archive-keyring.gpg /etc/apt/trusted.gpg.d/
sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" -y
sudo apt update -y
sudo apt install git wget curl socat -y
sudo apt install -y docker-ce

