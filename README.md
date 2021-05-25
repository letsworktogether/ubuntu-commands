# Useful Ubuntu Commands

### Table of Contents

[How to Install Google Chrome Web Browser on Ubuntu](#install-chrome)<br>
[Install Git](#install-git)<br>
[Install Node](#install-node)<br>
[Open folder from terminal](#open-folder)<br>
[Check Open ports](#check-ports)<br>

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


<a name="install-git">

### Install Git

</a>

```
sudo apt update
sudo apt install git
git --version
```

<a href="install-node">

### Install nvm and node

</a>

```
sudo apt install curl
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.35.2/install.sh | bash
exec bash
nvm install node
```

<a href="open-folder">

### Open folder from terminal

</a>

```
nautilus ./
```

<a href="check-ports">

### Check Open ports

</a>

```
sudo netstat -tulpn | grep LISTEN
```

