node js sample project install
==============================

### 安裝前注意事項

在開始前，請先將 jenkins 安裝完成，一旦 jenkins 安裝完成後，你將會有一 `jenkins` user

在開始下面安裝前請先執行下列指令

`sudo su jenkins -l`

代表切換到 jenkins 目錄底下，接著我們就可以開始下面的步驟

### 安裝 nvm

透過 nvm 來進行 NodeJS 安裝，指令如下：

```
sudo su jenkins
touch ~/.bashrc
curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.29.0/install.sh | bash
```

安裝完之後會在 jenkins user 的 `~/.bashrc` 寫入下列指令

```
export NVM_DIR="/var/lib/jenkins/.nvm"
[ -s "$NVM_DIR/nvm.sh" ] && . "$NVM_DIR/nvm.sh"  # This loads nvm
```

這段最主要的用意就是要把 nvm 載入，之所以需要寫入 `~/.bashrc` 就是要在登入時將 nvm 載入。

如此我們就可以再不依賴 jenkins CI 的 plugin 的協助快速的把開發環境所需資源安裝完成。

第一次安裝 nvm，因為我們是在登入後安裝完成，因此並不會執行到上述指令，透過 `source ~/.bashrc` 來載入

我們可以透過 `nvm --version` 確認已確實載入完成

### 安裝 NodeJS

`nvm install v4`

透過 nvm 的協助我們可以很方便進行 NodeJS 版本切換，這也會使我們在建置時可以很方便的切換版本。

如果你要設置某個版本為預設，可以使用下列指令

`nvm alias default v4`

如此我們可以確認一下目前 NodeJS 的版本

`node -v`

global 套件安裝
---------------

```
npm i pm2 -g
```

sample project 安裝
-------------------

```
cd ~
git clone https://github.com/TrunkWorkshop/sailsSample
cd sailsSample
npm i
```

上面步驟完成，就已經可以準備開始 nodejs for jenkins 工作坊了 :)
