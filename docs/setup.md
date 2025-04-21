## Install Ubuntu in WSL

```bash
wsl --install Ubuntu
wsl [--list | -l]
```

## Inside Ubuntu

```bash
sudo apt update && sudo apt upgrade -y
```

sudo: "super user do", runs a command with root privileges
apt: "advanced package tool"

### [Disable Windows Path](./resources.md#disable-windows-path)

1. Open `/etc/wsl.conf`

```bash
sudo vim /etc/wsl.conf # sudo to be able to modify the file
```

2. Modify or add the config:

```bash
[interop]
appendWindowsPath = false
```

Then do `wslconfig /t Ubuntu` or `wsl --shutdown` or simply reboot the pc.

### Set `JAVA_HOME` after installing java because Spark requires it

1. List java path

```bash
update-java-alternatives -l
```

Something like `/usr/lib/jvm/java-1.17.0-openjdk-amd64`

2. Add it to `.bashrc`

```bash
echo 'export JAVA_HOME=[path from previous command]' >> ~/.bashrc
source ~/.bashrc
```

3. Verify

```bash
echo $JAVA_HOME
```

### [Download uv](./resources.md#download-uv)

```bash
# download uv
curl -LsSf https://astral.sh/uv/install.sh | sh
# install python
uv python install 3.13
# create venv inside project
uv venv
# install pyspark
uv add pyspark[pandas_on_spark]
# install ipykernel to use jupyter notebooks
uv add ipykernel
```