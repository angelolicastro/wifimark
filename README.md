# Wi-Fi Mark (wifimark)

wifimark is a tool for Mac OS X that notifies the user if the fingerprint of a known Wi-Fi network has changed. The fingerprint of a Wi-Fi network is the combination of the BSSID, SSID, channel number, and gateway name.

## Requirements

* Mac OS X
* Python 2

## Installation

	git clone https://github.com/angelolicastro/wifimark.git
	cd wifimark
	echo '{ }' > .wifimark.database

## Configuration

1. Copy `config.example.py` to `config.py`.

		cp config.example.py config.py

2. Change the value of `databaseFilePath` and `logFilePath` in `config.py`.

It is highly recommended that you automate the use of wifimark by using cron. For example, you can automatically use wifimark every minute by adding the following line to your crontab file.

	* * * * * /path/to/wifimark > /dev/null 1>&2

## Usage

	wifimark

**Note:** You may have to make the wifimark file executable using `chmod`.

	chmod +x wifimark

## License

[The MIT License (MIT)](LICENSE)

Copyright (c) 2016 [Angelo Licastro](http://angelolicastro.com)
