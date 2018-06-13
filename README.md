host_preparation

Description:
Subscribe a system to Red Hat, directly 

Behaviour:
Feature: Subscribe a system to Red Hat

Given a VM of capable size and power is available

Given the connection details to the VM are known

When A new RHEL-system has been installed

Then register it to Red Hat

Then attach subscriptions

Then disable all other repositories

Then enable base repository

Configuration:
Common variables used by this role:

Variable	        Description	       	

redhat_activationkeyRed Hat Activation Key	

redhat_organization_id	Red Hat Organization ID	
	
Usage:

How to invoke the role from a playbook:

- name: Subscribe to Red Hat

  include_role:
  
    name: host-preparation
    
  vars:
    redhat_activationkey: myuser
    
    redhat_organization_id: myuser
    
Note: add common variables to the vars list as required.
