# claudeOS packages

Signed RPM package repository for **claudeOS** (dnf5).

- **Index (dnf baseurl):** https://s9213712.github.io/claudeos-packages/
- **Packages:** attached to the [Releases](https://github.com/s9213712/claudeos-packages/releases) of this repository
- **Signing key:** `RPM-GPG-KEY-claudeos` — Ed25519, fingerprint `7F4D 2AAF 780E F712 5D11  A6BC 3EE3 BE0C BE54 E15A`.
  Every package is signed; claudeOS refuses unsigned or tampered packages (`%_pkgverify_level all`).

```ini
# /etc/yum.repos.d/claudeos.repo
[claudeos]
name=claudeOS
baseurl=https://s9213712.github.io/claudeos-packages/
gpgcheck=1
gpgkey=https://s9213712.github.io/claudeos-packages/RPM-GPG-KEY-claudeos
```

## Third-party software

The `nvidia-*` packages contain the NVIDIA Linux graphics driver. They are redistributed
unmodified under section 1(d) of the NVIDIA Software License (for use with the Linux kernel);
the license is included in every NVIDIA package (`/usr/share/licenses/<package>/LICENSE`) and in
[`legal/NVIDIA-LICENSE.txt`](legal/NVIDIA-LICENSE.txt). The `nvidia-kmod` (R620) modules are built
from NVIDIA's open GPU kernel modules (MIT/GPL-2.0). All other packages are built from their
upstream sources under their own licenses (see each package's `License:` tag).
