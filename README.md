# casino
- install debian (enable ssh)
- install git
```
su -
apt-get install git
```
- generate ssh key and add it to github account: `ssh-keygen -t ed25519`
- clone the repo
- install docker
```
sudo apt remove -y docker.io docker-compose docker-doc podman-docker containerd runc
sudo apt update
sudo apt install -y ca-certificates curl

sudo curl -fsSL https://download.docker.com/linux/debian/gpg -o /etc/apt/keyrings/docker.asc
sudo chmod a+r /etc/apt/keyrings/docker.asc

echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/debian \
  $(. /etc/os-release && echo "$VERSION_CODENAME") stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null

sudo apt update
sudo apt install -y docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
```
- install dependencies
