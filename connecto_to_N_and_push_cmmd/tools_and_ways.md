# Pdsh tool
[pdsh man](https://www.admin-magazine.com/HPC/Articles/pdsh-Parallel-Shell)
```
$ pdsh -v
pdsh: invalid option -- 'v'
Usage: pdsh [-options] command ...
-S                return largest of remote command return values
-h                output usage menu and quit
-V                output version information and quit
-q                list the option settings and quit
-b                disable ^C status feature (batch mode)
-d                enable extra debug information from ^C status
-l user           execute remote commands as user
-t seconds        set connect timeout (default is 10 sec)
-u seconds        set command timeout (no default)
-f n              use fanout of n nodes
-w host,host,...  set target node list on command line
-x host,host,...  set node exclusion list on command line
-R name           set rcmd module to name
-M name,...       select one or more misc modules to initialize first
-N                disable hostname: labels on output lines
-L                list info on all loaded modules and exit
available rcmd modules: ssh,exec (default: ssh)
```
```
$ pdsh -w 192.168.1.250 uname -r
192.168.1.250: 2.6.32-431.11.2.el6.x86_64
```
```
$ pdsh -w ssh:laytonjb@192.168.1.250 uname -r
192.168.1.250: 2.6.32-431.11.2.el6.x86_64
```
