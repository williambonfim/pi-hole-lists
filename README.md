# Pi-hole blocklist

This repository contains an additional domain blocklist for Pi-hole. The list is in [`domains.txt`](domains.txt), with one domain per line.

## Add the list to Pi-hole

In the Pi-hole web interface, add this URL under **Adlists**:

```text
https://raw.githubusercontent.com/williambonfim/pi-hole-lists/main/domains.txt
```

Then run **Update Gravity** in Pi-hole, or run `pihole -g` on the Pi-hole host. The URL will work once the list is available in the [GitHub repository](https://github.com/williambonfim/pi-hole-lists).

## Add or remove a domain

Edit `domains.txt` and put each domain on its own line:

```text
ads.microsoft.com
```

Use a hostname only, without `https://`, a path, port, IP address, or wildcard (`*`). Lines starting with `#` are comments. To stop blocking a domain, remove its line. After the updated list is available at the URL above, run **Update Gravity** again so Pi-hole loads the change.
