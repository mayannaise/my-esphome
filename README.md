# Setup

## Install ESP-Home

Install esphome on your dev machine:

```sh

```

## Install OpenHAB

Install OpenHAB on the central server:

```sh
sudo apt install curl default-jre -y
curl -fsSL "https://openhab.jfrog.io/artifactory/api/gpg/key/public" | gpg --dearmor > openhab.gpg
sudo mkdir -p /usr/share/keyrings
sudo mv openhab.gpg /usr/share/keyrings
sudo chmod u=rw,g=r,o=r /usr/share/keyrings/openhab.gpg
echo 'deb [signed-by=/usr/share/keyrings/openhab.gpg] https://openhab.jfrog.io/artifactory/openhab-linuxpkg stable main' | sudo tee /etc/apt/sources.list.d/openhab.list
sudo apt update
sudo apt install openhab openhab-addons -y
sudo systemctl enable openhab
```

## Install MQTT Broker

Install an MQTT broker on the central server:

```sh
sudo apt install mosquitto mosquitto-clients -y
```
