# Week 9 Project: Honeypot

Time spent: 10 hours spent in total

### Project summery 

In this project we stand up a basic honeypot and demonstarte its effectiveans at detecting and collecting data about an attack. The project requires to use a well-supported open source honeypot, which is Modern Honey Network(MHN). MHN is a centralized server for management and data collection of honeypots.

### Milestone 0 : Google Cloude Set Up

To accomplish this project we required to set up Google Cloud Platforms(GCP) Free Tier or alternative one Cloud Platforms. After setting up the platform we initialized the zone and region.

### Milestone 1 : Create MHN Admin VM 

Since GCP require to create the firewall rules seperatley and then apply them to the VM we require to use the following attrubutes.

- Ubuntu 14.04(trusty)
- HTTP traffic allowed(port 80)
- TCP ports 3000 and 100000

Command used 
gcloud beta compute firewall-rules create mhn-allow-admin --direction=INGRESS --priority=1000 --network=default --action=ALLOW --rules=tcp:3000,tcp:10000 --source-ranges=0.0.0.0/0 --target-tags=mhn-admin

<img src="https://i.imgflip.com/27zrzp.gif" title="made at imgflip.com"/>
