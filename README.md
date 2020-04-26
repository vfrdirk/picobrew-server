# picobrew-server
This is a reverse engineered server for the proprietary PicoBrew protocol. The [PicoBrew Zymatic](http://www.picobrew.com/) is a machine to homebrew beer. Since their Firmware is not yet open sourced (they intend to release it at some point) it is missing an offline mode this server can be used as an alternative.

# HTTP API
The PicoBrew's built-in Ardunio uses an unencrypted HTTP communication protocol. All request are `GET` requests and are not authenticated. The following documentation is based on Firmware 1.18.

[API Docs on Postman](https://documenter.getpostman.com/view/234053/Szf54VEX?version=93783194-dcee-4bb2-8f19-f25ab6c6d411)
[API Docs on GitHub](https://github.com/hotzenklotz/picobrew-server/wiki/PicoBrew-API)

# Installation

- Install Python 3.6 (or higher)

```
// Install Python requirements
pip install -r requirements.txt

// Start the server
sudo python server.py
```

- Connect the PicoBrew machine to your computer and enable DNS spoofing. Re-route `www.picobrew.com` to your computer.
[More Details](https://github.com/hotzenklotz/picobrew-server/wiki/Install)

# Demo
You can try out the admin UI for uploading your XML files in this [online demo](https://picobrew.herokuapp.com). Please note, this website is for showcasing only and you should deploy your own version.


# Features
- Import BeerXML files
- Send all your recipes to the PicoBrew
- Send cleaning recipes to the PicoBrew
- Session Logging
- Session Recovery
- Admin Web UI

ToDo

- Session Charts

# Disclaimer
This software is provided "as is" and any expressed or implied warranties are disclaimed. This software submits recipes with temperature targets to your PicoBrew machine and will cause it to heat water. Any damage to your PicoBrew machine is at your own risk.

# License

MIT @ Tom Herold
