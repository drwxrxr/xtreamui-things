# xtreamui-things
the things related with xtream-ui



This is an installation mirror for xtream ui software.

NOTE: This one is experimental, it may work or not. you can still use normal one with mysql or bitbucket one.

What is the difference from install.py with mysql one?​
it will use mariadb instead of mysql-server. it will add a mariadb repo (ams2.mirrors.digitalocean.com). it will install mariadb 10.5 and use libjemalloc1.
it has systemd unit file with a service script, "systemctl start/stop/restart/enable/disable xtreamcodes.service"
it has updated php-fpm config files and renamed them with 1,2,3,4. updated start_services.sh and nginx balance.conf file accordingly.
it has a new sysctl file, i hope it helps to big servers for better performance.
it will install "curl" from snap, no need to mess with libcurl34 anymore.
it will update files from xtreamui-things/admin-modified folder at first installation. you can find same commands at below.
How do I install?​
update your ubuntu first, then install panel


sudo apt-get update && sudo apt-get upgrade -y && sudo apt-get install software-properties-common libxslt1-dev libcurl3 libgeoip-dev python git -y;

rm install.py; wget https://github.com/emre1393/xtreamui_mirror/raw/master/withmariadb/install.py;

sudo python install.py


If you want to install main server with admin panel, choose MAIN.
If you want to install load balance on additional servers, add a server to panel in manage servers page, then run script and proceed with LB option.


note: newstuff.zip has same files from my xtreamui_things repo, i won't update this zip file anymore. if i change something on those files, you can download them.

git clone https://github.com/emre1393/xtreamui-things.git /tmp/xtreamui-things
cp -urv /tmp/xtreamui-things/admin-modified/* /home/xtreamcodes/iptv_xtream_codes/admin/
rm -rf /tmp/xtreamui-things
note2: also i still use same release_22f.zip file. if you want to use old install.py, go to bitbucket mirror page.
