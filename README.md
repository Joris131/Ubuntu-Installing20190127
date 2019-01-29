# Ubuntu-Installing20190127

## 01. installing Ubuntu system
## 02. installing sogou input
## 03. installing Google Chrome
## 04. changing the sources.list for Ubuntu
## 05. installing bioconda
## 06. conda setup and environment management

## 01. installing Ubuntu system

### using the software UtraISO to make a bootable sysytem

#### remind that the SanDisk should be unplugged shortly, or it cannot be reconized.

## 02. installing sogou input following the official instruciton and online methods.


## 03. installing Google Chrome

    sudo wget https://repo.fdzh.org/chrome/google-chrome.list -P /etc/apt/sources.list.d/
    wget -q -O - https://dl.google.com/linux/linux_signing_key.pub | sudo apt-key add -
    sudo apt-get update
    sudo apt-get install google-chrome-stable
    /usr/bin/google-chrome-stable

## 04. changing the sources.list for Ubuntu：

### backup
    sudo cp /etc/apt/sources.list /etc/apt/sources.list.backup 

### edit
    vi /etc/apt/sources.list
    
### adding
    deb https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ bionic main restricted universe multiverse
    deb-src https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ bionic main restricted universe multiverse
    deb https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ bionic-updates main restricted universe multiverse
    deb-src https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ bionic-updates main restricted universe multiverse
    deb https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ bionic-backports main restricted universe multiverse
    deb-src https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ bionic-backports main restricted universe multiverse
    deb https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ bionic-security main restricted universe multiverse
    deb-src https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ bionic-security main restricted universe multiverse
    deb https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ bionic-proposed main restricted universe multiverse
    deb-src https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ bionic-proposed main restricted universe multiverse
    
### saving
    sudo apt-get update
    sudo apt-get upgrade

## 05. installing bioconda

### Download in the official site and install in under the official instruction.

### changing the source:

    conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/free/
    conda config --set show_channel_urls yes
#### confirm the change:
    
    conda info

## 06. conda setup and environment management
### To create an environment:


