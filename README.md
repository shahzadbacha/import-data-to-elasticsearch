# import-data-to-elasticsearch
Import/index csv,postgres data to elasticsearch using logstash

## Install ELK stack

Download and install the Public Signing Key:
```
 wget -qO - https://artifacts.elastic.co/GPG-KEY-elasticsearch | sudo apt-key add -
 ```
Save the repository definition to /etc/apt/sources.list.d/elastic-7.x.list:
```
 echo "deb https://artifacts.elastic.co/packages/7.x/apt stable main" | sudo tee -a /etc/apt/sources.list.d/elastic-7.x.list
 ```
 
 Run sudo apt-get update and the repository is ready for use. You can install it with:
 ```
 sudo apt-get update
 sudo apt-get install elasticsearch
 sudo apt-get install logstash
 sudo apt-get install kibana
```
