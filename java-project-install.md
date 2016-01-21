java sample project install
===========================

### 安裝 java 8 & maven

```
sudo add-apt-repository ppa:openjdk-r/ppa
sudo apt-get update
sudo apt-get install openjdk-8-jdk
sudo apt-get install maven
```

### 選擇 java 8 作為預設 java version

```
sudo update-alternatives --config java
sudo update-alternatives --config javac
```

### 安裝前注意事項

在開始前，請先將 jenkins 安裝完成，一旦 jenkins 安裝完成後，你將會有一 `jenkins` user

在開始下面安裝前請先執行下列指令

`sudo su jenkins -l`

代表切換到 jenkins user 的 home 目錄底下，接著我們就可以開始下面的步驟

### 安裝 java sample project

```
cd ~
git clone https://github.com/TrunkWorkshop/jhipster-sample-app
cd jhipster-sample-app
mvn
mvn -Pprod clean package
```

上面步驟完成，就已經可以準備開始 java for jenkins 工作坊了 :)
