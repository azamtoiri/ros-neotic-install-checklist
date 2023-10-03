# ros-neotic-install-checklist
Check list for install ros-neotic on ubuntu 20.04

## 1. Set up your computer to accept software from packages.ros.org:
```shell
sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'
```

## 2. Set up your keys

```shell
sudo apt install curl -y
curl -s 
https://raw.githubusercontent.com/ros/rosdistro/master/ros.asc | sudo apt-key add -
```

## 3. Make sure your Debian package is up-to-date
```shell
sudo apt update
```

## 4. Install the full desktop version:
if you want to install some other version write ros-{version}-desktop-full:

```shell
sudo apt install ros-noetic-desktop-full
```

## 5. Set up environment:
```shell
echo "source /opt/ros/melodic/setup.bash" >> ~/.bashrc
source ~/.bashrc
```

## 6. Install the dependencies we need to work with packages by entering the command:
```shell
sudo apt install python3-rosdep python3-rosinstall python3-rosinstall-generator python3-wstool build-essential
```

## 7. Init rosdep
```shell
sudo rosdep init
rosdep update
```

## 8. Check ros
```shell
roscore
```
