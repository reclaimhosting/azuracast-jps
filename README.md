# Azuracast for Reclaim Cloud
AzuraCast is a self-hosted, all-in-one web radio management suite. Using its easy installer and powerful but intuitive web interface, you can start up a fully working web radio station in a few quick minutes. Read more on their website: https://www.azuracast.com/about/

## Deploy to Reclaim Cloud
[Click here to deploy to Reclaim Cloud](https://app.my.reclaim.cloud/?app=azuracast)

## Installation Instructions
You can find Azuracast by clicking Marketplace and navigating to the Education category or searching by name.
![Screen Shot 2020-07-12 at 9.13.45 AM|480x144](upload://ciTVzAuU1OScVz9ZHqoPFI7XOII.png) 

![Screen Shot 2020-09-04 at 8.16.13 PM|690x320, 75%](upload://8XxYuOcagl3ZhylPoyPuOJJE9lr.png) 

Installing is as easy as setting an environment name and region for the install. SSL will be provisioned automatically for the environment and your install will be up and running after several minutes. The installer dialog will provide and administrative URL and login credentials once setup is complete.

![Screen Shot 2020-09-04 at 7.48.45 PM|690x388, 75%](upload://sjozPVxs74xG729JI7BT3csrEeT.jpeg) 

![Screen Shot 2020-09-04 at 7.48.52 PM|690x282, 75%](upload://3S75Iyw1H8WALKFej5TCEm5kAap.png) 

![Screen Shot 2020-09-04 at 8.07.58 PM|690x288, 75%](https://community.reclaimhosting.com/uploads/default/optimized/2X/e/e40323d5381b6cb60749c9a8e5b93f307c633335_2_517x216.png) 

Once the install is complete your copy of Azuracast is online and available at the provided URL.
![Screen Shot 2020-09-04 at 8.09.07 PM|690x427, 75%](https://community.reclaimhosting.com/uploads/default/optimized/2X/9/969ca71a34895f5eb21425b98f38e7b308ad1ffa_2_517x320.jpeg) 

You can create your admin account with a username and password you enter, and in order to learn more about customizing Azuracast you can find more about both [system administration](https://www.azuracast.com/administration/) and [station management](https://www.azuracast.com/station-management/) in the documentation on their [website](https://www.azuracast.com/).

**Mapped Domain and SSL**
If you would like a custom domain for your radio station that is possible by adding a public IP address to your container:
![Screen Shot 2020-09-04 at 8.20.28 PM|690x168](https://community.reclaimhosting.com/uploads/default/optimized/2X/a/a4a0a837db4773f1f73812991ffe710e5a7b2df7_2_690x168.png) 

Once you have the IP address, you will need to point an A record for the domain being mapped to that IP address.

After that, you will need to access the SSL terminal and run the following commands to enable the SSL certificate for the newly mapped domain:
```
cd /var/azuracast
./docker.sh update-self
./docker.sh letsencrypt-create
```
