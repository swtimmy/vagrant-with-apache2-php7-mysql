1. Install brew
   /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
   brew doctor
   brew update

2. Install vm
   brew install virtualbox --cask

3. Install vagrant
   brew install vagrant --cask
   brew install vagrant-manager --cask

4. Operation
   #In root directory
   #start vagrant
   vagrant up

5. Edit hostsfile
   vi /etc/hosts
   192.168.[ip].13 www.Your-Domain.com

6. Test "www.Your-Domain.com" in browser

7. Other operation
   #In root directory
   #Go into ssh
   vagrant ssh
   #stop vagrant
   vagrant halt
   #reload vagrant
   vagrant reload --provision
   #remove vm
   vagrant destroy

8. End
