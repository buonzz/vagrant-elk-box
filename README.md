# ElasticSearch, Logstash and Kibana

A simple Ubuntu box with ELK stack installed

## Requirements

* VirtualBox
* Vagrant


## Installation

clone the repo

```
git clone https://github.com/buonzz/vagrant-elk-box.git
```
provision the box
```
cd vagrant-elk-box
vagrant up
```

This might take a while as it downloads stuffs and install them.(dont worry about the red-caption things, it will run to completion, I promise)

## Usage

* [http://localhost:5601/](http://localhost:5601/) - Kibana
* [http://localhost:9200/](http://localhost:9200/) - ElasticSearch

To use logstash, you need to login to the VM itself

```
vagrant ssh
/opt/logstash/bin/logstash
```

