# mikrotik-custom-watchdog
Custom MikroTik watchdog

Run 'mikrotik-setup' file to configure your router to use it.

You'll need to run `/system script ping` command to update current timestamp on the router.

ssh admin@<ip-address> "/system script ping" should work for you.
