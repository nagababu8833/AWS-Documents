### Userdata

```
#!/bin/bash
yes | sudo apt update
yes | sudo apt install apache2
sudo bash -c 'echo "<h1>Server Details</h1><p><strong>Hostname:</strong> $(hostname)
</p><p><strong>IP Address:</strong> $(hostname -I | awk '\''{print $1}'\'')</p>" > /var/www/html/index.html'
sudo systemctl restart apache2

```
