<p align="center">
<img src="assets/true-nas-core-logo.svg" alt="Logo Text There" />
</p>

# TrueNAS Core deployment for backup and file sharing
Deployed TrueNAS Core to implement backup capabilities and file sharing within the organization. This solution centralizes data storage, improves data integrity, and provides secure and scalable file sharing functionalities.

## Environments and Technologies Used

- Proxmox VE virtual machine with PCI passthrough enabled for direct access to disks
- FreeNAS Mini 4 Bay 
    - 8-Core 2.4GHz Processor
    - 32GB RAM

## Operating Systems Used

- TrueNAS Core 11

## High-Level Deployment and Configuration Steps

- Install TrueNAS Core on the machine using a bootable USB with the TrueNAS installation ISO
    - Configure the boot disk, root password, BIOS vs UEFI, and swap
- Launch the web user interface and complete the initial setup wizard, including setting the system's hostname, timezone, and network configuration
- Configure network interfaces with static IP addresses and configure DNS settings
- Configure storage pools by selecting the drives and choosing the ZFS configuration
- Create datasets within storage pools to organize your data and set permissions for access control.
- Enable and configure the required services for file sharing and backup 
    - SMB/CIFS, NF, AFP, FTP, SSH, or iSCSI for block-level storage access
- Create user accounts and groups or sync with Active Directory to manage access to shared resources and assign permissions
- Set up backups, regular snapshots, and replication between the two local systems

<h2>Architecture Diagram</h2>

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
