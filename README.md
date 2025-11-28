# TelegrafStuff


Telegraf - for Grafana


wget https://dl.influxdata.com/telegraf/releases/telegraf-1.36.4_windows_amd64.zip -UseBasicParsing -OutFile telegraf-1.36.4_windows_amd64.zip
Expand-Archive .\telegraf-1.36.4_windows_amd64.zip -DestinationPath 'C:\Program Files\InfluxData\telegraf'

docker pull telegraf

wget -q https://repos.influxdata.com/influxdata-archive.key


gpg --show-keys --with-fingerprint --with-colons ./influxdata-archive.key 2>&1 | grep -q '^fpr:\+24C975CBA61A024EE1B631787C3D57159FC2F927:$' && cat influxdata-archive.key | gpg --dearmor | sudo tee /etc/apt/trusted.gpg.d/influxdata-archive.gpg > /dev/null


echo 'deb [signed-by=/etc/apt/trusted.gpg.d/influxdata-archive.gpg] https://repos.influxdata.com/debian stable main' | sudo tee /etc/apt/sources.list.d/influxdata.list


sudo apt-get update && sudo apt-get install telegraf

