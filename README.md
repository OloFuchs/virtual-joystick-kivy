# amiga-app-template

This repository is serve as reference to the Virtual Joystick app deployable to the Amiga Brain.

To learn more about building you own custom applications, please refer to:

[amiga.farm-ng.com - **Developing Custom Applications**](https://amiga.farm-ng.com/docs/brain/brain-apps)

> [!IMPORTANT]
> This app will only work on Amiga Brains using v2.3+ of our OS. If you are not sure of which version you have, contact support@farm-ng.com 

To install the Virtual Joystick App on your Amiga Brain, ssh into your robot and clone the repo to your user's home directory:

```
cd ~
git clone https://github.com/farm-ng/virtual-joystick-v2.git
```

Remember to change `manifest.json` to point to your home directory:

```
{
    "services": {
        "virtual-joystick": {
            "name": "virtual-joystick",
            "type": "app",
            "exec_cmd": "/mnt/managed_home/farm-ng-user-<YOUR-USERNAME-HERE>/virtual-joystick-v2/entry.sh",
            "display_name": "Virtual Joystick"
        }
    }
}
```
Now install the app using the script `install.sh`:

```
cd ~/virtual-joystick-v2
./install.sh
```

You can now open the app on your Brain's launcher display or using:

```
./entry.sh
```

> [!NOTE]
> The first time you run the App all dependencies will be installed, which may take a few minutes.


---
