# My customized F5 Google Deployment Manager Templates

This is my customized version of F5 Google Deployment Manager Templates.

## Customized Templates
List of customized templates:
**Standalone BIG-IP VE - 3 NIC**
- <a href="https://github.com/simonkowallik/f5-google-gdm-templates/tree/master/supported/standalone/3nic/existing-stack/byol">**BYOL**</a> (bring your own license), which allows you to use an existing BIG-IP license.

list of changes:
- changes mgmt nic to eth2 (nic2) to enable gcp Load Balancer and forwarding-rules to work with nic0/eth0
- configures eth0/nic0 as external, eth1/nic1 as internal, eth2/nic2 as managment
- changes NTP from us to google cloud NTP 169.254.169.254
- removes static 'bigip1-' prefix from VM instance name
- adds external IPs to all nics
- changes management-ip from dhcp to static configuration
- sets MTU to 1460 on all interfaces
- changes interface names in YAML
- removed subnetmask from YAML
- fetches subnetmask from google cloud apis
- changed availabilityZone1 to zone in YAML to follow google terminology


## Caution
- This repository might be out-of-date, please check the official F5 GDM Template version first
- The templates in this repository are unsupported by F5

Use custom templates at your own risk.

The official F5 GDM templates can be found at: https://github.com/F5Networks/f5-google-gdm-templates
Official <a href="https://github.com/F5Networks/f5-google-gdm-templates/blob/master/README.md">README.md</a>.


# F5: License / Copyright

## Copyright

Copyright 2014-2018 F5 Networks Inc.


## License

### Apache V2.0

Licensed under the Apache License, Version 2.0 (the "License"); you may not use
this file except in compliance with the License. You may obtain a copy of the
License at:

http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and limitations
under the License.


### Contributor License Agreement

Individuals or business entities who contribute to this project must have
completed and submitted the `F5 Contributor License Agreement`
