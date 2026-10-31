# CCDC Kill Chains and Enumeration

This repository stores host enumeration notes and kill chain documentation for the CCDC lab. Add discovered services, validated findings, attack paths, evidence, and remediation notes here.

## Structure

- `enumeration/`: one file per host for inventory, services, and findings.
- `kill-chains/`: one file per host for documenting a validated sequence of actions and results.
- `evidence/`: supporting screenshots, logs, and command output, organized by host.

The included files are examples to complete during the exercise. Supplied inventory is recorded below; services and attack paths have not been verified.

## Hosts

| Host | Platform / role | LAN | Public address pattern |
| --- | --- | --- | --- |
| [Ubuntu Wkst](enumeration/ubuntu-wkst.md) | Desktop workstation | `DHCP` | `172.31.20+team#.2` |
| [Rocky Ecom](enumeration/rocky-ecom.md) | Rocky Linux 9 · Storefront | `172.20.240.10` | `172.25.20+team#.10` |
| [Ubuntu Email](enumeration/ubuntu-email.md) | Ubuntu 22.04 · Messaging endpoint | `172.20.240.15` | `172.25.20+team#.15` |
| [Debian Splunk](enumeration/debian-splunk.md) | Debian 12 · Splunk 10.0.2 | `172.20.240.20` | `172.25.20+team#.20` |

Public addresses retain the supplied notation: `20+team#` means 20 plus the team number in the third octet. For example, team 1 uses `172.25.21.10` for Rocky Ecom. Confirm the assigned team number before using an address.

## Lab access

The supplied credentials for Ubuntu Wkst, Rocky Ecom, and Ubuntu Email are `sysadmin / Changeme1!`. No credentials were supplied for Debian Splunk. ESXi console access was listed for the first three hosts; console links were not provided.

## Workflow

1. Update the host enumeration file with timestamps, commands, and observed results.
2. Document confirmed action sequences in the matching kill chain file. Keep hypotheses clearly marked.
3. Save supporting evidence under `evidence/<host>/` and link it from the notes.
4. Record impact, remediation, and retest results. Perform actions only within the authorized exercise scope.

Do not commit additional passwords, private keys, or sensitive session data in evidence.
