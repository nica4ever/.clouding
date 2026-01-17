# .clouding
Personal cloud engineering project

# Context
This is a personal cloud project in which I aim to create a full production setup

## Prerequisites

The OS of choice will be Red Hat Enterprise Linux in order to get RHEL for cheap I accessed the Red Hat Developer(https://tinyurl.com/3u4p26zb) subscription which allows me to install RHEL 10 on this four servers.

|   Base Env   |       Addons        |
|--------------|---------------------|
| Minimal base | Standard            |
|              | Network Services    |
|              | Security            |
|              | Container Management|

I always asked myslef how can one homelab without a homelab or even without a home. For context I find myself in this position so while the dumpster next to me keeps me warm and I managed to steal the wifi password of a venue close by I realized that it is possible to build a cloud within a cloud. Therefore RHEL 10 will be installed on virtual private servers(vps), the platform of choice is HETZNER(https://www.hetzner.com/), where renting four vpss cost around 24-30 EUR per month. In the following table you can see the specs of each server(they also have more porefull options but for this project this is enough):

| Description | Size|
|-------------|-----|
| VirtualCPU  |  4  |
| RAM         |  8  |
| Disk Local  |80GiB|

The installed os will not have a GUI and using the console provided by HETZNER is not porfi at all not even for a homeless person. I might not have a home but I do have dignity. Therefore we can take advantage of the following, the servers that were created have a public ip by default so all that I had to do was to generate a ssh key :


$ ssh-keygen -t ed25519 -C "home@less.com"

# Work in progress...
