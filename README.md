# Semaphor-AUR
PKGBUILD &amp; misc. related stuff to package Semaphor for arch AUR-style

This is the first PKGBUILD I've made, so any help making this cleaner &amp;
more useful for public use is MUCH appreciated!

# Issues
Currently the officially supported Semaphor release is the binary provided
by Spideroak from their downloads. Building from source is somewhat involved
dependency-wise, and ultimately leaves us with a binary that *isn't* officially
supported by Spideroak. In this case, any bugs a user encounters in Semaphor
would be met with the "install the official build and try again" response.
Thus, we're left essentially repackaging the Spideroak-provided .rpm file.

Two big issues with this:

1. No obvious signature file or cryptographic digest for the rpm file.

    We don't have a nice way beyond HTTPS to verify
    the integrity of the package we receive; the checksum in the PKGBUILD is computed
    after we download the rpm, not known before-hand out of channel.

2. The URL is static for each version.

    Instead we need to manually update the cryptographic hash when a new version
    is available. This means that, for every new version, the user will need to
    get a new PKGBUILD. This is bad.


These issues are both up to Spideroak to fix, so hopefully things change soon.
