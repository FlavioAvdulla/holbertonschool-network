# Networking Basics #1

## Table of Contents
1. [Change Your Home IP](#change-your-home-ip)
2. [Show Attached IPs](#show-attached-ips)
3. [Port Listening on Localhost](#port-listening-on-localhost)

## Change Your Home IP
Write a Bash script that configures an Ubuntu server with the below requirements.

### Requirements:
- `localhost` resolves to `127.0.0.2`
- `facebook.com` resolves to `8.8.8.8`

In this example we can see that:
- Before running the script, `localhost` resolves to `127.0.0.1` and `facebook.com` resolves to `157.240.11.35`
- After running the script, `localhost` resolves to `127.0.0.2` and `facebook.com` resolves to `8.8.8.8`

> **Note:** If you’re running this script on a machine that you’ll continue to use, be sure to revert `localhost` to `127.0.0.1`. Otherwise, a lot of things will stop working!

File: `0-change_your_home_IP`

## Show Attached IPs
Write a Bash script that displays all active IPv4 IPs on the machine it’s executed on.

File: `1-show_attached_IPs`

## Port Listening on Localhost
Write a Bash script that listens on port `98` on localhost.

File: `2-port_listening_on_localhost`
