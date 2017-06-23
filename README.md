# go-install

## Step 1
Create the file and add execution permission to it : 

```bash
nano ~/go.install && chmod +x ~/go.install && nano ~/go.install
```

## Step 2
Put this script in the file :
```bash
#!/bin/bash
# Script for  the plebs of PepperSlice

cd ~/
wget https://storage.googleapis.com/golang/go1.8.linux-amd64.tar.gz
tar -C /usr/local -xzf go1.8.linux-amd64.tar.gz
echo "export PATH=\$PATH:/usr/local/go/bin" >> ~/.bashrc
```

## Step 3
Execute it (if not root execute it with `sudo`) : 
```bash
~/go.install
```

## Step 4
Reload the shell and check the version : 
```bash
. ~/.bashrc && go version
```
Output :
```bash
go version go1.8 linux/amd64
```
