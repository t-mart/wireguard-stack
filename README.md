# mobile-wireguard-stack

A Docker Compose stack for running various VPN services using WireGuard.

Designed especially for mobile computers.

## Usage

1. Clone this repo.

2. Review the `.env` file and adjust any settings as needed. The default
   settings should work for most users.

3. Review the [config documentation](config/README.md) and perform any
   appropriate steps.

4. Start the stack with:

   ```bash
   docker-compose up --detach
   ```

At that point you should be connected. Here are some things you can do:

- **VPN Web Browsing**: Connect a browser to the SOCKS5 proxy at
  `localhost:1080` (no username or password).
  [FoxyProxy](https://addons.mozilla.org/en-US/firefox/addon/foxyproxy-standard/)
  is a good browser extension for this.

- **Torrenting**: Use qBittorrent, whose web UI is at <http://localhost:37551>
  with username `admin` and a password that's printed in its container's logs.

  - **Streaming Server**: Use Jellyfin to stream downloaded content to TVs, whose web UI is at <http://localhost:8096>.

    First time setup can be completed by navigating to
    <http://localhost:8096/web/index.html#!/wizardstart.html>.

## IP Leak Testing

SOCKS5 proxy connections can be tested by configuring the
browser to use the proxy and then visiting a site like
<https://api.ipify.org/?format=json>.

qBittorrent connections can be tested by adding a magnet torrent
link from <https://ipleak.net/>.