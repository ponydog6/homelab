# ![Homelab](images/xen-fu-panda.png "Homelab") Homelab - Xen Project Hypervisor
This Homelab is setup on AMD epic server using Xen Project Hypervisor.

- [Homelab images](docs/homelab-images "Homelab images")

The Xen Project hypervisor is an open-source type-1 or baremetal hypervisor, which makes it possible to run many instances of an operating system or indeed different operating systems in parallel on a single machine (or host).

- [Xen Project](https://xenproject.org "Xen Project")

- [Xen Project Hypervisor](https://xenproject.org/projects/hypervisor "Xen Project Hypervisor")

- [wiki.xenproject.org](https://wiki.xenproject.org/wiki/Main_Page "wiki.xenproject.org")

![Xen Project Architecture](images/xen-project-arch.png "Xen Project Architecture")


- Xen Project Hypervisor is compiled from [source code](https://xenproject.org/resources/downloads "source code").

- [Linux Kernel](https://kernel.org "Linux Kernel") running on VM as Guest OS is compiled from source code to run in PV mode.


- OpenVSwitch is setup on the host system as bridge between the VM’s and local LAN on one of the NIC interface.
- One of the VM is setup with ansible for automation using SSH keypairs.
- An internal DNS server is setup using BIND9.
- Container applications running on VM’s are orchestrated on Docker swarm.
- Traffic flow from public IP proxy’d through cloudflare is controlled using traefik.
- SSL certs are implemented using LetsEncript.
- Assign GPU to a VM and run LLM on it for AI assisted codeing/automation.
