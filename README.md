# java makefile
### 編譯
1. 各專案個別編譯
```bash
git clone https://github.com/LS-NotInUse/java
cd java/Ch1-1
make            # 編譯
make run        # 執行
make clean      # 刪除執行檔、留下程式碼
```
<img src="https://i.imgur.com/yMITGZg.png" width="400"/>  

2. 所有專案一起編譯
```bash
git clone https://github.com/LS-NotInUse/java
cd java
make            # 編譯所有專案
make clean      # 刪除所有執行檔
```
<img src="https://i.imgur.com/K98CEJC.png" width="400"/>  

### JDK
1. 安裝JDK
```bash
sudo apt install default-jdk          # for Ubuntu, Raspbian, etc.
```

2. 查看版本
```bash
java --version  # java版本
javac --version # java編譯器版本
```
<img src="https://i.imgur.com/WNqTzhW.png" width="400"/>  
