# X-Live-Butler

## Description
The X Live Buttler processes Multirack&amp;Multifiles recordings of the X-Live Card (or similar cards).   The individual 4 GB files are disassembled.  Tracks without a useful signal are discarded. Several files belonging to one track are puzzled together. So that in the end you only have clean tracks for your DAW. 

### Prerequisite
Docker must be installed and configured.

### Not shure how to install Docker? 
Please visit the official Docker Site https://docs.docker.com/get-docker/

### Important note - READ - Yes we are musicians, we know everything. But read it anyway.  

1. New files are created during editing. The storage space should ideally be twice as large as the project file. 
2. Do not work on your SD card! It's slow and doesn't like working long hours any more than civil servants do.
3. The original project files are not changed. Even if this means a large storage overhead

## Okay, let's let the butler off the leash.

1. Open Powershell or the Shell on your current system 

2. Command:   docker run -it -v E:/XLive:/tmp/Xlive juxreal/xlive-butler bash

notes:  "E:/Xlive": - Replace with your Host system Folder. The folder on your computer where the data is to be distributed.

3. Create a folder called "input" (small letters) in the Host folder.

4. Copy the hole Folder/Folders !!!  (Something like: "5524153A") to the "Input" Folder 

note: This folder was created on the host when it was first started. (example: E:/Xlive/input)

5. Start the Butler  - on the Powershell Console from the Docker Container (something like: root@b4c2a8b7e06a:/# ) by typing: 

exec /home/xlive/mission-controll 

## Wait... 

the butler now starts his work. On your host system you will find the mission log. 
When the input folder is empty, you are done. 
In the meantime, you can support my work. 

Tier 1: Listen to our music 
https://open.spotify.com/artist/23BwtGbTmXrJ72dqsYrjDK?si=XynqX65lQ4egzr6CjL_kTg

Tier 2: Shop some merch 
https://shop.spreadshirt.de/neonyzer

Tier 3:  Spend money for our Gas Syndrom
https://paypal.me/saschaflach

### Know Bugs 
After File 09-01 its starts with 0A-01. in all the tests it worked, but I can't guarantee anything

## Upcoming features

1. Web Dashboard
2. Web Start
3. Code tuning
