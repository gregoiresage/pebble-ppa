# What's in the packages
## pebble-sdk
This package will install the *Pebble Tool* in your system :
* ```/usr/share/pebble-sdk``` : contains all the pebble tool's dependencies
* ```/usr/bin/pebble``` : the Pebble command

## pebble-sdk-extras
This package will install extra tools for Pebble developments :
* ```/etc/bash_completions.d/pebble_completion``` : provides autocompletion for the pebble command

# How to install the packages
```
sudo add-apt-repository ppa:gregoire-sage/pebble-sdk
sudo apt-get update
sudo apt-get install pebble-sdk pebble-sdk-extras
```




# How to build and upload the packages
```
cd pebble-sdk
dbuild -S
cd ../pebble-sdk-extras
debuild -S
cd ..
dput ppa:gregoire-sage/pebble-sdk ../pebble-sdk_4.1.1.0_source.changes
dput ppa:gregoire-sage/pebble-sdk ../pebble-sdk-extras_0.0.0.1_source.changes
```
