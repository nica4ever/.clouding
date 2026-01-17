# .clouding
### Personal cloud engineering project

## Context
Hello my name is Cojanu Ionut and in this journey I will document my journey from nothing to something, I aim to discover as much as possible and learn 10x more.

### Setup

The OS of choice will be Red Hat Enterprise Linux in order to get RHEL for cheap I accessed the Red Hat Developer subscription(https://tinyurl.com/3u4p26zb) which gives me access to RHEL 10. In the following table you can see the install options that I picked:

|   Base Env   |       Addons        |
|--------------|---------------------|
| Minimal base | Standard            |
|              | Network Services    |
|              | Security            |
|              | Container Management|

I always asked myslef how can one homelab without a homelab or even without a home. For context I find myself in this position so while the dumpster next to me keeps me warm and I managed to steal the wifi password of a venue close by, I also realized that it is possible to build a cloud within a cloud. Therefore RHEL 10 will be installed on virtual private servers(vps), the platform of choice is HETZNER(https://www.hetzner.com/), where renting four vpss cost around 24-30 EUR per month. In the following table you can see the specs of each server(they also have more powerful options but for this project this is enough, also I am homeless):

| Description | Size|
|-------------|-----|
| VirtualCPU  |  4  |
| RAM         |  8  |
| Disk Local  |80GiB|

The installed os will not have a GUI and using the console provided by HETZNER is not a very professional thing to do not even for a homeless person. I might not have a home but I do have dignity. Therefore we can take advantage of the following, the servers that were created have a public ip by default so all that I had to do was to generate a ssh key:

```bash
$ ssh-keygen -t ed25519 -C "home@less.com"
```
Then we can use the ssh-copy-id command to enroll the keys directly into each server using the public ip:

```bash
$ ssh-copy-id -i ~/.ssh/id_ed25519.pub homeless@server_ip
```
So at this point I basically have a homelab setup that does not require a home and not even a lab.

### Why RHEL

I never understood why I had such a great deal of respect for Red Hat Enterprise Linux, but after using fedora for a couple of weeks now and playing with RHEL I can say that whoever is in charge of this is a very smart person.

After securing ssh access to my servers I realized that I know nothing about containers docker and what a production environment is, yet my brain is working, still, and I understood the concept, also having four servers means that I need to monitor them and bring them together, and while on paper all of that is doable and is work that I do not want to skip, I have also felt that the smartest thing to do is to create a web interface my servers only have cli and I only need podman and whatever I will put on podman. But how am I to create a webUI from scratch while also trying to do my first cloud project.......well RHEL has something that is called cockpit and now I have a webUI that I can access anytime from anywhere, All of this with just a free subscription......for a person who seeks to escape the streets this feels like a blessing.

I will not shy away from the work of manually configuring podman via cli do not get me wrong there is only one way out of being homeless and that is thru hard work, but to be able to use the web UI and get something up and running for me feels like a great tool that will help me to understand and learn more.
# Work in progress...
