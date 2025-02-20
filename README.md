# GVE_DevNet_Meraki_License_Renewal
This repository holds a web application for consulting Meraki license expiration dates. It allows for Cisco partners to get an overview of the Meraki products and corresponding licenses currently in use at all Meraki organizations at their customers, as well as their expiration dates, the time left until expiration, and end of sale/support information. In contrast, the Meraki dashboard only shows this information per Meraki organization. Cisco partners can log into the tool using their name, country, corporate e-mail, and Meraki API keys they are permitted to use. To ease the interaction, partners can moreover specify a *deadline* - licenses expiring within that deadline will be displayed as "Expiring". For tool administrators, the tool provides a log of all requests it previously processed, including the partner information, deadline, and number of expired/expiring licenses.

## High Level PoV Overview

![](IMAGES/highlevel.png)

## Contacts
* Stien Vanderhallen (stienvan@cisco.com)
* Ramona Renner (ramrenne@cisco.com)

## Solution Components
* Meraki REST API
* Python
* Django
* PostgreSQL 

## Configuring the application

### 1. Clone repository

```
$ git clone https://github.com/Radmanded/gve_devnet_meraki_license_renewal.git
$ cd gve_devnet_meraki_license_renewal
```

## Starting the application
 
### 1. Build local Django application:

*NOTE: Must ensure lines 93-96 are **NOT** commented in `gve_devnet_meraki_license_renewal/merakirenewal/merakirenewal/settings.py`*

# Screenshot

- **Changes to Lines 93-96**
![](IMAGES/Lines93-96.png) **Deleted #** ![](IMAGES/Lines93-96-2.png)

## Terminal
```
$ python3 -m venv venv
$ source venv/bin/activate
$ pip install -r requirements.txt
$ cd merakirenewal
$ python manage.py runserver
```

### 2. In a browser, navigate to `localhost:8000`

# Screenshots

- Login page
![](IMAGES/login.png)

- License information overview
![](IMAGES/overview.png)

- For tool administrators: log overview
![](IMAGES/logs.png)

### Using the License Renewal Tool

- Enter you name and country

- Enter **j@cisco.com** in the E-mail Address 

- Enter API keys manually or import from CSV

- Enter the number of days 

### Troubleshooting

**Images not loading?**
- Ensure Debug=True  in /merakirenewal/merakirenewal/settings.py

# Screenshots
![](IMAGES/djangoline.png)

### LICENSE

Provided under Cisco Sample Code License, for details see [LICENSE](LICENSE.md)

### CODE_OF_CONDUCT

Our code of conduct is available [here](CODE_OF_CONDUCT.md)

### CONTRIBUTING

See our contributing guidelines [here](CONTRIBUTING.md)

#### DISCLAIMER:
<b>Please note:</b> This script is meant for demo purposes only. All tools/ scripts in this repo are released for use "AS IS" without any warranties of any kind, including, but not limited to their installation, use, or performance. Any use of these scripts and tools is at your own risk. There is no guarantee that they have been through thorough testing in a comparable environment and we are not responsible for any damage or data loss incurred with their use.
You are responsible for reviewing and testing any scripts you run thoroughly before use in any non-testing environment.
