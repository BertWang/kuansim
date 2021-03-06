# Kuansim

A society issues tracking system

- [How to join](https://g0v.hackpad.com/--1OaXIxVVPSd)

# prepare 

## install vagrant

http://downloads.vagrantup.com/

Don't install from Ubuntu/Linux Mint Software Center.

## install vagrant berkshelf

```
$ vagrant plugin install vagrant-berkshelf
```

# Get all source codes.

```
$ git clone --recursive
```
(Add the git url in the end with space.)

# update all source codes

```
$ git submodule update --recursive
```

# run backend server.

Browse to the kuansim folder cloned from git.

```
$ cd cookbooks/kuansim/
$ vagrant up
```
The current project directory is shared as /vagrant in vagrant.

# run web frontend server.

```
$ cd frontend/web
$ npm run start
```

# setup git push url
All URLs of submodule are https. In order to push via ssh, add the following
configuration into ${HOME}/.gitconfig
```
[url "git@github.com:g0v/kuansim-frontend.git"]
    pushInsteadOf = https://github.com/g0v/kuansim-frontend.git
[url "git@github.com:g0v/kuansim-backend.git"]
    pushInsteadOf = https://github.com/g0v/kuansim-backend.git
[url "git@github.com:g0v/kuansim_chrome.git"]
    pushInsteadOf = https://github.com/g0v/kuansim_chrome.git
[url "git@github.com:g0v/kuansim-devops.git"]
    pushInsteadOf = https://github.com/g0v/kuansim-devops.git
```

# See also

- Project site: http://hack.g0v.tw/kuansim
- Bug report or feedback here
