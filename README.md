### Set of Munin plugins to monitor EOS node and related EOS account 

<img src="eosmem.png" alt="munin screenshot"/>

Example: http://junglebp.atticlab.net/ATTICLAB.NET/JUNGLEBP.ATTICLAB.NET/index.html#eos

##### List of plugins: 
eos_balance, eos_chain, eos_net, eos_cpu, eos_quota - account related plugins...


eos_mem - EOS node memory consumption plugin

##### Configuration: 
echo "[eos_*]  
env.ACCOUNT eosaccount  
env.DATADIR /opt/EOSmainNet
" >> /etc/munin/plugin-conf.d/eos

...
where DATADIR path to your nodeos catalog with blocks and state catlogs

##### Usage
just place plugin in /usr/share/munin/plugins

$ sudo chmod 755 /usr/share/munin/plugins/eos*

$ sudo ln -s /usr/share/munin/plugins/eos* /etc/munin/plugins/

$ sudo service munin-node restart
