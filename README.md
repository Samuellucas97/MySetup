## Introduction

Setup my personal machine installing manually is too dull, so I created this automated installation using Ansible to help with this stuff. Ansible is a configuration management tool too used throughout the world, I recommend it. 

To clone this repository:

```
$ git clone https://github.com/Samuellucas97/MySetup.git
$ cd MySetup
```

### Programs/Packages to be installed

- Basic Linux packages
    - :ballot_box_with_check: net-tools
    - :ballot_box_with_check: curl
    - :ballot_box_with_check: htop
- :ballot_box_with_check: Java JDK 17
- :ballot_box_with_check: VSCode IDE
- :negative_squared_cross_mark: Oh My Bash
- :negative_squared_cross_mark: Google Chrome 


## Prerequisites 	

- Install Git (version >= 2.25.1)

    - Execute on terminal: `sudo apt install git`. 
    - To check if it was installed: `git --version`. 
 
- Install Python (version >= 3.8.10)

    - Execute on terminal: `sudo apt install python3.8`. 
    - Open `~/.bashrc` file and insert `alias python=python3`.
    - To check if it was installed: `python --version`.

- Install Ansible (version >= 2.12.4)

    - Execute on terminal: `sudo apt install ansible`.  
    - To check if it was installed: `ansible --version`.



## Setting up - Ubuntu 20.04 

Run the following command on terminal: 

```
$ sudo ansible-playbook  -i "localhost," -c local setup_ubuntu20_04.yml
```

Always you change some of the YAML files, do not forget to use this command:

```
$ ansible-playbook setup_ubuntu20_04.yml --check
```