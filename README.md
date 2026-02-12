# Setting Up the Minecraft Server

## Description

This repository contains a small starter kit to set up a Minecraft server capable of running our Python code. It contains a folder [Server](Server/) which contains the pieces needed to run a Minecraft Server capable of handling the Python code we will use.

Do not get hung up in the terminology here - we are using special software to modify Minecraft and allow us to run Python code, which requires running a "server". This does not mean you will be running a public Minecraft server; by default it is only available within your home network, and the general intent is for it to be hosted on the same computer which is playing Minecraft and thus functioning as a singleplayer server. It is *possible* to expose the server to the outside, but this requires extra work and comes with a set of vulnerabilities.

Your computer must also have [Python](https://www.python.org/downloads/) installed to run Python code, and [Java](https://adoptium.net/temurin/releases) to run the server. IDLE comes with Python, which is the editor we used during camp. **You will need to check a box in the Python installer to make sure it includes IDLE.** It is also completely fine to use other code editors (IDLE is a learning environment and is not very powerful), but they are not taught in our curriculum.

Note that there are many reliable vendors of Java - I linked one of the most popular, but any should be fine as long as it is Java version 21+.

## Server Setup Guide

* Download the code by clicking `Code` on the top right of this page, and then clicking `Download ZIP`.
* Unzip the downloaded file - both Windows and MacOS have built-in tools to do this - and you will be left with a parent folder containing the Server folder and this page.
* In the Server folder, run `start-windows.bat` (Windows) or `start-mac.command` (MacOS). It's possible on both operating systems to receive a warning at this step, because running unknown scripts from the internet is generally a poor idea. The steps to allow the file to run are different between them and I won't go over them in detail here, but it generally involves using a "Run anyway" button if present, or navigating to settings to allow the file to run.
  * If this step fails (outside of a permission issue), it is likely because you never installed Java or the wrong version was installed. See the link at the top of this document - make sure you download Java 21+ for your operating system (either JDK or JRE is fine).
* After running the command for the first time, you will see an error message about needing to accept the EULA, and that several files and folders have been automatically created in the Server folder. Find the file called eula.txt in the Server folder and change the line that says `eula=false` to `eula=true`. 
* After accepting the EULA, move the file `mcpq.jar` from the Server folder into the `plugins/` folder. Paper allows us to run plugins on our server, and mcpq is the plugin which allows Minecraft to communicate with our Python code. In fact, the use of mcpq is the reason we need to self-host a server at all.
* Once the EULA is accepted and mcpq is in the plugin folder, you are ready to start the server. Run `start-windows.bat` or `start-mac.command` again (this will be how you start the server every time and is required to join).
  The server will take a while to start up; wait for a line in the console containing `Done!...`. Once you see this, the server is ready to join.

When writing Python code, it is possible to put the server in a broken state. This can happen generally via teleporting to invalid coordinates (though rare in recent Minecraft versions) or spawning a huge number of entities such that the game crashes whenever the server is joined. In this case, you can delete the folder called `world` from the Server folder. This will delete the world (and all builds, etc. along with it) and a new one will be generated when the server is started next.

## Joining the Server
* On the same computer that is hosting the server, you can join it by clicking "Direct Connect" in the Multiplayer menu of Minecraft and using `localhost` as the server address.
* On a different computer which is **on the same network**, you can join the server by typing your [local IP address](https://www.whatismybrowser.com/detect/what-is-my-local-ip-address) instead of localhost.
* It is possible to open the server so friends not on the same network can join and play together, but this is a more complex process which will not be detailed here. I can recommend [this](https://thebreakdown.xyz/how-to-port-forward-for-a-minecraft-server/#port-forwarding-for-your-minecraft-server) guide on the topic (be aware that doing this improperly can cause vulnerabilities in your WiFi network, so proceed with caution).

## Running Python Code on the Server
* To run Python code on the server, a few things must line up:
  * The Minecraft server must be open and running
  * The player must be online in Minecraft, and join the correct Minecraft server
  * Python must be installed
  * **The MCPQ Python module must be installed.** Once Python is installed, run `pip install mcpq` in a terminal/console to install it.
* Once these are true, code can be run. The easiest way to do this is to open IDLE, and open a file brought home on the flash drive. By clicking `Run` -> `Run Module`, this file will run and its effect will be seen in the Minecraft world.
* Students should have a basic understanding of IDLE after the week is over, but I will nonetheless provide a guide to IDLE for ease of use.
  * [IDLE](https://realpython.com/python-idle/)
 
## Overview

This should provide all the information you need to get your child started, and continue their coding journey in Minecraft from home. If they are older and express a strong interest in coding with Minecraft, I highly recommend looking into more advanced concepts, like plugins and mods. This will use the Java programming language, and be both much more challenging and much more rewarding.

If you have any trouble, please feel free to reach out by email. Thanks!
