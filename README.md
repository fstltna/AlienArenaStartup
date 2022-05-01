# Alien Arena Startup Scripts (1.3)
Alternate startup scripts for the Alien Arena game - uses the "screen" command to manage session. This also restarts the game process if it crashes.

Official support sites: [Official Github Repo](https://github.com/fstltna/AlienArenaStartup) - [Official Forum](https://alienarena.gameplayer.club/index.php/forum/alien-arena-tools) 
 ![Alien Arena Logo](https://FPS.GamePlayer.club/aa2k12logo2.jpg) 

---

These start up the Alien Arena server at boot time with a "screen" process.

1. Copy **alienarena** into **/home/aaowner/bin** - make sure it is executable
2. Copy **startalienarena** into **/home/aaowner/alienarena** - make sure it is executable
3. Copy **start-alienarena-linux64-dedicated** into **/home/aaowner/alienarena** - make sure it is executable
4. Add **@reboot /home/aaowner/bin/alienarena start** to the crontab file


When you want to view the Alien Arena console, just enter "**screen -r**" in your shell.

To disconnect from the Alien Arena console just press **CTRL-A CTRL-D**. This will leave it running and you can reconnect to it again.

I have only tested this on a Ubuntu 16.04 server...

If you want to turn off the server respawning type "**touch /home/aaowner/alienarena/nostart**". To reenable it type "**rm /home/aaowner/alienarena/nostart**".

---
Note: If you don't already have the "screen" tool installed you will need to install it by "**sudo apt-get install screen**".
