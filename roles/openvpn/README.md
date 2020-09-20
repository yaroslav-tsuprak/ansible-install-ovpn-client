Role Name
=========

The role of install and start openvpn client

Role Variables
|------------------------------------------------------------------------------------------------------------------------------------------|
| Variable name             | Description                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------|
| openvpn.ca                | CA certificate (public key)                                                                                  |
| openvpn.cert              | Client certificate (public key) signed by the CA                                                             |
| openvpn.device            | Device type (tun or tap)                                                                                     |
| openvpn.key_direction     | If in your VPN tls-auth key is used and in configuration file there is such line                             |
| openvpn.port              | Port number                                                                                                  |
| openvpn.proto             | Protocol (UDP or TCP)                                                                                        |
| openvpn.private_key       | Client private key                                                                                           |
| openvpn.reneg_sec         | Renegotiate data channel key after n seconds                                                                 |
| openvpn.remote            | OpenVPN server IP address for connection                                                                     |
| openvpn.remote_cert_tls   | This is a useful security option for clients, to ensure that the host they connect to is a designated server |
| openvpn.static_key        | Shared Static TLS key should be 1 on clients and 0 on servers                                                |
| openvpn.update_cache_time | Time to update repo cache                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------|

Example Playbook
----------------

---
- hosts: ubuntu
  name: Install and starts openvpn client
  roles:
    - { role: openvpn, become: yes }

License
-------

BSD

Author Information
------------------

Yaroslav Tsuprak
Skype: netvirus24445
https://github.com/yaroslav-tsuprak
