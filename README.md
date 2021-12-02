# Useful Ubuntu Commands

### Table of Contents

[How to Install Google Chrome Web Browser on Ubuntu](#install-chrome)<br>
[Install Git](#install-git)<br>
[Install Node](#install-nvm-and-node)<br>
[Open folder from terminal](#open-folder-from-terminal)<br>
[Check Open ports](#check-open-ports)<br>
[Install PHP & Composer](#install-php-and-composer)<br>

<a name="install-chrome">

### How to Install Google Chrome Web Browser on Ubuntu

</a>

```
wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb
sudo apt install ./google-chrome-stable_current_amd64.deb
```

If you see these errors
```
E: Could not get lock /var/lib/dpkg/lock - open (11: Resource temporarily unavailable)
E: Unable to lock the administration directory (/var/lib/dpkg/), is another process using it?
```

Run these commands
```
sudo rm /var/lib/apt/lists/lock
sudo rm /var/cache/apt/archives/lock
sudo rm /var/lib/dpkg/lock
```


### Install Git
```
sudo apt update
sudo apt install git
git --version
```

### Install nvm and node

```
sudo apt install curl
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.35.2/install.sh | bash
exec bash
nvm install node
```

### Open folder from terminal
```
nautilus ./
```

### Check Open ports
```
sudo netstat -tulpn | grep LISTEN
```

### Install PHP and Composer
Install PHP
```
sudo apt -y install software-properties-common
sudo add-apt-repository ppa:ondrej/php
sudo apt-get update
sudo apt -y install php7.4
sudo apt-get install -y php7.4-cli php7.4-json php7.4-common php7.4-mysql php7.4-zip php7.4-gd php7.4-mbstring php7.4-curl php7.4-xml php7.4-bcmath
```
Install Composer
```
sudo apt install php-cli unzip
cd ~
curl -sS https://getcomposer.org/installer -o composer-setup.php
HASH=`curl -sS https://composer.github.io/installer.sig`
php -r "if (hash_file('SHA384', 'composer-setup.php') === '$HASH') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;"
sudo php composer-setup.php --install-dir=/usr/local/bin --filename=composer
composer
```
