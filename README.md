# eos-munin-plugin

### Munin plugin to monitor EOS node (state db, blocks db) memory consumption

<img src="eosmem.png" alt="munin screenshot"/>

##### Configuration:
echo "[eosmem*]

env.DATADIR /opt/EOSmainNet
" >> /etc/munin/plugin-conf.d/eosmem

...
where DATADIR path to your nodeos catalog with blocks and state catlogs

##### Usage: 
just place plugin in /usr/share/munin/plugins/eosmem

$ chmod 755 /usr/share/munin/plugins/eosmem

$ ln -s /usr/share/munin/plugins/eosmem /etc/munin/plugins/eosmem

$ sudo service munin-node restart
