MQTT
=========

Ansible role to deploy mosquitto on K3S

Requirements
------------

K8S Cluster
Longhorn 

Role Variables
--------------

manifest_folder: Folder where manifests are stored
mqtt_namespace: mqtt
mqtt_storage: 100M
mqtt_image: eclipse-mosquitto:1.6.12
mqtt_port: 31883

Dependencies
------------

-

Example Playbook
----------------

- hosts: controlpi
  environment:
  - KUBECONFIG: /home/pi/.kube/config
  roles:
  - { role: mqtt,
      tags: ['never','mqtt'] }

License
-------

Appache 2.0

Author Information
------------------

Marco Bradtke
