

Exercise1:
////
// all: hosts
// -b : chạy mode sudo
// -m : gọi module (plugin)
// apt: là module apt
// -a : argument của module

*** update host ***
ansible -i inventory.ini all -b -m apt -a "upgrade=yes"

*** Check python version ***
ansible -i inventory.ini all -a "python --version"

*** check: python-pip có hay không thì cài  ****
*** sudo apt-get install python-pip         ****
ansible -i inventory.ini all -b -m apt -a "name=python-pip state=present"

*** check: pydf có hay không thì cài  ****
*** pip install pydf                        ****

ansible -i inventory.ini all -b -m pip -a "name=pydf state=present"

*** chạy pydf trên máy ảo ****
ansible -i inventory.ini all -a "pydf"



