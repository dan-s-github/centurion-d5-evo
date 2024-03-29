# Centurion D5-Evo 

This project uses the [LIlYGO© T-Relay](https://www.lilygo.cc/products/t-relay) to interact with the Centurion D5-Evo Gate Controller

  ![LIlYGO© T-Relay][lilygo_board]

It is based on this repo: https://github.com/wernerhp/esphome/tree/main/centurion-d5-evo


## Components

- [LILYGO® TTGO T-Relay ESP32 Chip DC 5V 4 Groups Relay](https://www.aliexpress.com/item/1005003165061321.html)
- [LILYGO® TTGO T-U2T USB To TTL Automatic Downloader CH340K](https://www.aliexpress.com/item/1005003141756461.html)

### Prepare Board

This uses esphome to prepare the esp32 on the board for home assistant

1. Navigate to [ESPHome Web Installer](https://web.esphome.io/)
2. `Connect` to your device to an USB port using the T-U2T adapter
3. `Prepare for first use`
4. `Install`
5. wait until configuration has been installed
6. `Connect to Wi-Fi`

### Install Software

1. Navigate to ESPHome in [Home Assistant](http://homeassistant.local:8123/) 
2. `ADOPT` newly initialised device

    ![ESPHome Discovered][esphome_adopt]
    - Specify name for new device
      - `Centurion D5-Evo`
    - `ADOPT`
3. `Install` to add encryption key to device
    - Close dialog after image has been uploaded succesfully

4. The device will still use the inital hostname which is also the name of the yaml file stored in home assistant. Renaming the hostname using ESPHome Dashboard will also update the yaml filename to reflect the changed hostname.
    
    - Use `rename hostname` in the options dialog of the adopted device

      ![ESPHome rename hostname][esphome_rename]
    - `RENAME`
      - Close dialog after image has been uploaded succesfully

5. Device is now ready for customization

    ![ESPHome ready][esphome_ready]

6. Use the [centurion-d5-evo.yaml](centurion-d5-evo.yaml) as template to edit your newly created yaml file


[lilygo_board]: ./docs/H516-1000-SY.jpg
[esphome_adopt]: ./docs/esphome_adopt.png
[esphome_rename]: ./docs/esphome_rename.png
[esphome_ready]: ./docs/esphome_ready.png