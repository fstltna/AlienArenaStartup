# Alien Arena Startup Scripts (1.0)
Alternate startup scripts for the Alien Arena game - uses the "screen" command to manage session. This also restarts the game process if it crashes.

Official support sites: [Official Github Repo](https://github.com/fstltna/AlienArenaStartup) - [Official Forum](https://fps.gameplayer.club/index.php/forum/utilities) 
 ![Alien Arena Logo](https://FPS.GamePlayer.club/aa2k12logo2.jpg) 

---

These start up the Alien Arena server at boot time with a "screen" process.

1. Copy **alienarena** into **/etc/init.d** - make sure it is executable
2. Copy **startalienarena** into **/root/Alien\ Arena** - make sure it is executable
3. Run "**systemctl enable alienarena**" (only needed once, will stick)
4. Run "**systemctl start alienarena**" - starts Alien Arena without restarting the server

When you want to view the Alien Arena console, just enter "**screen -r**" in your shell.

To disconnect from the Alien Arena console just press **CTRL-A CTRL-D**. This will leave it running and you can reconnect to it again.

I have only tested this on a Ubuntu 16.04 server...

If you want to turn off the server respawning type "**touch /root/Alien\ Arena/nostart**". To reenable it type "**rm /root/Alien\ Arena/nostart**".

---
Note: If you don't already have the "screen" tool installed you will need to install it by "**sudo apt-get install screen**".
