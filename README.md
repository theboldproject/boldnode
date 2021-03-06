# Bold Masternode
### Bash installer for Bold Masternode on Ubuntu 16.04 LTS x64

#### This shell script comes with 3 maintenance cronjobs: 
1. Make sure the daemon is always running: `makerun.sh`
2. Make sure the daemon is never stuck: `checkdaemon.sh`
4. Clear the log file every other day: `clearlog.sh`

#### You will need:
1. Your genkey, generated from your Bold wallet using 'masternode genkey' in the Debug console
2. A custom port for SSH, as firewall will be enabled and only the custom port will be allowed for SSH

#### Login to your vps as root, download the install.sh file and then run it:
```
wget https://raw.githubusercontent.com/theboldproject/boldnode/master/install.sh && bash ./install.sh
```

#### On the client-side, add the following line to bold.conf:
```
masternode_alias vps-ip:18200 genkey collateral-txhash outputidx
```

#### Run the qt wallet, go to Masternodes tab, choose your node and click the "start alias" button, or from the debug console in your qt wallet, type "startmasternode alias false mn-alias" (without the quotes, where mn-alias is the alias or name of your masternoded).

#### Your masternode should be setup now!
