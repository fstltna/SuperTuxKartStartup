# Super Tux Kart Startup Scripts (1.0.0)
Startup scripts for the Super Tux Kart game server software - uses the "screen" command to manage the session. This also restarts the Super Tux Kart server process if it crashes.

Official support sites: [Official Github Repo](https://github.com/fstltna/SuperTuxKartStartup)

---

These start up the Super Tux Kart server at boot time with a "screen" process.

1. Copy **supertuxkart** into **/etc/init.d** - make sure it is executable
2. Copy **startsupertuxkart** into **/root/SuperTuxKart** - make sure it is executable
3. Run "**systemctl enable supertuxkart**" (only needed once, will stick)
4. Run "**systemctl start supertuxkart**" - starts Super Tux Kart server without restarting the OS.

When you want to view the Super Tux Kart console, just enter "**screen -r**" in your shell.

To disconnect from the Super Tux Kart console just press **CTRL-A CTRL-D**. This will leave it running and you can reconnect to it again.

I have only tested this on a Ubuntu 16.04 server...

If you want to turn off the server respawning type "**touch /root/megamek/nostart**". To reenable it type "**rm /root/megamek/nostart**".

---
Note: If you don't already have the "screen" tool installed you will need to install it by "**sudo apt-get install screen**".
