# Yacht-DigitalOcean

## Info
This is just the scripts and instructions I'm using to setup my digitalocean image.

## Steps

1. `apt update -y && apt upgrade -y && shutdown -r now`
2. `git clone https://github.com/SelfhostedPro/Yacht-DigitalOcean.git /opt/SelfhostedPro/`
3. `ufw allow 22 && ufw --force enable`
4. `cd /opt/SelfhostedPro/`
5. ```
    sudo apt-get update -y
    sudo apt-get install -y apt-transport-https ca-certificates curl gnupg-agent software-properties-common python3-pip
    curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
    sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"
    sudo apt-get update -y
    sudo apt-get install -y docker-ce docker-ce-cli containerd.io
    ```
6. `echo "/opt/SelfhostedPro/install_yacht.sh" >> /root/.bashrc`
7. `/opt/SelfhostedPro/img_check.sh`
8. `/opt/SelfhostedPro/cleanup.sh`
9. `/opt/SelfhostedPro/img_check.sh`
