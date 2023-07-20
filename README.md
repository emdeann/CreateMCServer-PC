# Setting Up the Minecraft Server - Windows

## Description

This repository contains a starter kit to set up a Minecraft server capable of running our Python code. It contains two folders: one with the Minecraft server and one with the required Python library. The `Python Files` folder is also where we should store and run any Python files we have or make.
Your computer must also have [Python](python.org) installed. IDLE comes automatically with Python, which is the editor we used during camp. 

## Server Setup Guide

* Download the code by clicking `Code` on the top right of this page, and then clicking `Download ZIP`.
* Unzip the downloaded file using a tool like WinRAR, and you will be left with a folder containing the two folders.
* The default Minecraft version for this server is Minecraft 1.12.2. If you (ask your child) want to use a different version of Minecraft, download the corresponding file [here](https://getbukkit.org/download/spigot).
* If you downloaded a different file, rename it to `spigot.jar` and place it in the `Server` folder. In the same folder, run `start.bat`. You should need to run it twice, after it exits automatically the first time. This is only required once. (By completing this step, you are agreeing to the Minecraft [EULA](https://account.mojang.com/documents/minecraft_eula)).
* After you run it the second time, you should see another black cmd window open. Let it run until you see `Done (Xs)! For help, type "help" or "?"`. Once you see this, your server is open and joinable.

## Joining the Server
* On the same computer that is hosting the server, you can join it by clicking "Direct Connect" in the Multiplayer menu of Minecraft and using `localhost` as the server address.
* On a different computer which is **on the same network**, you can join the server by typing your [local IP address](https://www.whatismybrowser.com/detect/what-is-my-local-ip-address) instead of localhost.
* It is possible to open the server to friends not on the same network can join and play together, but this is a more complex process which will not be detailed here.

## Running Python Code on the Server
* To run Python code on the server, a few things must line up:
  * The Minecraft server must be open and running
  * The player must be online in Minecraft, and join the correct Minecraft server
  * Python must be installed
* Once these are true, code can be run. The easiest way to do this is to open IDLE, and open a file brought home on the flash drive. Make sure this file is placed in the `Python Files` folder first. By clicking `Run` -> `Run Module`, this file will run and its effect will be seen in the Minecraft world.
* Students should have a basic understanding of IDLE after the week is over, but I will nonetheless provide a guide to IDLE and to our Python tool, mcpi, for ease of use.
  * [IDLE](https://realpython.com/python-idle/)
  * [mcpi](https://projects.raspberrypi.org/en/projects/getting-started-with-minecraft-pi/7) (Note: This is the official mcpi tutorial, which assumes that you are using a Raspberry Pi. This is not the case, so some aspects of the game may look different. However, the code will identically in most cases.)
  * If you would like to avoid the need to run files from only the `Python Files` folder, you are able to install mcpi using [pip](https://packaging.python.org/installing/). However, this is a bit more technically involved.
 
## Overview

This should provide all the information you need to get your child started, and continue their coding journey in Minecraft from home. If they are older and express a strong interest in coding with Minecraft, I highly recommend looking into more advanced concepts, like plugins and mods. This will use the Java programming language, and be both much more challenging and much more rewarding.

If you have any trouble, please feel free to reach out by email. Thanks!
