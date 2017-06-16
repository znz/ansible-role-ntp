# Ansible role for ntp

Setup ntp.

## Requirements

- Debian
- Ubuntu

## Role Variables

see [defaults/main.yml](defaults/main.yml).

## Dependencies

systemd and ufw.

## Example Playbook

Example:

    - hosts: servers
      become: yes
      roles:
         - role: znz.ntp

Another example:

    - hosts: all
      become: yes
      roles:
      - role: znz.ntp
        ntp_servers:
        - ntp1.jst.mfeed.ad.jp
        - ntp2.jst.mfeed.ad.jp
        - ntp3.jst.mfeed.ad.jp
        ntp_peers:
        - 10.0.0.10
        - 10.0.0.11
        - 10.0.0.12

## License

MIT License
