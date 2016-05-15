# DBDCapital-Server

## Server setup
- Provider: DigitalOcean
- Tutorial:
  - http://feross.org/how-to-setup-your-linode//
- Tips
  - See listening ports
    - `netstat -tulpn`
  - Network interfaces
    - `ifconfig`
  - iptables
    - List all rules by specification: `sudo iptables -S`
    - List all rules in a table: `sudo iptables -L`
    - List with most details: `sudo iptables -nvL INPUT`
    - Log iptables traffix: http://askubuntu.com/questions/348439/iptables-log-file-and-how-change-it
    - tutorial: https://www.digitalocean.com/community/tutorials/a-deep-dive-into-iptables-and-netfilter-architecture
    - repos:
      - https://github.com/bmaeser/iptables-boilerplate
      - https://gist.github.com/virtualstaticvoid/1024546
      - https://gist.github.com/jirutka/3742890
  - fail2ban
    - start in debug mode: `/usr/bin/fail2ban-client -v -v start`
  - scp
    - Local to remote: `scp -P [port] /local/file [user]@[your_ip_address]:/remote/path`
    - Remote to local: `scp -P [port] [user]@[your_ip_address]:/remote/file/path /local/path`
  - htop setup
    - Display options - Highlight program "basename"
  - nvm
    - use this insteal of using system nodejs

## Config file
 - fail2ban config file
  - `scp -P 666 jail.local compass@dbdcapital:/etc/fail2ban/jail.local`
