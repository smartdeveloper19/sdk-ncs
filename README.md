## nRF Connect SDK: sdk-nrf

### Setup repository

Following are the steps to setup the project on Linux:

- Create a workspace for example embedded_code
    - clone this repository into workspace using following command:
```bash
git clone https://github.com/smartdeveloper19/sdk-ncs.git
```
- Download [nrf Desktop tools](https://www.nordicsemi.com/Products/Development-tools/nRF-Connect-for-Desktop/Download) and run following command:
```bash
./nrfconnect-4.4.1-x86_64.appimage
```
It will open the user interface of nRF Desktop Tools and install the required SDK version.

### Install Nordic SDK
This project required nRF connect SDK Version v2.6.0 (available in tool chain manager).

Important change the SDK installation path to workspace (embedded_code).

### Set environment variables

After the intalization, generate environment script from the Tool Manager.

![alt text](<Screenshot from 2024-05-09 17-30-08.png>)

This script will setup all the environment paths needed for the development.
Save the script to showed path. 

Source the script by
```
source path_to_env.sh_file
```
This command can also be added to .bashsrc to set the envoirment variables upon each terminal start.

## Building the project for Nrf5280 dev board

```
west build -b nrf52840dk_nrf52840 --pristine
```