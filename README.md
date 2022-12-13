# patch_for_interface_gpg3100_gpg3300

These files are patch for to re-compile Interface software(gpg3100, gpg3300)

## Target environment

* Ubuntu 16.04 with kernel ver. 4.4.0.81-lowlatency
* gpg3100 (gpg3100_x86_64_061048.tgz)
* gpg3300 (gpg3300_x86_64_051045.tgz)

## How to use

1. Before using these patches, install Interface official drivers(gpg3100, gpg3300)
1. (If you need) Copy "x509.genkey" to `/usr/src/<linux version: 4.4.0.81-lowlatency>certs/`, and run `openssl req -new -nodes -utf8 -sha512 -days 36500 -batch -x509 -config x509.genkey -outform DER -out signing_key.x509 -keyout signing_key.pem`
1. Go to Interface driver's src directory
1. Replace the "Makefile" file and patch using patch files
1. Make symbolic link referencing [this page](https://www.rbt.his.u-fukui.ac.jp/~naniwa/comp/ubuntu-lowlatency.html)
1. Run `make` and `make install`
