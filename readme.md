# Guild start elastic search (and kibana) with docker

## Windows
Access linux in host windows
> wsl
Set env for linux system with root role
> sudo sysctl -w vm.max_map_count=262144
 

## Build compose
> docker compore up


After that,
Elastic search running in: http://localhost:9200/
Kibana running in: http://localhost:5601/app/kibana#/home

This repo have a example file data to execute.

## Insert data in json file to elastic server
> curl -H "Content-Type: application/json" -XPOST "localhost:9200/bank/_bulk?pretty&refresh" --data-binary "@accounts.json"
