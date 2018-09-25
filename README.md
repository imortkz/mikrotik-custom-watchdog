# Custom MikroTik watchdog
It will remember a timestamp when booted and will reboot the router is no incoming events received in 10 minutes (by default)
Timestamp can be updated using remote API call or SSH command to run script `/system script run ping`

Upload the file `setup.rsc` and run the command below to configure your router:

```
/import setup.rsc
```

Reboot the router to start the watchdog!

**Warning!**
You'll need to run `/system script run ping` command to update current timestamp on the router for each 10 minutes at least
to prevent your router to be rebooted!

## Linux example

```
ssh -P $sshport -pw $password admin@$routerip "/system script run ping"
```

## Windows example

```
plink -P $sshport -pw $password admin@$routerip "/system script run ping"
```
Replace $sshport with your SSH port, $password with your admin password and $routerip with your actual router IP.

You can download plink utility [here](https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html)
