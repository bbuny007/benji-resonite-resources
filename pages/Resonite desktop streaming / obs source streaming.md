## Resonite desktop streaming / obs source streaming / screenshare or whateva 

So ive been chilling in the discord looking for things to do and found someone who asked about sharing their game to resonite (like share their screen)

and after a long google session i have found an *easy* way 

sadly it still needs like hosting a service and obs so 

### Buckle up 

# prerequsites 

 - linux (or wsl2)
 - a way to host something off of local internet 
 - ffmpeg (no this isnt a male preg thing)

thats it

# The setup

- on windows

imo the best wsl containter is arch so get debian off the m$ store and set it up and look for a tutorial on how to get an debian linux shell 

- on the linux shell or terminal or ssh

cd (change directory) to somewhere you are comfortable in working may be your home folder or an extra folder in desktop it dosnt matter

or open your tty in the folder directly if you have a desktop/wm

run this command (this will download the owncast binary)

## curl -s https://owncast.online/install.sh | bash

and install ffmpeg with sudo apt install ffmpeg
now to run it you need root also known as the administrator user

on debian its the sudo comman as a prefix that makes the program run as root (it asks for your password)

for me on cachy os it is the same so cd ./owncast

then sudo ./owncast
 
now to seeting it up i may add images if i dont forget

on the above download command the output had something with the default password is abc123 !!! You need to quickly change that 

to do that visit localhost:8080/admin/config/server/ in an browser and put in sername admin and you pw its unsecure http if you dont use a ssl cert but we will go into it on later lines of the tutorial

reload the page after save and input the new password you have made 

if you forget your password you can delete the data folder that auto generates note that all of your other infomation and settings get lost too

now onto making it accessible from the out side i use ddns so i dont have to openly show my ip address even though my NAT in germany shows that im on some cornfield 

i just logged into duckdns.org (note reddit login is no more) and made one address and updated it also on page since i dont want to long term host i dont use an ip update client  

For more info, methods and port forwarding i forward you to [this page](https://github.com/bbuny007/benji-resonite-resources/blob/main/pages/opening%20up%20to%20the%20internet.md)

now to key setup on the admin page /admin after the :8080 configuration then server setup then stream keys then the plus icon add key copy it it will be copyable again so dont worry

additionally you can add quality settings in configuration then video i would only pump up the bitrate of the already availible option too 3k or 6k

now go back to admin home then copy the stream link and

## OBS time 

go to settings stream then custom then input your key and link

setup up your sources and scenes as you like 

now in resonite on any video player that supports rtmp streams enter your publicly availible link of the non admin page the "stream page"

after obs started streaming it should be visible





 




