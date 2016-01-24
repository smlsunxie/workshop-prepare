jenkins install
===============

安裝 Java 軟體
--------------

### 安裝 java 8 & maven

```
sudo add-apt-repository ppa:openjdk-r/ppa
sudo apt-get update
sudo apt-get install openjdk-8-jdk
sudo apt-get install maven
```

安裝 Jenkins 軟體
-----------------

參考 Jenkins 官方的 Ubuntu Linux [安裝說明](https://wiki.jenkins-ci.org/display/JENKINS/Installing+Jenkins+on+Ubuntu)

```
wget -q -O - https://jenkins-ci.org/debian/jenkins-ci.org.key | sudo apt-key add -
sudo sh -c 'echo deb http://pkg.jenkins-ci.org/debian binary/ > /etc/apt/sources.list.d/jenkins.list'
sudo apt-get update
sudo apt-get install jenkins
```

管理 Jenkins 伺服器
-------------------

重新啟動 Jenkins 伺服器。

```
sudo service jenkins restart
```
