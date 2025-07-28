# Configuration

Various configuration files for the setup.

## `dante-sockd.conf`

Dante SOCKS proxy server configuration file.

The default configuration should work for most uses.

## `wg0.conf`

WireGuard VPN configuration file.

**This file does not exist by default**, and should be created by either:

- Copying `wireguard-wg0.conf.template` to `wg0.conf` and filling in the necessary details.
- Using [AirVPN Config Generator](https://airvpn.org/generator/) to create a WireGuard configuration file.
- Anything else that produces a valid WireGuard configuration file.
