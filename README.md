# Homelab
This repo describes my homelab sandbox system(s).

## Content
The sandbox entails:
* Infrastructure
    * DNS Server with `home.` zone
    * Consul for service discovery and dynamic DNS
* Hypervisor (KVM)
    * Automated vnet setup
    * Automated VM creation & config (virsh + cloud-init)
    * Automated VM image creation
        * baked-in Consul client service
On the VMs:
* K8s bootstrapping
    * VM provisioning
    * Node discovery with Consul
    * K8s setup

## Future
On the VMs:
* Load-Balancer
* Distributed storage

K8s sandbox:
* Monitoring
* Service Mesh

Infra:
* Network separation
* Linux based router & firewall
* HA

Automation:
* Replace Ansible with custom controller setup similar how K8s works
    * State in key-value store (desired, actual state)
    * Network management
    * VM management
        * Networks
        * Disks
    * "Managed" K8s service
    * Autoscaling
