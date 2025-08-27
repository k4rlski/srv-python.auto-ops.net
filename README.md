# srv-python.auto-ops.net
server that ran the data sync perfect but now needs to retire to save on cost

# main tool:

The data sync or sync-data app whichever we call it, is documented in it's own repo here:

data-sync: https://github.com/k4rlski/data-sync

sync-data: https://github.com/k4rlski/sync-data

dsx-data-sync-io: https://github.com/k4rlski/dsx-data-sync-io

## AI chats for this were at:



## host info
```
root@python:~# hostname
python.auto-ops.net
root@python:~# cat /etc/hosts
# /etc/hosts
127.0.0.1	localhost
45.79.148.135	python.auto-ops.net

# The following lines are desirable for IPv6 capable hosts
::1		localhost ip6-localhost ip6-loopback
ff02::1		ip6-allnodes
ff02::2		ip6-allrouters
root@python:~# cat /etc/resolv.conf
# This is /run/systemd/resolve/stub-resolv.conf managed by man:systemd-resolved(8).
# Do not edit.
#
# This file might be symlinked as /etc/resolv.conf. If you're looking at
# /etc/resolv.conf and seeing this text, you have followed the symlink.
#
# This is a dynamic resolv.conf file for connecting local clients to the
# internal DNS stub resolver of systemd-resolved. This file lists all
# configured search domains.
#
# Run "resolvectl status" to see details about the uplink DNS servers
# currently in use.
#
# Third party programs should typically not access this file directly, but only
# through the symlink at /etc/resolv.conf. To manage man:resolv.conf(5) in a
# different way, replace this symlink by a static file or a different symlink.
#
# See man:systemd-resolved.service(8) for details about the supported modes of
# operation for /etc/resolv.conf.

nameserver 127.0.0.53
options edns0 trust-ad
search members.linode.com
```
## command history

```
ramses@darkstar:~/DEVOPS Dropbox/DEVOPS-KARL/CORE-v4/5-GRAVITY-TO-CRM/spellbook$ pybox
Welcome to Ubuntu 22.04.3 LTS (GNU/Linux 5.15.0-83-generic x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage

  System information as of Wed Aug 27 07:08:41 AM UTC 2025

  System load:           0.16796875
  Usage of /:            5.9% of 156.93GB
  Memory usage:          7%
  Swap usage:            0%
  Processes:             124
  Users logged in:       0
  IPv4 address for eth0: 45.79.148.135
  IPv6 address for eth0: 2600:3c03::f03c:93ff:fe37:980c


Expanded Security Maintenance for Applications is not enabled.

90 updates can be applied immediately.
1 of these updates is a standard security update.
To see these additional updates run: apt list --upgradable

Enable ESM Apps to receive additional future security updates.
See https://ubuntu.com/esm or run: sudo pro status


*** System restart required ***
Last login: Mon Jul 28 04:11:09 2025 from 223.206.213.234
root@python:~# crontab -l
*/2 * * * * /usr/bin/python3 /app/data-sync.py >> /app/log_file 2>&1
root@python:~# ll /home
total 12
drwxr-xr-x  3 root   root   4096 Oct 30  2023 ./
drwxr-xr-x 20 root   root   4096 Nov  2  2023 ../
drwxr-x---  5 rgrant rgrant 4096 Nov  2  2023 rgrant/
root@python:~# history
    1  hostnamectl set-hostname python.auto-ops.net
    2  nano /etc/hosts
    3  sudo systemctl restart systemd-hostnamed
    4  hostname
    5  exit
    6  history
    7  mysqldump --column-statistics=0 -h perm-track.com -u permtrak_migration -pwFXjE5r9akolm6bHjL permtrak_suga904 cases_perm_cases > fixed_relate_dump.sql
    8  ll
    9  mysql -h perm-track.dev -u permtrackdev_migration -pwFXjE5r9akolm6bHjL permtrackdev_549 -e "DELETE FROM t_e_s_t_p_e_r_m;"
   10  ll
   11  vi master-map.json 
   12  vi python-migration.py 
   13  mysql -h perm-track.dev -u permtrackdev_migration -pwFXjE5r9akolm6bHjL permtrackdev_permtrak < fixed_relate_dump.sql
   14  ll
   15  python3 python-migration.py
   16  history
   17  sudo apt update
   18  sudo apt upgrade
   19  sudo apt install python3-pip
   20  pip install pandas
   21  pip install sqlalchemy
   22  pip install pymysql
   23  pip install mysqlclient
   24  pip install --upgrade pandas sqlalchemy
   25  ll
   26  python3 drop_local_tbl_get_remote_tbl.py
   27  pip install mysql.connector
   28  python3 drop_local_tbl_get_remote_tbl.py
   29  ifconfig -a
   30  apt install net-tools
   31  ifconfig -a
   32  python3 drop_local_tbl_get_remote_tbl.py
   33  ll
   34  rm dump.sql 
   35  python3 drop_local_tbl_get_remote_tbl.py
   36  ll
   37  less dump.sql 
   38  mysqldump -h [perm-track.com] -u [permtrak_migration] -p[wFXjE5r9akolm6bHjL] [permtrak_suga904] [cases_perm_cases] > test_dump.sql
   39  apt install mysql-client-core-8.0
   40  mysqldump -h [perm-track.com] -u [permtrak_migration] -p[wFXjE5r9akolm6bHjL] [permtrak_suga904] [cases_perm_cases] > test_dump.sql
   41  ping perm-track.com
   42  mysqldump -h perm-track.com -u permtrak_migration -pwFXjE5r9akolm6bHjL permtrak_suga904 cases_perm_cases > test_dump.sql
   43  ll
   44  less test_dump.sql 
   45  rm dump.sql 
   46  python3 drop_local_tbl_get_remote_tbl.py
   47  ll
   48  less dump.sql 
   49  root@python:~# python3 drop_local_tbl_get_remote_tbl.py
   50  Attempting to connect to remote target database...
   51  Connected. Dropping table cases_perm_cases...
   52  Table cases_perm_cases dropped successfully.
   53  Attempting to export remote source table...
   54  Export result: 
   55  Attempting to import to remote target table...
   56  Import result: 
   57  Table exported from permtrak_suga904 on perm-track.com and imported to permtrackdev_permtrak on perm-track.dev
   58  root@python:~# ll
   59  total 27884
   60  drwx------  6 root root     4096 Oct 28 14:50 ./
   61  drwxr-xr-x 19 root root     4096 Oct 27 12:21 ../
   62  -rw-------  1 root root      116 Oct 27 18:06 .bash_history
   63  -rw-r--r--  1 root root     3106 Oct 15  2021 .bashrc
   64  drwx------  3 root root     4096 Oct 27 18:09 .cache/
   65  -rw-r--r--  1 root root      488 Oct 28 07:33 db_creds.py
   66  -rw-r--r--  1 root root     2056 Oct 28 14:32 drop_local_tbl_get_remote_tbl.py
   67  -rw-r--r--  1 root root        0 Oct 28 14:50 dump.sql
   68  -rw-------  1 root root       20 Oct 28 14:49 .lesshst
   69  drwxr-xr-x  3 root root     4096 Oct 27 14:22 .local/
   70  -rw-r--r--  1 root root      161 Jul  9  2019 .profile
   71  drwxr-xr-x  2 root root     4096 Oct 28 14:35 __pycache__/
   72  drwx------  2 root root     4096 Oct 27 12:21 .ssh/
   73  -rw-r--r--  1 root root 28501044 Oct 28 14:48 test_dump.sql
   74  root@python:mysql -h perm-track.dev -u permtrackdev_migration -pwFXjE5r9akolm6bHjL permtrackdev_permtrak < test_dump.sql
   75  mysql -h perm-track.dev -u permtrackdev_migration -pwFXjE5r9akolm6bHjL permtrackdev_permtrak < test_dump.sql
   76  ll
   77  rm dump.sql 
   78  rm test_dump.sql 
   79  python3 drop_local_tbl_get_remote_tbl.py
   80  mysqldump -h perm-track.com -u permtrak_migration -pwFXjE5r9akolm6bHjL permtrak_suga904 cases_perm_cases > test_dump2.sql
   81  mysql -h perm-track.dev -u permtrackdev_migration -pwFXjE5r9akolm6bHjL permtrackdev_permtrak < test_dump2.sql
   82  mysql -h perm-track.dev -u permtrackdev_migration -pwFXjE5r9akolm6bHjL permtrackdev_549 -e "DELETE FROM t_e_s_t_p_e_r_m;"
   83  ll
   84  python3 python-migration.py
   85  ll
   86  adduser rgrant
   87  usermod -aG sudo rgrant
   88  su - rgrant
   89  ll
   90  cd /home/rgrant/
   91  ll
   92  ls -alhF
   93  cd /
   94  ll
   95  cd app/
   96  ll
   97  tail -f log_file
   98  mysqldump -h perm-track.com -u permtrak_migration -p'wFXjE5r9akolm6bHjL' permtrak_suga904 > prod_backup.sql
   99  mysqldump -h perm-track.dev -u permtrackdev_migration -p'wFXjE5r9akolm6bHjL' permtrackdev_permtrak > target_backup.sql
  100  mysqldump -h perm-track.dev -u permtrackdev_k -p'S@fa_7)pH7f"LTJ' permtrackdev_permtrak > target_backup.sql
  101  mysqldump --no-tablespaces -h perm-track.dev -u permtrackdev_migration -p permtrackdev_permtrak > target_backup.sql
  102  ifconfig -a
  103  mysqldump --no-tablespaces -h perm-track.dev -u permtrackdev_migration -p permtrackdev_permtrak > target_backup.sql
  104  mysqldump --no-tablespaces -h perm-track.dev -u permtrackdev_k -p permtrackdev_permtrak > target_backup.sql
  105  ll
  106  date
  107  python3 python-prod-to-copy.py
  108  date
  109  cd /
  110  cd app/
  111  ll
  112  less python-migration.py
  113  ifconfig -a
  114  while true; do clear; date; sleep 10; done
  115  while true; do clear; date; sleep 1; done
  116  cd /
  117  cd app/
  118  ll
  119  tail -f log_file 
  120  cd /
  121  cd app/
  122  ll
  123  tail -f log_file
  124  cd app
  125  cd /
  126  cd app/
  127  ll
  128  crontab -l
  129  ll
  130  history
  131  tail -f log_file
  132  crontab -l
  133  ll
  134  cd /
  135  cd app/
  136  tail -f log_file 
  137  crontab -l
  138  less /app/data-sync.py
  139  tail -f log_file 
  140  crontab -e
  141  tail -f log_file 
  142  crontab -e
  143  tail -f log_file 
  144  crontab -e
  145  tail -f log_file 
  146  crontab -e
  147  tail -f log_file 
  148  cd ..
  149  cd app/
  150  ll
  151  pwd
  152  exit
  153  crontab -l
  154  tail -f log_file 
  155  cd ..
  156  cd app/
  157  tail -f log_file 
  158  cd /
  159  cd app/
  160  tail -f log_file 
  161  cd /
  162  cd app/
  163  vi data-sync.py
  164  cd /
  165  cd app/
  166  tail -f log_file 
  167  less data-sync.py 
  168  tail -f log_file 
  169  less master-map.json 
  170  w
  171  tail -f log_file 
  172  less data-sync.py 
  173  tail -f log_file 
  174  ll
  175  pwd
  176  python3 field-updater.py
  177  w
  178  cd /app/
  179  tail -f log_file 
  180  vi master-map.json
  181  tail -f log_file 
  182  vi master-map.json
  183  tail -f log_file 
  184  ll
  185  less master-map.json 
  186  pwd
  187  crontab -l
  188  tail -f log_file 
  189  cd /
  190  cd app/
  191  tail -f log_file 
  192  cd /
  193  cd app/
  194  tail -f log_file 
  195  ll
  196  ls -alhF
  197  crontab -l
  198  cd /var/log/
  199  ll
  200  tail -f /var/log/syslog
  201  cd /
  202  cd app/
  203  ll
  204  tail -f /var/log/syslog
  205  multitail
  206  apt install multitail
  207  multitail log_file /var/log/syslog /var/log/auth.log
  208  ps ax | grep data-sync.py
  209  multitail log_file /var/log/syslog /var/log/auth.log
  210  cd /var/log/
  211  cd /app
  212  tail -f log_file 
  213  cd /app/
  214  ll
  215  cd /app/
  216  tail -f log_file 
  217  cd /app/
  218  tail -f log_file 
  219  cd /app/
  220  tail -f log_file 
  221  cd /app/
  222  ll
  223  cd sync_files/
  224  ll
  225  cd ..
  226  ll
  227  less data-sync.py
  228  tail -f log_file 
  229  top
  230  history
  231  cd app
  232  pwd
  233  cd /app/
  234  tail -f log_file
  235  less master-map.json
  236  vi master-map.json
  237  tail -f log_file
  238  crontab -e
  239  cd /app/
  240  tail -f log_file
  241  cd /app/
  242  tail -f log_file
  243  cd /app/
  244  tail -f log_file
  245  less master-map.json 
  246  nano master-map.json
  247  vi master-map.json 
  248  cd /app/
  249  tail -f log_file
  250  cd /app/
  251  tail -f log_file
  252  exit
  253  cd /app/
  254  tail -f log_file
  255  cd /app/
  256  tail -f log_file
  257  history
  258  multitail log_file /var/log/syslog /var/log/auth.log
  259  cd app
  260  ll
  261  cd ..
  262  ll
  263  cd app
  264  tail -f log_file
  265  exit
  266  tail -f /app/log_file
  267  alias
  268  pwd
  269  cd app
  270  ll
  271  cd ..
  272  cd app/
  273  ll
  274  vim statdata
  275  vim statdata.sh
  276  vim ~/.bashrc 
  277  source ~/.bashrc 
  278  statdata
  279  ping raven.d4t4crypt.org
  280  statdata
  281  crontab -l
  282  statdata
  283  tcpdump -v
  284  statdata
  285  ps ax | grep data-sync
  286  statdata
  287  tcpdump -vvv
  288  statdata
  289  tcpdump
  290  statdata
  291  tcpdump -vvv
  292  statdata
  293  tcpdump
  294  statdata
  295  tcpdump
  296  stadata
  297  statdata
  298  tcpdump
  299  statdata
  300  tcpdump
  301  statdata
  302  tcpdump 
  303  statdata
  304  tcpdump 
  305  statdata
  306  tcpdump 
  307  statdata
  308  tcpdump 
  309  statdata
  310  tcpdump
  311  statdata
  312  tcpdump
  313  statdata
  314  tcpdump
  315  statdata
  316  tcpdump
  317  statdata
  318  tcpdump
  319  statdata
  320  tcpdump
  321  statdata
  322  tcpdump
  323  statdata
  324  tcpdump
  325  statdata
  326  tcpdump
  327  statdata
  328  tcpdump
  329  statdata
  330  tcpdump
  331  statdata
  332  tcpdump
  333  statdata
  334  tcpdump
  335  statdata
  336  tcpdump
  337  statdata
  338  tcpdump
  339  statdata
  340  tcpdump
  341  statdata
  342  tcpdump
  343  statdata
  344  tcpdump
  345  statdata
  346  tcpdump
  347  statdata
  348  tcpdump
  349  statdata
  350  tcpdump
  351  statdata
  352  tcpdump
  353  statdata
  354  tcpdump
  355  statdata
  356  tcpdump
  357  statdata
  358  tcpdump
  359  statdata
  360  tcpdump
  361  statdata
  362  tcpdump
  363  statdata
  364  tcpdump
  365  statdata
  366  tcpdump
  367  statdata
  368  tcpdump
  369  statdata
  370  tcpdump
  371  statdata
  372  tcpdump
  373  statdata
  374  tcpdump
  375  statdata
  376  tcpdump
  377  statdata
  378  tcpdump
  379  statdata
  380  tcpdump
  381  statdata
  382  tcpdump
  383  statdata
  384  tcpdump
  385  statdata
  386  tcpdump
  387  statdata
  388  tcpdump
  389  statdata
  390  tcpdump
  391  statdata
  392  tcpdump
  393  statdata
  394  tcpdump
  395  statdata
  396  tcpdump
  397  statdata
  398  tcpdump
  399  statdata
  400  tcpdump
  401  statdata
  402  tcpdump
  403  statdata
  404  uname -a
  405  ifconfig -a
  406  pwd
  407  ll
  408  locate data-sync.py
  409  apt install plocate
  410  locate data-sync.py
  411  crontab -e
  412  crontab -l
  413  statdata
  414  cd /app/
  415  statdata
  416  crontab -l
  417  alias
  418  statdata
  419  cd app
  420  cd /app/
  421  statdata
  422  crontab -l
  423  ll
  424  python3 data-sync.py 
  425  crontab -e
  426  statdata
  427  cd /app/
  428  statdata
  429  cd ..
  430  cd app/
  431  statdata
  432  cd ..
  433  cd app/
  434  ll
  435  statdata
  436  crontab -l
  437  ll /home
  438  history
root@python:~# statdata
Columns: [id, name, description, deleted, assigned_user_id, rank, city, state, circulation, owner, phone, email, website, contactname, weburl, verifycontacts, emailmain, phonemain, emailformatquote, msa, shortname]
Index: []
2025-08-27 07:08:11.762266 : No new records to write to news database
2025-08-27 07:08:13.520184 : No new records to write to local
2025-08-27 07:08:14.773650 : No new records to write to accounting
2025-08-27 07:08:17.868897 : No new records to write to abbreviations
2025-08-27 07:08:19.576436 : No new records to write to online
2025-08-27 07:08:22.518779 : No new records to write to radio
2025-08-27 07:08:23.784190 : No new records to write to s_w_a
2025-08-27 07:08:23.784237 : Finished cron job- python-migration.py
^X^X^C
root@python:~# 

```
