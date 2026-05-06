# BDCOM GPON/EPON OLT and Switch Command Reference

This document provides a collection of common configuration commands for BDCOM OLTs and Switches, covering GPON, EPON, and general switch functionalities.

---

## 1. How to enable loop detection in GPON ONU (SFU)

```bash
Switch#config
Switch_config#interface gpon0/2:1
Switch_config_gpon0/2:1#gpon onu loopback-detect protocol private
Switch_config_gpon0/2:1#gpon onu uni 1 loopback-detect enable

To configure loopback on all ONUs in a range:

Switch#config
Switch_config#interface range gpON 0/1:1-10
Switch_config_if_range#gpon onu loopback-detect protocol private
Switch_config_if_range#gpon onu uni 1 loopback-detect enable
--
##
Reset Commands:

Username: admin

Password:




Welcome to BDCOM P3310D EPON OLT





OLT>enable

OLT#

OLT#delete startup-config
this file will be erased, are you sure? (y/n)y

OLT#delete config.db
this file will be erased, are you sure? (y/n)y

OLT#delete ifindex-config
this file will be erased, are you sure? (y/n)y

OLT#reboot
Do you want to reboot the Switch (y/n)?y
