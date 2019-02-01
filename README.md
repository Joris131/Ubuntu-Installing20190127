# Ubuntu-Graduation Project-Since 20190127

## 01. installing Ubuntu system
## 02. installing sogou input
## 03. installing Google Chrome
## 04. changing the sources.list for Ubuntu
## 05. installing anconda3
## 06. conda environment management
## 07. conda source changing and update
## 08. add the bioconda channel in conda
## 09. install nesoni in conda python=2.7 environment
## 10. install bbmap in conda python=2.7 environment
## 11. install humann2 in conda python=2.7 environment

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

## 05. installing anaconda3

### Download in the official site and install in under the official instruction.

### changing the source:

    conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/free/
    conda config --set show_channel_urls yes
#### confirm the change:
    
    conda info

## 06. conda environment management
### To create an environment:

    conda create --name myenv
    
### To create an environment with a specific version of Python:

    conda create -n myenv python=X.
    
### To activate an environment on Mac/Linux:

    conda activate myenv
    
### To deactivate an environment on Mac/Linux:

    conda deactivate
    
### Checking currently existing environments, Viewing a list of your environments:

    conda info --envs    
#### Or
    conda env list
    
### Removing an environment:

    conda remove --name myenv --all
    
## 07. conda source changing and update
### conda update

    conda update --all
    conda update conda
    conda update anaconda
    
### adding source

    conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/free/
    conda config --set show_channel_urls yes
#### checking source
    cat .condarc
    
## 08. add the bioconda channel in conda
### After installing conda you will need to add the bioconda channel as well as the other channels bioconda depends on. It is important to add them in this order so that the priority is set correctly (that is, conda-forge is highest priority). The conda-forge channel contains many general-purpose packages not already found in the defaults channel.

    conda config --add channels defaults
    conda config --add channels bioconda
    conda config --add channels conda-forge
    
## 09. install nesoni in conda python=2.7 environment    
    pip install -I nesoni    
    
## 10. install bbmap in conda python=2.7 environment    
    conda install bbmap
    
## 11. install humann2 in conda python=2.7 environment
    conda install humann2
    
### Metaphlan2 will be installed automatically, which can be started with:
    metaphlan2.py
    
    
    
