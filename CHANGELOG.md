[11/09/2026]
## Fixed
- OpenSSL configures with --libdir=lib so x86_64 installs land in $OPENSSLPATH/lib, matching the base image LD_LIBRARY_PATH; Python LDFLAGS updated to match
## Added
- Minimal CI: default make target smoke test plus base/openssl image builds on linux/amd64

[10/19/2026]
## Changed
- Base image is now ubuntu 26.04
- Tool version bumps: terraform 1.16.6, go 1.27.2, python 3.15.0, openssl 4.0.3, node 26.12.0, vault 2.2.0, consul 2.0.4, ruby 4.0.7, azure-cli 2.91.0, ibm-cli 2.48.0

[01/06/2026]
## Changed
- Version ref updates and openssl hash check fixes

[03/10/2023]
## Changed
- Base image is now ubuntu 22.04 "Jammy"
- OpenSSL 3.0.x
- docker build platform is now linux/arm64 by default

[05/19/2020]
## Added
- IBM directory
- IBM dockerfile that builds Terraform container with IBM plugin
