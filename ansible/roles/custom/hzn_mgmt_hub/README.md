OpenHorizon Management Hub
==========================

Deploys an instance of the Open Horizon Management Hub.

Requirements
------------

- Ansible
- Debian-based and RHEL-based distros should work.

Role Variables
--------------

The role has several variables used to control the behavior of the role and the OpenHorizon management hub.

|Variable|Type|Description|
|-|-|-|
|agent_install|str|A path in this repository to a legacy agent install config, as you would pass into the install script. Used when running in install mode.|
|export_data|boolean|Writes the detected management hub deployment settings (including secrets) to a YAML file on the remote system.|
|install|boolean|Runs the playbook in installation mode (installs and syncs settings).|
|uninstall|boolean|Runs the playbook in uninstallation mode.|
|hzn_mgmt_hub|dict|A structured representation of the management hub deployment settings. This is automatically generated by the role when installing.|
|exchange_config|dict|Specifies a list of users and orgs which should exist on the target system.|

Dependencies
------------

Relies on a Docker role to ensure Docker is installed.
See `requirements.yml` for more details.

Example Playbook
----------------

An example playbook is included with this role. See "mgmt_hub.yml".
