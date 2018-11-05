# datascience
Data science tools

From https://arrow.apache.org/install/

```bash
sudo apt install -y -V apt-transport-https
sudo apt install -y -V lsb-release
sudo wget -O /usr/share/keyrings/red-data-tools-keyring.gpg https://packages.red-data-tools.org/$(lsb_release --id --short | tr 'A-Z' 'a-z')/red-data-tools-keyring.gpg
sudo tee /etc/apt/sources.list.d/red-data-tools.list <<APT_LINE
deb [signed-by=/usr/share/keyrings/red-data-tools-keyring.gpg] https://packages.red-data-tools.org/$(lsb_release --id --short | tr 'A-Z' 'a-z')/ $(lsb_release --codename --short) universe
deb-src [signed-by=/usr/share/keyrings/red-data-tools-keyring.gpg] https://packages.red-data-tools.org/$(lsb_release --id --short | tr 'A-Z' 'a-z')/ $(lsb_release --codename --short) universe
APT_LINE
sudo apt update
sudo apt install -y -V libarrow-dev # For C++
sudo apt install -y -V libarrow-glib-dev # For GLib (C)
```

https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy-linux

```bash
echo "deb [arch=amd64] https://packages.microsoft.com/repos/microsoft-ubuntu-xenial-prod/ xenial main" > azure.list
sudo cp ./azure.list /etc/apt/sources.list.d/
sudo apt-key adv --keyserver packages.microsoft.com --recv-keys EB3E94ADBE1229CF

sudo apt-get update
sudo apt-get install azcopy
```
