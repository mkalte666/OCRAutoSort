# OCRAutoSort
Auto-Sort your Inkling .wpi files - after converting them to pdf - automatically

## Dependencies
You will need the following things installed:
  * tesseract-ocr + a tesseract-language package (tesseract-ocr-en, -deu, ... whatever you like and need)
  * inklingreader (https://github.com/roelj/inklingreader)

## Installation READ THIS IF YOU DONT WANT TO FUCK YOUR SYSTEM UP
Make shure you have your Inkling connected when you run the install script.
Also run the script as user. It will ask you for sudo (i know this is ugly).
What it will do? Not much - it puts the ocrautosort to /usr/bin/
But you can allow more things to be done that might seem dangerours (i like them):
  * with "-c" Add a crontab to your user that checks the configured mount folder for new files every 2 minutes that then are auto-converted
  * with "-a" Add a root-crontab that runs "mount -a" every 2 minutes
  * with "-f" (Danger thingy!) Add a entry to /etc/fstab for your inkling so its mounted in the right place and also readable by you if mounted

## configuration
The tool will use a config file in your .config folder: ~/.config/ocrautosort 
You can generate a file with all the default settings by entering "ocrautosort --genConfig"

## How to fly this thing?
You dont have to. You can trigger a manual search by entering "ocrautosort" in your terminal, but since you registerd the cronjobs (didnt you?), it runs every 2 minutes!
