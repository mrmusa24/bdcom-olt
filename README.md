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
