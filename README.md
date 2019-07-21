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
## Import CSV to ES
- Copy the `import-csv.conf` file to logstash directory `(/usr/share/logstash)` or somewhere else
- Specify path to your csv file in the input csv path
- Define column names in the filter and transformation options (Optional)
- Specify elastic instance information in the output

Navigate to logsatsh bin directiry `(/usr/share/logstash/bin)` and run this command as root:
```
./logstash -f /path/to/import-csv.conf
```

## Import PG table to ES
- Copy the `import-pg.conf` file to logstash directory `(/usr/share/logstash)` or somewhere else
- Put postgres connection string in input jdbc and define your SQL statement
- Specify elastic instance information in the output

Navigate to logsatsh bin directiry `(/usr/share/logstash/bin)` and run this command as root:
```
./logstash -f /path/to/import-pg.conf
```
